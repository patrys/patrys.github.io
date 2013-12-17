---
layout: post
status: publish
published: true
title: Dlaczego systemy szablonowe są ważne
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 290
wordpress_url: http://www.room-303.com/blog/2006/09/17/dlaczego-systemy-szablonowe-sa-wazne/
date: 2006-09-17 14:12:14.000000000 +02:00
categories:
- web
- software
- code
tags: []
comments:
- id: 4729
  author: 'NuLL'
  author_url: http://null.phpfreaks.pl
  date: '2006-09-17 15:32:15 +0200'
  date_gmt: '2006-09-17 14:32:15 +0200'
  content: SMARTY - powolnosc, krowowatosc i PHP4. Pozatym ta dziwaczna składnia.
    Kiedyś S wykorzystywalem w kazdym projekcie - teraz dla kazdego projektu szukam
    alternatywy dla niego. Co do systemow szablonowych - zgadzam sie, ze sa potrzebne
    na kazdym kroku :-)
- id: 4734
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-09-17 15:41:04 +0200'
  date_gmt: '2006-09-17 14:41:04 +0200'
  content: "NuLL:\r\n\r\nAle Smarty działa bez problemu z aplikacjami PHP5. PHP4 nie
    używamy i nie chodzi mi tylko o numerek :)"
- id: 4735
  author: jpc
  author_url: http://jpc.jogger.pl
  date: '2006-09-17 16:16:41 +0200'
  date_gmt: '2006-09-17 15:16:41 +0200'
  content: "Oczywiście, żeby uzywać młotka (PHP) musimy znać metalugię i materiałoznawstwo
    (techniki obiektowe), więc uzywajmy elektronicznej wbijarki do gwoździ (Smarty).\r\nZ
    całą resztą się oczywiście zgadzam, ale to już wiesz, bo przecież ja byłem tym
    ostatnim z wielu ludzi, którzy się Ciebie pytali. ;]"
- id: 4736
  author: carstein
  author_url: http://carstein.jogger.pl
  date: '2006-09-17 18:42:44 +0200'
  date_gmt: '2006-09-17 17:42:44 +0200'
  content: Taka mała uwaga - ślepe includowanie pliku, który trafia przez GETa albo
    POSTa powoduje jednak o wiele bardziej groźne Remote Code Execution (przy włączonym
    fopen rzecz jasna). W tym wypadku XSS to tylko taka wisienka na torcie.
- id: 4737
  author: stan
  author_url: ''
  date: '2006-09-17 19:11:43 +0200'
  date_gmt: '2006-09-17 18:11:43 +0200'
  content: "nie jestem większym programistą, jednak na podstawach języków programowania
    się znam.\r\n\r\nuważam, że jeżeli jest projekt który wymaga szybkiego wykonania,
    a magiczny deadline się zbliża. to rzeczywiście szablony są jak najbardziej przydatne.
    po pierwsze dlatego, że są sprawdzone, a po drugie nie trzeba wynajdywać koła
    od nowa.\r\n\r\nz drugiej jednak strony, myślę, że jeżeli zajmujemy się swoim
    autorskim projektem, i chcemy aby wszystko grało - należy cały kod znać, i często
    ważne jest ,że to nasz kod - więc wiemy co gdzie jest, i ew. co mogliśmy źle zrobić.
    jednak problemem jest to, że gdy większa ilość osób pracuje przy naszym kodzie(a
    nie jest robiony obiektowo) to potem szybko można się pogubić.\r\n\r\njak napisałeś
    - wszystko zależy od klienta i zapotrzebowania."
- id: 4739
  author: Elus
  author_url: ''
  date: '2006-09-17 21:58:48 +0200'
  date_gmt: '2006-09-17 20:58:48 +0200'
  content: "Nie znalazłem w Twojej wypowiedzi ani jednego argumentu dlaczego Smarty
    (i inne systemy szablonów) lepiej sprawdzają się w warstwie widoku niż czyste
    php. Jakieś historie o empiku, licznikach i rozdzieleniu pracy pomiędzy programistów
    i webmasterów-designerów. Ok. Ale tak naprawdę to nie znaduję w tym wszystkim
    potwierdzenia Twojej tezy.\r\n\r\nArgumentem na pewno nie jest to ze da sie Smarty
    nauczyć w przeciągu doby. Śmiem twierdzić, że żeby nauczyć się podstaw PHP w stopniu
    wystarczającym do zbudowaniu w oparciu o niego szablon wystarczy jeszcze mniej
    czasu. Zwłaszcza dla webmastera-designera, który w większości przypadków zna konstrukcję
    zwykłej pętli np. z JavaScript. Do  zbudowania samego szablonu nie trzeba przecież
    znajomości żadnych złożonych konstrukcji językowych/programistycznych. Mimo wszystko
    myśle że taki {section} jest o wiele bardziej skomplikowany niż zwykły for.\r\n\r\nChyba
    że w tym wszystkim chodzi o ograniczone zaufanie do webmastera-designera. Tzn
    dajemy mu jezyk szablonowy o bardziej ograniczonej (aczkolwiek w zupełności wystarczającej)
    gramatyce, tak by niczego \"nie popsuł\". Z tego jednak co widzę wiekszość systemów
    szablonowych zostawia w tej kwestii otwartą furtkę (w przypadku szablonu Smarty
    jest to np. tag {php}).\r\n\r\nNie bardzo rozumiem też akapitu o atakach XSS i
    tym podobych. Przecież tego typu ataki wynikają ze złej konstrukcji kontrolera
    (w przeciwnym razie nie można mówić o dobrym rozdzieleniu warstw modelu MVC).\r\n\r\nChoć
    nie uważam się za programistę PHP to ostatnio miałem okazję pracować na takim
    właśnie stanowisku. Popełniłem też kilka szablonów w oparciu o Smarty. I teraz
    z perspektywy czasu zastanawiam się, czy faktycznie dało mi to taką wygodę i korzyści
    o jakich się poprzednio nasłuchałem."
