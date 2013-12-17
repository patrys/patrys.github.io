---
layout: post
status: publish
published: true
title: Dlaczego PHP jest do niczego?
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 229
alias: /blog/2006/02/05/dlaczego-php-jest-do-niczego/
date: 2006-02-05 22:46:37.000000000 +01:00
categories:
- web
- software
- code
tags: []
comments:
- id: 3261
  author: Nivertius
  author_url: http://nivertius.uaznia.net/
  date: '2006-02-05 23:06:47 +0100'
  date_gmt: '2006-02-05 22:06:47 +0100'
  content: Aż za prawdziwe. Coraz bardziej żałuję, że się go nauczyłem a nie zacząłem
    np. od JSP. Tyle projektów, które robiłem jest w nim napisane i ich myśl o ich
    rozwoju mnie po prostu przeraża, właśnie ze względu na język. 'Kalafior', jak
    ktoś gdzieś kiedyś napisał.
- id: 3262
  author: sprae
  author_url: ''
  date: '2006-02-05 23:28:03 +0100'
  date_gmt: '2006-02-05 22:28:03 +0100'
  content: "Zapomniales o slawnych namespace ktorych nie ma. Oraz o tym ze wiekszosc
    koderow php woli pisac po raz 100 to samo niz wykorzystac zewnetrzne kody, lub
    budowac sobie warsztat z narzeniami.\r\nNa koniec warto wspomniec ze w takim c,
    kazdy wiekszy projekt trudno utrzymac, bez drogich lub zmyslnych narzedzi.\r\nCo
    do slawetnej nalepki jezyka dla idiotow zaczelo sie chyba od basica, potem przeszlo
    przez pascal i chyba stanelo na php."
- id: 3263
  author: Vee
  author_url: http://blog.stanowski.info
  date: '2006-02-05 23:44:25 +0100'
  date_gmt: '2006-02-05 22:44:25 +0100'
  content: "Czy ważne co kto o Tobie sądzi? Zapewne nie jeden jest człowiek, który
    z kompletu sql+php+(ajax/xul/gtk) zrobi aplikację lepszą i zgrabniej napisaną
    niż ta w C/C++.\r\n\r\nŻe już nie wspomne o przenośności takiego rozwiązania.
    Opinie wyrabiają właśnie osoby zajmujące się PHP od 2 tygodni... to one często
    są najaktywniejsze na forach/stronach/listach... i myśląć, że wiedzą dużo dają
    swoje \"profesjonalne rady\" innym.\r\n\r\n\"Prawdziwi maniacy\", który ten język
    wałkują od 4/6 lat (mój staż to właśnie jakieś 3,4 lata) często nie mają czasu/uchoty/siły
    udzielać pomocy w takich sprawach. Siedzą sobie cichutko i piszą dość dobre aplikacje
    mogące konkurować z tymi napisanymi w innych językach."
- id: 3264
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-02-06 00:04:59 +0100'
  date_gmt: '2006-02-05 23:04:59 +0100'
  content: "Vee:\r\n\r\nAle przyznasz, że sam język też jest daleki od doskonałości.\r\n\r\nZapomniałem
    wspomnieć, że drażni mnie bardzo archaiczna składnia języka, pełna zgodności wstecz
    z poprzednimi wersjami. Przez to brakuje wolnych symboli i nie istnieje wersja
    shorthand do definiowania wektorów i tablic. Pisanie za każdym razem array() jest
    dość denerwujące, jeśli chce się przekazać dwie liczby tylko.\r\n\r\nBrakuje mi
    też często nazwanych parametrów. Jeśli funkcja ma być elastyczna to albo podając
    jeden parametr trzeba podać ich 30 i wyzerować 29 pierwszych, albo musi przyjmować
    tablicę mieszającą, co z kolei zaśmieca kod w innych miejscach, ze względu na
    wspomniany brak wersji shorthand."
- id: 3265
  author: sprae
  author_url: ''
  date: '2006-02-06 01:21:32 +0100'
  date_gmt: '2006-02-06 00:21:32 +0100'
  content: Nie wiem jak wy, ale ja uwazam php za jezyk warstwy view. Do uzywania go
    do czegos wiecej troche traci myszka.
- id: 3267
  author: 'NuLL'
  author_url: http://www.null.avx.pl
  date: '2006-02-06 02:26:37 +0100'
  date_gmt: '2006-02-06 01:26:37 +0100'
  content: "Pisze w PHP 5 może 6 lat - dokładnie nie pamiętam i boli mnie to jak oczerniasz
    ten język. Nie mowie ze jest idealny, ale czesc rzeczy jakie pisujesz jest dosc
    dziwna.\r\n\r\n<blockquote>Brakuje mi też często nazwanych parametrów. Jeśli funkcja
    ma być elastyczna to albo podając jeden parametr trzeba podać ich 30 i wyzerować
    29 pierwszych, albo musi przyjmować tablicę mieszającą, co z kolei zaśmieca kod
    w innych miejscach, ze względu na wspomniany brak wersji shorthand.</blockquote>\r\nDziwnie
    projektujesz swoje funkcje albo podajesz absurdalne argumenty aby oczernic PHP
    - co jest zalosne. Pozatym istnieje func_get_args jesli pisujesz tak absurdalne
    funkcje.\r\n<blockquote>Nie wiem jak wy, ale ja uwazam php za jezyk warstwy view.
    Do uzywania go do czegos wiecej troche traci myszka.</blockquote>\r\nPobaw sie
    ezPublishem albo SugarCRM i zobacz co mozna w nim osiagnac.\r\n\r\nCo do zmiennych.
    Uwazam ze nie ma nic zlego w tym ze nie trzeba ich deklarowac. Ja wiem co jest
    w danej zmiennej - bynajmmiej staram sie nie miec takiego smietnika w kodzie aby
    nie wiedziec jakiego typu jest dana zmienna. Pozatym czy PHP broni ci jawnie konwertowac
    zmienne jesli tak ci to potrzebne bo mowisz ze masz burdel ( BTW to ze masz burdel
    to twoja wina ) ?\r\n<code>$zmienna=(string)$zmienna;//oto twoja konwersja</code>"
