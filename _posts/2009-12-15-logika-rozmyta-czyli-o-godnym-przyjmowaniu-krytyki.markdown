---
layout: post
status: publish
published: true
title: Logika rozmyta, czyli o godnym przyjmowaniu krytyki
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 674
wordpress_url: http://room-303.com/blog/?p=674
date: 2009-12-15 15:22:00.000000000 +01:00
categories:
- web
- software
tags: []
comments:
- id: 24616
  author: mcv
  author_url: http://mcv.mulabs.org/
  date: '2009-12-15 15:39:06 +0100'
  date_gmt: '2009-12-15 14:39:06 +0100'
  content: "„gdzie strukturę XML zapisano w postaci tablicy mieszającej PHP”\r\n\r\nJo
    żem pomyślał, że to JSON. Ale widzę, że to jeszcze wyższa abstrakcja…"
- id: 24617
  author: Patrys
  author_url: http://room-303.com/
  date: '2009-12-15 15:43:18 +0100'
  date_gmt: '2009-12-15 14:43:18 +0100'
  content: "mcv:\r\n\r\nTak po prawdzie to nie jest ani PHP, ani JSON - notacja słowników
    JS-owa, ale asocjacja ze strzałką, jak w PHP. To Ruby."
- id: 24618
  author: Tomash
  author_url: http://tomash.wrug.eu
  date: '2009-12-15 16:27:12 +0100'
  date_gmt: '2009-12-15 15:27:12 +0100'
  content: Takie firmy robią bardzo złą prasę programistom Ruby, kurwości :/
- id: 24619
  author: janu
  author_url: http://agiler.net
  date: '2009-12-15 16:42:05 +0100'
  date_gmt: '2009-12-15 15:42:05 +0100'
  content: '@Tomash - no bez przesady, złą prasę to sobie robią. Kto normalny powie,
    że programiści Ruby to idioci, bo inFakt zwraca słownik ruby-style?'
- id: 24620
  author: mcv
  author_url: http://mcv.mulabs.org/
  date: '2009-12-15 16:50:06 +0100'
  date_gmt: '2009-12-15 15:50:06 +0100'
  content: Ale tak z drugiej strony, to nie widzę problemu w specyfikacji aplikacji
    XML bez użycia „&lt;"?
- id: 24621
  author: Patrys
  author_url: http://room-303.com/
  date: '2009-12-15 16:50:30 +0100'
  date_gmt: '2009-12-15 15:50:30 +0100'
  content: "janu:\r\n\r\nNawet śmieszniej, bo zwraca formatkę XML, tylko \"dokumentacja\"
    z niezrozumiałych przyczyn pokazuje zamiast niej słownik w Rubym."
- id: 24623
  author: Hadret
  author_url: http://hadret.com/
  date: '2009-12-15 17:19:43 +0100'
  date_gmt: '2009-12-15 16:19:43 +0100'
  content: "A To Polska Właśnie, aż ciśnie się na usta. Zdanie:\r\n<blockquote>Brawo!!
    Mamy pełny obraz :-) Przygotowujecie kopię Infakt, nasyłacie kolegów do czarnego
    pr i uważacie że infakt jest be. Bomba</blockquote>\r\nmożna byłoby podsumować
    przysłowiem: każdy mierzy własną miarą."
- id: 24624
  author: Piotr Lewandowski
  author_url: http://piotrlewandowski.info
  date: '2009-12-15 18:50:54 +0100'
  date_gmt: '2009-12-15 17:50:54 +0100'
  content: 'A propos profesjonalizmu: poinformuj sponsora, żeby poprawił reklamę,
    bo aktualnie nie wygląda "profejsonalnie"...'
- id: 24625
  author: maniel
  author_url: http://maniel.jogger.pl/
  date: '2009-12-15 20:02:36 +0100'
  date_gmt: '2009-12-15 19:02:36 +0100'
  content: dżizas, ale ty masz szczęście[/pecha] do trolli;-)
- id: 24626
  author: Bartosz Małkowski
  author_url: http://bmalkow.malkowscy.net/
  date: '2009-12-15 20:57:27 +0100'
  date_gmt: '2009-12-15 19:57:27 +0100'
  content: Tak dalej pójdzie to będziesz się musiał oglądać przez ramię jak będziesz
    szedł przez miasto ;)
