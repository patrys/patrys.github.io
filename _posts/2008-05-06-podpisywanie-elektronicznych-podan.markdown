---
layout: post
status: publish
published: true
title: Podpisywanie elektronicznych podań
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 444
wordpress_url: http://room-303.com/blog/?p=444
date: 2008-05-06 14:26:42.000000000 +02:00
categories:
- software
tags: []
comments:
- id: 19472
  author: Hoppke
  author_url: http://repo.dobremiasto.net/
  date: '2008-05-06 14:53:17 +0200'
  date_gmt: '2008-05-06 13:53:17 +0200'
  content: "Co kwartał jeździć do urzędu i składać nowy wniosek?\r\nDla ludzi zatrudnionych
    na pełnym etacie / mających dalej do urzędów to męczące. Nie da się tego jakoś
    uniknąć?\r\n\r\nNajchętniej bym widział jednak jakieś rozwiązanie z fizycznym
    kluczoidentyfikatorem. Klucz przechowywany na komputerze to jednak łatwy łup dla
    trojanów, zwłaszcza gdyby Państwo opracowało jakieś swoje standardowe narzędzie
    do zarządzania kluczami/podpisywania dokumentów.\r\n\r\nI chyba zbyt optymistycznie
    szacujesz znikomy koszt oprogramowania -- nie wierzę, że ktoś da radę w ciągu
    wieczora skrobnąć na przykład stronę, która generuje Ci wnioski o \"key renewal\"
    z kodami kreskowymi etc. Chyba, że bardzo luzacko podchodzisz do jakości kodu
    i tzw. \"audytowalności\"."
- id: 19473
  author: mt3o
  author_url: ''
  date: '2008-05-06 15:00:45 +0200'
  date_gmt: '2008-05-06 14:00:45 +0200'
  content: "W porównaniu do obecnego systemu, to ten koszt rzeczywiście byłby niemal
    zerowy... \r\n\r\nCo do piątej różnicy - czyżby znów casus programu \"płatnik\"?
    Z elektronicznego podpisu się poważnie nie da korzystać na systemach bez logo
    microsoftu?"
- id: 19474
  author: Patrys
  author_url: http://room-303.com/
  date: '2008-05-06 15:03:59 +0200'
  date_gmt: '2008-05-06 14:03:59 +0200'
  content: "Hoppke:\r\n\r\nUstalenie ważności klucza na kwartał to termin wzięty z
    powietrza. W praktyce byłaby to pewnie wielokrotność roku (przy generowaniu klucza
    sam możesz sobie dowolnie ten termin skrócić).\r\n\r\nPrzechowywanie na fizycznym
    nośniku to kwestia drugoplanowa. Każdy klucz wymaga jakiegoś zabezpieczenia, czy
    to będzie certyfikat użytkownika, czy klucz GPG, czy fizyczny klucz do skrytki
    w banku.\r\n\r\nKoszt oprogramowania naprawdę jest znikomy, przenośne implementacje
    PGP z w pełni otwartym kodem istnieją od dawna, są też w powszechnym użyciu w
    innych aplikacjach (klient e-mail, komunikator).\r\n\r\nWniosek to zwykły PDF
    z imieniem, nazwiskiem, PESELem i datą ważności, a kod kreskowy nie jest niczym
    tajnym, bo jest tam identyfikator klucza publicznego, który nie zawiera więcej
    informacji niż właśnie imię i nazwisko. ReportLab z odpowiednią czcionką dla kodów
    kreskowych pozwoli ci zmieścić całość w +/- 100 liniach kodu Pythona. Kod kreskowy
    zaproponowałem tylko po to, żeby pani w okienku nie musiała przepisywać ciągów
    szesnastkowych ręcznie."
