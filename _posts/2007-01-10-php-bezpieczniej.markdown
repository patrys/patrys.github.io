---
layout: post
status: publish
published: true
title: PHP bezpieczniej
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 326
alias: /blog/2007/01/10/php-bezpieczniej/
date: 2007-01-10 23:29:54.000000000 +01:00
categories:
- web
- software
- code
tags: []
comments:
- id: 5995
  author: talen
  author_url: http://talen.jogger.pl
  date: '2007-01-11 00:15:29 +0100'
  date_gmt: '2007-01-10 23:15:29 +0100'
  content: "ufff... na szczęście, z Twojej prezentacji nie dowiedziałem się niczego,
    czego bym wcześniej nie wiedział :-)\r\n\r\nChoć przyznaje, że przy ostatnim punkcie
    ('upload'), zrobiłem szybki rachunek sumienia, czy gdzieś ostatnimi czasy nie
    popełniłem tego błędu :-)\r\n\r\nChyba najlepszym/najłatwieszym sposobem zabezpieczenia
    się przed bugami o których piszesz, to stosowanie framework'ów (np.: w zden framework
    metoda _redirect() robi header() + exit(); spróbujcie tylko napisać UnitTesty
    które to testują :-))).\r\n\r\nAlbo przynajmniej korzystanie z gotowców (klas/metod)
    mąrzejszych od nas, którzy już przez te problemy się przegryźli."
- id: 5996
  author: carstein
  author_url: http://carstein.jogger.pl
  date: '2007-01-11 00:19:02 +0100'
  date_gmt: '2007-01-10 23:19:02 +0100'
  content: "Podoba mi się ten dokumencik. Taka wiedza w pigułce. Niektórym bardzo
    się przyda. Zresztą połowa z tych błędów nie dotyczy tylko i wyłącznie PHP. \r\n\r\nCo
    do SQL injection - wielu ludzi naiwnie bazuje na magic_quotes, zapominając, że
    czasami przekazujemy wartości typu int. Bardzo ładnie to pokazałeś w tym dokumencie\r\n\r\nZ
    ciekawostek - warto pamiętać, żeby w configu wyłączyć opcję expose_php. Dlaczego?
    \r\nDlatego: http://carstein.kill-9.pl/~mike/check_version.py\r\n(kod naklepany
    w 5 minut). A po co ktoś ma wiedzieć, jakiej wersji PHP używacie? To samo zresztą
    dotyczy server_token w configu apache."
- id: 5997
  author: mcv
  author_url: http://mcv.jogger.pl
  date: '2007-01-11 00:25:14 +0100'
  date_gmt: '2007-01-10 23:25:14 +0100'
  content: A ja bym się przyczepił, że „inicjalizowania zmiennych”, a nie „inicjowania”.
    Inicjowanie to z rozpoczynaniem jakiegoś procesu raczej chyba…
- id: 5999
  author: Andrzej
  author_url: http://www.ab.waw.pl
  date: '2007-01-11 00:58:17 +0100'
  date_gmt: '2007-01-10 23:58:17 +0100'
  content: Dzięki za ten pdf. Na szczęście niczego nowego się nie dowiedziałem, ale
    to bardzo pożyteczny test.