- id: 24627
  author: Piotr Lewandowski
  author_url: http://piotrlewandowski.info/
  date: '2009-12-15 21:46:20 +0100'
  date_gmt: '2009-12-15 20:46:20 +0100'
  content: '@Bartosz: Nie sądzę, żeby Patrys musiał się bać... "Krowa, która dużo
    ryczy, mało mleka daje" - z tego co widać, to póki co inFakt stać jedynie na nieuargumentowane
    pyskówki... Czyżby ten "ktoś" z inFaktu to kolejna inkarnacja synaprezesa ??'
- id: 24628
  author: Bartosz Małkowski
  author_url: http://bmalkow.malkowscy.net/
  date: '2009-12-15 22:01:43 +0100'
  date_gmt: '2009-12-15 21:01:43 +0100'
  content: "Raaany! Syn Prezesa™ Zapomniałem o nim!\r\n\r\nPatrys! Ty to musisz wysyłać
    jakieś fluidy… Powiedzenie \"całe życie z wariatami\" nabiera w Twoim przypadku
    nowego znaczenia!"
- id: 24630
  author: Wiktor Sarota - Infakt.pl
  author_url: http://www.infakt.pl
  date: '2009-12-15 23:29:43 +0100'
  date_gmt: '2009-12-15 22:29:43 +0100'
  content: "A już odnosząc się do spraw technicznych: \r\n\r\n1. Pierwsza dokumentacja
    API w XML, która nie zawiera ani jednego znaku \" Nigdzie nie ma określenia API
    w XML. API było w początkowej wersji skierowane do implementacji przez klientów
    w Ruby. Tam stosuje się standardowe RESTowe podejście i pod takie podejście API
    infaktu jest skrojone. Samego xmla można jak najbardziej podglądnąć w przykładzie
    z php.\r\n\r\n2. Pierwsza dokumentacja API, gdzie strukturę XML zapisano w postaci
    tablicy mieszającej PHP Rubiego — to również nie żart, spodziewam się, że wersja
    0.7 w ramach dywersyfikacji wprowadzi również JSON i YAML.\r\n\r\n&gt; Jak wyżej,
    na początek podłączenie zakładaliśmy z klienta w Rubym, przy takiej opcji nie
    piszesz ani nie widzisz nawet ciecia znaku \"&lt;&quot;.\r\n\r\n3. Jedyna dokumentacja
    API, gdzie prawie wszystkie nazwy elementów zostały podane błędnie — autor, choć
    zapomniał o udokumentowaniu struktury, przytacza nazwy elementów w rodzaju , zupełnie
    nie przeszkadza mu fakt, że w rzeczywistości element ten to .\r\n\r\n&gt; Jeśli
    już odwołujemy się do xmla Patrys piszący nie zna standardu bo przewiduje on zarówno
    _ jak i - http://www.w3.org/TR/REC-xml/#NT-Name\r\n\r\n4. Jedyne API, które do
    dostępu wymaga, oprócz klucza, podania loginu i hasła — czemu nie chcemy używać
    loginu i hasła w dostępie do API? Aby w razie czego łatwo i bez ryzyka odciąć
    dany program. Zatem wprowadźmy klucze i wtedy wystarczy zmienić klucz, a autor
    aplikacji, nie znając loginu i hasła… wróć, o szit, o szit, o fak.\r\n\r\n&gt;
    Poprawia bezpieczeństwo. Tylko osoby które świadomie wygenerowały klucz mogą korzystać
    z API. Wszyscy inni mają API domyślne wyłączone. Trzeba znać nazwę użytkownika,
    hasło a dodatkowo jeszcze klucz aby mieć dostęp do danych.\r\n\r\n5. No nie wierzę,
    że nie umiem w trzech linijkach zrobić Basic Auth.\r\n\r\n&gt; A jednak trzeba
    uwierzyć w swoją omylność. Wszystkimi innym zadziałało, Patrysowi też gdyby podał
    poprawne dane.\r\n\r\n6. Biorę przykład InFaktu, napisany w PHP (z własnym klientem
    HTTP, stworzonym w technologii Copiego-Paste’a, włącznie).\r\n\r\n&gt; Przykład
    w php działa, jeśli u Patrysa nie działa ani przykład w PHP ani logowanie przez
    Basic Auth to tym bardziej trzeba sprawdzić poprawność podawanych danych. Poprawne
    dane zdecydowanie wystarczą do korzystania.\r\n\r\n7. Koniec końców zdawało się,
    że wczoraj sytuacja się unormowała. API InFaktu zaczęło \"magicznie\" działać
    (bez zmian w kodzie z mojej strony), więc uznałem, że z administratora zeszło
    ciśnienie i nas odblokował.\r\n\r\n&gt; API Infaktu działało cały czas. Nie było
    żadnych zmian w kodzie od kilkunastu dni. Administrator nikogo nie nakłania do
    używania programu ani tym bardziej nikogo nie blokuje.\r\n\r\n8. Wasze API aż
    prosi się o sensowną dokumentację i pozbycie się loginów i haseł (co na Blipie
    sugerowałem równie grzecznie, co bezskutecznie).\r\n\r\n&gt; Na pewno opis można
    polepszyć, ale loginy i hasła zdecydowanie zostają."
