---
layout: post
status: publish
published: true
title: 'Django: nie róbcie tego w domu'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 349
wordpress_url: http://room-303.com/blog/2007/02/23/django-nie-robcie-tego-w-domu/
date: 2007-02-23 13:04:16.000000000 +01:00
categories:
- web
- software
- code
tags: []
comments:
- id: 6784
  author: cezio
  author_url: ''
  date: '2007-02-23 15:27:38 +0100'
  date_gmt: '2007-02-23 14:27:38 +0100'
  content: a propos hackowania django.contrib.admin, a w szczególności model.User,
    to jest też ciekawa lektura na http://www.b-list.org/weblog/2007/02/20/about-model-subclassing
- id: 7321
  author: Brut[all]
  author_url: ''
  date: '2007-03-24 19:21:11 +0100'
  date_gmt: '2007-03-24 18:21:11 +0100'
  content: "Powiem szczerze, że dziwi mnie, czemu uważasz, że to taki straszny hack
    jest.\r\nWłaśnie dlatego w Django wszystko tu jest taki proste (generic views
    są najzwyklejszymi funkcjami, do których Django się najzwyczajniej odwołuje),
    aby można było z tym wyczyniać różne cuda.\r\n\r\nMnie się zdarzało już co najmniej
    parę razy nadpisywać działanie jakiegoś generic view poprzez napisanie własnej
    funkcji, która z tamtego korzystała.\r\n\r\nDajmy na to prosty przykład: chcemy
    mieć podstronę wyświetlającą informacje o jakimś obiekcie, ale tylko dla osób
    zalogowanych. Nie możemy skorzystać z django.views.generic.list_detail.object_detail,
    więc co, piszemy wszystko od początku? Nie, tworzymy funkcję, która nie robi nic
    innego, tylko wywołuje object_detail z tymi samymi parametrami, traktujemy ją
    dekoratorem login_required i już. Właściwie, to z naszej nowej funkcji możemy
    teraz korzystać jako z nowego generic view, wykorzystywać wszędzie, gdzie chcemy
    mieć object_detail tylko dla zalogowanych\r\n\r\n(właściwie, to dla pojedyńczej
    sytuacji nawet nie trzeba tworzyć dodatkowej funkcji - w samym urls.py można od
    razu wstawić funkcję dekorującą z naszym object_detail jako parametr)\r\n\r\nPodmienianie
    danych POST to już co innego - tu faktycznie stosujemy brzydki trik i przymus
    jego wykorzystania faktycznie jest spowodowany brakami w django.contrib.admin,
    ale jeśli chodzi o samo modyfikowanie widoku admina... to wydaje mi się jak najbardziej
    normalne.\r\n\r\n\r\nAha.\r\nJeśli mogę się przyczepić, to uważam, że jeszcze
    jedną rzecz mógłbyś zrobić dużo lepiej.\r\nNormalna funkcja add_stage z admina
    przyjmuje w parametrach nazwę aplikacji i modelu. Ty, nadpisując ją, pozmieniałeś
    te parametry, co wydaje mi się zupełnie bez sensu - to chyba normalne, że jeśli
    coś dziedziczymy, czy nadpisujemy, to staramy się zostawić na wejściu i wyjściu
    dokładnie to samo?\r\nDużo lepiej by było, gdybyś zrobił tak:\r\n\r\nreturn main.add_stage(request,
    *args, **kwargs)\r\n\r\nPo prostu tak - standardowa zasada przy nadpisywaniu:
    \"co przyszło, to wyjdzie\", czyli wszystko załatwiają za nas świetne *args, **kwargs
    Pythona.\r\nOczywiście w takim razie i do nadpisującej funkcji muszą przyjść odpowiednie
    parametry. W takim razie modyfikujemy jeszcze urls.py:\r\n\r\n(r'^admin/(aplikacja)/(model)/add/',
    'serwis.aplikacja.admin_views.add_stage')\r\n\r\nlub dodajemy nazwy 'aplikacja'
    i 'model' w słowniku w trzecim parametrze, choć to pierwsze rozwiązanie dużo lepsze.\r\n\r\nZyskujesz
    na tym:\r\n1. Możliwość wykorzystania dokładnie tej samej modyfikacji dla innej
    aplikacji/modelu, gdybyś kiedyś chciał.\r\n2. W cholerę i jeszcze trochę logiki,
    poprawności programistycznej, czy jakkolwiek tego jeszcze nie nazwiemy."
---
<p>Wczoraj byłem zmuszony szybko dodać dodatkową funkcjonalność do jednej z rozwijanych przez nas aplikacji. Widok, o który chodziło opiera się na automatycznym, scaffoldowanym widoku administratora. Brzmi prosto?</p>

<p>Problem polegał na tym, że dostosowywanie logiki administratora jest dopiero w fazie planów (gałąź <code>admin-newforms</code>). W związku z tym, rozbudowanie go o własną logikę jest teoretycznie na tym etapie niewykonalne.</p>

<p>Przekopałem się więc przez większość kodu modułu <code>django.contrib.admin</code> i okazało się, że można Django nieco oszukać. Widoki są funkcjami, z czego korzysta się często przy <q>generic views.</q> Nie można po nich dziedziczyć, ale można wołać jeden z drugiego.</p>

<h4>Brzydki hack</h4>

<p>Do pliku <code>urls.py</code> na samym początku (przed sekcją <code>admin</code>) dopisujemy:</p>

<blockquote><pre><code>(r'^admin/aplikacja/model/add/', 'serwis.aplikacja.admin_views.add_stage'),</code></pre></blockquote>

<p>Następnie zakładamy plik <code>serwis/aplikacja/admin_views.py</code>:</p>

<blockquote><pre><code>from django.contrib.admin.views import main

def add_stage(request, *args, **kwargs):
	post = request.POST.copy()
	if request.method == 'POST':
		post['user'] = request.user.id
	request.POST = post
	return main.add_stage(request, 'aplikacja', 'Model', *args, **kwargs)</code></pre></blockquote>

<p>Voila!</p>

<h4>Parę słów wytłumaczenia</h4>

<p>Pierwsza część jest chyba oczywista, w tym przypadku nadpisujemy widok dodawania dla konkretnego modelu. Ponieważ Django przetwarza mapę rutingu w takiej kolejności, w jakiej są podane regułki, nasza linijka przesłoni znajdujące się niżej automatyczne reguły wbudowanego panelu administratora.</p>

<p>Druga część to utworzenie osobnego pliku dla widoków administracyjnych (nie musi to być osobny plik, ale to dobra praktyka). W pliku tym umieszczamy definicję własnego widoku <code>add_stage</code>.</p>

<p>W powyższym przykładzie dodawany jest automatycznie właściciel dla tworzonej instancji modelu. Nie bardzo można zrobić to w samym modelu, bo model jest bezstanowy i nie ma dostępu do stanu aplikacji. Poza tym, chcemy, żeby pole to było ustawiane tylko w tym przypadku.</p>

<p>Obiekt <code>request.POST</code> jest domyślnie <code>immutable</code>, więc tworzymy jego kopię i właśnie tę kopię modyfikujemy, a następnie podmieniamy oryginalny obiekt.</p>

<p>Ostatnia linijka powoduje wywołanie oryginalnego, <q>magicznego</q> widoku administratora, dostarczonego przez Django. Z tą różnicą, że przekazujemy do niego nazwę aplikacji i modelu. W przypadku wywołania bezpośredniego, pochodzą one z wyrażenia regularnego w konfiguracji <code>urls.py</code>, tutaj musimy podać je jawnie.</p>