- id: 6000
  author: rozbit
  author_url: http://rozbit.com
  date: '2007-01-11 01:06:57 +0100'
  date_gmt: '2007-01-11 00:06:57 +0100'
  content: "Tak w kwestii dołączania plików .inc, to owszem, można je zastąpić plikami
    .php, ale można spokojnie używac .inc, dodając odpowiednią dyrektywę do pliku
    konfiguracyjnego Apache'a lub do pliku .htaccess. Wyglądałoby to mniej-więcej
    tak:\r\n\r\n      Order Deny,Allow\r\n      Deny from All\r\n\r\nOczywiście, jeśli
    nie mamy możliwości zmiany treści apache.conf lub mamy zabronione używanie .htaccess,
    to wtedy Twoja metoda jest jak najbardziej ok. W sumie zawsze jest ok, ale sygnalizuje
    tylko, że jest też inny sposób.\r\nCo do dołączania zewnętrznych plików (Ślepe
    dołączanie kodu) to metodą radzenia sobie z tym jest umieszczenia w kodzie funkcji
    sprawdzających, co wogóle jest nam dawane z zewnątrz.\r\nW przypadku obrony przed
    SQL Injection, również warto zaopatrzeć się w sprawdzacze tego, co jest wprowadzane
    przez formularze.\r\nBrakuje mi troche wzmianki o directory traversal, bo jestem
    ciekaw Twoich propozycji obrony przed takimi atakmi. Ogólnie bardzo ciekawa prezentacja
    (artykuł?):) Pisałem coś podobnego parę dni temu ale bardziej szerzej (temat:
    Bezpieczeństwo WWW, forma: konspekt ćwiczeń dla studentów na przedmiot Bezpieczeństwo
    i Ochrona Danych w Systemach Komputerowych)."
- id: 6001
  author: rozbit
  author_url: http://rozbit.com
  date: '2007-01-11 01:08:18 +0100'
  date_gmt: '2007-01-11 00:08:18 +0100'
  content: Przepraszam za bałagan, ale oczywiście w ostatnim zdaniu chodziło mi o
    "pisanie nie tylko o php". Pierwsza forma dziwnie wygląda;p
- id: 6002
  author: rozbit
  author_url: http://rozbit.com
  date: '2007-01-11 01:09:35 +0100'
  date_gmt: '2007-01-11 00:09:35 +0100'
  content: "Jejku, sen daje o sobie znać, ale i tak wybacz mi bardzo, zapomniałem
    o &lt; i &gt; przy dyrektywie... powinna ona wyglądać tak:\r\n&lt;FilesMatch \"\\.(inc)$\"&gt;\r\n
    \     Order Deny,Allow\r\n      Deny from All\r\n&lt;/FilesMatch&gt;"
- id: 6003
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-01-11 01:17:30 +0100'
  date_gmt: '2007-01-11 00:17:30 +0100'
  content: "rozbit:\r\n\r\nOd walidacji formularzy jest logika kontrolera, od przekazywania
    danych do bazy logika modelu. Model powinien zadbać o to, żeby nie zepsuć bazy
    nawet jeśli kontroler jest wadliwy i stąd preparowane zapytania albo procedury
    składowane (oba dają dodatkowy zysk wydajności).\r\n\r\nJeśli kod aplikacji jest
    bezpieczny, to chętnie pokażę ci całą strukturę katalogów serwera i nadal będę
    mógł spać spokojnie :)\r\n\r\nPS: to powyższe dotyczy ataków typu Directory Traversal
    - najprostsza metoda to trzymanie plików w postaci &lt;suma-kontrolna-md5&gt;.&lt;rozszerzenie-na-podstawie-typu-mime&gt;.
    Faktyczną nazwę trzeba znać tylko w momencie serwowania plików binarnych, przeznaczonych
    do zapisu na dysku, a wtedy można ją wygenerować na podstawie opisu pliku w bazie."
- id: 6004
  author: adam, Blog o Internecie
  author_url: http://blog.infoguru.pl
  date: '2007-01-11 01:17:53 +0100'
  date_gmt: '2007-01-11 00:17:53 +0100'
  content: "bardzo interesujące, dzię-ku-je-my!\r\n\r\n(chociaż dyskusyjne jest używanie
    tabl. $_REQUEST :)"
- id: 6005
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-01-11 01:21:12 +0100'
  date_gmt: '2007-01-11 00:21:12 +0100'
  content: "adam:\r\n\r\nW przypadku metod rutujących wykonanie kodu pomiędzy modułami,
    część parametrów czasem przyjdzie przez POST, a czasem przez GET - wygodniej użyć
    _REQUEST wtedy. Nie mówię o zastępowaniu nim jakichkolwiek odwołań."