- id: 24636
  author: Jakub Piotr Cłapa
  author_url: http://jpc.jogger.pl
  date: '2009-12-16 00:47:39 +0100'
  date_gmt: '2009-12-15 23:47:39 +0100'
  content: "Popracowałbyś Patrys przy elektronice to byś wiedział, że takie niedociągnięcia
    to jest pikuś.\r\nCo powiesz na protokół transmisji, w którego opisie bity nazywa
    się bajtami, a jeden bajt ,,on the wire'' reprezentują dwa znaki ASCII z heksadecymalną
    reprezentacją tegoż bajtu (no chyba, że bajt ten sam reprezentuje znak '?'; wtedy
    się go przesyła jak-jest). No i klient nie dostarcza nam do wglądu żadnego (SWOJEGO!)
    produktu, w którym działałby omawiany protokół komunikacji."
- id: 24637
  author: mcv
  author_url: http://mcv.mulabs.org/
  date: '2009-12-16 08:39:02 +0100'
  date_gmt: '2009-12-16 07:39:02 +0100'
  content: "„Jeśli już odwołujemy się do xmla Patrys piszący nie zna standardu bo
    przewiduje on zarówno _ jak i –”\r\n\r\nZnaki „_” i „-” nie są zamienne w XML-u.
    Element du_pa to zupełnie inny element niż du-pa."
- id: 24638
  author: Infakt
  author_url: http://www.infakt.pl
  date: '2009-12-16 09:25:01 +0100'
  date_gmt: '2009-12-16 08:25:01 +0100'
  content: "Od strony biznesowej:\r\n\r\n\r\n1. Wierzymy w uczciwość. Wszystkim, którzy
    chcą sobie wyrobić obiektywną opinię proponujemy przejrzenie dyskusji na blipie:\r\n\r\nhttp://blip.pl/users/infakt/dashboard
    plus dashboard patrys-a i mirumee\r\n\r\n\r\n2. Po to jest API, aby firmy z niego
    korzystały. W momencie jednak, kiedy Patrys praktycznie jednocześnie, bo o 16:44
    pisze w podobnym tonie informacje na blipie oraz w formularzu kontaktowym do Infakt.pl
    o 16:46 podpisując się innym nazwiskiem (Tomasz Rybarczyk) pyta o to samo - to
    nie wydaje się uczciwe: http://pokazywarka.pl/99nvva/\r\n\r\nA wystarczyło napisać:
    potrzebuję wsparcia, gdyż chcemy przygotować na poziomie API eksport danych.\r\n\r\n\r\nWszystkich
    zapraszamy do wdrażania/testowania naszego API i przykładu z dokumentacji, bo
    API działa. Z naszej strony wierzymy w uczciwość i prawdę i dostarczania łatwego
    i prostego softu do wystawiania faktur."
