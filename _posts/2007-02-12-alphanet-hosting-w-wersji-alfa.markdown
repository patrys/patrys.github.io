---
layout: post
status: publish
published: true
title: AlphaNet - hosting w wersji alfa
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 343
wordpress_url: http://room-303.com/blog/2007/02/12/alphanet-hosting-w-wersji-alfa/
date: 2007-02-12 01:25:29.000000000 +01:00
categories:
- web
- software
tags: []
comments:
- id: 6609
  author: http-byte.openid.pl-
  author_url: http://byte.openid.pl/
  date: '2007-02-12 06:18:47 +0100'
  date_gmt: '2007-02-12 05:18:47 +0100'
  content: Znam AlphaNet. Kiedyś to działało chyba całkiem zgrabnie, z tym większą
    przykrością czytam więc takie rzeczy.
- id: 6610
  author: Wojtosz
  author_url: http://www.blaszkowski.com
  date: '2007-02-12 07:38:20 +0100'
  date_gmt: '2007-02-12 06:38:20 +0100'
  content: eaccelerator w jednej z najnowszych wersji robił u mnie wprawdzie nieco
    inne wybryki co było powodem jego czasowego wyłączenia. jakieś info odnośnie wersji
    eaccelerator'a i samego interpretera PHP ?
- id: 6611
  author: Wojtosz
  author_url: http://www.blaszkowski.com
  date: '2007-02-12 07:46:25 +0100'
  date_gmt: '2007-02-12 06:46:25 +0100'
  content: "no więc małe dopowiedzenie.\r\npo pierwsze - zgaduję, że ów Łukasz nie
    napisał sobie własnej klasy, do której się odwołuje w swoich skryptach.\r\n\r\npo
    drugie:\r\nna alpha.pl czytamy, że PHP5: 5.1.4 (jako rozszerzenie CGI). Na jednym
    apaczu postawili 2 wersje PHP. Na dłuższą metę takie rozwiązanie obsysa, chociażby
    ze względu na fakt obliczenio-żerności (chyba jest takie słowo) tego rozwiązania.
    Prędzej czy później będą musięli zdecydować się na odpalenie drugiej sesji apacza
    na innym IP lub ogólnie przenieść na nową maszynę.\r\n\r\nPowyższy przykład jest,
    niestety, ceną jaką trzeba zapłacić za najnowsze, nie do końca wytestowane wersje
    oprogramowania."
- id: 6612
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-02-12 09:26:48 +0100'
  date_gmt: '2007-02-12 08:26:48 +0100'
  content: Ja bym raczej się pokusił o stwierdzenie, że zrobili to samo co Pro Futuro
    - upgrade PHP bez podbicia pakietów zależnych. W tamtym przypadku chodziło o ionCube,
    który też pojawiał się w <code>phpinfo()</code> i też nie działał (powodował za
    to segfault).
- id: 6613
  author: Xarafaxz
  author_url: ''
  date: '2007-02-12 09:27:40 +0100'
  date_gmt: '2007-02-12 08:27:40 +0100'
  content: PHP musi być wykonywane jako CGI ponieważ niema innej możliwości odseparowania
    kontekstów wykonywania skryptów należących do innych użytkowników. Kolejny problem
    to to że nadal trzeba udostępniać to nieszczęsne php4.
- id: 6614
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-02-12 09:32:39 +0100'
  date_gmt: '2007-02-12 08:32:39 +0100'
  content: "Xarafaxz:\r\n\r\nZgadza się, że CGI jest bezpieczniejsze. Ale wcale nie
    ma obowiązku udostępniania PHP4, w iCenter działa tylko PHP 5.2 i klienci się
    nie skarżą."
- id: 6615
  author: arekm
  author_url: ''
  date: '2007-02-12 10:20:23 +0100'
  date_gmt: '2007-02-12 09:20:23 +0100'
  content: eaccelerator_get() nie jest dostępne jeśli nie włączy się się SHMowego
    złomkostwa w eacceleratorze na poziomie kompilacji (a domyślnie jest to wyłaczone)