- id: 19475
  author: Patrys
  author_url: http://room-303.com/
  date: '2008-05-06 16:28:35 +0200'
  date_gmt: '2008-05-06 15:28:35 +0200'
  content: "mt3o:\r\n\r\nNie wiem, jak jest przy składaniu podań, tam prawo jest mocno
    nieprecyzyjne. Za to ustawa o podpisie elektronicznym wymaga użycia kwalifikowanego
    \"bezpiecznego urządzenia,\" co w praktyce oznacza programy dostarczone przez
    wystawcę certyfikatu. Wystawców mamy czterech, mamy też cztery różne programy.
    Każdy tylko i wyłącznie pod Windows."
- id: 19476
  author: harnir
  author_url: http://harnir.net/
  date: '2008-05-06 17:19:31 +0200'
  date_gmt: '2008-05-06 16:19:31 +0200'
  content: "Dobrze pomyślane Patrysie, podpisuję się ;) pod nim rękami i nogami. Teraz
    trzeba to podrzucić gdzieś do organów państwowych, niech się zastanowią nad tym
    rozwiązaniem...\r\n\r\nA przy okazji z klucza GPG obywatela urząd mógłby wyciągnąć
    jego adres e-mail i jeszcze bardziej usprawnić komunikację... Co prawda centralna
    sieć serwerów email/IM ma swoje zalety (a dodanie jeszcze jednego serwera SMTP/POP3/IMAP
    do swojego klienta poczty to pestka), ale z drugiej strony to ogromna pokusa dla
    crackerów i innych..."
- id: 19477
  author: Bartłomiej Dymecki
  author_url: http://www.dymecki.pl
  date: '2008-05-06 18:06:00 +0200'
  date_gmt: '2008-05-06 17:06:00 +0200'
  content: Jeśli chodzi o przechowywanie klucza, to bierz pod uwagę najsłabszy element
    takiego systemu - użytkownika. Wiadomo, jaka jest wiedza informatyczna w społeczeństwie...
    Projektując system trzeba brać pod uwagę słabości ludzi. Osobiście takie rozwiązanie
    wydaje mi się ryzykowne.
- id: 19480
  author: Patrys
  author_url: http://room-303.com/
  date: '2008-05-06 19:45:33 +0200'
  date_gmt: '2008-05-06 18:45:33 +0200'
  content: "Bartłomiej:\r\n\r\nKlucz trzeba przechowywać tak samo jak certyfikat.
    Użycie GPG nie wyklucza tu użycia zewnętrznego urządzenia. Z drugiej strony, klucz
    prywatny jest zabezpieczony hasłem, więc nikt nie będzie masowo kradł kluczy,
    bo nie starczy mu mocy na próby ich łamania."
- id: 19487
  author: wariat
  author_url: ''
  date: '2008-05-07 09:03:50 +0200'
  date_gmt: '2008-05-07 08:03:50 +0200'
  content: "Jeśli do wyboru jest:\r\n\r\n- klucz przechowywany nie wiadomo gdzie,
    bo raz na USB, raz na karcie chipowej, raz w katalogu z pr0nem a raz ... etc\r\n-
    1337 dostępnych programów obsługujących kodowanie za pomocą klucza\r\n\r\nlub\r\n\r\n-
    jeden z 4rech programów każdy powiązany ze specyficznym kluczem używanym w określonych
    momentach\r\n\r\ni jeśli pamiętać, że przeciętny ZU jest fanem przechowywania
    wirusów, trojanów i keyloggerów w swoim komputerze to ... rozwiązanie Patrysa
    wcale nie wydaje mi się mniej bezpieczne."