- id: 24639
  author: Patrys
  author_url: http://room-303.com/
  date: '2009-12-16 09:51:04 +0100'
  date_gmt: '2009-12-16 08:51:04 +0100'
  content: "Wiktor:\r\n\r\n<blockquote>Jak wyżej, na początek podłączenie zakładaliśmy
    z klienta w Rubym, przy takiej opcji nie piszesz ani nie widzisz nawet ciecia
    znaku “&lt;\".</blockquote>\r\n\r\nUdostępniacie API. W Polsce. I oczekujecie,
    że jedyna implementacja będzie w Ruby. Dlatego nie dokumentujecie aplikacji XML,
    którą stworzyliście na własne potrzeby. Świetnie.\r\n\r\n<blockquote>Jeśli już
    odwołujemy się do xmla Patrys piszący nie zna standardu bo przewiduje on zarówno
    _ jak i – http://www.w3.org/TR/REC-xml/#NT-Name</blockquote>\r\n\r\nStandard przewiduje
    nawet \"ć\" i \"½\", co nie zmienia faktu, że wasze API zwraca zupełnie inny znak,
    niż opisuje dokumentacja.\r\n\r\n<blockquote>Poprawia bezpieczeństwo. Tylko osoby
    które świadomie wygenerowały klucz mogą korzystać z API. Wszyscy inni mają API
    domyślne wyłączone. Trzeba znać nazwę użytkownika, hasło a dodatkowo jeszcze klucz
    aby mieć dostęp do danych.</blockquote>\r\n\r\nChyba żyjemy w innych czasach.
    Jeśli mam twój login i hasło, to mogę zwyczajnie zalogować się na twoje konto,
    zmienić dane i hasło. Nie bardzo widzę, gdzie poprawia to bezpieczeństwo. Do tego
    wasza dokumentacja sugeruje użycie basic auth po nieszyfrowanym protokole HTTP,
    co powoduje wysłanie loginu i hasła czystym tekstem przez pół internetu. Security
    my ass.\r\n\r\n<blockquote>A jednak trzeba uwierzyć w swoją omylność. Wszystkimi
    innym zadziałało, Patrysowi też gdyby podał poprawne dane.</blockquote>\r\n\r\nMea
    culpa, nawet curl musiał mieć w piątek słaby dzień, bo też źle implementował basic
    auth."
- id: 24640
  author: Patrys
  author_url: http://room-303.com/
  date: '2009-12-16 09:56:15 +0100'
  date_gmt: '2009-12-16 08:56:15 +0100'
  content: "Infakt:\r\n\r\nTak, zmieniłem nazwisko, a nawet założyłem na fałszywe
    nazwisko działalność gospodarczą specjalnie po to, żeby ukryć swoją prawdziwą
    tożsamość :D\r\n\r\nPrzy okazji pozdrawiam Tomka, który -- jako użytkownik InFaktu
    -- pomagał mi przy testowaniu API.\r\n\r\nPS: Tak, to objawy rozszczepienia osobowości,
    piszę sam do siebie. Właściwie to zatrudniam też sam siebie, bo podobno Mirumee
    to też ja :D"
- id: 24641
  author: DeeJay1
  author_url: http://princefool.blogspot.com/
  date: '2009-12-16 10:05:03 +0100'
  date_gmt: '2009-12-16 09:05:03 +0100'
  content: "@infakt: w podobnym tonie? Wiadomość z formularza kontaktowego nawet nie
    brzmi jak Patrys...\r\n\r\nEch, nie ma to jak dobry flejm od poranka..."
- id: 24642
  author: Tomasz Rybarczyk
  author_url: ''
  date: '2009-12-16 11:01:20 +0100'
  date_gmt: '2009-12-16 10:01:20 +0100'
  content: "Chciałbym pozdrowić bardzo serdecznie załogę infaktu, która raczy szastać
    moimi danymi i upubliczniać korespondencję. Zarazem mam gorącą prośbę: proszę
    nie publikować moich faktur publicznie (niestety usunąć ich nie mogę gdyż ogranicza
    mnie limit darmowego konta - dwa usunięcia i edycje miesięcznie - a płacić nie
    zamierzam).\r\n\r\nPozdrawiam paluh"