- id: 3269
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-02-06 10:01:23 +0100'
  date_gmt: '2006-02-06 09:01:23 +0100'
  content: "NuLL:\r\n\r\nPrzeczytaj jeszcze raz, a potem się unoś, bo głupoty piszesz.\r\n\r\n<blockquote>Dziwnie
    projektujesz swoje funkcje albo podajesz absurdalne argumenty aby oczernic PHP
    - co jest zalosne. Pozatym istnieje func_get_args jesli pisujesz tak absurdalne
    funkcje.</blockquote>\r\n\r\nŻałosna jest twoja neiznajomość nazywanych parametrów
    funkcyjnych. Często potrzebuję mieć funkcję, która może przyjmować kilka różnych
    kombinacji parametrów. Raz bierze pierwszy i trzeci, drugi raz pierwszy i siódmy
    albo trzeci i piąty. W takich przypadkach PHP zmusza mnie do przekazywania do
    funkcji tablicy asocjacyjnej:\r\n\r\n<blockquote><pre>foo( array( 'bar' => 1,
    'baz' => 'lorem ipsum' ) );</pre></blockquote>\r\n\r\nW sensowniej zbudowanych
    językach mógłbym napisać tylko:\r\n\r\n<blockquote><pre>foo( bar: 1, baz: 'lorem
    ipsum' );</pre></blockquote>\r\n\r\n<blockquote>Pozatym czy PHP broni ci jawnie
    konwertowac zmienne jesli tak ci to potrzebne bo mowisz ze masz burdel ( BTW to
    ze masz burdel to twoja wina ) ?</blockquote>\r\n\r\nJa nie mam burdelu w zmiennych,
    ale wystarczy literówka, żebym tego błędu musiał potem szukać przez godzinę. Jeśli
    mam zmienną <code>$foo</code> i chwilę później przypiszę coś do <code>$fooo</code>,
    to PHP nawet nie spróbuje mi powiedzieć, że -- świadomie lub nie -- stworzyłem
    sobie właśnie kolejną bezużyteczną zmienną.\r\n\r\nTak samo nie powie mi, że --
    niechcący -- zamiast <code>$foo->setBaz('a')</code> napisałem <code>$foo->getBaz('a')</code>,
    chociaż ta ostatnia metoda nie bierze wcale parametrów (PHP zakłada, że każda
    funkcja przyjmuje dowolną liczbę parametrów, bo przecież wewnątrz może się do
    nich dostać przez <code>func_get_arg</code>).\r\n\r\nW PHP programuję od 8 lat
    i możesz sobie darować zarzucanie mi nieznajomości języka czy nieumiejętność jego
    wykorzystania."
- id: 3270
  author: WooKy
  author_url: http://www.wooky.webea.pl
  date: '2006-02-06 10:54:40 +0100'
  date_gmt: '2006-02-06 09:54:40 +0100'
  content: "Ciekawe podsumowanie, niestety smutna prawda jest taka, że większości
    ludzi PHP kojarzy się z banalnym językiem skryptowym w którym co najwyżej można
    sobie napisać licznik odwiedzin na stronie albo prostą księgę gości.\r\n\r\nNiestety
    w sporej części wynika to z czystego braku wiedzy. Moja opinia jest bardzo prosta
    – PHP jest po prostu zdradziecki (jest jak MediaMarkt – ‘nie dla idiotów’ :D).
    Wydaje się łatwym językiem, który pozwala na bardzo dużo (w sensie składni). Jeżeli
    ktoś zaczyna od niego swoją przygodę z programowaniem to jest z góry na straconej
    pozycji i naprawdę czeka go sporo pracy zanim będzie mógł się nazwać programistą
    – fakt stworzy działającą aplikacje ale sam kod będzie tragiczny. \r\n\r\nTraktuje
    PHP jako narzędzie do osiągnięcia odpowiednich celów, nie odważę się pisać w nim
    czegoś co uznam za bardziej funkcjonalne w tradycyjnej aplikacji okienkowej. \r\n\r\nSytuacja
    wymusiła na mnie poznanie PHP jakieś 4 lata temu – wcześniej pisałem całkiem sporo
    w c++ i wydaje mi się, że takie przejście w znacznym stopniu ułatwiło mi całą
    sprawę jakości kodu i podejścia do programowania aplikacji w PHP.\r\nNie wiem
    dlaczego ale mimo tych wszystkich wad - polubiłem ten język."
- id: 3271
  author: onjin
  author_url: http://onjin.net/
  date: '2006-02-06 12:05:15 +0100'
  date_gmt: '2006-02-06 11:05:15 +0100'
  content: "PHP jest zdradziecki i zaczynająć od niego przygodę z programowaniem można
    mieć problemy z przejściem na kolejny poziom wiedzy o dobrym programowaniu.\r\n\r\nZ
    Perl'a przeniosłem się na Python'a, właśnie z powodu wymogu utrzymania odpowiedniej
    składni kodu, która w tym przypadku jest wymagana, a nie zalecana.\r\n\r\nPHP
    jest znany i popierany. Dodatkowo jego rozwój (PHP5) idzie w dobrą (lepszą?) stronę.
    Możemy na niego narzekać, ale i tak wielu z nas go używa. Lepiej więc zająć się
    promowaniem dobrego stylu programowania, informowaniem ludzi, że można tak programować
    właśnie w PHP i ... samemu tak robić.\r\n\r\nWiększe zainteresowanie zastosowaniem
    PHP w poważnych rozwiązaniach na pewno przyczyni się do jego rozwoju.\r\n\r\nBtw:
    ogólnie zgadzam się z podsumowaniem Patrysa."
- id: 3272
  author: Ktos
  author_url: http://www.ktos.info/notatki/
  date: '2006-02-06 12:41:16 +0100'
  date_gmt: '2006-02-06 11:41:16 +0100'
  content: "&gt; Język C, jako język kompilowany do postaci binarnej, posiada bardzo
    rygorystyczną\r\n&gt; kontrolę zgodności typów.\r\nJa, jako stary Pascalowiec,
    powiem, ze naprawdę rygoystyczną kontrolę typów to ma Pascal ;)\r\n\r\nSiedzę
    przy PHP od 3 lat, całkowicie hobbystycznie, i nie umiem go. Nie będę się ukrywał.
    Zwłaszcza, ze jestem zapóźniony, bo PHP5 na oczy prawie nie widziałem ;) Ale język
    mi się bardzo spodobał, zwłaszcza gdy go nieco bardziej poznałem niż \"echo\"
    oraz \"mysql_query\" :)\r\n\r\nZgodzę się, że ślęczenie nad kodem w poszukiwaniu
    literówki jest przerażające - zwłaszcza jeśli ma się nawyki, ze porównanie jest
    realizowane przez operator =, a nie ==. Bardzo mi brakuje rygorystycznej kontroli
    składni i typów Pascala, ale to raczej kwestia przyzwyczajenia. Choć wymóg formatowania
    kodu na wzór Pythona też by się przydał, gdy spoglądam na niektóre własne (i cudze)
    kody czasami.\r\n\r\nPHP nie jest uznawany za poważny język, czy jakikolwiek portal
    (większy) stoi na PHP? Raczej PHP jest językiem hobbystów, małych firm. Cały czas
    się rozwija i mam nadzieję, ze będzie się dało przekonać społeczność, że on już
    wyrósł - nie tylko księgę gości można w nim napisać."
- id: 3273
  author: pthread
  author_url: ''
  date: '2006-02-06 13:41:01 +0100'
  date_gmt: '2006-02-06 12:41:01 +0100'
  content: "Autor tych bzdur, niejaki Patrys nie popisal sie ..., Stary, jak mozesz
    porownywac c/c++, Pythona i PHP ? Przeciez pokazujesz tym samym ze nie rozumiesz
    podstaw sieci web i marketingu a prosciej mowiac zasad panujacych na rynku IT.
    Jestem zdegustowany tym co piszesz...\r\n\r\n1) PHP to prosty jezyk dla zastosowan
    WWW a nie wydajnych bibliotek i rozwiazan do ktorych stosuje sie c++. W czym napiszesz
    serwer proxy, w PHP ??? . Jak mozesz tak porownywac ? W czym napiszesz kolejny
    pakiet pod unixa, w PHP ?\r\n\r\n2) Bez jezyka PHP nie byloby polowy stron Polsce
    i na swiecie. Czy myslisz ze jakis mlokos jest wstanie znalezc serwer na ASP lub
    Java i strzelic taka sama aplikacje, z taka sama szybkoscia jak w PHP. Czy pan
    Zenek z warsztatu bedzie sie uczyl ASP lub Java ? NIE, on nauczy sie PHP bo to
    jest prosty jezyk do prostych rozwiazan. Strzeli sobie skrypt do wyswietlania
    kluczy i bedzie sie cieszyl.\r\n\r\n3) Kto zaplaci ci za duzy serwis w ASP lub
    w Java w takich warunkach jakie aktualnie mamy w Polsce? Bierzesz PHP stawiasz
    na tanim serwerze, bierzesz srednio rozgarnietego programiste (lub wspomnianego
    Pana Zenka) i w mc masz sklep internetowy. Kto ci zaplaci za alternatywne rozwiazania
    w drozszych technologiach ?\r\n\r\n4) Do jakiej bazy sie podpinasz piszac sklep
    internetowy?  Do SqlSerwera, a moze do Oracla 10g wymagajacego wiecej zasobow
    niz twoje wszystkie kompy w domu. Bierzesz malutka, szybka bazke (MySql,Postgres)
    i stawiasz na niej 50 tabelek. Szafa gra. Chcialbys tam uzyc ASP.NET i polaczenia
    z MS SQL ? Czy pan Zenek bedzie zakladal blokady na wiersze? Po jasna cholere
    wytaczac armate na muche? \r\n\r\n5) Jeszcze zrozumialbym gdybys zadal pytanie:
    Jakie znasz zalety i wady pisania w PHP, ale zeby od razu mowic ze caly jezyk
    jest zle napisany, ma zla koncepcje... Stary nad tym siedzialo setki ludzi zeby
    takie ludziki jak ty mogly powielac i rzezbic strony.\r\n\r\n7) Bez urazy, ale
    pisalem projekt w C++ pod debiana przez rok, od dluzszego czasu (&gt;1,5r) pisze
    duze aplikacje bankowe i twoje porownanie pasuje jak piesc do nosa. Zreszta jak
    mozna bedac monotematycznym (piszac tylko w PHP) porownywac jezyki. Po drugie
    przeciez jezyk w programowaniu jest wyjatkowo nieistotny, mozesz znalezc prawie
    kazde rozwiazanie ktore przeniesiesz pomiedzy wszystkimi jezykami pod weba. Polecam
    google. Poczytaj.\r\n\r\nPozdrawiam wylewnie"
- id: 3274
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-02-06 15:54:20 +0100'
  date_gmt: '2006-02-06 14:54:20 +0100'
  content: Aż mi się nie chce odpisywać, ubawiłem się setnie. Popracuj nad gramatyką,
    ortografią i czytaniem.
- id: 3279
  author: 'NuLL'
  author_url: http://www.null.avx.pl
  date: '2006-02-06 21:59:23 +0100'
  date_gmt: '2006-02-06 20:59:23 +0100'
  content: Patrys - nie jestes w stanie odpisac. Twoje zdanie nie jest nieomylne.
    Wnioski i argumenty ktore sa w twoim poscie sa bledne poprostu. A osoba piszaca
    powyzej ma racje - i nie wymiguj sie jezykiem polskim