- id: 19489
  author: Hoppke
  author_url: http://repo.dobremiasto.net/
  date: '2008-05-07 15:38:20 +0200'
  date_gmt: '2008-05-07 14:38:20 +0200'
  content: "@Patrys: rok czy dwa ważności dałoby się już przełknąć.\r\n\r\nAle trzeba
    pamiętać o specyfice użytkowników. To powinno być coś fizycznego, jak dowód osobisty
    czy karta kredytowa. To komplikuje oczywiście cały proces i podnosi koszt, ale
    trzeba pamiętać, że potencjalni użytkownicy będą przypominać raczej klientów naszej-klasy
    niż czytelników tego bloga.\r\n\r\nA wychodzę z założenia, że statystyczny Polak
    łatwiej zabezpieczy przed kradzieżą kartę w swoim portfelu niż plik na swoim dysku.\r\n\r\nZ
    tego samego powodu, jeśli trzymać się PGP, od razu musiałbyś mieć kryteria określające
    \"dostatecznie mocne\" hasło i nie pozwalające użyć kluczy słabo zabezpieczonych
    (względnie proste jeśli klucz przechowywany jest na karcie chipowej, trudniejsze
    jeśli utrzymujesz go w postaci pliku na prywatnym komputerze) . Inaczej użytkownicy
    pójdą po najmniejszej linii oporu i nie zabezpieczą hasłem w ogóle, lub użyją
    hasła ze słownika. I założenie \"nikt nie będzie kradł kluczy, bo nie wystarczy
    mu mocy na łamanie haseł\" stanie się fantazją.\r\n\r\nNiestety nie można tu powiedzieć
    \"jak się nie zabezpieczysz odpowiednio to sam sobie jesteś winien\", bo system
    implementowany na taką skalę powinien jednak wymuszać pewien minimalny poziom
    bezpieczeństwa.\r\n\r\n\"Przenośne implementacje PGP z w pełni otwartym kodem
    istnieją od dawna\"\r\n\r\nPewnie, że tak. Kryptografia też stoi mocno, mamy nawet
    w Polsce masę ludzi którzy się naprawdę na tym znają. Problem w tym, że nie ma
    odpowiedniego nasycenia fachowcami w tych warstwach, które podejmują decyzje,
    hmm, \"administracyjne\". Myślę, że w takich projektach większy udział powinny
    brać ośrodki akademickie. Może nawet na zasadzie opracowywania konkurencyjnych
    rozwiązań (Kraków kontra Warszawa kontra Wrocław...). Oczywiście bez dodatkowych
    dotacji ze skarbu państwa, dla samego prestiżu. No, zwycięzca mógłby dostać jakiś
    grant uznaniowy.\r\n\r\nImplementację może już potem robić firma z przetargu,
    ale architekturę powinni opracowywać naukowcy i specjaliści z danej dziedziny
    (i oczywiście API/protokoły powinny być jawne).\r\n\r\n\"są też w powszechnym
    użyciu w innych aplikacjach (klient e-mail, komunikator)\"\r\n\r\nW powszechnym
    użyciu jest też SMTP, a wiadomo jakie są z nim problemy... ;)"
- id: 19501
  author: Chris Trynkiewicz
  author_url: http://blog.eldoras.com
  date: '2008-05-08 01:58:36 +0200'
  date_gmt: '2008-05-08 00:58:36 +0200'
  content: "Mi sie wydaje, ze glownym problemem, o ktorym sie nie mowi publicznie,
    a ktorego boi sie rzad, jest stworzenie serwera z kluczami publicznymi dla milionow
    polakow... Obciazenie - pierwszy problem. Drugi to bezpieczenstwo danych (a jak
    rzad NIE potrafi ochraniac danych dobrze wiadomo), trzeci to kwestia operowania
    na tak wielkiej bazie (tego ja sie boje - stworza jedna tabele, sekretarka niechcacy
    wpisze truncate...)... Dla informatykow to nie problem, ale rzad ma to do siebie,
    ze zatrudnia jako wykonawcow cieniasow.\r\nZ kolei tez Polska nie jest chyba do
    konca gotowa na taka rewolucje - panie za okienkami, ktore super widza bledy w
    pitach, nagle trzeba bedzie wyszkolic do obslugi komputera - a to dodatkowe koszty.\r\nPodsumowujac,
    nie wierze w szybkie zinformatyzowanie tego kraju :/"
- id: 19528
  author: Patrys
  author_url: http://room-303.com/
  date: '2008-05-08 20:01:13 +0200'
  date_gmt: '2008-05-08 19:01:13 +0200'
  content: "Chris:\r\n\r\nMój klucz publiczny jest powszechnie dostępny, nie trzeba
    go chronić. Do podpisania potrzebny jest klucz prywatny, którego nie zamierzam
    rządowi nigdy pokazywać (na tym polega cała idea PGP)."