- id: 24643
  author: nbw
  author_url: http://enbewu.net/blog/
  date: '2009-12-16 18:30:27 +0100'
  date_gmt: '2009-12-16 17:30:27 +0100'
  content: "W zasadzie całą debatę można skrócić do tego, że obie strony są siebie
    warte. Osobie/osobom ze strony inFaktu zabroniłbym logowania do blipa dopóki nie
    nauczą się prowadzić dyskusji, programistów wysłałbym na doszkolenie. Podobną
    terapię proponuję użytkownikowi logującemu się na konto Mirumee razem z powtórką
    z niedokarmiania trolli. \r\n\r\nA tak poza sprawą, czytanie o tej akcji uświadmia
    mi, jak kurewsko smutny jest ten polski grajdołek, w którym dwie poważne firmy
    zatrudniające dorosłych ludzi przebijają się, która jest większym trollem. Takie
    rzeczy to się załatwia między sobą, przez prawników albo na utwardzonym polu."
- id: 24645
  author: Mirek Mencel
  author_url: http://centrumfaktur.pl
  date: '2009-12-16 22:17:45 +0100'
  date_gmt: '2009-12-16 21:17:45 +0100'
  content: "nbw:\r\n\r\nMam wrażenie, że jednak niedokładnie prześledziłeś tą dyskusję,
    chociaż rozumiem, nam też cała ta sytuacja się nie podoba. Zostaliśmy publicznie
    zaatakowani i bezpodstawnie pomówieni, że oto Patrys który dla nas pracuje podszywa
    się pod kogoś innego, a co więcej jest przez nas \"nasyłany\" z czarnym PRem.
    Wybacz, ale ograniczyliśmy się do minimum wyjaśnień, które naszym zdaniem należały
    się użytkownikom.\r\nPozdrawiam."
- id: 24646
  author: matipl
  author_url: http://matipl.pl/
  date: '2009-12-17 11:46:45 +0100'
  date_gmt: '2009-12-17 10:46:45 +0100'
  content: Patrys, olać sprawę i niech żyje inFakt w swojej pięknej bajce. Żal i tyle.
---
<p><em>Disclaimer:</em> Na wstępie chciałem ostrzec, że tekst dotyczy moich kontaktów z <a rel="nofollow" href="http://infakt.pl/">InFaktem</a>, który to serwis z racji umowy wiążącej mnie z <a href="http://mirumee.com/blog/">Mirumee</a> niektórzy mogą uznać za moją konkurencję.</p>

<p>Cenimy InFakt (i mówiąc <q>my</q> nie mam na myśli <q>ja, właściciel CentrumFaktur</q>, do czego jeszcze dojdziemy). Mamy również pełną świadomość tego, że sporo firm właśnie ich wybrało do wystawiania faktur. Udawanie, że jest inaczej, mijałoby się z celem. Tyle tytułem wstępu.</p>

<p>Pojawili się pierwsi użytkownicy CentrumFaktur i razem z nimi pierwsze życzenia. Zupełnie nie byliśmy zdziwieni, kiedy ktoś wskazał na API InFaktu, prosząc o dodanie możliwości importu danych. Dostałem link do dokumentacji, dostałem dane dostępowe do konta, zabrałem się do pracy.</p>

<p>Zaczęło się od dokumentacji, czy może raczej <q>dokumentacji</q>. <a href="http://infakt.pl/files/Infakt_pl_api_dokumentacja_ver_0.6.pdf">Plik PDF</a> ma bowiem 3,5 strony i przedstawia cały interfejs w pięciu <em>prostych</em> punktach. Akcent na słowo <q>prostych</q> pada celowo, gdyż autorowi udało się pominąć wiele jakże nudnych kwestii technicznych, skupiając się na szlifowaniu swego kunsztu literackiego.</p>

<p>Chciałem niniejszym nominować API InFaktu do następujących wyróżnień:</p>

