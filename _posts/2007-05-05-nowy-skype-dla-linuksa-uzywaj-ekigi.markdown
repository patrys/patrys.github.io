---
layout: post
status: publish
published: true
title: Nowy Skype dla Linuksa, używaj Ekigi
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 370
wordpress_url: http://room-303.com/blog/2007/05/05/nowy-skype-dla-linuksa-uzywaj-ekigi/
date: 2007-05-05 22:21:55.000000000 +02:00
categories:
- linux
- software
tags: []
comments:
- id: 7833
  author: Andrzej Dopierała
  author_url: http://andrzej.dopierala.name/
  date: '2007-05-05 22:59:47 +0200'
  date_gmt: '2007-05-05 21:59:47 +0200'
  content: "hm.. glowna zaleta skypa to \"bezserwerowa\" mozliwosc rozmowy z obustronnym
    NAT-em. \r\n\r\nA jak tutaj sprawia sie ekiga(albo sip? ;))"
- id: 7834
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-05-05 23:01:39 +0200'
  date_gmt: '2007-05-05 22:01:39 +0200'
  content: "Undefine:\r\n\r\nOd tego są bramki STUN, chyba że ktoś ma NAT symetryczny,
    ale z tym nie radzi sobie i Skype."
- id: 7835
  author: Bers
  author_url: http://www.blog.glegula.pl
  date: '2007-05-06 00:43:41 +0200'
  date_gmt: '2007-05-05 23:43:41 +0200'
  content: Tak, tylko że Skype to ponad 3 300 000 polskich użytkowników. Mnie też
    doskwiera ten problem, ponieważ codziennie gadam na skype po kilka godzin (pracując
    na projektami). Nie ma kamerki, nie ma niektórych przydatnych funkcji i do tego
    jeszcze bugi(Szególnie denerwujący jest ten, że jak wsześniej chatuje na windowsie
    i później loguje się na Skype na Linuksie to te ostatnie chaty mi wyskakują oO).
