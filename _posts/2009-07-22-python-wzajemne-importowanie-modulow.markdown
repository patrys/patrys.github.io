---
layout: post
status: publish
published: true
title: 'Python: wzajemne importowanie modułów'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 629
wordpress_url: http://room-303.com/blog/?p=629
date: 2009-07-22 11:25:15.000000000 +02:00
categories:
- software
- code
tags: []
comments:
- id: 24479
  author: jarek
  author_url: ''
  date: '2009-07-22 15:43:25 +0200'
  date_gmt: '2009-07-22 14:43:25 +0200'
  content: "Dla mnie zmorą są importy zaszyte np. w środku (pół biedy gdy są zaraz
    obok definicji) metody/funkcji. \r\nCzasami ciężko się połapać w takich potworkach
    jeśli są nieudokumentowane przez co wdrażanie/testowanie aplikacji jest o wiele
    bardziej upierdliwe nie mówiąc o pracy z takim kodem."
- id: 24480
  author: japhy
  author_url: http://www.pasternacki.net/
  date: '2009-07-22 16:00:48 +0200'
  date_gmt: '2009-07-22 15:00:48 +0200'
  content: "Eee… a czy w trzeciej linijce bar.py nie powinno być przypadkiem \"import
    c\" albo \"import a\"?  Nie do końca rozumiem, jak to miałoby działać - czy jeśli
    importowana z pętli zmienna jest zdefiniowana (przypisana) powyżej, a następnie
    zredefiniowana *poniżej* importu tworzącego pętlę - czy z pętli dostaniemy pierwszą
    wartość, czy błąd?  Co jeśli zamiast redefinicji mamy zmianę mutowalnego stanu?\r\n\r\nWydaje
    mi się, że częściowe wsparcie dla pętli importów to więcej zamętu niż korzyści.
    \ Bo i właściwie po co?"
- id: 24481
  author: Patrys
  author_url: http://room-303.com/
  date: '2009-07-22 16:12:09 +0200'
  date_gmt: '2009-07-22 15:12:09 +0200'
  content: "japhy:\r\n\r\nPowinno być \"a\", literówka.\r\n\r\nDlaczego \"częściowe\"
    wsparcie? Jest kompletne. Po co? Choćby Haystack - pierwsza z brzegu aplikacja
    Django, która importuje pozostałe aplikacje projektu, zbierając modele ORM do
    indeksowania. Z kolei twój kod chciałby pewnie móc coś w tym ideksie wyszukać,
    co wymaga zaimportowania Haystacka."
- id: 24482
  author: japhy
  author_url: http://www.pasternacki.net/
  date: '2009-07-22 19:57:15 +0200'
  date_gmt: '2009-07-22 18:57:15 +0200'
  content: "Jest częściowe, bo kompletnego nie bardzo jest jak zaimplementować (nie
    zrobisz \"from foo import *\", a nawet \"import foo\" w bar.py, prawda?).\r\n\r\nA
    Haystacka albo importuję w models.py i sam wołam haystack.site.register() - albo:\r\n1.
    w urls.py projektu importuję haystack\r\n2. wołam haystack.autodiscover()\r\n3.
    autodiscover importuje search_indexes.py w tych aplikacjach, w których jest dostępne\r\n4.
    search_indexes.py może spokojnie zaimportować haystack - już został wcześniej
    zaimportowany przez urls.py, moduł jest już w pamięci.\r\nDiscovery nie leci w
    czasie importowania haystacka - jest wykonywane później.  Więc pudło."
- id: 24483
  author: Patrys
  author_url: http://room-303.com/
  date: '2009-07-22 21:00:44 +0200'
  date_gmt: '2009-07-22 20:00:44 +0200'
  content: "japhy:\r\n\r\nOczywiście, że w jedną stronę możesz zażyczyć sobie <code>import
    foo</code> albo i <code>from foo import *</code>. Sprawdzenie tego nie zajmie
    ci więcej czasu niż napisanie komentarza.\r\n\r\nW cale nie pudło. Ostatnio problem
    w biurze był właśnie z aplikacją third-party (nazwy nie podam), która do spółki
    z Haystackiem tworzyła pętlę zależności (Haystack <em>wymusza</em> wczesne załadowanie
    <code>urls</code>, sprawdź w kodzie; obie aplikacje robiły swoje autodiscover
    metodą brute-force)."
- id: 24484
  author: japhy
  author_url: http://www.pasternacki.net/
  date: '2009-07-22 22:34:20 +0200'
  date_gmt: '2009-07-22 21:34:20 +0200'
  content: "Zabawne, i \"print foo.c\" w bar.py rzuca AttributeError, a nie błąd w
    imporcie - czyli dostajemy częściowo załadowany moduł; cel pewnie jest taki, żeby
    móc się do całości modułu odwołać już w funkcji czy metodzie, wtedy nazwa rozwijana
    jest dopiero po załadowaniu całego foo - ale fajnie musi się coś takiego debugować
    ;)\r\n\r\nO Haystacku pisałem na podstawie jego dokumentacji, jeszcze go nie używałem;
    może bardziej zaawansowane wykorzystanie robi pętle - ale to IMO więcej kłopotu
    niż to warte (właśnie ze względu na zabawę z debugowaniem jeśli jednak coś pójdzie
    inaczej, niż myślimy - a kiedyś pójdzie)."
---
<p>Nie jestem pewien, skąd wzięło się takie przeświadczenie, ale ostatnio kilka osób próbowało mnie przekonać, że w Pythonie nie da się wykonać dwukierunkowego importu.</p>

<p>Rozważmy naiwny przykład programu ładującego wtyczkę, która z kolei chce korzystać z API swojego hosta. Zgadzam się, że takie dwukierunkowe zależności to na ogół oznaka bardzo złego designu, są jednak sytuacje, w których ciężko ich uniknąć.</p>

<p>Pozostaje problem implementacji. Okazuje się, że zwolennicy teorii <q>nie da się</q> dzielą się na tych, którzy nigdy nie próbowali, ale <q>ktoś coś wspominał</q> oraz na tych, którzy oczekiwali od Pythona zdolności myślenia. Dwukierunkowy import na poziomie globalnym modułów nie wymaga specjalnych zabiegów, trzeba być jednak przygotowanym na dwa ograniczenia:</p>

<ul>
<li>Importować można tylko wstecz, a więc wyłącznie symbole zdefiniowane przed importem, który doprowadził do powstania pętli (co jest dość logiczne, gdyż w pozostałych przypadkach mamy do czynienia z problemem jajka i kury)</li>
<li>W pewnych okolicznościach kod zostanie wykonany dwukrotnie</li>
</ul>

<p>Działającą pętlę importów pokazuje poniższy przykład:</p>

<p><strong>Uwaga:</strong> na diagramie jest literówka, oczywiście moduł <code>bar</code> powinien importować symbol <code>a</code> zamiast <code>b</code>.</p>

<p class="strip simple"><a href="http://www.flickr.com/photos/patrys/3745795314/" title="Circular dependencies in Python by patrys, on Flickr"><img src="http://farm3.static.flickr.com/2506/3745795314_7e1462f940_o.png" width="465" height="238" alt="Circular dependencies in Python" /></a></p>