- id: 19529
  author: Budyń
  author_url: ''
  date: '2008-05-08 21:17:58 +0200'
  date_gmt: '2008-05-08 20:17:58 +0200'
  content: "@Chris\r\n\r\nGdzie niby ta Pani ma wpisać 'truncate' ? To się na na poziomie
    MySQL/phpMyAdmin wyłączyć (nie wierzę, że tego nie wiesz), poza tym Pani nie będzie
    miała dostępu do RDBMSa, tylko do ładnego GUI do procedur składowanych i tyle...
    poza tym - wierz lub nie - ale administracja ma do dyspozycji naprawdę dobrych
    specjalistów; dość, by to co opisał Patrys wdrożyć. Tylko że fatalnie z nich korzysta,
    a poza tym w takim układzie nie zarobiłby żadnen Prokom - więc sprawa nie przejdzie.
    W Polsce to nie technika, ani nawet nie kapitał są barierami - tyklo mentalność
    i KULTURA ORGANIZACYJNA. I tak w Polsce jedną prostą korwetę buduje się tyle,
    co we Francji atomowy okręt podwodny, a w rok naprawia tyle torów kolejowych,
    ile Brytyjczycy wymieniają w weekend.\r\n\r\n@Patrys\r\n\r\nInformatyzacja to
    nie jest przenoszenie istniejącego bałaganu do komputerów, ew. tworzenie nowego...
    \ problem polega na tym, że w Polsce NIPów, PESELi (a jak masz działalność, to
    i REGONów) masz stanowczo za dużo. Wystarczyłby, po amerykańsku jeden identyfikator
    jawny (np. PESEL(2)) i jeden klucz, zapisany na JEDNYM dokumencie którym byłby
    dowód osobisty w postaci karty mikroprocesorowej. Zauważ, że poręczny kod kreskowy
    mógłby być indentyfikatorem jawnym - służącym tylko do wskazania lokalizacji /
    nazwy klucza w systemie. Takie narodowe OpenID..."
- id: 19530
  author: Patrys
  author_url: http://room-303.com/
  date: '2008-05-08 21:29:40 +0200'
  date_gmt: '2008-05-08 20:29:40 +0200'
  content: "Budyń:\r\n\r\nZ czym zostanie połączony klucz to jedna kwestia. Mi chodzi
    bardziej o to, że PGP nadaje się do składania podpisów, ma dużo szersze zastosowania
    niż kwalifikowane certyfikaty i przede wszystkim dużo prościej jest taki klucz
    unieważnić i wymienić."
- id: 19539
  author: Hoppke
  author_url: http://repo.dobremiasto.net/
  date: '2008-05-09 10:12:15 +0200'
  date_gmt: '2008-05-09 09:12:15 +0200'
  content: "A to prawda. PGP jako implementacja kluczy obywatelskich i mechanizm podpisu
    elektronicznego to bardzo dobry pomysł.\r\n\r\nI podzielam zdanie Budynia -- ograniczyć
    burdel robiąc jeden identyfikator -- mikrochipowy dowód osobisty, który jednocześnie
    byłby elektronicznym sygnetem, a przy okazji może nawet dałoby się jakoś e-voting
    na tym oprzeć i ustrzelić dwa ptaki jednym strzałem? (choć to już całkiem insza
    inszość)."
- id: 19540
  author: abec
  author_url: ''
  date: '2008-05-09 10:29:49 +0200'
  date_gmt: '2008-05-09 09:29:49 +0200'
  content: "Budyń napisał bardzo ważną rzecz. Staram się i staram - i nie rozumiem,
    \ po co mi jednocześnie PESEL i NIP. W kontakcie z urzędem skarbowym podaję jedno
    i drugie - po kiego ch...?\r\nRozumiem, że NIP to coś więcej, dotyczy też osób
    prawnych itd. Ale skoro mnie identyfikuje, to po co mi PESEL? Że PESEL dostaję
    przy urodzeniu, a NIP nie? Skoro są procedury nadawania PESELU przy urodzeniu,
    to nadawajmy w ten sam sposób NIP i tyle. Czepianie się do nazwy (Numer Identyfikacyjny
    Podatnika) puszczam mimo uszu."