- id: 3280
  author: mroq
  author_url: http://mroq.jogger.pl
  date: '2006-02-06 23:16:30 +0100'
  date_gmt: '2006-02-06 22:16:30 +0100'
  content: "Nie jestem za ani przeciw zdaniu Patrysia (jak to odmieniac?), zauważam
    jednak pewną niepokojącą rzecz w notkach takie jak ta. \r\n\r\nOtóż piszesz Patrys,
    że Cię boli kilka rzeczy w PHP, wymieniasz je i okazuje się, że w przeważającej
    części są to bolączki polegające na zbyt dużej dowolności języka. W życiu mi się
    nie zdarzyło, żebym narzekał na wolny wybór w jakiejś kwestii.\r\n\r\nOdsiewając
    te rzeczy, przechodzimy do kolejnych Twoich argumentów, o których na końcu notki
    piszesz, cytuję:\r\n\r\n<blockquote>Na szczęście, przynajmniej część z tych problemów
    zostanie lub została już zniwelowana.</blockquote>\r\n\r\nPozostają może z dwa
    poważne zarzuty przeciwko PHP, które też jakby nie mają racji bytu z powodu specyfiki
    tego języka i jego zastosowań.\r\n\r\nReasumując napisałeś notkę, która mami mnogością
    argumentów przeciwko PHP, a tak naprawdę, gdyby ją okroić ze zbędnych zabiegów,
    zostałoby może z 10 linijek wartościowego tekstu. Próbujesz zasłaniać się wątkiem
    \"postrzegania PHP przez społeczność\" programistyczną, ale o tym \"postrzeganiu
    piszesz\" jakby przy okazji. \r\nPoruszone przez Ciebie zagadnienia to temat rzeka,
    który próbujesz zmieścić w kilku ciasnych argumentach.\r\n\r\nPozdrawiam\r\nmroq"
- id: 3281
  author: m
  author_url: ''
  date: '2006-02-07 00:43:58 +0100'
  date_gmt: '2006-02-06 23:43:58 +0100'
  content: "Tak czytam te komentarze i... postaram się odpowiedzieć jednak w mało
    dosadny sposób, choć część autorów takich autorytarnych, a tym samym głupich,
    komentarzy, na takie miłe traktowanie bystrością swoich wniosków nie zasłużyła.\r\n\r\n1.
    Kilka najgłupszych komentarzy błądzi wokół tego, że Patrys rzekomo napisał, że
    php jest do dupy. Polecam powstrzymanie się przed dzieleniem swoim wylewnym ego
    i przeczytanie najpierw tytułu \"Dlaczego PHP jest do niczego?\", a potem pierwszego
    zdania \"Nie jest.\".\r\n\r\n2. Języki z dynamicznym typowaniem marnie się sprawdzają
    w budowanie dużych systemów. I nie, ezpublish czy inne pierdoły to nie są duże
    systemy. Duże systemy wymagają nakładu pracy przekraczającego 100 osobolat. I
    takie systemy powstają przede wszystkim w językach silnie typowanych, bo tylko
    takie języki pozwalają na wyłapywanie wielu bzdurnych błędów na etapie kompilacji.
    A php... oj, przecież php nie ma kompilacji! A może to zaleta... oczywiście! Ale
    w przypadku budowania małych systemów, nie dużych.\r\n\r\n3. Debugowanie. Czy
    ktoś wie, jak wprowadzić do php ciągłą integrację, jak zrobić przeźroczyste logowanie,
    jak sprawdzać jakość kodu aplikacji php, jak debugować aplikację produkcyjną działającą
    online? Nie.... ale nie dlatego, że nie wie, ale dlatego, że nie ma w ogóle świadomości
    istnienia takich problemów.\r\n\r\n4. Ktoś tu wspomina zaśliniony o pisaniu aplikacji
    php w mc. I właśnie o takich ludziach pisze Patrys - to oni sprawiają, że php
    jest postrzegane jako gówniany język. Ta teza nie jest dyskusyjna - to fakt. Ktoś
    także wspomina o tym, że wprowadza taki porządek w \"swoim kodzie\", że wszystko
    jest OK. Zapomina jednak o tym, że nie ma czegoś takiego jak \"mój kod\" - każdy
    fragment kodu musi być czytelny dla każdego w zespole. A jeśli tych taki zespół
    składa się z ponad 10 osób? A z 50? Prawda jest taka, że zdecydowana większość
    aplikacji php5 nie jest pisana obiektowo, bo ten język ani nie wspiera od podstaw
    dwóch paradygmatów obiektowości, jakimi są dziedziczenie, polimorfizm i enkapsulacja
    (ba! oczywiście, że można to zrobić w php, ale trzeba chcieć - sam język konstrukcji
    obiektowych nie wymusza). A faktem jest, że po przekroczeniu pewnego progu rozwijanie
    aplikacji strukturalnych jest zajebiście trudne, bo nie można ich sensownie i
    czytelnie modelować i analizować na poziomie abstrakcji wyższym niż kod.\r\n\r\n5.
    I jeszcze jedna sprawa - ktoś pisze, że mnogość rozwiązań języka nie powinna być
    wadą. Niestety, ale w zastosowaniach komercyjnych, przemysłowych i po prostu poważnych
    - jest. Gdyby aplikacja tworzona była w języku, który udostępniałby konstrukcje
    strukturalne, obiektowe i funkcyjne, to przy większym projekcie rozwijanym przez
    wiele osób powstałby z tego jeden wielki nieczytelny śmietnik. To nieukninione.
    Popularność C# i Java w ogromnych systemach finansowych, bankowych, raportujących
    nie wzięła się znikąd. Te języki wspierają czysty kod, C/C++ pilnują przytomności
    programisty, a php ma to wszystko gdzieś, co zresztą objawia zwykle dopiero podczas
    wykonania w zwykle nieczytelny sposób.\r\n\r\n6. Programowałem w php wystarczająco
    długo, żeby wiedzieć, kiedy stosować php, a kiedy nie.\r\n\r\n7. PHP to fajny
    język, ale rozwijanie w nim maciupeńkich projektów 4-osobowych staje się w dłuższym
    okresie bardzo bardzo kłopotliwe. A kłopoty to strata czasu i pieniędzy.\r\n\r\nJeśli
    ktoś ma więcej niż 5 lat (łącznie) komercyjnego doświadczenia w wytwarzaniu oprogramowania,
    pracował przy projekcie większym niż ja-kolega-koleżanka, jest nie tylko programistą,
    ale też projektantem i potrafi odróżnić opinię od dekretu, to proszę o komentarz.
    Innym radzę poczekać aż mamy przestaną nos wycierać."
- id: 3282
  author: m
  author_url: ''
  date: '2006-02-07 01:13:32 +0100'
  date_gmt: '2006-02-07 00:13:32 +0100'
  content: I jeszcze jeden wielki bzdet - Oracle 9i i 10g oraz SQL Server 2000 i 2005
    spokojnie chodzą na developerskich stacjach roboczych nie tylko jako serwery baz
    relacyjnych, ale też jako hurtownie danych i systemy analityczne. Systemy webowe
    to straszny pryszcz w porównaniu z naprawdę dużymi systemami OLTP czy OLAP. A
    do wymagań choćby DB2 obu tym serwerom bardzo, bardzo daleko. No ale najpierw
    trzeba mieć jakiekolwiek doświadczenie, żeby móc sformułować choćby choć trochę
    wiarygodną opinię...
- id: 3284
  author: qvist
  author_url: http://stadiony.net
  date: '2006-02-07 02:09:15 +0100'
  date_gmt: '2006-02-07 01:09:15 +0100'
  content: bo w Polsce jest problem z czytaniem ze zrozumieniem. wszystko wina PiS-u
- id: 3286
  author: mroq
  author_url: http://mroq.jogger.pl
  date: '2006-02-07 02:16:50 +0100'
  date_gmt: '2006-02-07 01:16:50 +0100'
  content: "m:\r\n\r\n<blockquote>\r\n5. I jeszcze jedna sprawa - ktoś pisze, że mnogość
    rozwiązań języka nie powinna być wadą. Niestety, ale w zastosowaniach komercyjnych,
    przemysłowych i po prostu poważnych - jest. Gdyby aplikacja tworzona była w języku,
    który udostępniałby konstrukcje strukturalne, obiektowe i funkcyjne, to przy większym
    projekcie rozwijanym przez wiele osób powstałby z tego jeden wielki nieczytelny
    śmietnik.\r\n</blockquote>\r\n\r\nOburzasz się na komentarze zaślinionych nie
    potrafiąc jednocześnie wyciągnąć sensu z prostych zdań. Niestety nie wiem co gorsze,
    czy ludzie zaślepieni w swoim uwielbieniu dla danego języka, czy programiści z
    tzw. \"doświadczeniem\" piszący truizmy, o których ma pojęcie każdy średnio rozwinięty
    szympans.\r\n\r\nBtw. dyskutować o przewadze javy czy c# nad PHP w rozwiązaniach
    bankowych to według mnie dokładnie tak jak przytakiwać hiszpanowi, gdy ten mówi,
    że portugalski to język dla wieśniaków."