- id: 6007
  author: warp.
  author_url: http://www.tne.pl/
  date: '2007-01-11 08:53:20 +0100'
  date_gmt: '2007-01-11 07:53:20 +0100'
  content: fajny art., dzięki
- id: 6010
  author: jps
  author_url: ''
  date: '2007-01-11 10:01:46 +0100'
  date_gmt: '2007-01-11 09:01:46 +0100'
  content: "Uffff :) też się cieszę że błędy wymienione przez Patrysa mnie nie dotyczą
    (ale za to tępię je u innych :&gt;). \r\nCo do pracki - bardzo dobra, skupiasz
    się na najczęstszych błędach :) \r\nDaję 4 :&gt; \r\nPozdr"
- id: 6014
  author: Luken
  author_url: http://luken.jogger.pl/
  date: '2007-01-11 12:48:08 +0100'
  date_gmt: '2007-01-11 11:48:08 +0100'
  content: Praca jest jak najbardziej wporządku. Chociaż dodał bym jakieś obrazki
    i może strony, na których jest napisane szerzej o bezpieczeństwie.
- id: 6016
  author: Tomek
  author_url: ''
  date: '2007-01-11 15:22:11 +0100'
  date_gmt: '2007-01-11 14:22:11 +0100'
  content: Export z AbiWorda ssie. Same kwadraciki widze.
- id: 6017
  author: carstein
  author_url: http://carstein.jogger.pl
  date: '2007-01-11 15:31:13 +0100'
  date_gmt: '2007-01-11 14:31:13 +0100'
  content: Znaczy, że nie masz dobrych czcionek w systemie.
- id: 6020
  author: bazyl
  author_url: http://blog.bazyl.net
  date: '2007-01-11 16:06:35 +0100'
  date_gmt: '2007-01-11 15:06:35 +0100'
  content: "Uwaga na temat .htaccess jest calkiem na miejscu. Samo istnienie konfiguracji
    w pliku .php moze nie wystarczyc. Poza tym strzezonego Pan Bog strzeze ;]\r\n\r\nPrzerzuc
    sie poza tym na latexa ;] Znacznie milej to wyglada :)\r\n\r\nArt dobry, choc
    uwazam, ze za ostry w slowach. Ludzie, ktorzy popelniali takie bledy do momentu
    przeczytania arta moga poczuc sie urazeni. Zamiast \"wyzywac\" mozna by ujac to
    delikatniej w slowach.\r\n\r\nAle to juz jest licentia poetica :)\r\n\r\nPozdrawiam"
- id: 6023
  author: andrzejk
  author_url: http://www.andrzejk.info
  date: '2007-01-11 19:31:13 +0100'
  date_gmt: '2007-01-11 18:31:13 +0100'
  content: "Jak już wspomniało parę osób powyżej. Nowych rzeczy dla mnie.. brak.\r\n\r\nJednak
    z punktu widzenia osoby dopiero stawiającej kroki w programowaniu w PHP, bardzo
    przydatny."
- id: 6028
  author: jpc
  author_url: http://jpc.jogger.pl
  date: '2007-01-12 00:46:23 +0100'
  date_gmt: '2007-01-11 23:46:23 +0100'
  content: 'carstein: od tego jest PDF, żeby czcionki niestandardowe załączyć. Ale
    kto teraz potrafi wygenerować dobrego PDFa. (prócz pdflateksa ;)'