- id: 19541
  author: abec
  author_url: ''
  date: '2008-05-09 10:33:09 +0200'
  date_gmt: '2008-05-09 09:33:09 +0200'
  content: "Hoppke - to nie jest insza inszość. \r\nJa bym wolał jednolitą identyfikację
    na potrzeby wszystkich uprawnionych urzędów i niech się ode mnie odczepią raz
    na zawsze. Raz, a dobrze rozwiązać kwestię identyfikacji elektronicznej osoby
    i dać nam spokój - czy to nie byłoby piękne?"
- id: 19616
  author: Fuzzy
  author_url: ''
  date: '2008-05-13 01:11:27 +0200'
  date_gmt: '2008-05-13 00:11:27 +0200'
  content: "Tylko NIP i PESEL... szczęśliwi z was ludzie, niektórzy mają jeszcze REGON
    :).\r\n\r\nNajbardziej mnie bawią te radosne druki z ZUSu (nota bene, nie można
    ich wydrukować samemu co uważam za totalny absurd), kiedyś wypełniłem wszystkie
    okienka i mnie odesłali, bo \"za dużo danych i niezgodnie z instrukcją\". Instrukcja
    jest taka: \"Wpisać NIP i REGON, a w razie gdy płatnikowi składek nie nadano tych
    numerów lub jednego z nich - numer PESEL; jeśli płatnikowi nie nadano również
    numeru PESEL - serię i numer dowodu osobistego albo paszportu. Tym samym numer
    PESEL, seria i numer dowodu osobistego albo paszportu powinny być podawane jedynie
    wówczas, gdy płatnik nie posiada identyfikatorów NIP i REGON lub jednego z nich\"...
    Po prostu piękne.\r\n\r\nA co do ustawy, to pewnie największy problem z propozycją
    Patrysa byłby w pogodzeniu jej z ustawą o ochoronie danych. Nie dotarłem wprawdzie
    do tego jak jest teraz, ale w/g pomyłu Patrysa wszyscy dostają przynajmniej interfejs
    do tłumaczenia klucz publiczny -&gt; imie i nazwisko + pewnie jeszcze jaką informacja,
    bo np. Janów Kowalskich to trochę jest. Pewnie lepszym rozwiązaniem byłoby api
    w stylu klucz + imie + nazwisko + pesel/nr. dowodu/cokolwiek -&gt; weryfikacja
    zgodności (tu dochodzi konieczność zmiany klucza przy zmianie innych danych).
    No bo na wprowadzenie jednego numeru na chipie w dowodzie liczyć w najbliższej
    przyszłości nie można."
- id: 21017
  author: kosa
  author_url: http://like-a-geek.jogger.pl
  date: '2008-08-13 17:49:00 +0200'
  date_gmt: '2008-08-13 16:49:00 +0200'
  content: "Popieram Chrisa: mimo, że pomysł jest fajny, to polski rząd nie byłby
    w stanie go sensownie wdrożyć. \r\n\r\nBTW Bardzo fajny blog:)"
- id: 24688
  author: Życzenia na nowy rok &laquo; Room 303
  author_url: http://room-303.com/blog/2009/12/31/zyczenia-na-nowy-rok/
  date: '2009-12-31 15:04:41 +0100'
  date_gmt: '2009-12-31 14:04:41 +0100'
  content: '[...] co nam imienny certyfikat przy składaniu podań? Przecież to sprzętowy
    odpowiednik podpisu potwierdzonego notarialnie [...]'
---
<p>Vagla zwraca uwagę na <a href="http://prawo.vagla.pl/node/7839">nieścisłości w przepisach</a> regulujących kwestię składania wniosków do urzędów drogą elektroniczną. Ja się za to zastanawiam, kto i ile wziął pieniędzy za te wszystkie wynalazki. Nie można było prościej?</p>