- id: 4744
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-09-18 11:56:38 +0200'
  date_gmt: '2006-09-18 10:56:38 +0200'
  content: "Nigdzie nie napisałem, że każdy ma używać akurat Smartów.\r\n\r\ncarstein:\r\n\r\nMnie
    tam uczyli na bezpieczeństwie systemów, że ataki typu RCE zaliczają się do XSS
    (nie tylko JS/HTML injection).\r\n\r\nElus:\r\n\r\n<blockquote>Chyba że w tym
    wszystkim chodzi o ograniczone zaufanie do webmastera-designera. Tzn dajemy mu
    jezyk szablonowy o bardziej ograniczonej (aczkolwiek w zupełności wystarczającej)
    gramatyce, tak by niczego “nie popsuł”. Z tego jednak co widzę wiekszość systemów
    szablonowych zostawia w tej kwestii otwartą furtkę (w przypadku szablonu Smarty
    jest to np. tag {php}).</blockquote>\r\n\r\nChodzi głównie o to. Tag {php} w Smarty
    wyłącza się jedną linijką w konfiguracji tegoż. Właśnie dlatego, żeby nikt tam
    ani kawałka kodu nie mógł wstawić.\r\n\r\n<blockquote>Nie bardzo rozumiem też
    akapitu o atakach XSS i tym podobych. Przecież tego typu ataki wynikają ze złej
    konstrukcji kontrolera (w przeciwnym razie nie można mówić o dobrym rozdzieleniu
    warstw modelu MVC).</blockquote>\r\n\r\nA co powstrzyma pana Stefana przed napisaniem
    <code>include($_GET['plik']);</code>?"
- id: 4747
  author: carstein
  author_url: http://carstein.jogger.pl
  date: '2006-09-18 15:15:48 +0200'
  date_gmt: '2006-09-18 14:15:48 +0200'
  content: "Patrys:\r\nJa mam nieco inną klasyfikację powieszoną na ścianie w takim
    razie :)\r\n\r\nXSS rozróżniam od RCE ponieważ w pierszym przypadku narażone jest
    wyłącznie (jeśli mówimy o HTML/JS injection) bezpieczeństwo klientów serwisu,
    natomiast atak RCE ukierunkowany jest bardziej na sam site."
---
<p>Masa ludzi zadaje mi ciągle to samo pytanie &mdash; skoro <abbr title="PHP HyperText Preprocessor">PHP</abbr> został stworzony jako język prezentacyjny, to jaki jest sens implementowania w nim kolejnego języka prezentacyjnego &mdash; systemu szablonów?</p>

<p>To prawda, że <abbr>PHP</abbr> powstał właśnie jako język do osadzania wewnątrz kodu <abbr title="HyperText Markup Language">HTML</abbr>. Prawdą jest, że do dzisiaj mnóstwo ludzi w ten właśnie sposób go używa. Nic dziwnego, podczas wczorajszej wycieczki do <a href="http://www.empik.com/">Empiku</a>, natknęliśmy się z Qwiatem na stustronicową książeczkę o wdzięcznym tytule <q><abbr>PHP</abbr> &mdash; to proste.</q></p>

<h4>Już nie tylko liczniki</h4>

<p>Sam język jednak przeszedł od czasów wersji pierwszej ogromne zmiany, największe z nich miały miejsce pomiędzy trzecim i piątym wcieleniem. Skupiają się one na umożliwieniu łatwego budowania dużych aplikacji. Aplikacji, gdzie mieszanie warstwy widoku i kontrolera jest co najmniej wysoce niewskazane, ze względu na czytelność i łatwość zarządzania kodem.</p>

<p>Minęły czasy, kiedy języków server-side używało się do budowania liczników. Często całość treści jest generowana właśnie przez kod. Tyczy się to tak samo <abbr>PHP</abbr>, jak każdego innego języka, który może działać po stronie serwera. Zmieniły się oczekiwania, wzrosła skala projektów, logika wewnątrz strony przestała wystarczać.</p>