- id: 6029
  author: wojtosz
  author_url: http://www.blaszkowski.com
  date: '2007-01-12 02:58:22 +0100'
  date_gmt: '2007-01-12 01:58:22 +0100'
  content: "Patrys:\r\n\r\nślepe dołączanie kodu -&gt; należało by wspomnieć o apparmor,
    który w opisanym przypadku byłby dodatkowym zabezpieczeniem.\r\ncookie injection
    -&gt; jeśli już mówimy o nieinwazyjności w sesję PHP trzeba by tu wspomnieć, że
    dobrze jest zdefiniować samodzielnie session_save_path('/some/path/');\r\ninny
    pomysł - może niezbyt świeży - to próba zabezpieczenia aplikacji przed wstrzyknięciem
    obcego kodu używając mod_rewrite, jeśli aplikacja z założenia nie ma używać _żadnych_
    zewnętrznych URL przekazywanych via $_GET.\r\n\r\nPisząc o bezpieczeństwie aplikacji
    www nie wspomniałeś o umiejętnościach, jakie powinien posiadać administrator danego
    serwera www oraz (bardzo często) o konieczności współpracy programisty i admina
    (a'propos mojego wcześniejszego nawiązania do apparmor).\r\n\r\nPodsumowując -
    w bardzo udany sposób przedstawiłeś tu problematykę bezpieczeństwa aplikacji web,
    brawo !"
- id: 6030
  author: xero666
  author_url: http://xero666.kgb.pl/
  date: '2007-01-12 02:59:52 +0100'
  date_gmt: '2007-01-12 01:59:52 +0100'
  content: "Przyjemne antybugowe repetytorium.\r\n\r\nmcv: A ja bym się przyczepił,
    że „inicjalizowania zmiennych”, a nie „inicjowania”. Inicjowanie to z rozpoczynaniem
    jakiegoś procesu raczej chyba…\r\n\r\nPozwole sobie zacytowac, bo jest to czesto
    popelniany blad (Patrys go nie popelnil):\r\nTłumacze tekstów informatycznych
    z godną podziwu konsekwencją angielski termin initialization tłumaczą jako inicjalizacja
    zamiast np. inicjowanie (chyba lepiej) lub inicjacja. Będę wdzięczna za opinię
    na ten temat.\r\nAnna Mazik\r\n\r\nW słowniku języka polskiego (dostępnym na naszych
    stronach WWW) nie ma słowa inicjalizacja. Jest natomiast inicjacja oraz inicjowanie.
    Inne słowniki też nie notują inicjalizacji. W tekstach informatycznych jeśli coś
    jest inicjowane przez coś innego (np. gdy obiekt po utworzeniu wymaga jeszcze
    dodatkowego zainicjowania go do działania) użyłbym słowa inicjowanie, natomiast
    gdy coś inicjuje się samo (np. podczas utworzenia wykonuje automatycznie wszelkie
    procedury niezbędne do działania) mówiłbym o inicjacji.\r\n— Adam Zaparciński,
    PWN"
- id: 6034
  author: ljarochowski
  author_url: ''
  date: '2007-01-12 10:11:54 +0100'
  date_gmt: '2007-01-12 09:11:54 +0100'
  content: "co do plików .inc, to najlepiej jest trzymać wszystko poza Document Root,
    po co te pliki mają być wogóle osiągalne od strony klienta? (trochę tak jak pliki
    wykonywalne są w /bin, a nie ma tam przecież bibliotek, prawda?)\r\n\r\nco do
    configuracji, to czy mądre/sensowne jest trzymanie configa w zmiennej $_SERVER['my_config']
    ? Czy to jest bezpieczne? Czytałem kiedyś o tym, i się zastanawiam.\r\n\r\nPozdrawiam\r\nŁukasz
    Jarochowski"
- id: 6036
  author: wojtosz
  author_url: http://www.blaszkowski.com
  date: '2007-01-12 10:40:04 +0100'
  date_gmt: '2007-01-12 09:40:04 +0100'
  content: "ljarochowski: nie zgadzam się z trzymaniem .inc poza zasięgiem klienta
    - przy poprawkach admin będzie zamęczany w przypadku poprawek/zmian/innych genialnych
    pomysłów klienta.\r\nPowyższe proszę traktować jako poparcie pomyslu Patrysa:
    pliki PHP trzymaj z rozszerzeniem .php."
- id: 6037
  author: ljarochowski
  author_url: ''
  date: '2007-01-12 10:59:20 +0100'
  date_gmt: '2007-01-12 09:59:20 +0100'
  content: "wojtosz: oczywiście że pliki powinny mieć rozszerzenie .php, ale myślę
    że warto tak zaprojektować aplikację, żeby dawała możliwość umieszczenia logiki
    poza \"sceną\", żeby klient nie musiał mieć dostępu do plików poza Document Root,
    można w tym celu użyć np. set_include_path('nasz-katalog-poza-doc-root'), albo
    to i do tego jeszcze __autoload, żeby nie mieć require'ów rozsianych po wszystkich
    plikach.\r\n\r\nNie wiem czemu admin - (kto to jest admin, administrator aplikacji,
    serwera, zespół programistów?) - miałby mieć z taką konfiguracją jakiekolwiek
    problemy. Poza tym - po co trzymać szablony w zasięgu klienta?"
- id: 6040
  author: 3ED
  author_url: ''
  date: '2007-01-12 14:06:32 +0100'
  date_gmt: '2007-01-12 13:06:32 +0100'
  content: Co do include w "Ślepe dołączanie kodu" to myślę że ominięciem problemu
    jest po prostu stworzenie ponumerowanej listy plików np. dla "?id=1" odpowiada
    jakiś plik, dla "?id=2" jakiś inny, a dla "?id=33", "?id=bujakasza.html" czy "?id=www.google.pl"
    dostaniesz else czyli błąd 403. :) Mylę się?
