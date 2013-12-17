---
layout: post
status: publish
published: true
title: 'Warsztat: PHP'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 259
alias: /blog/2006/05/23/warsztat-php/
date: 2006-05-23 20:35:49.000000000 +02:00
categories:
- web
- software
- code
tags: []
comments:
- id: 3752
  author: slav
  author_url: http://jasinski.us
  date: '2006-05-23 20:55:47 +0200'
  date_gmt: '2006-05-23 19:55:47 +0200'
  content: hmm... eAccelerator, lighttpd, smarty, adodb nic wiecej do szczescia nie
    jest potrzebne... no i odrobina cierpliwosci ;)
- id: 3753
  author: kwdowicz
  author_url: http://wdowicz.com
  date: '2006-05-23 21:15:23 +0200'
  date_gmt: '2006-05-23 20:15:23 +0200'
  content: "ja staram sie nigdy nie korzystać z PEAR'a, AdoDB jest świetne ale też
    nie korzystam :),\r\njabber class i magic RSS a owszem, ale aplikacje się na nich
    nie opierają wiec można ich uzywać... nigdy jeszcze nie próbowałem czy mój serwer
    ma cos takiego jak te accleleratory ... jak to sprawdzić ?"
- id: 3754
  author: KeyBi
  author_url: http://www.keybi.jawnet.pl
  date: '2006-05-23 21:47:05 +0200'
  date_gmt: '2006-05-23 20:47:05 +0200'
  content: Z tego co mi wiadomo to w PHP6 ma już nie być ani register_globas ani magic_quotes
    ... dobrze bo od zawsze były one powodem kłopotów.
- id: 3755
  author: MySZ
  author_url: http://urzenia.net/
  date: '2006-05-23 21:47:32 +0200'
  date_gmt: '2006-05-23 20:47:32 +0200'
  content: "Do maili: phpmailer\r\nSzablony: FastTemplates (jako zaszłość), jak coś
    nowego to OPT\r\n\r\nJeśli coś z jabberem związanego, to też class.jabber.php.\r\n\r\nDo
    DB kiedys natywnych funkcji (tylko mysql, nigdy prawie nie używałem innej bazy),
    teraz PDO.\r\n\r\nW sumie tyle. Resztę mam własną, albo piszę z palca czasem.
    Przymierzam się tez do Cake, żeby poznać co nieco, ale ostatnio nie mam czasu
    żeby go na to poświęcić :/"
- id: 3756
  author: qcol
  author_url: http://www.probit.net
  date: '2006-05-23 22:04:18 +0200'
  date_gmt: '2006-05-23 21:04:18 +0200'
  content: "w samych smarty pluginy: smartyvalidate, smartypaginate, thumb (http://www.cerdmann.com/thumb/)\r\n\r\nczęsto
    jeśli wystarczają to odpowiedniki kombajnów: smarty lite i adodb lite"
- id: 3757
  author: carstein
  author_url: http://carstein.jogger.pl
  date: '2006-05-23 22:24:09 +0200'
  date_gmt: '2006-05-23 21:24:09 +0200'
  content: Ja ze względów bezpieczeństwa to bym jeszcze fopen wyłączył. No wszystkie
    niepotrzebne moduły.
- id: 3758
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-05-23 22:30:59 +0200'
  date_gmt: '2006-05-23 21:30:59 +0200'
  content: "carstein:\r\n\r\nA fopen blokować w jakim celu? Smarty blokują includowanie
    zewnętrznych plików, a bez tego ciężko choćby RSS parsować."
- id: 3759
  author: Draakhan
  author_url: http://draakhan.jogger.pl/
  date: '2006-05-23 22:36:10 +0200'
  date_gmt: '2006-05-23 21:36:10 +0200'
  content: "Jak chodzi o ułatwianie sobie życia i przede wszystkim oszczędność czasu
    przy debugowaniu to przede wszystkim jakaś prosta klasa wyciągająca informacje
    o stosie wywołań funkcji w przypadku pojawienia się błędu.\r\n\r\nmagic_quotes_gpc
    - fakt, porażka. A jeszcze ciekawiej jest jak ktoś włączy magic_quotes_sybase.
    A tak na boku, jeśli już zacytujesz $_REQUEST to pozostałych trzech chyba już
    nie trzeba. :)\r\n\r\nNowych rzeczy to nie dorzucę bo generalnie używam tego co
    już wymieniłeś.\r\n\r\n@kwdowicz: A czemu starasz się nie korzystać z PEAR'a?
    Moim zdaniem jeden z lepszych zbiorów bibliotek. Fakt, czasem coś tam trzeba poprawić
    w nich i posprawdzać pod względem bezpieczeństwa ale mimo wszystko wydaje mi się,
    że nie ma sensu z palca pisać tego co już ktoś napisał."