<h4>Wymagana infrastruktura</h4>

<ol>
<li>Jeden miejski (bądź centralny) urząd ewidencji ludności;</li>
<li>Jeden serwer kluczy PGP administrowany przez tenże urząd;</li>
<li>Jedna para kluczy (klucz publiczny i prywatny) PGP wygenerowana przez tenże urząd i fakt udostępnienia klucza publicznego na serwerze urzędu, zaś jego identyfikatora odcisku na stronie tegoż urzędu;</li>
<li>Jedna baza danych, która pozwala do każdego klucza publicznego przypisać jeden identyfikator PESEL;</li>
<li>Jedna pani w okienku</li>
</ol>

<h4>Rejestracja wzoru podpisu</h4>

<ol>
<li>Obywatel generuje parę kluczy PGP o okresie ważności nie dłuższym niż przewidziany ustawowo (powiedzmy, że będzie to kwartał);</li>
<li>Obywatel generuje zlecenie unieważnienia swojego klucza publicznego;</li>
<li>Obywatel drukuje zlecenie unieważnienia w formie przyswajalnej przez komputer, na przykład w postaci kodu kreskowego, co pozwoli skorzystać z niego w okienku (po okazaniu dowodu osobistego) w przypadku utracenia wyłącznej kontroli nad kluczem prywatnym;</li>
<li>Obywatel umieszcza swój klucz publiczny na serwerze kluczy dostarczonym przez urząd;</li>
<li>Obywatel drukuje identyfikator odcisku swojego klucza publicznego w formie przyswajalnej przez komputer (kod kreskowy) na wniosku o poświadczenie odcisku klucza;</li>
<li>Obywatel z wydrukowanym powyżej wnioskiem udaje się do urzędu, gdzie składa wniosek legitymując się dowodem osobistym;</li>
<li>Pani w okienku przykłada formularz do czytnika, jej komputer pobiera informacje o kluczu z serwera urzędu i pozwala na potwierdzenie imienia i nazwiska z formularzem i okazanym dokumentem tożsamości;</li>
<li>Serwer podpisuje wskazany klucz publiczny obywatela z poświadczeniem pełnego zaufania dla umieszczonych tam danych za pomocą klucza prywatnego urzędu, po czym publikuje go ponownie na serwerze urzędu;</li>
<li>Serwer umieszcza w swojej bazie danych informację o skojarzeniu danego klucza z numerem PESEL nadanym obywatelowi;</li>
</ol>

<h4>Złożenie podpisu pod dokumentem</h4>

<ol>
<li>Obywatel pobiera bądź tworzy dokument, który ma następnie zostać podpisany;</li>
<li>Obywatel podpisuje dokument za pomocą klucza prywatnego odpowiadającego kluczowi umieszczonemu i podpisanemu wcześniej na serwerze urzędu;</li>
<li>Obywatel dokument wraz z podpisem przesyła do urzędu;</li>
<li>Urząd przesyła obywatelowi poświadczenie w postaci złożonego wcześniej podpisu podpisanego ponownie kluczem prywatnym urzędu;</li>
</ol>

<h4>Unieważnienie wzoru podpisu</h4>

<p>Zawsze może zdarzyć się tak, że obywatel utraci swój klucz prywatny lub klucz ten wpadnie w ręce osób trzecich. Wersja pierwsza:</p>

<ol>
<li>Obywatel generuje zlecenie unieważnienia klucza publicznego za pomocą swojej kopii klucza prywatnego;</li>
<li>Obywatel importuje unieważnienie do swojego lokalnego pęku kluczy, tym samym unieważniając lokalną kopię swojego klucza publicznego;</li>
<li>Obywatel publikuje ponownie swój klucz publiczny na serwerze urzędu, tym samym unieważniając swój wzór podpisu;</li>
<li>Ponowne złożenie podpisu wymaga ponownego przejścia przez procedurę rejestracji wzoru podpisu;</li>
</ol>