- id: 7836
  author: Andrzej Dopierała
  author_url: http://andrzej.dopierala.name/
  date: '2007-05-06 01:13:44 +0200'
  date_gmt: '2007-05-06 00:13:44 +0200'
  content: "Patrys: \"praca\" z skype wygląda dla mnie ostatnio tak:\r\n- włączam
    skype\r\n- rejestruję się (na jakieś nowe konto, bo swojego hasła wiecznie nie
    pamiętam ;)\r\n- wyszukuję nicka osoby z którą chcę pogadać\r\n- call.. i rozmawiam\r\n\r\nNie
    obchodzi mnie to że ja jestem za jakimś dziwnym natem zaa pixa/mikrotika/blackboxa,
    że osoba z którą rozmawiam również jest za natem z liveboxa/przyciętej sieci wydziałowej.
    Wogóle nie muszę wiedzieć co to jest nat ;)\r\nPo prostu \"call\". I działa. Niestety
    pod linuksem bez obrazu z kamerki :(\r\n\r\nA pod ekigą? Musiałbym wiedzieć co
    to jest jakiś tam nat, wiedzieć coś o jakiś bramkach stun (czy tego nie trzeba
    ustawić na routerze?), jakieś konta sip... dupa panowie, dupa!\r\n\r\nDo tego
    ekiga nie chce mi na laptopie pod AC się uruchomić :("
- id: 7837
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-05-06 01:19:06 +0200'
  date_gmt: '2007-05-06 00:19:06 +0200'
  content: "Undefine:\r\n\r\nEkiga sama wykrywa rodzaj NATu, dostarcza też własną
    bramkę STUN. A konto SIP ma format taki sam jak konto Jabbera, czy email."
- id: 7838
  author: calebr
  author_url: http://nic-nac-project.de/~calebr/
  date: '2007-05-06 08:02:11 +0200'
  date_gmt: '2007-05-06 07:02:11 +0200'
  content: W skype dziwne jest to, że tryb invisible działa w połowie. Można poznać
    czy ktoś się ukrywa czy nie po żółtej informacji w oknie statusu typu "nie dostarczono
    wiadomości...".
- id: 7839
  author: yZZuF
  author_url: ''
  date: '2007-05-06 10:19:03 +0200'
  date_gmt: '2007-05-06 09:19:03 +0200'
  content: "Z ekigą jest problem tak jak już ktoś wspomniał wcześniej. Ilość użytkowników
    ekigii jest mizerna. Wszyscy moi znajomi używają skype'a, jak mam znowu zacząć
    ich przekonywać podobnie jak to robiłem z jabber'em to mi się odechciewa.\r\nSkype,
    podobnie jak Gadu-Gadu, wygrywa swoją maksymalną prostotą. Nie trzeba się znać
    na komputerach aby założyć sobie konto w obydwu usługach. W ekiga atakują Cię
    detekcją jakiś natów sratów, w jabberze wyborem serwera. Może wydaje się to głupie,
    ale większość ludzi przy tak \"skomplikowanych\" pytaniach najzwyczajniej w świecie
    wymięka.\r\nTaka oto jest nasza smutna rzeczywistość, nie wygrywa to co jest lepsze."
- id: 7840
  author: Jajcuś
  author_url: http://blog.jajcus.net/
  date: '2007-05-06 13:14:26 +0200'
  date_gmt: '2007-05-06 12:14:26 +0200'
  content: "yZZuF: Ale z Ekigą nie jesteś ograniczony do userów Ekigi. Równie dobrze
    możesz się komunikować z użytkownikami Wengophone, Gizmo  i z użytkownikami setki
    innych dostawców SIP. Z SIP jest też trochę lepiej niż z Jabberem, bo zwykle dostaje
    się usługę wraz ze sprzętem/oprogramowaniem -- uruchamiasz Ekigę i od razu możesz
    założyć konto. Kupujesz \"telefon IP\" od jakiegoś operatora i dostajesz i adres
    SIP i sprzęt (telefon albo bramkę).\r\nWłaściwie, gdyby nie Skype, dzisiaj świat
    VoIP byłby piękny -- masa operatorów, sprzętu i oprogramowania do wyboru i wszystko
    ze wszystkim działa... niestety, Skype wystartował, gdy w świecie SIP mało co
    działało, nałapał użytkowników, a teraz ich będzie trzymał za wszelką cenę..."
- id: 7842
  author: yZZuF
  author_url: ''
  date: '2007-05-06 18:54:13 +0200'
  date_gmt: '2007-05-06 17:54:13 +0200'
  content: 'Jajcuś: Znam możliwości Ekigii, wiem, że nie muszą to być userzy Ekigii.
    Ale co mi po tym jak nie mam znajomych którzy by tego używali, co kolwiek związanego
    z SIP i normalnym VoIP. Wszyscy mają Skype''a. Nie chcą słyszeć o czymś innym,
    bo ich znajomi też mają Skype''a. I tak do zajeb...'
- id: 7843
  author: krystian
  author_url: http://krystian.openid.pl/
  date: '2007-05-06 20:18:52 +0200'
  date_gmt: '2007-05-06 19:18:52 +0200'
  content: IMO SIP i tak wygra. Co raz więcej firmowych centralek abonenckich ma wbudowany
    (albo dostępny w postaci modułu) serwer SIP, sprzętowe bramki SIP więc z konieczności
    pracownicy tych firm będą mieć klienta SIP...
- id: 7844
  author: Tomasz Torcz
  author_url: http://zdzichu.openid.pl/
  date: '2007-05-06 22:51:15 +0200'
  date_gmt: '2007-05-06 21:51:15 +0200'
  content: Jakby Linux obslugiwal moja kamerke, to bym nie musial do rozmow bootowac
    Windows (i Skype).
- id: 7845
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-05-06 23:33:37 +0200'
  date_gmt: '2007-05-06 22:33:37 +0200'
  content: "Zdzichu:\r\n\r\nJaki model?"
- id: 7846
  author: yZZuF
  author_url: ''
  date: '2007-05-06 23:35:24 +0200'
  date_gmt: '2007-05-06 22:35:24 +0200'
  content: 'Zdzichubg: Może czas zmienić kamerkę? No chyba, że jest wbudowana.'
- id: 7851
  author: h.
  author_url: ''
  date: '2007-05-08 09:14:04 +0200'
  date_gmt: '2007-05-08 08:14:04 +0200'
  content: "Serwery STUn w pewnych sytuacjach nie daja rady.\r\nDobry operator posiada
    swoje media proxy, ktore sa uzywane w razie potrzeby i skutecznie eliminuja problem
    natow. \r\nSkype powoil bedzie tracil na rzecz SIP."
- id: 7852
  author: empathon
  author_url: http://blog.empathon.net
  date: '2007-05-08 11:40:38 +0200'
  date_gmt: '2007-05-08 10:40:38 +0200'
  content: "Wiesz co Patrys nadziei ludziom robisz a potem rozczarowanie. Jak zacząłem
    czytać ten wpis, jeszcze nie dokładnie, przed oczami stanął mi   skype na linuxa
    z opcjami dostępnymi w tym na win - pomyślałem \"WRESZCIE!!1\". A potem takie
    rozczarowanie ;)\r\nSkype 1.3 to kompletna porażka, używam 1.2 bo jakoś mam z
    nim mniej problemów i _w ogóle_ działa...\r\nW skrócie skype ma tak samo w dupie
    userów linux'a i mac'a jak gg... a szkoda.\r\nJeśli chodzi o gg to wszystko było
    by ok, bo z komunikatorami nie ma problemu, gdyby nie ostatnie jazdy z blokowaniem
    dostępu..."
- id: 7994
  author: evil_core
  author_url: ''
  date: '2007-05-30 23:55:35 +0200'
  date_gmt: '2007-05-30 22:55:35 +0200'
  content: 'empathon: z gg nie ma problemow....pozatym ze wyglada to jak baner reklamowy,
    jestes zmuszony do jednego serwera, zreszta czesto poadajacym ktory ma cie w dupie
    bo nie ma konkurencji. Jabber jest o tyle zajebistrzy ze rozproszony, admin jednego
    serwera pokaze uzytkownikom gdzie ich ma, to przenosza sie na inny, tak jak z
    kontami mialowymi(nadal chcialbys sie ceiszyc 2mb kontem na onecie z doklejanymi
    reklamami). Ludzie nie widza jakie gg jest do dupy, poniewaz nie poznali jeszcze
    lepszych rozwiazan.'
- id: 10827
  author: 'Ludwik C. Siadlak :: blog &raquo; Blog Archive &raquo; Połączenia ze Skypem
    bez Skype&#8217;a?'
  author_url: http://blog.ludwikc.net/2007/11/30/polaczenia-ze-skypem-bez-skypea/
  date: '2007-11-30 10:57:12 +0100'
  date_gmt: '2007-11-30 09:57:12 +0100'
  content: '[...] Na górze logo Ekigi, bo to właśnie o niej był artykuł na Mad Penguin,
    ktory doprowadził mnie do bramki zhinka. Więcej o Ekidze można przeczytać właśnie
    w w/w artykule albo po polsku, u Patrysa. [...]'
- id: 23378
  author: woti
  author_url: http://www.portalrodzinny.pl
  date: '2008-12-13 17:50:01 +0100'
  date_gmt: '2008-12-13 16:50:01 +0100'
  content: 'Mam kamerkę, ktora chodzi pod Ubu, ale słabo, bo dla sn9vc102 obraz zielony,
    a dla v4l za ciemny i brązowy. Byc może przesiadłbym się na ekigę, choc musiał
    bym uczyć się toto zainstalować. Ale: wszyscy znajomi mają windy i skypa. Oni
    na pewno nie zechcą zmieniać, bo i tam dla nich za trudno. Dokładnie tak samo
    jest z gg - tyle, że w linuchu mamy kadu itp. itds. Kiedy tak stanie się z ekiga/skype?'
---
<p>Na garażowym blogu Skype pojawiła się <a href="http://share.skype.com/sites/garage/2007/05/skype_for_linux_14_alpha_relea.html">zapowiedź kolejnej wersji dla Linuksa</a>. Zmienił się interfejs (nie, nie przesiedli się na <abbr title="GIMP Toolkit">GTK+</abbr>).</p>

<p>Pojawiły się też nowe funkcje, takie jak wysyłanie wiadomości <abbr title="Short Message Service">SMS</abbr> i rozmowy wideo. Ehh, rozmarzyłem się. Nic się nie pojawiło, Skype dla Linuksa nadal tkwi w epoce pingwina łupanego i jest więcej niż wystarczającym powodem dla śmiechu ze strony użytkowników Windows.</p>

<p>Dlatego proponuję upgrade w formie zamiany Skype'a na <a href="http://ekiga.org/">Ekigę</a>:</p>

<p class="strip"><a href="http://www.flickr.com/photos/patrys/468986688/" title="Photo Sharing"><img src="http://farm1.static.flickr.com/177/468986688_c4074d0b4a.jpg" width="500" height="293" alt="Ekiga - spread the love ;)" /></a></p>

<p>Działa tak samo pod Windows i pod Linuksem, a do tego używa powszechnie uznanych za standardowe protokołów <abbr title="Session Initiation Protocol">SIP</abbr> (co oznacza tyle, że można rozmawiać z użytkownikami dowolnego klienta <abbr title="Voice Over Internet Protocol">VOIP</abbr>). Używam od dawna, a od niedawna mam też okazję pobawić sie kamerą, polecam.</p>