- id: 3760
  author: kwdowicz
  author_url: http://wdowicz.com
  date: '2006-05-23 22:44:15 +0200'
  date_gmt: '2006-05-23 21:44:15 +0200'
  content: '@Draakhan: jak dla mnie strasznie kobylaste, chcesz skorzystać z jednej
    czy dwóch klass musisz mieć zainstalowane 12 różnych. Jak już naprawdę nie ma
    co pisać z palca to wole poszukać coś sprytniejszego, a i tak od jakiegoś czasu
    wszytsko buduje na cakePHP i najwyżej dołącze kilka drobnych vendorów typu FCK,
    smarty (ewentualnie jak sam nie robie HTMLA, bo jak robie to ), jabber.class czy
    magic rss.'
- id: 3761
  author: kwdowicz
  author_url: http://wdowicz.com
  date: '2006-05-23 22:45:31 +0200'
  date_gmt: '2006-05-23 21:45:31 +0200'
  content: sory... (...) bo jak robię to używam zwykłego php, bez szablonów (...)
- id: 3762
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-05-23 23:06:32 +0200'
  date_gmt: '2006-05-23 22:06:32 +0200'
  content: "Do debugowania to polecam narzędzia typu <a href=\"http://dd.cron.ru/dbg/\"
    rel=\"nofollow\">DBG</a>.\r\n\r\nW naszych aplikacjach każdy błąd i ostrzeżenie
    są wyłapywane przez klasę obsługi i jeśli aktywny jest tryb rozwojowy, to wyrzucany
    jest cały backtrace. Podobnie z klasą do obsługi bazy (klasa dziedzicząca po mysqli)."
- id: 3764
  author: qwiat
  author_url: ''
  date: '2006-05-23 23:51:58 +0200'
  date_gmt: '2006-05-23 22:51:58 +0200'
  content: Jak mieliśmy się okazję przekonać że DBG ma sens tylko na serwerze deweloperskim,
    na produkcji odradzam.
- id: 3779
  author: normanos
  author_url: http://normanos.com
  date: '2006-05-24 10:32:43 +0200'
  date_gmt: '2006-05-24 09:32:43 +0200'
  content: "szablony: OPT, przy malutenkich sajtach albo odchudzony OPT albo (kiedys)
    smarty-lite.\r\n\r\nobsluga baz: PDO z nakładką OPD\r\n\r\nTeraz Polska! :D"
- id: 3784
  author: carstein
  author_url: http://carstein.jogger.pl
  date: '2006-05-24 12:43:19 +0200'
  date_gmt: '2006-05-24 11:43:19 +0200'
  content: "Patrys:\r\nTu się właśnie kłania cała pierdołowatość języka PHP: brak
    rozgraniczenia pomiędzy odczytem z zewnętrnzych serwerów, a wnętrza serwera. \r\n\r\nFopen
    blokuje się po to, aby uniemożliwośc wykonywanie ataków XSS. Zdaje sobie sprawę,
    że często nie można tego zrealizować. Niemniej jednak, czasami warto to choćby
    rozważyć."
- id: 3785
  author: medyk
  author_url: http://www.medikoo.com
  date: '2006-05-24 13:53:49 +0200'
  date_gmt: '2006-05-24 12:53:49 +0200'
  content: "Konfiguracja tak jak wyżej.. jeszcze dorzucę, że określam dostęp wszystkich
    metod klasy (public, protected czy private) jak i kiedy tylko możliwe określam
    typ parametrów funkcji.. to też dosyć istotne w wyłapywaniu błędów.\r\nDo debugowania
    Xdebug, efektywniejsze mi się wydaje analizowanie przejścia kodu niż klikanie
    F12 i zgadywanie gdzie coś skręcilo nie tam gdzie trzeba. Do przetrawiania trace'a
    napisałem dodatkowy skrypt, który w czytelniejszy wypluwa na stronę przejście
    przez algorytm.\r\nJeśli chodzi o szablony, wyjściowe dokumenty to tylko XML'e
    w moim przypadku, napisałem klasy, poprzez które buduję czy też wypluwam drzewo
    DOM. Kiedy pracuję nad kodem drzewo faktycznie jest budowane poprzez rozszerzenie
    DOM i automatycznie walidowane jeśli mam takie życzenie. Natomiast kiedy wystawiam
    stronę na zewnątrz wszystko od razu jest przekierowywane na wywołania 'echo' by
    nie wykonywać nie potrzebnych operacji. Parę miesięcy zacząłem w ten sposób pracować
    i co raz bardziej sobie cenię to podejście."