- id: 6044
  author: wojtosz
  author_url: http://www.blaszkowski.com
  date: '2007-01-12 17:13:40 +0100'
  date_gmt: '2007-01-12 16:13:40 +0100'
  content: "ljarochowski: \r\nadmin -&gt; administrator serwera.\r\n\r\nPo pierwsze,
    na początku nie napisałeś, że chodzi o aplikację opartą o szablony - ustosunkowałem
    się to tego co było napisane (nie wiem jaki był Twój zamysł, przesłanie). \r\n\r\nPo
    wtóre - nie napisałem, że admin będzie miał problemy, tylko że będzie zamęczany
    w przypadku poprawek, co należy rozumieć: admin kocha swój spokój i nie lubi marnować
    cennego czasu na podmianę zawartości plików konfiguracyjnych, bo takie jest życzenie
    usera o 2 w nocy.\r\n\r\nNa zakończenie prośba: pisz treściwie i dopełniaj treść
    wyrażanych opinii, a nie będzie potrzeby stosowania sprostowań :)"
- id: 6048
  author: empathon
  author_url: http://event-horizon.ovh.org/
  date: '2007-01-12 22:41:13 +0100'
  date_gmt: '2007-01-12 21:41:13 +0100'
  content: "Bardzo fajny art z pewnościa przyda się osoba rozpoczynajacym swoja przygode
    z php i chcacym pisać bezpiecznie.\r\nBrakuje mi tu tylko paru słów na temat przechowywania
    haseł w db. Może coś o soli jak w systemach unix'owych?\r\nSwoja droga słyszałem,
    że lepiej od mime_content_type jest używać $_FILE. Nagłówek zawsze moża spreparować
    a dalej wstawić treść wykonywalną."
- id: 6049
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-01-12 22:52:27 +0100'
  date_gmt: '2007-01-12 21:52:27 +0100'
  content: "empathon:\r\n\r\nCo masz na myśli, mówiąc o $_FILE?\r\n\r\nI co da spreparowanie
    nagłówka PNG, skoro plik binarny zostanie zapisany właśnie jako .png w związku
    z tym (bez różnicy, jakie miał oryginalnie rozszerzenie)?"