- id: 3289
  author: Librarian
  author_url: ''
  date: '2006-02-07 03:03:14 +0100'
  date_gmt: '2006-02-07 02:03:14 +0100'
  content: "Nigdy bym się nie spodziewał, że reakcję <strong>części programistów (?*)</strong>
    na wpis Patrysa będę mógł porównać do histerii <strong>części wyznawców islamu**</strong>,
    wywołanej karykaturami Allacha i Mahometa.\r\nTo przykre.\r\n\r\nCzytam regularnie
    blog Patrysa. Interesuje mnie to, co ma do powiedzenia. I nic więcej.\r\nTo normalne?\r\n\r\nZnam
    jednak ludzi, którzy chcą być Patrysem. Nie przesadzam. Czytają ten blog, bo widzą
    w nim odbicie swoich własnych przemyśleń i cieszą się, że <em>Patrys myśli tak
    samo jak ja</em>. Dokładnie w tej kolejności. Raz na jakiś czas, w celu zachowania
    100% kompatybilności z Patrysem, zmienią kolejność. Przy okazji zmienią doctype
    z XHTML 1.1 na 1.0 Transitional bo <a href=\"http://www.room-303.com/blog/2005/12/15/uwazaj-na-xhtml/\"
    title=\"Uważaj na XHTML\" rel=\"nofollow\">trzeba</a> uważać.\r\nTo również jest
    przykre.\r\nCzasami myślę, że to jest syptom chorobowy.\r\n\r\nSą też gorsze przypadki.
    Nie wiem jak je kwalifikować. Chcą być Patrysem, ale nie mogą? Brakuje im czegoś?
    A może zajmuje ich miejsce? Ma swoje zdanie? Co? Aha, że w ogóle jest jakiś Patrys.\r\nOdpadam.
    Nie rozumiem.\r\n\r\nCoraz bardziej chcę uruchomić własny blog. Znajdę chwilę
    wolnego czasu i to zrobię. Nikt specjalnie mnie nie zna. Znajomi, przyjaciele.
    Wiem jednak, że obok czytelników pojawiac się będą bezmyślne human-boty, akceptujące
    jedynie nagłówki i poirytowane tym, że ktoś oprócz umiejętności zbudowania wypowiedzi
    wielokrotnie złożonej ma swoje prwatne zdanie na jakiś temat.\r\nAle wk*****nie
    bywa bardzo inspirujące.\r\n\r\nNie żyję z budowania aplikacji webowych. Bardzo
    lubię PHP. To fajny język. Nie jestem jednak jakimś wyjątkowym fachurą. Czasami
    tak samo jak wielu z Was spędzam bezsensowne godziny na poszukiwaniu głupiej literówki.
    Wtedy bardzo nie lubię PHP. To najgorszy syf jaki świat widział. Czuję się jakbym
    pod moim biurkiem zamiast wydajnej stacji roboczej czaił się Eniac, a ja muszę
    wleźć mu do środka w poszukiwaniu uszkodzonej lampy. Tej jednej z 18 800 sztuk.\r\nI
    to jest bardzo frustrujące.\r\n\r\nNajgorsze, że tak samo zachowuje się moje Renault
    Clio. Nigdy przed odpałką nie powie, że dziś nici z jazdy. Nie powie też dlaczego.
    Przyjdzie niedługo pora na coś lepszego. Lubie to moje pierwsze, stare już autko,
    ale nie chcę widzieć smutnej miny synka dzień po tym, jak któregoś letniego popołudnia
    obiecam mu, że jutro śmigniemy nad morze.\r\nWiem, że to normalne.\r\nNikt mnie
    nie przekona, że jest inaczej.\r\n\r\nPozdrawiam\r\n\r\nPS. Przepraszam za rozgadnie.
    Względnie patos."
- id: 3293
  author: m
  author_url: ''
  date: '2006-02-07 11:04:02 +0100'
  date_gmt: '2006-02-07 10:04:02 +0100'
  content: "<blockquote>\r\nBtw. dyskutować o przewadze javy czy c# nad PHP w rozwiązaniach
    bankowych to według mnie dokładnie tak jak przytakiwać hiszpanowi, gdy ten mówi,
    że portugalski to język dla wieśniaków.\r\n</blockquote>\r\n\r\nSęk tylko w tym,
    że niektórzy myślą, że:\r\n- php to język, który nadaje się do wszystkiego,\r\n-
    php to język, który nadaje się do niczego.\r\n\r\nOba te stwierdzenia nie są prawdziwe
    i zarówno oryginalny wpis Patrysa, jak i mój komentarz, są próbą wykazania, dlaczego.
    Nie oburzaj się więc, że porównujemy \"coś z czymś\", bo porównania to podstawa
    sprawa podczas wybierania. A wielu webdeveloperów wybiera właśnie php, co z jednej
    strony nie zawsze musi być dobrą decyzją, a z drugiej wiążą się z takim wyborem
    pewne przykre następstwa, o których piszemy. Nie musisz się z tym zgadzać - ale
    nie możesz też zarzucać nam nieprawdy."
- id: 3294
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-02-07 12:08:42 +0100'
  date_gmt: '2006-02-07 11:08:42 +0100'
  content: "<blockquote>1) PHP to prosty jezyk dla zastosowan WWW a nie wydajnych
    bibliotek i rozwiazan do ktorych stosuje sie c++. W czym napiszesz serwer proxy,
    w PHP ??? . Jak mozesz tak porownywac ? W czym napiszesz kolejny pakiet pod unixa,
    w PHP ?</blockquote>\r\n\r\nNie na temat. Jeśli pominąć błąd rzeczowy -- pakietów
    się nie pisze -- zupełnie bez związku z moim postem.\r\n\r\n<blockquote>2) Bez
    jezyka PHP nie byloby polowy stron Polsce i na swiecie. Czy myslisz ze jakis mlokos
    jest wstanie znalezc serwer na ASP lub Java i strzelic taka sama aplikacje, z
    taka sama szybkoscia jak w PHP. Czy pan Zenek z warsztatu bedzie sie uczyl ASP
    lub Java ? NIE, on nauczy sie PHP bo to jest prosty jezyk do prostych rozwiazan.
    Strzeli sobie skrypt do wyswietlania kluczy i bedzie sie cieszyl.</blockquote>\r\n\r\nI
    bardzo dobrze, że by nie było. Połowa stron na świecie nadaje się absolutnie do
    niczego. Języki programowania nie są rozwijane dla script kiddies tylko dla programistów.
    Dalej nie na temat, bo nigdzie nie napisałem, że PHP jest złe.\r\n\r\n<blockquote>3)
    Kto zaplaci ci za duzy serwis w ASP lub w Java w takich warunkach jakie aktualnie
    mamy w Polsce? Bierzesz PHP stawiasz na tanim serwerze, bierzesz srednio rozgarnietego
    programiste (lub wspomnianego Pana Zenka) i w mc masz sklep internetowy. Kto ci
    zaplaci za alternatywne rozwiazania w drozszych technologiach ?</blockquote>\r\n\r\nBierzesz
    kiepskiego programistę i masz kiepski kod w kiepskim projekcie z kiepskimi perspektywami
    na rozwój i utrzymanie. A, na dłuższą metę, na horyzoncie rysuje się refaktoring
    za 10 razy większe pieniądze.\r\n\r\n<blockquote>4) Do jakiej bazy sie podpinasz
    piszac sklep internetowy? Do SqlSerwera, a moze do Oracla 10g wymagajacego wiecej
    zasobow niz twoje wszystkie kompy w domu. Bierzesz malutka, szybka bazke (MySql,Postgres)
    i stawiasz na niej 50 tabelek. Szafa gra. Chcialbys tam uzyc ASP.NET i polaczenia
    z MS SQL ? Czy pan Zenek bedzie zakladal blokady na wiersze? Po jasna cholere
    wytaczac armate na muche?</blockquote>\r\n\r\nJeśli twój Oracle wymaga takich
    zasobów, to chyba prowadzisz na nim system rozliczeń międzybankowych. Z powodzeniem
    mogę sobie Oracla trzymać jako usługę na swoim laptopie. Bez problemu przeżyłby
    obciążenie generowane przez średnich rozmiarów sklep internetowy. MS SQL nie używam,
    bo nie lubię -- uważam jego dialekt za niewygodny, poza tym -- MS SQL nie działa
    w dalszym ciągu na maszynach *niksowych. Pan Zenek i cały punkt jest dalej off-topic.\r\n\r\n<blockquote>5)
    Jeszcze zrozumialbym gdybys zadal pytanie: Jakie znasz zalety i wady pisania w
    PHP, ale zeby od razu mowic ze caly jezyk jest zle napisany, ma zla koncepcje…
    Stary nad tym siedzialo setki ludzi zeby takie ludziki jak ty mogly powielac i
    rzezbic strony.</blockquote>\r\n\r\nWypisałem wady i zalety. Nikogo o nic nie
    pytam, bo to mój prywatny blog, a nie serwis z poradami na lepsze życie. A zdanie
    o źle napisanym języku świadczy o braku umiejętności czytania ze zrozumieniem.
    Ostatni argument jest na poziomie <q>oglądaj Idola i BigBrothera, miliony ludzi
    nie mogą się mylić.</q>\r\n\r\n<blockquote>7) Bez urazy, ale pisalem projekt w
    C++ pod debiana przez rok, od dluzszego czasu (>1,5r) pisze duze aplikacje bankowe
    i twoje porownanie pasuje jak piesc do nosa. Zreszta jak mozna bedac monotematycznym
    (piszac tylko w PHP) porownywac jezyki. Po drugie przeciez jezyk w programowaniu
    jest wyjatkowo nieistotny, mozesz znalezc prawie kazde rozwiazanie ktore przeniesiesz
    pomiedzy wszystkimi jezykami pod weba. Polecam google. Poczytaj.</blockquote>\r\n\r\nBez
    obrazy, ale ja przy budowaniu oprogramowania pracuję od dawna i nie zamierzam
    się prześcigać w długości przyrodzenia. Wystarczy powiedzieć, że pracowałem przy
    podobnego rozmiaru aplikacjach, pisanych tak w C++, jak i webaplikacjach budowanych
    w C#, Pythonie, Perlu, PHP czy nawet CGI na ANSI C.\r\n\r\nNie zmienia to faktu,
    że nie zrozumiałeś nic z mojej notki. A wynika z niej tylko tyle, że PHP jest
    powszechnie uważany za język dla idiotów (co potwierdzasz sam swoim Panem Zenkiem),
    że spora część programistów PHP nie ma pojęcia o architekturze kodu i produkcji
    kodu, który będą w stanie czytać i analizować ludzie (co potwierdza kilka komentarzy
    wyżej, choćby ten o <q>porządku w kodzie</q>), że PHP momentami mnie za bardzo
    ogranicza (a nie ma nic gorszego dla morale programisty niż uczucie, że mógłby
    pracować wydajniej, gdyby tylko język się do tego nadawał -- odechciewa się wszystkiego)
    i że elastyczność PHP utrudnia jakiekolwiek próby sensownego debugowania i śledzenia
    kodu za pomoca konwencjonalnych narzędzi (przez co nie nadaje się do dużych projektów
    -- ryzyko wyłapania regresji po deployu na produkcję jest zbyt duże, nawet przy
    zastosowaniu prostych bibliotek do budowania unit-testów)."