- id: 3790
  author: h
  author_url: ''
  date: '2006-05-24 16:08:56 +0200'
  date_gmt: '2006-05-24 15:08:56 +0200'
  content: "Odnosnie magic_quotes, to lepiej chyba , ze jest on wlaczony, niz nie.\r\nNa
    pewno wielu aplikacjom to pomoglo, przed tzw ,,popsuciem''.\r\n\r\nFakt, ze czasem
    trzeba stripowac te slashe, ale koniec koncem i tak stosuje sie rozne funkcje
    do cytowania jak np mysql_real_escape etc. \r\nCzy moze sie myle?"
- id: 3792
  author: medyk
  author_url: http://www.medikoo.com
  date: '2006-05-24 19:09:14 +0200'
  date_gmt: '2006-05-24 18:09:14 +0200'
  content: "-&gt; h\r\nMyślę, że zdecydowanie powinno się mieć wyłączone magic_quotes.
    Jak masz dobrze zaprojektowaną aplikacje, rozbitą na moduły, moduł który dodaje
    dane do wprowadzenia bazy powinien dostać dane w takiej formie w jakiej powinny
    one się znaleźć się w bazie. To on powinien odpowiadać za przygotowanie zapytania
    i jego wykonanie, myślę, że powinien on być niezależny od źródła pochodzenia danych.
    Być może, kiedyś będziesz chciał wstawiać dane na przykład z pliku XML.. itd itd."
- id: 3793
  author: h
  author_url: ''
  date: '2006-05-24 20:46:21 +0200'
  date_gmt: '2006-05-24 19:46:21 +0200'
  content: Znaczy tak, rozumiem, tez tak uwazam, myslalem tylko, wzgledy przeciw maja
    jakies glebsze podloze
- id: 3794
  author: medyk
  author_url: http://www.medikoo.com
  date: '2006-05-24 21:34:13 +0200'
  date_gmt: '2006-05-24 20:34:13 +0200'
  content: "-&gt; h\r\nGdzieś kiedyś czytałem, że ciągi znaków, do wprowadzania do
    bazy MySQL należy cytować tylko za pomocą mysql_real_escape(), bo tylko ta funkcja
    robi to prawidłowo.. tak więc byłby to kolejny argument przeciw magic_quoutes,
    które po prostu aplikują addslashes()\r\nNie mniej nie wiem do końca jaka dokładnie
    jest różnica między między real_escape a addslashes, prawdopodobnie chodzi o inne
    zastrzeżone znaki w mysql, które mogą okazać się kłopotliwe w przypadku jakiś
    specyficznych ciągów znaków."
- id: 3970
  author: smoku
  author_url: http://staff.xiaoka.com/smoku/
  date: '2006-06-19 12:57:39 +0200'
  date_gmt: '2006-06-19 11:57:39 +0200'
  content: class.jabber.php został podjęty i jest rozwijany
- id: 3979
  author: Michał Fikus
  author_url: ''
  date: '2006-06-21 13:56:09 +0200'
  date_gmt: '2006-06-21 12:56:09 +0200'
  content: "magic_quotes_gpc - masakra, najlepiej off. Zawsze lepiej przelecieć tablice
    \"ręcznie\" a do sql'a używać jakiejś natywnej funckji dla db (np. mysql_real_escape_string).\r\nerror_reporting
    - preferuje ustawiać w .htaccess : php_value error_reporting 4095 (bo często przy
    przenoszeniu aplikacji z warsztatu na inny serwer nie mogę korzystać z php.ini
    - a .htaccess coraz częściej jest dostępny)"