- id: 6616
  author: Ja
  author_url: http://brak
  date: '2007-02-12 15:04:49 +0100'
  date_gmt: '2007-02-12 14:04:49 +0100'
  content: "\"Czym prędzej odpisał i host, a helpdesk pomoc swą zaoferował w te słowy:\"\r\n\r\nraczej:
    \"tymi słowy\" jeśli już to \"w te słowa\""
- id: 6617
  author: Wojtosz
  author_url: http://www.blaszkowski.com
  date: '2007-02-12 16:34:41 +0100'
  date_gmt: '2007-02-12 15:34:41 +0100'
  content: "Ja:\r\nJan Miodek się znalazł. Jeśli nie popełniasz błędów to proszę,
    rzuć kamieniem!"
- id: 6618
  author: s
  author_url: ''
  date: '2007-02-12 18:15:26 +0100'
  date_gmt: '2007-02-12 17:15:26 +0100'
  content: pewnie na moim serwie tez dziala tylko 5.2 i aden klient sie nie skarzy,
    tez dziala eaccelerator i wszystko jest git, a niekompatybilnosc skryptow w wersji
    4 do 5 to jakis mit jest, zadnego problemu nie spotkałem do tej pory
- id: 6620
  author: Xarafaxz
  author_url: ''
  date: '2007-02-12 21:25:32 +0100'
  date_gmt: '2007-02-12 20:25:32 +0100'
  content: "Parys:\r\n\r\nEz Publish to nie jest jakiś super wzorcowy CMS, do dzis
    oficjalnie nie działa w PHP5."
- id: 6621
  author: Wojtosz
  author_url: http://www.blaszkowski.com
  date: '2007-02-12 21:26:36 +0100'
  date_gmt: '2007-02-12 20:26:36 +0100'
  content: "s:\r\nszacunek dla speca od programowania obiektowego :)\r\n\r\nno więc,
    w PHP4 jest ono bardzo-pseudo-obiektowe, w PHP5 jest mniej-pseudo-obiektowe. \r\nnie
    chcę być niegrzeczny, ale jak byś trochę więcej poklikał kodu to takie teorie
    zapewne by tu nie padły."
- id: 6622
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-02-13 16:39:28 +0100'
  date_gmt: '2007-02-13 15:39:28 +0100'
  content: "Wojtosz:\r\n\r\nTo ja klikam kod PHP od lat i nie miałem ze swoim kodem
    problemów jakoś. Po przesiadce z 3 na 4 kod działał, tylko go wyczyściłem z czasem,
    korzystając z obiektowości 4. Po przesiadce z 4 na 5 kod dalej działa, z czasem
    tylko zastąpiłem obejścia pseudoobiektowości 4 czystym kodem dla 5.\r\n\r\nXarafaxz:\r\n\r\nEz
    Publish to wcale nie jest CMS, to jest jeden wielki WTF. Pisałem już o nim kiedyś
    na tym blogu."
- id: 6655
  author: Luken
  author_url: http://luken.jogger.pl/
  date: '2007-02-14 01:14:45 +0100'
  date_gmt: '2007-02-14 00:14:45 +0100'
  content: Obiektówka z PHP5 nie chodzi na PHP4. O to tu chodzi pewnie. :)
- id: 6668
  author: eRiZ
  author_url: http://eriz.pc-inside.org/weblog
  date: '2007-02-15 00:58:00 +0100'
  date_gmt: '2007-02-14 23:58:00 +0100'
  content: "No, dzisiaj trzeba naprawdę się namęczyć, żeby znaleźć porządny hosting
    i jednocześnie za niewielkie pieniądze...\r\n\r\nZaliczyłem już boo, domenyhosting,
    powiem krótko - nie dać się skusić na niską kasę i ładnie wyglądające parametry.\r\n\r\nJak
    się samemu nie sprawdzi, to nie ma bata.\r\n\r\nLepiej już wyłożyć trochę więcej
    kasy i zainwestować w markę niż walczyć z nerwami i przeklinać adminów, bo nie
    robią tego, co powinni."