- id: 3295
  author: mroq
  author_url: http://mroq.jogger.pl
  date: '2006-02-07 12:24:29 +0100'
  date_gmt: '2006-02-07 11:24:29 +0100'
  content: "m:\r\n\r\noch, przecież pisanie o wadach PHP czy javy jest bez najmniejszego
    sensu. Raz, że w sieci jest kupa takich tekstów, a dwa, że nie można powiedzieć
    o wyborze danego języka do nauki programowania jako złej decyzji (z takich czy
    innych przyczyn). \r\n\r\nZłota zasada programistów mówi o \"stosowaniu odpowiednich
    rozwiązań do odpowiednich problemów\" i uwierz mi, że mimo iż\r\n\r\n<blockquote>\r\nniektórzy
    myślą, że:\r\n- php to język, który nadaje się do wszystkiego,\r\n- php to język,
    który nadaje się do niczego.\r\n</blockquote>\r\n\r\nto prędzej czy później życie
    ich z tego myślenia wyleczy i według mnie każdy musi się o tym przekonać na własnej
    skórze. Mniej pożytku będzie z programisty, który przeczytał, że nie wolno w TYM
    pisać TAKICH projektów, bo parzy niż z człowieka, który sparzył się i zaczął samodzielnie
    myśleć.\r\n\r\nMoim zdaniem tekst Patrysia (odmiana?) aż prosił się o te wszystkie
    flejmy u góry, a mając w pamięci jedną z jego ostatnich notek nt. \"dobrego contentu\"
    mocno się zdziwiłem, że zdecydował się na umieszczenie tego wpisu na blogu. \r\n\r\nMało
    tego, ten blog coraz mocniej jest utożsamiany z takim radosnym miejscem, gdzie
    flejmy są na porządku dziennym, a szkoda.\r\n\r\nBtw. mnogość rozwiązań w przypadku
    PHP to jedna z jego największych zalet, a że niektórzy próbują w tym pisać rozległe
    aplikacje bankowe.. no cóż."
- id: 3296
  author: m
  author_url: ''
  date: '2006-02-07 12:54:03 +0100'
  date_gmt: '2006-02-07 11:54:03 +0100'
  content: "<blockquote>\r\noch, przecież pisanie o wadach PHP czy javy jest bez najmniejszego
    sensu. Raz, że w sieci jest kupa takich tekstów, a dwa, że nie można powiedzieć
    o wyborze danego języka do nauki programowania jako złej decyzji (z takich czy
    innych przyczyn).\r\n</blockquote>\r\n\r\nZnasz jakiś kompetentny tekst o wadach
    php w poważnych rozwiązaniach? Mógłbyś podać linka? I od razu wskaż miejsce, gdzie
    ktoś z nas napisał o \"wyborze danego języka do nauki programowania\".\r\n\r\n<blockquote>\r\nto
    prędzej czy później życie ich z tego myślenia wyleczy i według mnie każdy musi
    się o tym przekonać na własnej skórze.\r\n</blockquote>\r\n\r\nTo twoje zdanie.
    Kompletnie nieprawdziwe, gdy przestaniesz gdybać, a zaczniesz poważnie traktować
    swoją pracę.\r\n\r\n<blockquote>\r\nmnogość rozwiązań w przypadku PHP to jedna
    z jego największych zalet\r\n</blockquote>\r\n\r\nNie zgadzam się, o czym już
    pisałem.\r\n\r\n<blockquote>\r\nMało tego, ten blog coraz mocniej jest utożsamiany
    z takim radosnym miejscem, gdzie flejmy są na porządku dziennym, a szkoda.\r\n</blockquote>\r\n\r\nMam
    dziwne wrażenie, że to m.in. drążysz temat bez wyraźnego kierunku..."
- id: 3297
  author: mroq
  author_url: http://mroq.jogger.pl
  date: '2006-02-07 13:13:28 +0100'
  date_gmt: '2006-02-07 12:13:28 +0100'
  content: "m:\r\n\r\njestem zbyt leniwy, żeby przytaczać Ci linki do opracowań. Ktoś
    komu zależy na tym, na pewno je znajdzie.\r\n\r\n<blockquote>\r\nTo twoje zdanie.
    Kompletnie nieprawdziwe, gdy przestaniesz gdybać, a zaczniesz poważnie traktować
    swoją pracę.\r\n</blockquote>\r\n\r\nOjojoj, personalnie po mnie nie jedź, nieładnie
    tak. Poza tym nie masz wyłączności na \"bycie doświadczonym mastahaka programingu
    i siedmiu niebios\". Podważanie kompetencji to strasznie niski argument w dyskusji.\r\n\r\n<blockquote>\r\nNie
    zgadzam się, o czym już pisałem.\r\n</blockquote>\r\n\r\nMasz zupełne prawo do
    tego.\r\n\r\n<blockquote>\r\nMam dziwne wrażenie, że to m.in. drążysz temat bez
    wyraźnego kierunku…\r\n</blockquote>\r\n\r\nPróbuję jedynie napiętnować kilka
    nieścisłości, które mnie nurtują w sposób, według mnie, dośc kulturalny... jeśli
    jest to flejm to może pora zrezygnować z publicznych dyskusji w tym kraju? ;]"
- id: 3298
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-02-07 15:29:47 +0100'
  date_gmt: '2006-02-07 14:29:47 +0100'
  content: "Czy ja jestem Kottke? Dlaczego ludzie mają mi mówić, co mogę umieścić
    na <em>swoim</em> <strong>blogu</strong>. To jest moje miejsce w sieci i nie bardzo
    rozumiem narzekania.\r\n\r\nJak się wam podoba, to bardzo się cieszę, możecie
    czytać do woli i komentować -- jeśli nie są to osobiste wycieczki po cudzych kompetencjach.
    Dyskusja albo jest na poziomie albo jest bezcelowa. A jak ktoś nie widzi tu żadnej
    wartości, to zapraszam na <code>/dev/drzewo</code>, ustawowego obowiązku czytania
    moich wypocin nie ma.\r\n\r\nNie wiem, czemu, kilku osobom zdaje się przyśniło,
    że są na forum Onetu albo na stronach jakiegoś miesięcznika komputerowego. Nikt
    mi nie płaci za prowadzenie tej strony, nic z tego nie mam i nie zamierzam się
    dostosowywać do żadnych wymagań.\r\n\r\nTo jest miejsce, gdzie wyrażam swoje opinie,
    a te są jak dupa -- każdy ma swoją. Umiejętność dyskutowania polega na swobodnej
    wymianie opinii i zdolności podpierania ich argumentami wyższych lotów niż <q>a
    ja mam dłuższego.</q> Nie jestem bogiem i nie jestem nieomylny, zawsze chętnie
    usłyszę zdanie drugiej strony, ale wtrącenia zealotów (<q>nie masz racji, PHP
    jest boski</q>) i trolli (<q>piszesz tak, bo znasz tylko jeden język i to słabo,
    a w ogóle, to ja nie potrzebuję takich głupot</q>) nie wnoszą nic -- poza zbędnym
    zamieszaniem."
- id: 3300
  author: Wołow
  author_url: ''
  date: '2006-02-07 16:59:40 +0100'
  date_gmt: '2006-02-07 15:59:40 +0100'
  content: 'Patrys a teraz to zachowujesz sie jak riddle: moj blog, moja przestrzen,
    moje cukierki i samodziki. Jeszcze komentarze wylacz ;D'
- id: 3301
  author: m
  author_url: ''
  date: '2006-02-07 18:33:39 +0100'
  date_gmt: '2006-02-07 17:33:40 +0100'
  content: 'Wołow: bo nikt nie lubi, jak ktoś się bezsensownie przypierdala?'