- id: 3983
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-06-22 02:30:39 +0200'
  date_gmt: '2006-06-22 01:30:39 +0200'
  content: "Michał:\r\n\r\nCo do cytowania danych dla SQL -- na ogół wystarczy zwykłe
    cytowanie cudzysłowów i apostrofów.\r\n\r\nUstawianie error_reporting z poziomu
    .htaccess to paskudna metoda. To są predefiniowane stałe i nikt nie da ci gwarancji
    (i nie powinien), że wartości liczbowe będą identyczne w kolejnych wersjach PHP.
    Od tego jest funkcja ini_set(...)."
- id: 3996
  author: Michał Fikus
  author_url: ''
  date: '2006-06-22 18:55:53 +0200'
  date_gmt: '2006-06-22 17:55:53 +0200'
  content: "Na ogół tak... ale w pewnych znanych i być może w takich co dopiero wyjdą
    w praniu nie da rady, a funkcje o których mówiłem napewno będą nieustannie uaktualniane.\r\nWięc
    wolę pozostać przy pewnej metodzie.\r\n\r\nini_set() - tak, w sumie zapomniałem
    o tym... ale z tego powodu, że kiedyś odrzuciłem to ze względu na szybkość (mimo,
    że w praktyce jeszcze nie tworzyłem oprogramowania pod silnie obciążony sprzęt,
    to jednak chęć optymalizacyjna zawsze jakaś jest). Rzeczywiście, dobre to rozwiązanie
    (oczywiście dla nie wszystkich projektów - choć zdecydowanej większości owszem).\r\nA
    co do wartości liczbowych... tak, gwarancji nikt nie daje. Jednak biorąc pod uwagę
    historię stanie się to raczej na długi czas standardem.\r\nEwentualny upgrade
    aplikacji w związku z taką zmianą nie powinien stanowić problemu... a jakiej dokładnie
    Ty metody używasz? E_ALL | E_STRICT? Z tego co kiedyś gdzieś czytałem, to wywołane
    to z poziomu php przez error_reporting() nie pokazuje jednak wszystkich błędów."
- id: 3999
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-06-22 19:40:52 +0200'
  date_gmt: '2006-06-22 18:40:52 +0200'
  content: "Michał:\r\n\r\nNie pokazuje błędów na poziomie parsera/leksera PHP, ale
    błędy składniowe raczej cię chyba nie interesują (wyłapują się zawsze same i są
    nie do pominięcia)."
---
<p>Najładniejsze szablony nie sprzedadzą się same, kiedy klient oczekuje, że serwis będzie robił coś więcej niż prezentacja statycznej treści. Tutaj potrzebne są języki server-side, a ja akurat specjalizuję się w <abbr title="PHP Hypertext Preprocessor">PHP</abbr> (co nie przeszkadza mi swobodnie poruszać się w Perlu, Pythonie i w miarę sprawnie radzić sobie z kodem Ruby — nie uważam <abbr>PHP</abbr> za najlepszy język i o jego wadach już kiedyś pisałem).</p>

<h4>Konfiguracja środowiska</h4>

<p>Na potrzeby rozwoju aplikacji mamy uruchomione własne mini-środowisko, klasyczny <abbr title="Linux, Apache, MySQL &amp; PHP">LAMP</abbr>, z <abbr>PHP</abbr>5 na pokładzie. Większość konfiguracji to wierna kopia ustawień maszyn produkcyjnych, na których aplikacje są wdrażane, jest jednak kilka kwestii technicznych, o których warto wspomnieć.</p>

<dl>
<dt><code>error_reporting</code></dt>
<dd>zawsze ustawiony na najwyższy poziom, z <code>E_STRICT</code> włącznie, <abbr>PHP</abbr> wybacza za dużo, żeby pozwolić sobie na zignorowanie <em>choćby jednego notice</em></dd>

<dt><code>register_globals</code></dt>
<dd>bezwzględnie wyłączony, poleganie na tym mechanizmie to proszenie się o kłopoty (wystarczy powiedzieć, że spory odsetek ataków na serwisy wynika właśnie ze stosowania automatycznie rejestrowanych zmiennych), a zastosowanie w ten sposób uzyskanych zmiennych w środowisku obiektowym — nikłe</dd>