<p>Ktoś powie zaraz, że przecież można oddzielić warstwę widoku i nadal korzystać tam z <abbr>PHP</abbr>, tak jak robi to <a href="http://cakephp.org/">CakePHP</a>. Można, czasem jednak nie warto. Cake powstał jako klon uznanego frameworku <a href="http://rubyonrails.com/">Ruby on Rails</a>. Oba celują w projekty rozwijane &mdash; przynajmniej w pierwszych stadiach życia &mdash; metodą programowania ekstremalnego. Koncentrują się na jak łatwiejszym zbudowaniu proof-of-concept i dalszym jego rozwoju, już po odkręceniu dodatkowych kółeczek od roweru.</p>

<h4>Serwisy budują projektanci, a nie programiści</h4>

<p>Oczywiście, są aplikacje, przy budowie których pracują prawie wyłącznie programiści. Niech będzie to <a href="http://gmail.com/">Google Mail</a>, <a href="http://youtube.com/">YouTube</a>, czy <a href="http://wrocek.pl/">Wrocek</a>. Prawda jest jednak taka, że większość komercyjnych serwisów internetowych jest budowana dla konkretnego klienta przez agencje interaktywne.</p>

<p>Ich ceny oscylują w przedziale od kilku do kilkunastu/kilkudziestu tysięcy i zyski z tego typu działalności ciężko przeznaczyć na zatrudnienie połowy Microsoftu. Dlatego też do zadań programisty często należy tylko przygotowanie silnika, zaś resztę pracy wykonują projektanci &mdash; webmasterzy lub graficy, w których gestii jest przygotowanie odpowiedniego kodu <abbr>HTML</abbr>, arkuszy <abbr title="Cascading Style Sheets">CSS</abbr> i połączenie tego w całość &mdash; produkt, który można oddać klientowi.</p>

<p>Co z tego wynika? Ano wynika tyle, że przy zatrudnianiu ważniejsza jest doskonała znajomość obu wyżej wymienionych technologii, niż zdolności programistyczne. Nie każdy webmaster zna <abbr>PHP</abbr> (Javę, Pythona, platformę .NET). <a href="http://smarty.php.net/">Smarty</a> można opanować w ciągu jednej doby, to zdecydowanie za mało na poznanie choćby części filozofii projektowania zorientowanego obiektowo.</p>

<h4><q>This sit3 haxx0rd by scr1pt kiddi3z</q></h4>

<p>Wyżej wspomniałem, że nie każdy jest programistą. Praktyka uczy też, że nie każdy powinien. Miałem w życiu wiele sytuacji, w których zmuszony byłem współpracować z ludźmi, którzy zdawali się całą swoją wiedzę pozyskać ze wspomnianej empikowej książeczki. Dość powiedzieć, że podatność na <abbr title="Structured Query Language">SQL</abbr> injection to najlżejsze z popełnianych przewinień.</p>

<p>Popularne grzechy to ślepe <code>include</code>'owanie pliku, którego nazwa trafiła przez wywołania <code>GET</code> lub <code>POST</code> (najczęstsza, poza korzystaniem z <code>register_globals</code>, przyczyna ataków <abbr title="Cross-Site Scripting">XSS</abbr>), trzymanie ważnych danych w ciasteczkach przeglądarki, rekordzista umieścił tam nawet całe zapytania <abbr>SQL</abbr>. Z pewnością wystarczyłoby na wypełnienie kalendarza <a href="http://thedailywtf.com/">Daily <abbr title="What The Fuck">WTF</abbr></a> na najbliższy rok.</p>

<p>Silniki szablonów mają tę ogromną zaletę, że zapewniają piaskownicę (<q>sandbox</q>), w której można bezpiecznie wywołać kod nieznanego pochodzenia (czytaj: cudzy kod). Nazwa pochodzi od terminu, jakim saperzy nazywają specjalne pojemniki i pomieszczenia do badania i rozbrajania znalezionych przedmiotów, gdzie ewentualna eksplozja nie naraża niczyjego życia.</p>

<p>W tym przypadku niczyje życie nie jest bezpośrednio zagrożone, ale ciężko wypracować sobie reputację, kiedy co drugie wdrożenie twojego silnika kończy się włamaniem na serwer. Korzystanie w przypadku prezentacji z prostego języka, zbudowanego specjalnie do tego celu, daje pewność, że nawet najmniej kompetentny człowiek nie będzie w stanie nic zepsuć.</p>

<p>W zasadzie tyle chciałem napisać, ale może ktoś ma zupełnie inny pogląd na te sprawy? Z góry zapowiadam, że nie interesują mnie argumenty na poziomie <q>Smarty to nieakceptowalny narzut rzędu dziesiątej części sekundy na każdą wyświetlaną stronę.</q></p>