- id: 3302
  author: Wołow
  author_url: ''
  date: '2006-02-07 18:42:44 +0100'
  date_gmt: '2006-02-07 17:42:44 +0100'
  content: 'm: czy bezsensownie to sprawa dyskusyjna.'
- id: 3303
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-02-07 19:14:28 +0100'
  date_gmt: '2006-02-07 18:14:28 +0100'
  content: "Ja nie cenzuruję wypowiedzi, tylko proszę o rozmowy konstruktywne i na
    temat. Gównem można się za darmo poobrzucać na podwórku.\r\n\r\nI zanim ktoś napisze
    komentarz to dobrze, żeby chociaż postarał się przeczytać całą notkę i ją zrozumieć.
    Dzieci tu nie ma, więc zakładam, że każdy maturę z polskiego zdał kiedyś."
- id: 3314
  author: hn
  author_url: ''
  date: '2006-02-09 09:16:04 +0100'
  date_gmt: '2006-02-09 08:16:04 +0100'
  content: "Zdolnosc czytania ze zrozumieniem zanika, gdy obiekt czytajacy natrafia
    na tekst traktujacy o jego religijnych przekonaniach... nothing new under sun...
    :x\r\n\r\nMoja kilkumiesieczna przygode z PHP wspominam raczej srednio. Powody:\r\n-
    PHP to jezyk 'smieciowy', a konkretniej jest to warstwa na warstwie, dorzucane
    bez ladu i skladu kolejne ficzery, bez mysli przewodniej, spojnej skladni (do_something
    vs doSomething vs DoSomething vs do_smth vs blablabla)\r\n- glupia literowka,
    na temat ktorej kompilator (interpreter) ani sie zajaknie (bo przeciez skladniowo
    i semantycznie wszystko gra) a ty szukaj wiatru w polu. Przy braku dobrych narzedzi
    debuggujacych to koszmar\r\n- swiadomosc wsrod programistow PHP, ze przy jezykach
    dynamicznie typowanych (a PHP jest do tego 'weak typed') testy jednostkowe to
    calkiem mily koncept jest zatrwazajaco nieobecna\r\n- refactoring (ten termin
    juz sie przebija w srodowisku programistow pHP, rite? :p) to fajna sprawa, lecz
    znowu dynamicznie typowanie utrudnia tu sprawe - niestety Smalltalk jest tu wyjatkiem
    potwierdzajacym regule, i to bardzo specyficznym wyjatkiem\r\n- srodowiska programistyczne
    troche zassysaja (tak, wiem... vi, emacs, a ostatnio slyszalem, ze prawdziwi programisci
    uzywaja mc...)\r\n\r\nTak to wyglada z mojej perspektywy i z mojego doswiadczenia
    przy pisaniu niezbyt skomplikowanej w sumie aplikacji. W sumie calkiem niedlugo
    moja znajomosc z PHP moze byc odnowiona, ale na szczescie w moim aktualnym miejscu
    pracy ludzie maja doswiadczenia z roznymi jezykami/platformami co mam wrazenie
    przeklada sie na lepsze programowanie takze w PHP..."
- id: 3315
  author: marcink
  author_url: http://blog.elksoft.pl
  date: '2006-02-09 10:51:26 +0100'
  date_gmt: '2006-02-09 09:51:26 +0100'
  content: "<blockquote cite=\"hn\">PHP to jezyk ’smieciowy’, a konkretniej jest to
    warstwa na warstwie, dorzucane bez ladu i skladu kolejne ficzery, bez mysli przewodniej,
    spojnej skladni (do_something vs doSomething vs DoSomething vs do_smth vs blablabla)</blockquote>\r\n\r\nO
    to to.  Jedno z głównych zażaleń, jakie ludzie zawsze mieli do Perla, to chaos
    w nazewnictwie i działaniu funkcji, ale tam wynikał on z przejęcia mnóstwa rozwiązań
    z sh, bash, sed, awk, sed, więc ludzie którzy wcześniej spotykali się z tymi narzędziami
    mieli przynajmniej w jakimś fragmencie ułatwiony start.  W PHP jest po prostu
    chaos wynikający z braku projektu czy chociaż chwili zastanowienia się, jak to
    może wyglądać jeśli język się rozrośnie -- ot, dorzucano nowe funkcje w razie
    potrzeby, bez wprowadzenia jakichkolwiek zasad co do nazewnictwa czy chociażby
    kolejnosci parametrów.  I pisz tu, człowieku, kod z array_push i in_array bez
    zaglądania do dokumentacji.\r\n\r\nPHP rzeczywiście uzyskał etykietkę \"języka
    dla wszystkich\", bo bardzo łatwo i bez jakiegokolwiek przygotowania można sobie
    napisać i wystawić na świat proste hello world.  Próg na wejściu jest prawie zerowej
    wysokości, więc zaczyna w nim programować także wielu ludzi którzy sobie nie dają
    rady z trudniejszymi językami (zanim ktoś to wyrwie z kontekstu wyjaśniam -- nie
    napisałem, że użytkownicy PHP to ci, którzy nie dają sobie rady z trudniejszymi
    językami, proszę czytać uważnie).  Takich ludzi jest bardzo dużo i niestety większość
    kodu PHP z jakim można się zetknąć została napisana bez specjalnych umiejętności
    programistycznych.  To nie jest wina języka, ale jeśli większość napisanego w
    nim kodu jest beznadziejna to sam język niestety też się źle kojarzy."
- id: 3316
  author: Maciej Łebkowski
  author_url: http://lebkowski.info
  date: '2006-02-09 11:11:59 +0100'
  date_gmt: '2006-02-09 10:11:59 +0100'
  content: "@marcink, zamiast dokumentacji możesz spróbować załatwić sobie tzw. API
    do Twojego edytora, który raz, że będzie Ci podpowiadał nazwy funkcji, dwa, kolejność,
    nazwy i typ jej parametrów. Polecam <a href=\"http://scintilla.org/SciTE\" rel=\"nofollow\">SciTE</a>
    lub inne edytory oparte o silnik Scintilla. \r\nPoza tym możesz sobie podpiąć
    spersonalizowanego helpa do PHP, który będzie Cię odsyłał do php.net/keyword,
    na przykład.\r\nP.S, nie, to nie jest żaden argument za/przeciw, jedynie dygresja.
    :)"
- id: 3317
  author: Tomash
  author_url: ''
  date: '2006-02-09 13:36:54 +0100'
  date_gmt: '2006-02-09 12:36:54 +0100'
  content: "Bardzo fajna dyskusja. Osobiście uważam się za programistycznego n00ba,
    ale PHP nie był moim pierwszym językiem programowania (nie był też drugim), a
    i w javie (także tej webowej) trochę popisałem. Patrysa oraz m. mają rację, PHP
    jest postrzegany jak język dla idiotów, bo ci idioci tworzą najwięcej szumu na
    forach. Skrajny przykład - grono tematyczne o PHP. Zresztą Patrys i m. mają rację
    także w innych kwestiach, ale bardzo lubię czytać wypowiedzi \"profesjonalnych
    programistów\" z drugiej strony, na blogu o programowaniu to zawsze odświeżające
    poczytać wypowiedzi ludzi, którzy w swoim \"profesjonalizmie\" zgubili gdzieś
    umiejętność czytania ze zrozumieniem.\r\n\r\nNatomiast jeśli Patrys pisze że Oracla
    bez problemu uciągnie jego domowy laptop - no i dobrze, uciągnie, skoro ten sam
    laptop uciągnie i Quake 4 ;) Ale zjedzone dwieście-trzysta mb ramu \"na dzień
    dobry\" to nie jest szczyt marzeń każdego programisty, nierzadko pracującego na
    mocno wysłużonym sprzęcie."
- id: 3341
  author: ech
  author_url: 'http://:'
  date: '2006-02-11 18:53:09 +0100'
  date_gmt: '2006-02-11 17:53:09 +0100'
  content: "Tytuł powinien brzmieć ,,Piszę w PHP, ale chcę być l33t, guys, wait for
    me!''\r\n\r\nAutofellatio czystej wody."
- id: 3369
  author: become
  author_url: ''
  date: '2006-02-17 14:27:44 +0100'
  date_gmt: '2006-02-17 13:27:44 +0100'
  content: "Windows też niby jest badziewny a używa go 80% ludzi.\r\nNatura ma jeden
    cel - iść na skróty - nigdy pod prąd.\r\nProblem z PHP jest inny. Jest to język
    naturalny, prosty, dla każdego i z tego powodu jest atakowany za tą swoją ogromną
    zaletę.\r\nWielkie Głowy oburzają się, bo w PHP trudno się czymś wyróżnić - każdy
    potrafi programować w PHP.\r\n\r\nLudzie - kto chce niech płynie pod prąd i się
    męczy.\r\nJa tam wolę obrać kurs z nurtem rzeki."