- id: 6676
  author: Wojtosz
  author_url: http://www.blaszkowski.com
  date: '2007-02-15 11:21:05 +0100'
  date_gmt: '2007-02-15 10:21:05 +0100'
  content: "Wszystkich zainteresowanych uruchamianiem aplikacji przeznaczonych dla
    PHP4 na interpreterze PHP5 odsyłam tu: \r\nhttp://www.zend.com/manual/migration5.incompatible.php\r\n\r\njak
    widać różnice są :)"
- id: 6677
  author: Wojtosz
  author_url: http://www.blaszkowski.com
  date: '2007-02-15 11:29:16 +0100'
  date_gmt: '2007-02-15 10:29:16 +0100'
  content: "Luken:\r\ndziękuję za próbę sprostowania :) jednak chodzi mi o sytuację
    odwrotną.\r\nprzykład podany przez Ciebie również jest prawdziwy.\r\n\r\nSwoją
    drogą, z utęsknieniem czekam na zmiany jakie przyniesie PHP6. PHP wreszcie zaczyna
    przypominać 'prawdziwy' język programowania, idąc w kierunku rozwiązań proponowanych
    przez Redmond. podoba mi się odejście od old-schoolowych wynalazków, PHP wreszcie
    przestanie wybaczać podstawowe błędy (o niektórych pisał Patrys w jednym z poprzednich
    wpisów)."
- id: 6679
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-02-15 11:39:40 +0100'
  date_gmt: '2007-02-15 10:39:40 +0100'
  content: "Wojtosz:\r\n\r\nRóżnice, oczywiście, są. My przy przejściu na PHP5 zapuściliśmy
    grep na katalogach klientów i poprawiliśmy kilka (dosłownie kilka) serwisów ręcznie.
    Zajęło jedną noc (komputerowi na grep) i pół godziny (mi na poprawienie kodu)
    ;)\r\n\r\nWiększość z pozostałych różnic wynika z tego, że kod był niepoprawny
    (albo napisany niezgodnie ze sztuką) już w PHP4."
---
<p>Ze strony <a href="http://alpha.pl/">alpha.pl</a> krzyczą do nas najnowsze wersje oprogramowania. Na konto skusił się też kiedyś mój kolega, Łukasz Olejnik. Jego serwis od jakiegoś czasu nie działa.</p>

<p>Dostawca usług nie raczył o tym poinformować, poinformował za to wdzięcznie skrypt crona. I informuje nadal, ze szwajcarską punktualnością, dokładnie co godzinę.</p>

<p>Serwis ma tego pecha, że od początku swego istnienia korzysta z funkcjonalności eAccelerator, który niegdyś na wspomnianym hostingu zwykł działać. Być może wtedy była to jeszcze wersja beta, a do wersji alfa przeszli niedawno?</p>

<p><q>Cóż, zdarza się,</q> pomyślał Łukasz i czym prędzej zgłosił problem swojemu hostowi. Czym prędzej odpisał i host, a helpdesk pomoc swą zaoferował w te słowy:</p>

<blockquote><p>eAccelerator działa. Proszę zobaczyć w <code>phpinfo()</code></p></blockquote>

<p>Uspokoiło go to nieco i utwierdziło w przekonaniu, że może spokojnie zignorować wyświetlane zamiast strony:</p>

<blockquote><p>Call to undefined function: <code>eaccelerator_get()</code></p></blockquote>

<p>Do dziś ignoruje więc komunikaty, pracuje także nad przekonaniem swoich odwiedzających, że biała strona z czarnym napisem nie jest warta uwagi i świadczy o normalnej pracy serwera.</p>

<p>Dziękujemy zatem panom z AlphaNetu za wyczerpującą odpowiedź. Gratulujemy także czasu reakcji na zgłoszenie, a tak wspaniałego hostingu na resztę życia i sobie i wam życzę.</p>