<dt><code>magic_quotes_gpc</code></dt>
<dd>cóż — chciałoby się napisać, że to zło, ale jeszcze przez jakiś czas aplikacja, przy której pracujemy, będzie wymagać tego ustawienia — brak wsparcia dla preparowanych zapytań w pierwszych wersjach sprawił, że teraz jeszcze trudniej byłoby je zaimplementować — w najbliższym czasie do projektu dołączy kod, który usuwa automatyczne cytowanie, jeśli jest aktywne, a następnie cytuje ponownie zawartość tablic <code>$_GET</code>, <code>$_POST</code>, <code>$_REQUEST</code> i <code>$_COOKIE</code></dd>
</dl>

<h4>Biblioteki</h4>

<dl>
<dt><a href="http://pear.php.net/"><abbr title="PHP Extension and Application Repository">PEAR</abbr></a></dt>
<dd>niewątpliwie, najobszerniejsza biblioteka rozszerzeń językowych dla <abbr>PHP</abbr>, paczki <a href="http://pear.php.net/package/Mail">Mail</a> i <a href="http://pear.php.net/package/Mail_Mime">Mail_Mime</a> stanowią podstawową część większości z naszych aplikacji</dd>

<dt><a href="http://cakephp.org/">CakePHP</a></dt>
<dd>szkielet do szybkiego prototypowania i wdrażania aplikacji o średnim i małym poziomie skomplikowania — pozwala minimalnym nakładem kodu uzyskać maksimum funkcjonalności, a przy tym posiada wygodne narzędzia do testowania aplikacji</dd>

<dt><a href="http://smarty.php.net/">Smarty</a></dt>
<dd>jeden z najwygodniejszych i najłatwiej rozszerzalnych silników szablonowych dla <abbr>PHP</abbr>, zbudowany na bazie wtyczek i pozwalający na wykonywanie praktycznie dowolnych operacji na przekazanych przez silnik danych — jednocześnie chroni wnętrze aplikacji przed złośliwymi zmianami w szablonach i optymalizuje czas wykonania kodu przez utrzymywanie cache szablonów w postaci skompilowanej do kodu <abbr>PHP</abbr></dd>

<dt><a href="http://cjphp.netflint.net/">class.jabber.php</a></dt>
<dd>od dłuższego czasu nierozwijany, ale wciąż jeden z najbardziej wszechstronnych interfejs do sieci Jabber, używany przeze mnie do wysyłania automatycznych powiadomień z poziomu serwisów</dd>

<dt><a href="http://magpierss.sourceforge.net/">Magpie <abbr title="Really Simple Syndication">RSS</abbr></a></dt>
<dd>bardzo wygodna klasa do parsowania wszelakiej maści kanałów informacyjnych, wbrew nazwie, świetnie sobie radzi z dokumentami Atom</dd>
</dl>

<h4>Bezpieczeństwo kodu</h4>

<dl>
<dt><a href="http://www.ioncube.com/">ionCube <abbr>PHP</abbr> Encoder
</a></dt>
<dd>jeden z wiodących na rynku pakietów do nieodwracalnego szyfrowania kodu, tańszy od konkurencyjnego rozwiązania <a href="http://www.zend.com/products/zend_guard">Zend Guard</a> i oferujący praktycznie identyczną funkcjonalność, a przy tym powszechnie dostępny na polskich serwerach</dd>

<dt><a href="http://eaccelerator.net/">eAccelerator</a></dt>
<dd>darmowy, ale znacznie uboższy w funkcje kuzyn komercyjnych narzędzi do zabezpieczania kodu, wywodzący się z bazy kodowej popularnego przodka — Turck mmCache, jedyne dostępne narzędzie w przypadku serwerów home.pl</dd>
</dl>

<p>A czego wy używacie w codziennej pracy? O edytorach postaram się podyskutować następnym razem, więc póki co, zostańmy przy języku.</p>

Technorati Tags: <a href="http://technorati.com/tag/php" rel="tag">php</a>, <a href="http://technorati.com/tag/encoder" rel="tag">encoder</a>, <a href="http://technorati.com/tag/accelerator" rel="tag">accelerator</a>, <a href="http://technorati.com/tag/template" rel="tag">template</a>, <a href="http://technorati.com/tag/smarty" rel="tag">smarty</a>, <a href="http://technorati.com/tag/jabber" rel="tag">jabber</a>, <a href="http://technorati.com/tag/pear" rel="tag">pear</a>, <a href="http://technorati.com/tag/cakephp" rel="tag">cakephp</a>, <a href="http://technorati.com/tag/rss" rel="tag">rss</a>, <a href="http://technorati.com/tag/tools" rel="tag">tools</a>