- id: 3370
  author: n00b
  author_url: ''
  date: '2006-02-17 14:34:37 +0100'
  date_gmt: '2006-02-17 13:34:37 +0100'
  content: "Ła jesli chodzi o programowanie to nie boje sie nazywac lama bo mialem
    troche wspolengo z cpp i pascalem. Nie jestem w stanie rozsadzic tego sporu, ale
    wyglada to jak klotnia nad wyzszoscia jednych swiat nad drugimi.\r\n\r\nPatrys
    slusznie zauwazyl ze kazdy ma swoje zdanie i najciekawsze jest to ze w tym wypadku
    powinno dojsc raczje do proby przekonania jedenje strony do drugiej a nie zarzucania
    sie nowymi wizjami\r\n\r\nChyba pojde na psychologie :)"
- id: 3559
  author: aart3k
  author_url: http://www.aart3k.be
  date: '2006-04-16 12:54:14 +0200'
  date_gmt: '2006-04-16 11:54:14 +0200'
  content: "Nieststy część Twojej opinii jest prawdziwa ale nie oceniaj PHP po grupce
    lamerów tytułujących się mianem programistów PHP. Wystarczy wejść na stronkę php.pl
    i poczytać parę postów ludzi profesjonalnie zaznajomionymi z PHP. Ja sam osobiscie
    jestem samoukiem i pierwsze moje skrypty w PHP zaiste były lamerskie, pamięciożerne
    i powolne, lecz dziś, po 3 latach piszę swój framework w oparciu o cechy PHP5,
    z cache'owaniem zbudowanym na XML'u, z możliwością modułowej rozbudowy/modyfikacji
    \ całego systemu (nie odpowiada ci klasa odpowiedzialna za bazę: wymień ją (byle
    byłaby zgodna z interfejsem) , przełącz w konfiguracji i działa bez zarzutu).
    uważam to za dosyć profesjonalne podejście do PHP, z rzutowaniem typów jestem
    zaznajomiony i myślę że brak wiedzy na temat woogóle istnienia typów zmiennych
    wynika z braku potrzeby posiadania takowej eurydycji.\r\n\r\nA co do 11-latków
    fanatyków php: kiedyś jeżeli podtrzymają fascynację zostaną dobrymi informatykami,
    ja sam osobiście zaczynałem od skryptów w AmigaDOS i wcale nieźle to szło (a nawet
    pętli nie umiałem zrobić). IMHO pomogło mi to w dzisiejszym programowaniu i rozumowaniu
    algorytmicznym (co chyba jest najważniejsze w programowaniu).\r\n\r\nJęzyk dla
    wszystkich? Chodzę do technikum informatycznego i 80% mojej grupy nie pojmuje
    PHP. Dziwne? Raczej nie, przyszli do nas sprzętowcy etc. którzy po prostu nie
    mają żyłki do programowania."
- id: 3565
  author: TWOJA STARA
  author_url: htp://twojastara.eu
  date: '2006-04-17 09:36:54 +0200'
  date_gmt: '2006-04-17 08:36:54 +0200'
  content: Ziomek pojebało cie O_o jak  php byłby do dupy to 90% stro w internecie
    byłoby w htmlu lolku patentowy. PHP nie dość że jest banalny to na dodatek tak
    elastyczny, że tylko idiota by sobie nie mógł poradzić
- id: 3581
  author: reod
  author_url: http://reod.ovh.org/home/
  date: '2006-04-22 19:29:39 +0200'
  date_gmt: '2006-04-22 18:29:39 +0200'
  content: "<blockquote cite=\"TWOJA STARA\"> PHP nie dość że jest banalny to na dodatek
    tak elastyczny, że tylko idiota by sobie nie mógł poradzić.</blockquote>\r\nNo
    właśnie napisał o takich jak ty..."
- id: 7656
  author: Miki
  author_url: http://www.maxishop.org
  date: '2007-04-16 01:00:53 +0200'
  date_gmt: '2007-04-16 00:00:53 +0200'
  content: "Ech, zarówno ktoś atakujący Giewont półtorakilowym młotkiem, jak i używający
    dziesięciokilowego młota do łupania orzechów to współczesne odmiany don Kichotów.
    \r\n\r\nPHP to język interpretowany, przeznaczony do zadań domowych i małych projektów.
    Jego podstawową zaletą jest licencja GNU GPL. \r\n\r\nZdejmując czapkę przed doświadczonymi
    kolegami pozwolę sobie jednak zauważyć, że ani narzędzi, ani baz danych, wymienianych
    tutaj nie rozdają za darmo. \r\n\r\nJednym słowem każdemu według potrzeb."
- id: 8502
  author: Tomek
  author_url: http://www.wp.pl
  date: '2007-09-29 08:28:17 +0200'
  date_gmt: '2007-09-29 07:28:17 +0200'
  content: "W PHP pisze od niedawna, kilka miesięcy do roku. \r\nJęzyk ten spodobał
    mi sie, ze względu na podobną składnie do C++, ktorego znam lepiej niż PHP.\r\n\r\nW
    PHP jeszcze nie dorosłem do obiektów, narazie pisze strukturalnie.\r\nW moim widzeniu
    ten język jest dość prosty w nauczeniu, jezeli chodzi o proste aplikacje. \r\n\r\nNapisałem
    kilka mniejszych projektów (niestety strukturalnie) i teraz jezeli bym cos chciał
    zmienić to naprawde bym sie pogubił. \r\nNarazie nie pisze przejrzyście i czasem
    pisze dziwne kilko-linijkowe stwory, ktore mozna zastapic czasem dwoma wyrazami.\r\n\r\nNatomiast
    jesli chodzi o same PHP to język jest w porządku, ale nie jest bez wad.\r\n\r\nOsobiście
    podoba mi sie, ze przed zmiena nie trzeba pisać typu, ponieważ skraca to kod,
    zawsze mozna rzutować.\r\nZ drugiej strony brakuje kontroli typów i czasem mozna
    popełnic powazny błąd logiczny, a parser nas o tym nie poinformuje."
- id: 19112
  author: qqrq
  author_url: ''
  date: '2008-04-11 07:59:25 +0200'
  date_gmt: '2008-04-11 06:59:25 +0200'
  content: "Stary ten wpis, ostatni komentarz dawno temu, ale...\r\n\r\nPo pierwsze
    nie rozumiem jak można miarodajnie ocenić PHP po kilkumiesięcznej przygodzie z
    nim. Ostatnio nawet czytałem jakiś kurs/tutorial Ruby-ego (link do niego jest
    nawet na oficjalnej stronie Ruby-ego -&gt; http://www.apohllo.pl/dydaktyka/ruby/intro/),
    w którym autor pisze o swoim \"doświadczeniu\" z PHP. Polecam przeczytać - autor
    zaczął od dupy strony i tamże skończył. Może jakby się wziął za Prado, czy Symfony
    inaczej by śpiewał.\r\nPo drugie, aart3k =&gt; pisanie swojego frameworka po 3
    latach doświadczenia w PHP to GŁUPI pomysł. Lepiej naucz się jednego z już napisanych.
    Mój kolega powiedział kiedyś, że 10 lat doświadczenia to minimum dla swoich rozwiązań
    tego typu i raczej się z nim zgadzam. Poza tym jakość tekstów na php.pl jest raczej
    dyskusyjna.\r\n\r\nPozdrawiam\r\n\r\nBTW, tekst jest w porządku ;), ale jak dla
    mnie za mało szczegółów."
- id: 19154
  author: majkel
  author_url: http://www.cycki.laski-bikini.pl
  date: '2008-04-15 18:40:51 +0200'
  date_gmt: '2008-04-15 17:40:51 +0200'
  content: super stronka, pozdrawiam
- id: 22981
  author: automatyk
  author_url: ''
  date: '2008-11-20 11:27:22 +0100'
  date_gmt: '2008-11-20 10:27:22 +0100'
  content: "No cóż. Może wypowiem się tutaj jako osoba \"doczepiona z innej branży
    \".\r\nOd 2 lat zajmuję się aplikacjami web. Amatorsko podkreślam. Przerabiałem
    już Ruby, PHP, Pascala, i parę tam innych. Co mnie udeżyło w PHP ? To, że składnia
    tego języka to rzeczywiście, jak to ktoś tu wspomniał \"burdel na kółkach\".\r\nProgramowałem
    zawodowo m.in.maszyny produkcyjne, i czasami było tak, że od danego algorytmu
    mogło zależeć wszystko: awaria maszyny, bezpieczeństwo obsługujących itp.\r\nDlatego
    mam wyrobione nawyki tworzenia algorytmów LOGICZNYCH I DZIAŁĄJĄCYCH.\r\nUjmę w
    skrócie. Programowanie w każdym języku który przez te 2 lata poznałem to dla mnie
    przyjemność. Gdy posiedziałem trochę nad PHP przeżegnałem się nogą.\r\nJest to
    niezgrabny, przeładowany niepotrzebną funkcjonalnością twór, będący karykaturą
    języka programowanie."