<ul>
	<li><em>Pierwsza dokumentacja API w XML, która nie zawiera ani jednego znaku <q>&lt;</q></em> &mdash; to zadziwiające, ale autorowi udało się opisać aplikację XML bez choćby wspominania jej schematu.</li>
	<li><em>Pierwsza dokumentacja API, gdzie strukturę XML zapisano w postaci tablicy mieszającej <del>PHP</del> <ins>Rubiego</ins></em> &mdash; to również nie żart, spodziewam się, że wersja 0.7 w ramach dywersyfikacji wprowadzi również JSON i YAML.</li>
	<li><em>Jedyna dokumentacja API, gdzie prawie wszystkie nazwy elementów zostały podane błędnie</em> &mdash; autor, choć zapomniał o udokumentowaniu struktury, przytacza nazwy elementów w rodzaju <code>&lt;nazwa_firmy/&gt;</code>, zupełnie nie przeszkadza mu fakt, że w rzeczywistości element ten to <code>&lt;nazwa-firmy/&gt;</code>.</li>
	<li><em>Jedyne API, które do dostępu wymaga, oprócz klucza, podania loginu i hasła</em> &mdash; czemu nie chcemy używać loginu i hasła w dostępie do API? Aby w razie czego łatwo i bez ryzyka odciąć dany program. Zatem wprowadźmy klucze i wtedy wystarczy zmienić klucz, a autor aplikacji, nie znając loginu i hasła&hellip; wróć, <em>o szit, o szit, o fak</em>.</li>
</ul>

<p>Zamiast sensownego opisu, mamy <q>dokumentację przez implementację</q>. <q>Dokumentację</q> postanowiłem zatem w skrócie nazywać <q>doku</q>. W skrócie od <q>do kurwy nędzy</q>. Cóż, przynajmniej nie użyli SOAP (którego to protokołu nazwa słusznie sugeruje rozkosze kojarzone ze schylaniem się pod prysznicem). Bywa i tak, damy radę. Rach-ciach-ciach i&hellip; dupa.</p>

<blockquote><pre><code>401 Unauthorized</code></pre></blockquote>

<p>No nie wierzę, że nie umiem w trzech linijkach zrobić Basic Auth.</p>

<p>Sprawdzam ponownie, kod wygląda ok &mdash; podać login i hasło-sklejone-z-kluczem do modułu autoryzacji, wywołać GET, wydrukować wynik (a potem napisać sobie samemu dokumentację schematu). Biorę przykład InFaktu, napisany w PHP (z własnym klientem HTTP, stworzonym w technologii Copiego-Paste'a, włącznie). Zmieniam login, zmieniam hasło, zmieniam klucz. Uruchamiam, dupa. Mam już dwie dupy i wciąż ani jednego klienta, żyć nie umierać.</p>

<p>Pytam na Blipie, tu zaczęła się prawdziwa przygoda. Zaczęło się dość sympatycznie:</p>

<blockquote><p>Tak to jest jak konkurencja czyta API:-) Powiedz co dokładnie Ci nie działa</p></blockquote>
&mdash; <cite><a href="http://blip.pl/dm/25863998">InFakt</a>, Blip</cite>

<p>Po chwili odbijania piłeczki (<q>nie lubimy nieczystej gry</q>) dowiedziałem się, że jestem właścicielem CentrumFaktur. Otóż nie jestem, jakkolwiek by się przy tym nie upierać, właścicielem Portfeo i CentrumFaktur jest Mirumee. Na pieczątce, którą mam przed sobą, stoi <q>Mirumee Software, Mirosław Mencel</q>. Ja najbliżej literki <q>M</q> byłem, gdy nadawano mi drugie imię <q>Michał</q>, którego jednak nie używam.</p>

<p>Wszelkie próby dogadania się na szczeblu technicznym (ze wskazaniem na fakt, że nie naruszam regulaminu InFaktu włącznie) spełzły na niczym. Dyskusja na poziomie <q>a my i tak wiemy lepiej, Balcerowicz musi odejść</q>.</p>

<p>Wreszcie rozmowa przeradza się w rasowy flejm ze stosowną argumentacją w komplecie:</p>

<blockquote><p>Brawo!! Mamy pełny obraz :-) Przygotowujecie kopię Infakt, nasyłacie kolegów do czarnego pr i uważacie że infakt jest be. Bomba</p></blockquote>
&mdash; <cite><a href="http://blip.pl/dm/25873307">InFakt</a>, Blip</cite>

<p>Otóż wierzcie mi Państwo, że w obliczu zastanego profesjonalizmu, <q>czarny PR</q> rozdaję całkiem charytatywnie. Trochę pokory, panowie. Faktycznie, InFakt mocno przyczynił się do powstania CentrumFaktur. Byłem przy tym, to wiem. A skoro wiem, to opowiem.</p>