<p>Wersja druga:</p>

<ol>
<li>Ponieważ obywatel utracił swoją kopię klucza prywatnego (na przykład w wyniku kradzieży), udaje się do urzędu z wydrukowanym wcześniej unieważnieniem klucza;</li>
<li>Pani w okienku przeciąga unieważnienie przez czytnik;</li>
<li>Serwer importuje unieważnienie, a następnie ponownie publikuje unieważniony już klucz na serwerze kluczy;</li>
<li>Pani mówi <q>dziękuję, następny;</q></li>
<li>Ponowne złożenie podpisu wymaga ponownego przejścia przez procedurę rejestracji wzoru podpisu;</li>
</ol>

<p>Wersja trzecia:</p>

<ol>
<li>Ponieważ obywatel utracił swoją kopię klucza prywatnego i zgubił wydrukowane wcześniej zlecenie unieważnienia, wypełnia formularz unieważnienia na papierze, podając powód i swoje dane osobowe i udaje się z nim do urzędu;</li>
<li>Pani w okienku sprawdza zgodność danych na wniosku, dokumencie tożsamości i w bazie danych;</li>
<li>Serwer unieważnia swój wcześniejszy podpis zaufania pod kluczami publicznymi skojarzonymi z numerem PESEL obywatela, a następnie publikuje je ponownie, tym samym wyłączając je z użytku jako podpis akceptowany przez urzędy;</li>
<li>Ponowne złożenie podpisu wymaga ponownego przejścia przez procedurę rejestracji wzoru podpisu;</li>
</ol>

<p>Wersja czwarta:</p>

<ol>
<li>Wygasa data ważności klucza obywatela;</li>
<li>Ponowne złożenie podpisu wymaga ponownego przejścia przez procedurę rejestracji wzoru podpisu;</li>
</ol>

<h4>Zmiana klucza prywatnego urzędu</h4>

<p>Para kluczy urzędu ze względów bezpieczeństwa również powinna mieć ograniczony czas ważności. Może się również zdarzyć, że klucz prywatny urzędu dostanie się w niepowołane ręce:</p>

<ol>
<li>Urząd generuje nową parę kluczy GPG;</li>
<li>Nowy klucz publiczny urzędu zostaje opublikowany na serwerze kluczy;</li>
<li>Identyfikator odcisku klucza publicznego zostaje opublikowany na stronie urzędu;</li>
<li>Serwer podpisuje dotychczas podpisane klucze publiczne obywateli za pomocą nowego klucza prywatnego urzędu, udzielając im pełnego zaufania;</li>
<li>Serwer unieważnia dotychczas używany klucz publiczny urzędu za pomocą jego klucza prywatnego, jako powód podając zastąpienie go nowym kluczem;</li>
</ol>

<h4>Różnice w stosunku do stanu obecnego</h4>

<ol>
<li>Koszty utrzymania infrastruktury są praktycznie zerowe;</li>
<li>Fizyczny koszt uzyskania wzoru podpisu przez obywatela jest zerowy;</li>
<li>Nakład urzędu w celu przyjęcia bądź unieważnienia wzoru podpisu jest minimalny;</li>
<li>Forma ta nie faworyzuje żadnych podmiotów gospodarczych;</li>
<li>Całość działa również poza platformą Windows;</li>
<li>Stosowne aplikacje klienckie można przygotować w ciągu jednego wieczoru, w dowolnym języku programowania i nie wymaga to milionowych przetargów;</li>
<li>Wiele innych serwisów (nie tylko państwowych) może użyć kluczy podpisanych urzędowo choćby w celu weryfikacji rejestrujących się użytkowników (serwis nie dostaje żadnych informacji o obywatelu poza jego imieniem i nazwiskiem, ale zaufanie urzędu gwarantuje, że organy ścigania są w stanie &mdash; na podstawie odcisku klucza &mdash; ustalić tożsamość podejrzanego);</li>
<li><strong>Update:</strong> Pozwala podpisać ten sam dokument dowolnej liczbie osób;</li>
</ol>