- id: 22983
  author: Łukasz Adamczuk
  author_url: http://adamczuk.net.pl
  date: '2008-11-20 15:02:48 +0100'
  date_gmt: '2008-11-20 14:02:48 +0100'
  content: "Programuję w PHP od dobrych 5 lat, również obiektowo i zgadzam się, że
    sam język ma wiele braków. To, że pewne rzeczy pozwala robić łatwiej i szybciej
    to jedno. Inna sprawa, że pewnych rzeczy nie pozwala robić wcale, bo wspiera archaiczne
    rozwiązania sprzed lat.\r\n\r\nJednak to jakim każdy jest programistą zależy od
    niego. Jeśli potrafi być zdyscyplinowany i tworzyć logiczny kod, mimo tego, że
    sam PHP pozwala na wszystko to jego sukces. Jeśli pomimo tego, braki w PHP utrudniają
    nam pracę to istnieje wiele innych podobnych technologii. Tylko od nas zależy
    jaki kod będziemy udostępniać."
- id: 24324
  author: Jam
  author_url: ''
  date: '2009-02-26 22:37:08 +0100'
  date_gmt: '2009-02-26 21:37:08 +0100'
  content: "Kumpel ma taki własny, prywatny projekt, PPhp. Zamierza napisać \"łatkę\"
    na PHP... korzystając z PHP. W jego klasie umieszczaszlink do folderu z plikami
    w jego języku, a on je live przetwarza na poprawione PHP, ewentualnie wyświetla
    błąd, zapisuje i wyświetla. Swoistego rodzaju projekt poprawiający jakość kodu
    ;) \r\n\r\nJak dla mnie to szaleństwo"
- id: 24580
  author: Stachu
  author_url: ''
  date: '2009-11-22 11:12:02 +0100'
  date_gmt: '2009-11-22 10:12:02 +0100'
  content: "Tomash \r\n9. lut 2006 at 13:36 \r\nnapisał:\r\n\r\n\"Patrysa oraz m.
    mają rację, PHP jest postrzegany jak język dla idiotów, bo ci idioci tworzą najwięcej
    szumu na forach. \"\r\n\r\nTo wejdź sobie na polskie forum RoR. Zobacz ile tam
    szunu robią inni idioci.\r\nDyskusje tak beznadziejne o dupie marynie i RoR jako
    ósmym cudzie świata, że nie\r\nwiesz, czy im wspóczuć, czy się za nich pomodlić.\r\n\r\nA
    Patrys to jedna z tych osób, która po prostu czuje się lepsza, gdy korzysta z
    czegoś odmiennego niż większość gawiedzi.\r\nSkoro ma uznanie wśród kolegów dla
    tego, że programuje w Pythonie pewnie nie dawał sobie z PHP rady.\r\n\r\nKtoś
    kiedyś napisał \"nie potrafisz pojąć php - spróbuj czegoś innego\".\r\nPo takich
    blogach jak ten i forach RoR czy Pythona poznać, że miał rację."
- id: 24853
  author: taktu
  author_url: ''
  date: '2010-02-27 15:10:09 +0100'
  date_gmt: '2010-02-27 14:10:09 +0100'
  content: taka opinia jaki programista
---
<p>Nie jest. Tytuł powinien brzmieć raczej:</p>

<ul>
<li>Dlaczego, kiedy mówię, że programuję w C/C++, ludzie czują respekt?</li>
<li>Dlaczego, kiedy mówię, że programuję w Pythonie, podają mi rękę?</li>
<li>Dlaczego, kiedy mówię, że programuję w <abbr title="PHP Hypertext Preprocessor">PHP</abbr>, ludzie śmieją się do rozpuku?</li>
</ul>

<p>To trochę jak z Polakami za granicą. Ludność autochtoniczna ocenia ich nie po tym, kim naprawdę są, ale po tych jednostkach, które widać najbardziej. Po kiepsko ubranych, niedomytych pijusach spod marketów. Podobnie jest z programistami <abbr>PHP</abbr>.</p>

<p>Język zaczął jako mało popularny silnik do osadzania prostych, krótkich skryptów wewnątrz kodu <abbr title="HyperText Markup Language">HTML</abbr>. Nie oferował wiele -- programowanie proceduralne, zmienne bez reguł typowania, wektory zwykłe i tablice mieszające. Z czasem nabrał popularności i zrobiło się o nim w sieci głośno. Pojawiały się kolejne tutoriale, pisane tak przez doświadczonych ludzi, jak przez laików. Język był tak prosty, że nawet dziecko było w stanie wykonać w nim proste operacje i podzielić się swoją pracą z innymi.</p>

<p>Z czasem platforma ewoluowała i zyskiwała na funkcjonalności. Zyskała sobie poklask wśród firm hostingowych ze względu na łatwość utrzymania -- wystarczyło dodać jeden moduł do serwera <abbr title="World Wide Web">WWW</abbr> i wszystko zaczynało <q>magicznie</q> działać. Lawina nabrała masy i zaczęła napędzać się sama. Już kilka lat temu można było bez trudu znaleźć strony jedenasto-/dwunastolatków zafascynowanych <abbr>PHP</abbr>. Kolejne wydawnictwa prześcigały się w publikacji tomów opiewających wspaniałość języka. Pozycje książkowe były lepsze lub gorsze, z przewagą tych pierwszych. Powtórzyła się sytuacja z językiem <abbr>HTML</abbr>.</p>

<p>Od kiedy <abbr>PHP</abbr> uzyskało etykietkę <q>języka dla wszystkich,</q> język zaczął gwałtownie tracić w oczach środowiska profesjonalistów. Zaczął być kojarzony ze wspomnianymi dziećmi i niedzielnymi <q>hakerami,</q> którzy wdrożenie aplikacji rozpoczynali od lektury dwóch, wątpliwej jakości, tutoriali w sieci, a następnie tytułowali się ekspertami w dziedzinie webaplikacji. Tak jest do dziś -- <abbr>PHP</abbr> kojarzone jest z proceduralnym kodem, brakiem separacji warstw logiki i prezentacji, brakiem dokumentacji projektowej, konstrukcjami składniowymi na miarę niesławnego Visual Basica i aplikacjami, które raz napisane, nie nadają się ani do powtórnego użycia ani późniejszej modyfikacji.</p>

<p>Co z językiem jest nie tak? Jest bardzo elastyczny, momentami za bardzo. Język C, jako język kompilowany do postaci binarnej, posiada bardzo rygorystyczną kontrolę zgodności typów. Ostrzega nawet przed konwersją typów, które są właściwie identyczne w reprezentacji binarnej, ale posiadają różne nazwy, stąd nawet rzutowanie wskaźników wymaga jawnej konwersji w kodzie. Python posiada bardzo rygorystyczną składnię -- wymusza poprawne (i czytelne) formatowanie kodu źródłowego, bo jego wygląd decyduje o przepływie sterowania. Co ma <abbr>PHP</abbr>? Burdel na kółkach.</p>

<p>Najbardziej boli w codziennej pracy jedno z jego początkowych założeń -- brak typowania zmiennych. Uniemożliwia to kontrolę poprawności kodu jeszcze przed jego uruchomieniem i skutkuje godzinami ślęczenia nad kilkunastoma tysiącami linii w celu wyłapania literówki lub tak zwanego <q>efektu kofeinowego deficytu.</q></p>

<p>Boli też domyślna konfiguracja serwerów deweloperskich, gdzie poziom raportowania błędów jest dostosowany do maszyny produkcyjnej i spory procent <q>programistów</q> nie ma nawet pojęcia, że język oprócz błędów krytycznych potrafi też raportować ostrzeżenia i powiadomienia (a od wersji piątej także błędy naruszenia rygoru składni).</p>

<p>Jeszcze bardziej boli domyślne aktywowanie na serwerach opcji <code>register_globals</code> i <code>magic_quotes_gpc</code>. Pozwala pisać niechlujny kod, a dodatkowo uniemożliwia jego uruchomienie na poprawnie skonfigurowanych maszynach.</p>

<p>Boli brak narzędzi interaktywnych i wbudowanej obsługi testów jednostkowych, co pozwoliłoby błyskawicznie wyłapywać regresje w kodzie bez potrzeby pisania specjalnych interfejsów do uruchamiania poszczególnych elementów silnika.</p>

<p>Boli brak zunifikowanej struktury dostępu do systemów bazodanowych. Brakuje też podobnej struktury dostępu do danych pochodzących ze źródeł zewnętrznych.</p>

<p>Na szczęście, przynajmniej część z tych problemów zostanie lub została już zniwelowana. Od <abbr>PHP 5.1</abbr> dostępny jest szkielet dostępu do danych potencjalnie niebezpiecznych -- <code>input_filter</code>. Pojawił się też uniwersalny silnik dostępu do baz danych - <abbr title="PHP Data Objects">PDO</abbr>. W wersji szóstej całkowicie usunięte zostanie wsparcie dla <code>magic_quotes</code> i <code>register_globals</code>. Nic jednak nie naprawi ludzi, którzy budują to, jak język jest postrzegany. Jeśli ktoś nie chce się uczyć, to najlepsze zmiany nic nie dadzą. Tak jak nic nie dadzą narzędzia, z których nie chce korzystać.</p>

<p>Zanim zacznie się flejm -- jestem programistą i utrzymuję się głównie z tworzenia aplikacji we wspomnianym wyżej języku. Znam jego mocne i słabe strony. Tekst wyraża moje i tylko moje zdanie na ten temat.</p>

Technorati Tags: <a href="http://technorati.com/tag/php" rel="tag">php</a>, <a href="http://technorati.com/tag/code" rel="tag">code</a>