<p>Pracowałem ci ja sobie spokojnie nad Portfeo, kiedy to zaistniała w ekipie Portfeo potrzeba regularnego wystawiania faktur VAT. Wobec tego Mirek bez zastanowienia (idąc za głosem rekomendacji) założył konto na InFakcie (w jakże doskonale zakamuflowanej domenie <code>portfeo.infakt.pl</code>, co dowodzi naszego przebiegłego szpiegostwa). Po paru próbach użycia okazało się, że serwis nie spełnia jego oczekiwań i zaproponował mi kontrakt na stworzenie alternatywy. Dwa podpisy później konto na InFakcie wyszło z użycia.</p>

<p>Ot i cała historia inspiracji, jakiej dostarczył nam InFakt. Historie o kopiowaniu interfejsu czy możliwości proponuję włożyć między bajki. Trochę pokory, do bajek wrócimy, kiedy w przyszłym roku InFakt udostępni moduł ofertowania. Co zaś się tyczy inspiracji, to wzorowaliśmy się na <a href="http://getballpark.com/">Ballparku</a> i nie wstydzimy się tego zupełnie &mdash; wszak jeśli się uczyć, to od lepszych od siebie.</p>

<p>Koniec końców zdawało się, że wczoraj sytuacja się unormowała. API InFaktu zaczęło <q>magicznie</q> działać (bez zmian w kodzie z mojej strony), więc uznałem, że z administratora zeszło ciśnienie i nas odblokował. Dziś jednak cyrk zaczął się na nowo, a do mnie wpadły (między innymi) takie wiadomości:</p>

<blockquote><p>Ujawniliśmy publicznie Wasze nieetyczne zachowanie. Próbujecie wykorzystać nasze API do transferu Klientów. Żałosne ale prawdziwe.</p></blockquote>
&mdash; <cite><a href="http://blip.pl/dm/26676045">InFakt</a>, Blip</cite>

<blockquote><p>Infakt udostepnił API publicznie, nikomu nie blokuje dostępu, nawet Wam, tym którzy szukają drogi na skróty w zdobywaniu Klientów</p></blockquote>
&mdash; <cite><a href="http://blip.pl/dm/26678805">InFakt</a>, Blip</cite>

<p>Nie mam pojęcia, kto we wspomnianym wcześniej serwisie operuje kontem <a rel="nofollow" href="http://infakt.blip.pl/">^infakt</a>, ale z całą pewnością nie przysługuje się wizerunkowi firmy. Gdybym był złośliwy, to napisałbym, że limit 160 znaków sugeruje, że może to być autor dokumentacji. Ale nie jestem, prawda?</p>

<p>Drogi użytkowniku ^infakt, spieszę poinformować, że twoja logika nie trzyma się kupy. W jakiż to sposób CentrumFaktur miałoby <q>ukraść</q> wam użytkowników? Emaksem przez sendmejla (potrójna ścianka ognia) zdobyć wszystkie loginy i hasła, wygenerować klucze API i dokonać migracji na siłę? No bo, proszę ja was, po mojemu to dane klientów i faktury są własnością firmy, a nie InFaktu i user ma prawo je sobie migrować gdzie chce.</p>

<p>Wersja dla opornych: użytkownicy muszą najpierw samodzielnie założyć konto w CentrumFaktur, następnie wpisać z własnej nieprzymuszonej woli dane do logowania i nacisnąć przycisk <q>Importuj</q>. Nikt tu nikogo pod pistoletem nie trzyma. Kiedy skończę pracować nad API CentrumFaktur, będziecie mile widzianym jego konsumentem.</p>

<p>Apeluję zatem: trochę dystansu. CentrumFaktur z pewnością daleko jest do ideału, ale nie widziałem, żeby Mirek z tego powodu naskakiwał na krytyków. Wasze API aż prosi się o sensowną dokumentację i pozbycie się loginów i haseł (co na Blipie <a href="http://blip.pl/dm/25864210">sugerowałem</a> równie grzecznie, co bezskutecznie). Mam również nadzieję, że pracownicy InFaktu będą łaskawi zejść wreszcie z moich pleców, bo wierzcie mi, że licytację na techniczne niedoróbki można kontynuować, ale nie przyjdzie to z zyskiem dla żadnej ze stron.</p>