- id: 6054
  author: empathon
  author_url: http://event-horizon.ovh.org/
  date: '2007-01-13 14:14:05 +0100'
  date_gmt: '2007-01-13 13:14:05 +0100'
  content: "Mistejk, wyglada na to że mime_content_type zwraca to samo co $_FILE.
    Tak to jest jak coś pisze po kilkunastu godzinach siedzenia nad ksiażkami (eh
    sesja).\r\nSorry za zamieszanie. Pozdrawiam"
- id: 6137
  author: '...'
  author_url: http://www.google.pl
  date: '2007-01-17 20:13:29 +0100'
  date_gmt: '2007-01-17 19:13:29 +0100'
  content: "\"Wstęp\r\nNiniejszy tekst powstał jako forma ostrzeżenia przed błędami,
    które popełniają nawet zawodowi programiści.\"\r\n\r\nMam do Ciebie duzo szacunku
    i nie chce pisac co mysle w tej chwili o Tobie po przeczytaniu tego PDF'a, dlatego
    tylko chce prosic o zmiane powyzszego zdania. Najlepiej bedzie jesli usuniesz
    fragment od przecinka do kropki.\r\n\r\nJesli \"zawodowi programisci\" popelniaja
    takie bledy, to lepiej zeby trole przejely Internet."
- id: 6138
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-01-17 20:24:51 +0100'
  date_gmt: '2007-01-17 19:24:51 +0100'
  content: "...:\r\n\r\nTak, takie błędy popełniają zawodowi programiści. Zawodowi,
    jako \"pracujący od lat w zawodzie,\" a nie jako \"specjaliści.\"\r\n\r\nI widziałem
    je w naprawdę dużych firmach, gdzie spodziewałbym się, że przy dziesięciu chętnych
    na miejsce jest spory odsiew. Widziałem takie kwiatki w wykonaniu ludzi, którzy
    pracowali wcześniej dla dużych portali (to wyjaśnia, czemu wiele portali tak szybko
    padło) :]"
- id: 6146
  author: Qp3k
  author_url: ''
  date: '2007-01-18 16:11:41 +0100'
  date_gmt: '2007-01-18 15:11:41 +0100'
  content: Dobrze, ze ktos o tym wszystkim napisal. Przyznac bowiem musze, ze zaczynajac
    przygode z PHP popelnialem wiekszosc z tych bledow. Nie zdawalbym sobie z tego
    sprawy, gdyby kilka bardziej zaawansowanych osob mnie nie uswiadomilo. Byc moze
    ten artykul rowniez kogos uswiadomi.
- id: 6321
  author: frob
  author_url: http://sysrq.net
  date: '2007-01-24 17:59:46 +0100'
  date_gmt: '2007-01-24 16:59:46 +0100'
  content: "Najbardziej ubawilem sie widzac te linie:\r\nzrobCosStrasznego();\r\n\r\n:]"
- id: 7322
  author: Brut[all]
  author_url: ''
  date: '2007-03-24 19:52:10 +0100'
  date_gmt: '2007-03-24 18:52:10 +0100'
  content: "Faktycznie całkiem niezła esencja bezpieczeństwa.\r\n\r\nBrakuje mi w
    zasadzie dwóch (choć pewnie o czymś sobie teraz nie przypominam) rzeczy:\r\n\r\n1.
    Właściwie, to nie potrafię zrozumieć, czemu nikt o tym nie wspomniał, bo to zdecydowanie
    najczęściej popełniany błąd:\r\nHTML Injection\r\nZbyt dużo chyba mówić nie muszę,
    połowa amatorskich for, systemów komentarzy, itp. posiada taką dziurę, choć to
    chyba akurat pierwsza dziurą, którą młody programista się uczy omijać.\r\n\r\nJednak
    nie należy jej z tego powodu lekceważyć: nieraz ludzie nieco bardziej zaawansowani,
    nie wiem, czy z rutyny, czy czegoś innego, pamiętają o zabezpieczenia \"głównych\"
    miejsc, jak treści postów, itp., a nie zabezpieczają tych \"bzdurek\".\r\nPamiętam,
    że swego czasu Spinacz escape'ował kod HTML w treściach postów, natomiast w ich
    tytułach, nazwach zdjęć, itp. już nie. A Chojnaca za amatora bynajmnmiej nie uważam.\r\nPodobnie
    zdarza się nieraz proste kopiowanie (lub z modyfikacją) czegoś z GET na wyjście
    aplikacji - i wtedy znów odpowiednio spreparowany link i jest problem.\r\n\r\n2.
    Bardzo ważne ze względu na to, że jest to dość wyjątkowa dziura: niewiele ludzi
    o niej wie, nie sprawia wrażenia groźnej, a jednak.\r\nChodzi mianowicie o to,
    aby nie zezwalać na requesty POST z obcym refererem (lub nawet i z pustyym - zależnie
    od tego, jak restrykcyjni chcemy być).\r\nWydaje się naprawdę śmieszną bzdurką,
    prawda?\r\n\r\nAle jeśli w jakimś serwisie podam linka na zewnętrzny serwer, gdzie
    umieszczę formularz z odpowiednio wypełnionymi danymi i go autosubmituję poprzez
    JS, to wyjdzie na to, że każdy, kto tu wejdzie zmieni sobie np. dane profilu osobowego.\r\nJeśli
    jeszcze lepiej pokombinuję i zrobię jakąś prowizoryczną stronę z jakimiś treściami
    z dupy, aby tylko przytrzymać na niej trochę kolesia, a w ukrytej ramce zacznę
    wysyłać całą serię takich formularzy praktycznie bez wiedzy wchodzącego, to mogę
    nawet wywołać małą reakcję łańcuchową. Bo jeśli załóżmy przykładowe Grono by nie
    było zabezpieczone na tego referera, przygotowałbym tak tego mojego \"wirusa\",
    że każdy wchodzący zaczyna na Gronie wysyłać posty do przypadkowych tematów z
    linkiem do tej mojej strony, to wszystko by już poszło lawinowo - domyślam się,
    że po dobie od zamieszczenia przeze mnie pierwszy raz linka linków tych by już
    było na całym gronie i parędziesiąt tysięcy.\r\n\r\nWarte przemyślenia."
- id: 8347
  author: rowery
  author_url: http://www.twomark.pl
  date: '2007-08-10 13:56:32 +0200'
  date_gmt: '2007-08-10 12:56:32 +0200'
  content: PHP i aplikacje WWW - ciekawie napisana praca.Gratuluję.
- id: 8570
  author: tłumaczenia angielski
  author_url: http://www.1800.pl
  date: '2007-10-15 09:44:11 +0200'
  date_gmt: '2007-10-15 08:44:11 +0200'
  content: Często tu zaglądam. Piszecie ciekawe arty.
---
<p>W ramach eksternistycznego zaliczenia kursu <abbr title="PHP Hypertext Preprocessor">PHP</abbr> na studiach, prowadzący zaoferował mi przygotowanie krótkiej prezentacji o języku. Prezentacje nie są tym, co programiści lubią najbardziej. Zamiast prezentacji wyszedł krótki tekst, a zamiast możliwości języka są błędy ludzi.</p>

<p>Całość zamieszczam i tutaj, może się komuś na coś przyda. O ile wierzę w swoją wiedzę, to zastrzegam z góry, że praca nie była jeszcze oceniana. Przepraszam też za wielkość, ale to AbiWord taki duży plik wygenerował :)</p>

<p>Pobierz <del>PHP i aplikacje WWW</del> (290 <abbr title="kilobajtów">kB</abbr>, <abbr title="Portable Document Format">PDF</abbr>)</p>
