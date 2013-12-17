---
layout: post
status: publish
published: true
title: Global GPRS, Global UMTS
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 442
wordpress_url: http://room-303.com/blog/?p=442
date: 2008-04-15 14:28:17.000000000 +02:00
categories:
- linux
- software
tags: []
comments:
- id: 19155
  author: jpc
  author_url: http://jpc.jogger.pl
  date: '2008-04-15 19:01:44 +0200'
  date_gmt: '2008-04-15 18:01:44 +0200'
  content: Rozprawadzania loginów bym się nie czepiał, bo to akurat byłoby bardzo
    wygodne. (no chyba, ze autor sam wszedł w ich posiadanie w sposób leniwy i tylko
    sprzedaje czyjąś robotę) Oczywiście lepiej na GPLu, ale jak się nie ma co się
    lubi...
- id: 19156
  author: Użytkownik_Globala
  author_url: ''
  date: '2008-04-15 19:57:58 +0200'
  date_gmt: '2008-04-15 18:57:58 +0200'
  content: "Patryku zamiast opluwać ludzi, którzy tworzą przydatne ludziom programy,
    mógłbyś się chwilę zastanowić zanim napiszesz taki ostry tekst.\r\n\r\nUżywałeś
    kiedyś programy Global GPRS i Global UMTS ? Ja miałem okazję używać ich na kilku
    dystrybucjach. Na OpenSuse wyskoczyło mi kiedyś okienko, że program nie obsługuje
    tej dystrybucji wraz z kilkoma sensownymi poradami co można spróbować zrobić (nie
    pamiętam w tej chwili co tam było). Najprawdopodobniej dlatego program stara się
    ustalić czy jest uruchomiony na OpenSuse, aby wyświetlić jakiś sensowny komunikat.\r\n\r\nGdybyś
    przed napisaniem tego tekstu przyjrzał się choć trochę programowi i uruchomił
    zapis wybranej konfiguracji GPRS w programie, to byś zauważył, że kdesu i gksu
    służą do wyświetlenia okienka z pytaniem o hasło do wykonania komendy cp (kopiowania
    skryptów) To jest bardzo eleganckie rozwiązanie, bo użytkownik wie do czego są
    używane uprawnienia roota i że program nic nie zmienia w systemie bez jego zgody.
    Ma wyraźnie napisaną na ekranie komendę cp z listą kopiowanych ustawień gprs na
    którą wyraża zgodę. Program nie wymaga uruchomienia z uprawnianiami root-a i tylko
    prosi o zgodę na skopiowanie jako root skrytpów komunikacyjnych do  /etc/pppd/peers/
    \ To jest rzadko spotykane w programach do gprs dla Linuksa, większość z nich
    działa jako root\r\n\r\nA widziałeś to okno z prośbą o zgodę na kopiowanie wybranej
    przez użytkownika konfiguracji do /etc/pppd/peers/? Nie? To po cholerę zabierasz
    się za ocenianie programu, jak nie oglądałeś w nim nawet najważnieszego okna z
    konfiguracją gprs i modemu. \r\n\r\nDane konfiguracji gprs są dostępne na stronach
    operatorów, a loginy i hasła, operatorzy mają puste (lub: anyuser anypassword),
    więc o czym ty mówisz? Każdy może się tym posługiwać zwłaszcza, że nie ma tam
    normalnych haseł :)\r\n\r\nMoże sam byś poświęcił kilkaset godzin darmowej pracy
    na rozwijanie przydatnego ludziom programu zamiast opluwać ludzi, którzy chcą
    coś zrobić pożytecznego dla innych (Global GPRS był przez 4 miesiące rozdawany
    całkiem za darmo. Global UMTS można używać za darmo, ale wtedy czeka się 6 min
    na uruchomienie, więc pewnie niektórzy płacą drobne datki na rozwój projektu)\r\n\r\nTaki
    ostry tekst na temat przydatnego programu tylko dlatego, że wydaje się tobie,
    że  \"autor jest słabym programistą\" ?\r\n\r\nWeź sobie pół roku urlopu, popracuj
    za darmo i podaruj użytkownikom Linuksa lepszy program do GPRS\r\n\r\nZ powodu
    jakiejś osoby która wyraziła (jak podejrzewam) pozytywną opinię o programie, zaczynasz
    wyżywać się na autorze programu? Odbiło Ci? \r\n\r\nParę miesięcy temu miałem
    okazję wymienić kilka listów z autorem. Narzekał na nawał pracy, ogromne ilości
    listów od fanów, a mimo to ciągle rozwijał ten program. Należą mu się tylko GRATULACJE
    !\r\n\r\nA ty Partyku jak ochłoniesz, to lepiej skoryguj ten tekst na mniej oskarżycielski
    i weź się do testowania tego programu w wirtualnej maszynie i potem napisz profesjonalną
    recenzję."
- id: 19157
  author: Patrys
  author_url: http://room-303.com/
  date: '2008-04-15 20:39:38 +0200'
  date_gmt: '2008-04-15 19:39:38 +0200'
  content: "Drogi \"użytkowniku, który boi się podpisać, bo jest tym samym spamerem,
    o którym mowa we wstępie i pewnie jednocześnie autorem programu:\"\r\n\r\nTo jest
    mój blog, mogę tu wyrażać takie opinie, jakie mi się podoba. Jeśli uważam, że
    program jest podejrzanego pochodzenia, to mogę tak napisać. Nie mam obowiązku
    go uruchamiać i recenzować. Zwłaszcza, jeśli strings mówi mi dostatecznie dużo
    o jakości kodu. Jeśli zapłacisz za mój czas i dostarczysz mi pełne źródła, wtedy
    możemy rozmawiać o recenzji, ale obawiam się, że nie będzie specjalnie pochlebna.\r\n\r\nOczywiście,
    że nie widziałem żadnego okna, bo <strong>uruchamianie programów, których źródła
    się nie zna jest cholernie niebezpieczne</strong>.\r\n\r\nDo zestawiania konfiguracji
    GPRS służy z powodzeniem pakiet NetworkManager w aktualnej wersji rozwojowej,
    nie trzeba za niego nikomu płacić, czekać X minut, ani uruchamiać wątpliwej jakości
    programów. Tak, wątpliwej jakości, skoro \"radzi sobie\" przez szukanie urządzeń
    via grep i nadpisywanie konfiguracji, którą można zmienić w locie (skoro program
    musi działać przez cały czas połączenia, to po co miałby cokolwiek gdzieś kopiować?)."
- id: 19158
  author: Użytkownik_Globala
  author_url: ''
  date: '2008-04-15 20:39:52 +0200'
  date_gmt: '2008-04-15 19:39:52 +0200'
  content: "Jak będziesz pisał porządną recenzję tych programów, to zwróć uwagę, że
    oba w numerze wersji mają beta 1\r\nWiesz co to znaczy? To bardzo wstępna wersja
    programu, więc pewnie część rzeczy jest robiona prowizorycznie, byleby tylko móc
    go udostępnić użytkownikom do pierwszych testów. \r\n\r\nMnie zdziwiło to, że
    jak na betę działa on bardzo stabilnie i ani razu się zawiesił."
- id: 19159
  author: Użytkownik_Globala
  author_url: ''
  date: '2008-04-15 23:20:36 +0200'
  date_gmt: '2008-04-15 22:20:36 +0200'
  content: "Patryku napisałeś:\r\n \"Tak, wątpliwej jakości, skoro \"radzi sobie\"
    przez szukanie urządzeń via grep i nadpisywanie konfiguracji, którą można zmienić
    w locie (skoro program musi działać przez cały czas połączenia, to po co miałby
    cokolwiek gdzieś kopiować?).\"\r\n\r\nWiększych bzdur dawno nie czytałem. Bawisz
    się w jasnowidza oglądając program z zewnątrz i nie uruchamiając go. Program nie
    szuka urządzeń przez dmesg i grep  tylko zwala to na barki użytkowników wyświetlając
    ludziom okienko zawierające logi wyświetlone przez dmesg i grep (uruchamiane przyciskiem
    Port Podpowiedź) aby użytkownicy w razie wątpliwości sami poszukali sobie właściwy
    port komunikacyjny. W końcu to wczesna wersja testowa  beta 1, więc nie można
    mieć pretensji do Dariusza, że nie dodał jeszcze do programu automatycznego szukania
    portów ani innych bajerów. Ale na szczęście podpowiada jakich oznaczeń portów
    szukać. W pracy mam kartę Option PCMCIA , która dostaje nietypowy port /dev/noz0
    Gdyby nie to okno z podpowiedzią wyświetlające dmesg nigdy bym tego nie odnalazł.
    \ Dmesg i grep to chyba największa bzdura, którą tu napisałeś. Tak to jest jak
    się nigdy nie uruchomiło programu, a zaczyna się go opisywać.\r\n\r\nWszystkie
    poradniki o gprs w internecie mówią o kopiowaniu konfiguracji gprs do /etc/pppd/peers
    bo tam jest jej miejsce. Wszyscy ludzie i program robią to samo, ale ty masz wyjątkowe
    wymagania, życzysz sobie by robił to inaczej! Wygląda na to, że nie masz najmniejszego
    pojęcia o czym piszesz. Widziałeś kiedyś poradnik dla początkujących o konfiguracji
    gprs? Czy miałeś kiedykolwiek w ręku modem PCMCIA lub telefon komórkowy z gprs?\r\n\r\nNapisałeś,
    że program musi działać cały czas podczas połączenia. Kolejna bzdura. O tym, że
    można go wyłączyć informuje w okienku podczas nawiązywania połaczenia (co oczywiście
    nie raczyłeś obejrzeć)\r\n\r\nWidać, że lubisz tylko open source, a ja nie wymagam
    od Dariusza by dawał mi kod źródłowy na licencji GPL i pełne prawa do dystrybucji
    programu. Wybór licencji to jego wola. Pracuje najprawdopodobniej sam, więc licencja
    GPL pomagająca dzielić się kodem nie jest mu do niczego potrzebna.\r\n\r\npozdrawiam,\r\nMirek
    Krycz"
- id: 19162
  author: Użytkownik_Globala
  author_url: ''
  date: '2008-04-16 00:05:28 +0200'
  date_gmt: '2008-04-15 23:05:28 +0200'
  content: "Oczywiście powinno być /etc/ppp/peers/ a nie pppd :)\r\n\r\npozdrawiam,\r\nMirek
    Krycz"
- id: 19164
  author: Filip
  author_url: ''
  date: '2008-04-16 02:15:46 +0200'
  date_gmt: '2008-04-16 01:15:46 +0200'
  content: "Zaciekawiony programem postanowiłem go wypróbować\r\n\r\nJak na wersję
    beta 1 wszystko działa bez problemów. Łatwo połączyłem się przez swoją komórkę
    Program nie wymaga podawania tylu danych co Network Manager - wybrałem tylko model
    komórki, port i operatora, nic więcej nie trzeba znać.  Część okienek jak statystyki
    nie jest jeszcze w pełni zrobiona ale program o tym informuje\r\n\r\nOgólnie przydatna
    rzecz\r\n\r\nTekst artykułu w blogu prezentuje tylko dziwny stan emocjonalny autora
    bloga a nie rzeczywiste wady programu\r\n\r\nDyskusje o wyższości FLOSS nad innymi
    licencjami nie uprawniają do tak agresywnej krytyki pożytecznego programu"
- id: 19172
  author: Krzyś
  author_url: ''
  date: '2008-04-16 17:37:54 +0200'
  date_gmt: '2008-04-16 16:37:54 +0200'
  content: Autor bezsensownie pluje jadem na lewo i prawo, posługując się wątpliwej
    jakości argumentami. Pogrepował stringsami przez ldd binarkę, coś mniej lub bardziej
    konkretnego znalazł, i zachowuje się jakby programista zgwałcił mu siostrę. Trochę
    umiaru.
- id: 19173
  author: Fuzzy
  author_url: ''
  date: '2008-04-16 17:40:16 +0200'
  date_gmt: '2008-04-16 16:40:16 +0200'
  content: "Patrys, czy ty przypadkiem nie pisałeś, że grywasz na playstation? Masz
    źródła tych gier? Uprzedzam odpowiedź, że tam nie można nic popsuć: można pewnie
    wykasować wszystko z karty pamięci/dysku (nie wiem co teraz w tych konsolach montują).\r\nGeneralnie
    uważam wymaganie źródeł do uruchomienia programu za poważne zboczenie :). Uspokojony
    samą ich obecnością pewnie i tak byś do nich nie zajrzał lub pooglądał jedynie
    po łebkach (czasem niesłusznie zakładając, że \"jakby tam było coś nie tak, to
    ktoś by o tym ostrzegł\") i program i tak mógłby ci zrobić mielonkę z systemu.
    No bo np. czy przeglądałeś dokładnie źródła FF, którego (pewnie) używasz? Może
    jakiś nowy plugin do niego wysłał już twoje hasła do spamerów?"
- id: 19174
  author: Patrys
  author_url: http://room-303.com/
  date: '2008-04-16 17:58:00 +0200'
  date_gmt: '2008-04-16 16:58:00 +0200'
  content: "Fuzzy:\r\n\r\nNie wkładam czegokolwiek do napędu, nie uruchamiam nieznanych
    programów i nie toleruję spamu. Zwłaszcza bezczelnego wklejania tej samej reklamy
    pod każdą notką na każdym blogu, gdzie tylko pojawiło się słowo sieć i GNOME (zanim
    napisałem powyższą notkę, kilka osób skarżyło się na dokładnie ten sam spam, jaki
    ja dostałem pod czterema notkami na dwóch blogach, po fakcie poskarżyło się jeszcze
    kilka). Miałem więc pełne prawo podejrzewać, że jest to kolejny trojan/worm i
    tylko dlatego zacząłem w nim dłubać.\r\n\r\nOdpowiadając na resztę twoich wątpliwości:
    czytam masę źródeł programów (bo jestem między innymi programistą i packagerem
    dla PLD). Gram na konsoli, ale nie wkładam do niej \"czegokolwiek.\" Nawet, gdybym
    wkładał, to ze spokojem, bo oprogramowanie uruchamiane jest w zwirtualizowanym
    środowisku i do pisania po dysku poza swoimi plikami wymaga każdorazowej zgody
    użytkownika. Nie bez powodu też Firefox (który skraca się do Fx, a nie FF) nie
    pozwala na instalację wtyczek z nieznanych domen, a Outlook blokuje uruchamianie
    załączników z poczty.\r\n\r\nNiestety, większość ludzi ma takie podejście do bezpieczeństwa,
    jak ludzie powyżej. Im właśnie zawdzięczamy tony spamu, które przewalają się między
    serwerami poczty. Uprzedzając wątpliwości: spamu nie wysyła pan Roman ze swojego
    schronu w Prypeciu, spam wysyłają botnety zbudowane z milionów komputerów zwykłych
    użytkowników, którzy uruchamiają każdy napotkany program."
- id: 19175
  author: Krymzon
  author_url: ''
  date: '2008-04-16 18:56:07 +0200'
  date_gmt: '2008-04-16 17:56:07 +0200'
  content: "Patrys, przyznaj się, czy ten wpis to prowokacja, żeby zwabić rzekomych
    'zachwyconych użytkowników'?\r\n\r\nW grudniu, gdy obsługujący takie modemy NetworkManager
    był mocno rozwojowy, uruchomiłem ten program z dala od cywilizacji, by umożliwić
    tacie dostęp do netu pod Linuksem. Prawie natychmiast jednak, w obawie o bezpieczeństwo,
    postanowiłem pokonfigurować wszystko ręcznie. Tak też zrobiłem i tata jest chyba
    zadowolony z dwóch launcherów na panelu wywołujących pppd. Możliwe, że autor ma
    dobre intencje, ale przejawia je dość nietypowo, angażując się głównie w bezpośrednią
    promocję swojego tworu...\r\n\r\nAle swoją drogą Ty też nie wszystko na GPLu udostępniasz
    (choć dużo i coraz więcej, co bardzo miłe jest)"
- id: 19176
  author: Patrys
  author_url: http://room-303.com/
  date: '2008-04-16 19:07:36 +0200'
  date_gmt: '2008-04-16 18:07:36 +0200'
  content: "Krymzon:\r\n\r\nA czego nie udostępniam, chciałbyś zobaczyć i jest moje
    (czytaj: nie jest własnością któregoś z pracodawców)?"
- id: 19177
  author: Fuzzy
  author_url: ''
  date: '2008-04-16 19:18:50 +0200'
  date_gmt: '2008-04-16 18:18:50 +0200'
  content: "Patrys:\r\n\r\n\"Gram na konsoli, ale nie wkładam do niej “czegokolwiek.”
    Nawet, gdybym wkładał, to ze spokojem, bo oprogramowanie uruchamiane jest w zwirtualizowanym
    środowisku i do pisania po dysku poza swoimi plikami wymaga każdorazowej zgody
    użytkownika.\" - tzn ufasz twórcom gier/konsol, czy widziałeś źródła OS'a z PS
    i *wiesz* że nie ma tam jakiegoś buffer overflow i możliwości ominięcia tej zgody?
    Dlaczego ufasz Sony (po aferze z rootkitami na dyskach audio :)) a nie np. Microsoftowi?\r\n\r\n\"czytam
    masę źródeł programów (bo jestem między innymi programistą i packagerem dla PLD)\"
    - tak, wiem, czytam twój blog od czasów SynaPrezesa(tm). Ale zadałem bardzo konkretne
    pytanie, czy przejrzałeś źródła Fx (niech będzie ten skrót :))?\r\n\r\nAle dość
    czepiania się szczegółów... Czasem trzeba komuś zaufać :). Choćbyś je miał, to
    nie wszystkie źródła przejrzysz. Ja np. używam opery mini do logowania się na
    stronę banku i wiem, że takie połączenie jest niebezpieczne i opera.com widzi
    moje hasła i stany kont... no coż, ufam im. :)\r\n\r\nCałą tę żółć wylewasz moim
    zdaniem tylko przez ten spam. Jakby nie to to nawet jakbyś program dostał od kolegi,
    najwyżej stwierdziłbyś \"po co mi to, mam pliki konfiguracyjne\" i na tym by się
    skończyło."
- id: 19178
  author: Patrys
  author_url: http://room-303.com/
  date: '2008-04-16 19:49:06 +0200'
  date_gmt: '2008-04-16 18:49:06 +0200'
  content: "Fuzzy:\r\n\r\nUfam Sony tak samo jak Microsoftowi. Płacę i wymagam, w
    razie czego mam podstawy do roszczeń na drodze prawnej. Odnośnie tego, czy wiem,
    że wirtualizator nie ma dziur - wiem, bo śledzę rozwój linuksowych sterowników
    dla procesora RSX, wszystkie dziury, jakie udało się znaleźć zostały w ciągu dni
    załatane przez Sony. W tej chwili jedyna metoda uruchomienia czegokolwiek poza
    certyfikowanym oprogramowaniem, to zmuszenie konsoli do pobrania aktualizacji
    przez lokalne proxy, które podrzuci spreparowany plik. Przy czym, podmienić można
    dane, konsola i tak nie pozwoli na uruchomienie kodu.\r\n\r\nGdyby autor miał
    głowę na karku, to promowałby się przez GnomeFiles i kontakty ze środowiskiem
    okołouniksowym/okołognomowym, a nie przez spam na blogach ludzi, którzy i tak
    podobnych programów nie potrzebują."
- id: 19179
  author: Krymzon
  author_url: ''
  date: '2008-04-16 19:50:49 +0200'
  date_gmt: '2008-04-16 18:50:49 +0200'
  content: "Patrys:\r\n\r\nRacja, chyba faktycznie to co nie jest własnością pracodawców
    już udostępniłeś, zwracam honor :)"
- id: 19180
  author: VDR
  author_url: ''
  date: '2008-04-16 20:19:33 +0200'
  date_gmt: '2008-04-16 19:19:33 +0200'
  content: "Czytuje tego bloga regularnie, ale ten wpis to strzal w stope, choc moze
    nawet i w kolano... \r\nAlbo piszesz o spamie albo piszesz o programie... Jak
    o tym drugim to lekcje nalezy odrobic dokladnie a nie po lebkach ;] Jako programista
    chyba powinienes znalezc sposob aby nie wrozyc z fusow, ooo wroc, ze strings a
    sprawdzic dokladnie program i napisac normalna recenzje ??\r\nW zasadzie esencja
    tego co chciales przekazac jest dopiero w komenatarzach.  \r\n\r\nPoprzednie wpisy
    zobowiazuja, popraw sie ;] ;] ;] \r\n\r\nP.s nie uzywam tych progsow -- NM mi
    wystarcza - to tak jakbys stwierdzil, ze mam zwiazki z autorem badz jestem fanem
    tych progsow. Nie jestem."
- id: 19182
  author: Dariusz
  author_url: ''
  date: '2008-04-16 23:14:30 +0200'
  date_gmt: '2008-04-16 22:14:30 +0200'
  content: "Witam\r\nJestem autorem programu Global GPRS.\r\n\r\nPodesłano mi link
    do tej awantury.\r\nWspominano tu o jakiś niewłaściwych postach informujących
    o programie.\r\n\r\nJa osobiście nie mam potrzeby reklamować programu, bo istnieje
    on już od pół roku i napisano o nim wiele artykułów w najważniejszych polskich
    portalach jak www.dobreprogramy.pl   www.linuxnews.pl  czy  www.jakilinux.org
    \ W sumie kilkadziesiąt stron poświęconych Linuksowi publikujących regularnie
    newsy\r\ntworzy co parę miesięcy informacje o Global GPRS. Pod artykułami toczy
    się dyskusja o potrzebie istnienia takich wygodnych graficznych konfiguratorów
    GPRSu i niedostatkach obecnie istniejących programów. To wszystko jest do sprawdzenia
    w google - wpiszcie \"global gprs\". \r\nŚmieszne jest podejrzewanie, że ja sam
    osobiście mam potrzebę angażować się w pisanie jakiś postów z linkami do programu.
    Przecież co kilka godzin na forach linuxowych przybywa kolejny link do Global
    GPRS, bo użytkownicy sami radzą innym wypróbowanie jego w razie problemów z nietypowym
    modemem UMTS. Co 2 tygodnie kolejne blogi tworzą artykuły opisujące mój program.
    Czy śpię, czy opalam się na słońcu, linki i artykuły tworzą się same!\r\n\r\nWiele
    razy obserwowałem jak zadowolony użytkownik Global GPRS lub Global UMTS (który
    spędził wcześniej wiele miesięcy na skomplikowanych próbach konfiguracji modemu),
    nagle zaczyna udzielać się na stronach opisujących problemy z innym modemem informując,
    że takie urządzenie widział na liście obsługiwanego sprzętu w Global GPRS / UMTS.
    Podobnie może być z blogiem, co mogło kogoś zirytować. \r\n\r\nNie mogę brać odpowiedzialności
    za fanów programu. Trzeba się przyzwyczaić do postów o Global GPRS i Global UMTS,
    tak samo jak teraz akceptujemy teksty o innych programach: Firefoxie, Amaroku,
    K3B, Network Managerze. Takich postów na blogach będzie coraz więcej, bo mój program,
    choć jest niewielki, stał się jednym z często używanych programów dla Linuksa.
    Trudno wyrzucać posty o Network Managerze, czy zamkniętych sterownikach ATI i
    Nvidii. Czy tego chcemy czy nie, czas zaakceptować istnienie w świadomości użytkowników
    popularnego programu do modemów.\r\n\r\nChciałbym się odnieść do tematu opisującego
    mój program na tym blogu. Szanuję prawa autora blogu do jego swobodnej wypowiedzi.
    Ale z uwagi na to, że doszło tutaj do nieporozumienia, a dyskusja o spamie zepsuła
    opinię niewinnego programu. (na szczęście wszystkie wątpliwości zostały już wyjaśnione).
    Czy nie można by usunąć tego wprowadzającego czytelników w błąd tematu i stworzyć
    dwa osobne tematy o spamie i drugi o zaletach i wadach otwartego i zamkniętego
    oprogramowania? \r\n\r\nTylko proszę nie wspominać tam mojego programu! Chłopców
    do bicia znajdziemy gdzie indziej: zamknięte sterowniki w kernelu, Sony które
    popisało się podejrzanie działającym programem, czy różne dziwne pluginy do Firefoxa.
    Pluginom łatwo wyrządzić szkodę użytkownikowi, bo są częścią przegladarki normalnie
    łączącej się z internetem. Opera ma też zamknięty kod. Dlatego proszę - ani słowa
    o moim programie. On nawet nie łączy się z internetem, bo przecież robi to za
    niego systemowy pppd. Program tylko ułatwia użytkownikom zmianę operatorów komórkowych,
    komend modemów itp. To tylko kilkanaście różnych wyrazów wpisywanych do plików
    tekstowych w /etc/ppp/.  W działaniu przypomina program do zmiany ustawień tapety
    na pulpicie. Po co więc mieszać go z jakimiś zagrożeniami? Jak się nie ma dowodów,
    to trzeba milczeć!\r\n\r\nOd pół roku (pracując za darmo) mozolnie buduję bazę
    zadowolonych użytkowników Global GPRS, a tu nagle ktoś takim dziwnym komentarzem
    (jak się potem okazało bezpodstawnym) zaczyna psuć jego opinię. Od razu odechciewa
    się tworzyć darmowe, pomagające ludziom programy w środowisku pełnym (przepraszam
    za to określenie) fanatyków otwartego oprogramowania, wietrzących wszędzie różne
    spiski. Przypominam, że ponad 90% oprogramowania na świecie nie ma otwartego kodu.
    Autorzy mają prawo wybierać licencję inną niż GPL. \r\n\r\nWiem, że o wiele proszę.
    Usunięcie tematu z ulubionego bloga autora nie przychodzi łatwo. Ale mam nadzieję,
    że autor w życiu kieruje się etyką, poczuciem przyzwoitości i nie odpisze z arogancją
    \"To mój teren więc przywoitość tu nie obowiązuje\" \r\n\r\nW życiu zdarzają się
    nieporozumienia i dziwne sytuacje, ale to sami użytkownicy internetu i autorzy
    blogów mają wpływ na to, czy internet będzie nazywany szambem czy też blogi będą
    zawierały prawdziwe informacje.\r\n\r\nTych czytelników i znajomych autora, którzy
    nie zgadzają się na przeprowadzaną przez niego egzekucję pożytecznego projektu
    (przez bezpodstawne psucie mu opinii), proszę o przekonanie go do usunięcia tego
    bezsensownego tematu."
- id: 19189
  author: Hoppke
  author_url: http://repo.dobremiasto.net/
  date: '2008-04-17 11:36:55 +0200'
  date_gmt: '2008-04-17 10:36:55 +0200'
  content: "Patrys, piszesz, że uruchamianie nieznanych binarek jest niebezpieczne.
    Owszem.\r\n\r\nAle przecież nie jesteś ZU, wiesz jak postawić szybko jakiegoś
    jaila, uruchomić livecd w maszynie wirtualnej czy zestawić jakąkolwiek inną piaskownicę.\r\n\r\nZamiast
    tego ograniczyłeś się do \"analizy\" przez przegrepowanie binarki i na takich
    podstawach zacząłeś siać FUD-y, łącznie z podważaniem prawdziwości imienia i nazwiska
    autora softu.\r\n\r\nTak się nie robi.\r\n\r\nTym bardziej, że z łatwością byłbyś
    w stanie przeprowadzić naprawdę rzetelną analizę, łącznie z jakimś (s|l)tracem
    binarki w bezpiecznym środowisku, ba, mogłeś nawet łatwo sprawdzić co się dzieje
    gdy odpalisz program na OpenSuSE. Wirtualizacja pod Linuksem jest obecnie dziecinnie
    prosta. Ale chyba z góry założyłeś, że autor to \"słaby programista\", a Ty masz
    o wiele wyższe kompetencje, więc nie ma co angażować się w rzeczową analizę programu
    skoro można od razu zacząć smażyć zjadliwą antyreklamę na blogu.\r\n\r\nTak się
    nie robi, to nieprofesjonalne.\r\n\r\nPS: A gdyby stringi poleceń do wykonania
    zaszyte w kodzie były choćby zrot13-owane i przez to niewykrywalne prymitywnym
    searchem, to ten wpis by pewnie nie powstał, prawda?"
- id: 19193
  author: Bold
  author_url: ''
  date: '2008-04-17 22:35:11 +0200'
  date_gmt: '2008-04-17 21:35:11 +0200'
  content: "Uśmiałem się czytając twój artykuł z łatwą przecież do wykonania analizą
    poprzez string. Ośmiesza cię on w oczach czytelników.  Cytat:\r\n\"Nie dotykać,
    pomacać przez ldd i strings. Ten drugi pokazuje, że program szuka gksu albo kdesu.
    Po co? Pokazuje też, że autor jest słabym programistą i szuka urządzeń przez dmesg
    | grep \"\r\n\r\nZademonstruję jak wiele można wyczytać bez uruchomienia programu
    dzięki prostemu uruchomieniu string: Zajmę się najpierw twoim dziwnym pytaniem
    po co programowi gksu i kdesu. Po uruchomieniu string bardzo łatwo jest tam znaleźć
    taki tekst:\r\n\r\n\" Nie masz zainstalowanego programu gksu lub kdesu.\r\n  Dlatego
    nie można automatycznie skopiować plików\r\n  Zainstaluj jeden z tych programów
    lub skopiuj pliki \r\n  ręcznie np. w ten sposób\r\n  W Konsoli (Terminalu) uruchom
    komendę su \r\n  aby otrzyma prawa administratora i potem napisz:\r\n  cp\r\n\"\r\n\r\nNawet
    bez uruchamiania programu można uzyskać odpowiedź do czego programowi potrzebne
    jest  gksu i kdesu\r\nPrzecież sam o tym informuje użytkownika! Jak udało się
    tobie  przeoczyć taką oczywistą rzecz? A jakbyś choć raz uruchomił program, to
    byś ujrzał okno kdesu pytające o zgodę na kopiowanie ustawień przy pomocy cp.
    \r\n\r\nW następnym zdaniu sugerujesz, że autor jest słabym programistą, bo rzekomo
    szuka urządzeń przez   dmesg | grep\r\nString pokazuje, że tylko w jednym miejscu
    programu występuje  dmesg | grep\r\n\r\n dmesg | grep USB  --after-context=10
    \ --after-context=6   &gt;&gt; /tmp/t6053129742-1\r\n dmesg | grep ACM  --after-context=10
    \ --before-context=6  &gt;&gt; /tmp/t6053129742-1\r\n\r\nŁatwe do zrozumienia
    parametry  --after-context=10  --after-context=6   służą do wyświetlania w sumie
    16 linii znajdujących się wokół wystąpienia słowa USB. Od razu widać, że to nie
    jest szukanie urządzenia aby go użyć, ale generowanie logów, które opisują sposób
    rozpoznania tego urządzenia przez kernel. Jak można było tego nie zrozumieć?  Komunikaty
    występujące przed i po wystąpieniu słowa USB informują czytającego te logi czy
    sprzęt został poprawnie rozpoznany. Logi są zapisywane do pliku  /tmp/t6053129742-1
    \ Każdy student pierwszego roku informatyki rozumie te zapisy.  Jak udało się
    tobie  zaliczyć zajęcia z informatyki?\r\n\r\nNawet nie uruchamiając programu
    można znaleźć dzięki string  czemu program sprawdza, czy jest uruchomiony na Suse,
    bo zaraz po instrukcji sprawdzającej czy to Suse (która jest tuż obok, bez żadnego
    odstępu!) jest tekst:\r\n\r\n\"Program nie działa na Suse. Spróbuj innej dystrybucji.
    Pełna lista jest w dołączonym do programu pliku README.TXT\"\r\n\r\nTwoja rada
    aby program nie sprawdzał na jakiej dystrybucji działa jest idiotyczna. Widać,
    że nie masz większego pojęcia o pisaniu programów dla Linuksa. Wiele dystrybucji,
    w tym Suse mocno różni się od pozostałych i program musi je rozpoznać aby działać
    na nich w inny sposób.\r\n\r\nWięcej głupot nie chce mi się komentować. Idz sobie
    do jakiejś szkoły.\r\n\r\nZabieranie się za wyszukiwanie błędów w wersji beta
    1 cudzego programu świadczy o jakiś kompleksach. Przecież wiadomo, że wersja beta
    1 jest wczesną wersją testową, a nie finalną i zawiera zwykle wiele niedoskonałości
    (których ty jednak nie znalazłeś).\r\n\r\nChciałeś ośmieszyć autora programu,
    ale twój artykuł ośmiesza ciebie. Pewnie twój pracodawca i klienci kiedyś go przeczytają.
    W dowolnej firmie informatycznej za każdą z wymienionych tu elementarnych pomyłek
    \ od razu wyleciałbyś z pracy. Trzymasz na blogu artykuł będący piękną prezentacją
    twoich umiejętności zawodowych. To idealny dodatek do twojego CV !  :)"
- id: 19197
  author: Patrys
  author_url: http://room-303.com/
  date: '2008-04-18 00:03:47 +0200'
  date_gmt: '2008-04-17 23:03:47 +0200'
  content: "Bold:\r\n\r\nJeden. Nauka czytania: poświęciłem programowi całe 2 minuty,
    jedną na ściągnięcie, drugą na przegrepowanie strings na obecność głównych podejrzanych.
    Nikt mi nie płaci za recenzowanie spamu i nie zamierzam poświęcać mu swojej uwagi.
    Ty bierzesz wszystkie tabletki na powiększanie penisa, których reklamy wpadają
    do twojej skrzynki i opisujesz skutki ich działania? Nie? Ja też nie. Wyjaśniłem
    wyżej, czemu nie uruchamiam przypadkowych binarek. Zwłaszcza utrzymywanych w darmowej
    domenie.\r\n\r\nDwa. Odnośnie twojej Ciętej Riposty&trade; - grepowanie za urządzeniami
    uważam za skrajną głupotę, od tego jest HAL. Niezależnie od tego, czy autor uznał,
    że 16 linii z dmesga mu się do czegoś przyda (co też jest głupotą, bo dmesg jest
    rotowany i jakimkolwiek źródłem informacji może być tylko tuż po włączeniu urządzenia).\r\n\r\nTrzy.
    Nie szukam i nie szukałem żadnych błędów. Autor nie zadał sobie żadnego trudu
    w poinformowaniu reszty świata o swoim programie (z uniksami i GNOME mam na tyle
    dużo wspólnego, że dowiedziałbym się choćby z chińskiego serwisu o GTK+), za to
    przychodzi jakiś kretyn i wkleja prawie słowo w słowo ten sam komentarz po kilkudziesięcioma
    notkami na blogach. Już w pierwszym akapicie zaznaczyłem, co było powodem napisania
    notki.\r\n\r\nCztery. Informacje o \"inności\" SuSE świadczą tylko o metodzie,
    jaką próbuje się rozwiązać problem. Mówię to z pełną świadomością, jako współautor
    jednej z dystrybucji. Patrz wyżej - HAL jest wszędzie, podobnie jak pppd."
- id: 19201
  author: dely
  author_url: http://daniel.kozminski.info
  date: '2008-04-18 08:08:22 +0200'
  date_gmt: '2008-04-18 07:08:22 +0200'
  content: "Nie jestem programistą, ale uważam stwierdzenie \"uruchamianie programów,
    których źródła się nie zna jest cholernie niebezpieczne.\" zakrawa na paranoję.\r\n\r\nDruga
    sprawa, że pisanie o kimś, że jest kiepskim programistą, bez nawet uruchomienia
    jego programu jest nieładne, nie wspominając o radzie aby program skasować i napisać
    od nowa."
- id: 19205
  author: wojtosz
  author_url: http://www.blaszkowski.com
  date: '2008-04-18 09:51:07 +0200'
  date_gmt: '2008-04-18 08:51:07 +0200'
  content: "@dely\r\nmam swoją politykę bezpieczeństwa, Ty masz swoją, Patrys ma swoją.
    Jeśli Patrys wybrał paranoisalny model tej polityki - jego sprawa i miał do tego
    prawo. Osobiście zgodzę się ze stwierdzeniem że \"uruchamianie programów, których
    źródła się nie zna jest cholernie niebezpieczne\".\r\n\r\nDodatkowo, wydaje mi
    się, że zdecydowana większkość z Was tu piszących nadal nie rozumie przesłania
    tego posta."
- id: 19230
  author: Hoppke
  author_url: http://repo.dobremiasto.net/
  date: '2008-04-19 21:02:52 +0200'
  date_gmt: '2008-04-19 20:02:52 +0200'
  content: "wojtosz: bo wpis nie ma przesłania, zaczyna się od spamu a kończy pomawianiem
    konkretnego człowieka. Jakieś przesłanie miałby, gdyby wyciąć z niego te wycieczki
    osobiste na temat kompetencji Dariusza czy krytykę jego kodu na podstawie \"statycznej
    analizy ASCII\".\r\n\r\nPatrys dostał spam, wkurzył się, naskoczył na autora (który
    jak rozumiem ze spamem nie miał nic wspólnego), przy okazji sobie pojechał po
    jego kompetencjach (\"adding insult to injury\"), opierając wszystko na wątłych
    poszlakach.\r\n\r\nGłupio wyszło, no.\r\n\r\nWypada tylko przeprosić Dariusza,
    spełnić jego prośbę i wywalić oskarżycielski tekst, a w przyszłości może spróbować
    się najpierw skontaktować z autorem softu nim się mu zacznie dupę obrabiać w internecie.\r\n\r\nWpadki
    się zdarzają, ale tę akurat da się łatwo odkręcić :)"
- id: 19237
  author: Global UMTS pozywa at Room 303
  author_url: http://room-303.com/blog/2008/04/20/global-umts-pozywa/
  date: '2008-04-20 18:04:42 +0200'
  date_gmt: '2008-04-20 17:04:42 +0200'
  content: '[...] del.icio.us          &laquo; Global GPRS, Global UMTS [...]'
- id: 19252
  author: kozik
  author_url: http://www.kozik.net.pl
  date: '2008-04-20 22:29:15 +0200'
  date_gmt: '2008-04-20 21:29:15 +0200'
  content: "Zatrważający jest poziom determinacji urażonego autora programu - w kontekście
    rzekomego pozwu jak i komentarzy tutaj (nie wątpię, że część anonimów była tego
    samego autora)... Trochę przykre widzieć taki poziom ograniczenia jak i takie
    ego... Cóż, internet daje trolom dużo odwagi. Życzę powodzenia w trzymaniu swojej
    linii i swojego zdania!\r\n\r\n\r\nP.S. \"dmesg | grep\" mnie normalnie krzesła
    zrzucił, aczkolwiek analiza strings i ldd nie jest dość mocnym argumentem. Jakiś
    strace/ltrace czy inny uruchomiony na wirtualnej maszynie byłby tu lepszy... W
    końcu od tego są wirtualne systemy, by je psuć, czyż nie?"
- id: 19281
  author: zdzichuBG
  author_url: http://zdzichubg.jogger.pl/2008/04/21/ilustrowany-blueconnect-w-fedora-9/
  date: '2008-04-21 15:38:30 +0200'
  date_gmt: '2008-04-21 14:38:30 +0200'
  content: "<strong>Ilustrowany BlueConnect w Fedora 9...</strong>\n\nOd jakiegoś
    czasu korzystam z dostępu do Internetu poprzez modem \r\nHuawei E220 w usłudze\r\nEra
    BlueConnect. Ponieważ słyszy się wiele mitów o trudnościach w \r\nkonfiguracji
    podobnych urządzeń pod linuksem, postanowiłem napisać tą notkę,\r[....."
- id: 19396
  author: Bartek
  author_url: ''
  date: '2008-04-30 16:00:34 +0200'
  date_gmt: '2008-04-30 15:00:34 +0200'
  content: Jesteś skończonym idiotą, który nie ma pojęcia nawet o takich rzeczach
    jak bezpieczeństwo przy uruchamianiu "binarnych" programów, jakbyś potrafił to
    byś wiedział, że można binarki przeanalizować pod IDA / OllyDbg / WinDbg / Hiew
    / HTEdit, a już analizowanie stringów zakrawa na kpinę (tak się analizowało, ale
    20 lat temu). Nie pisz o czymś o czym nie masz pojęcia, bo tylko się ośmieszasz.
- id: 19397
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2008-04-30 16:05:15 +0200'
  date_gmt: '2008-04-30 15:05:15 +0200'
  content: "Bartek:\r\n\r\nPieprzysz głupoty za przeproszeniem. Tutaj jest UNIX i
    do analizy służą maszyny wirtualne i rozszerzenia kernela: apparmor, grsec, strace
    i dtrace."
- id: 19413
  author: Artur Malicki
  author_url: ''
  date: '2008-05-01 21:31:54 +0200'
  date_gmt: '2008-05-01 20:31:54 +0200'
  content: "Analizowanie programu poprzez strings było stosowane kilkanaście lat temu
    w czasach DOS-u przez początkujących użytkowników komputera. To pomysły z innej
    epoki. Nie było wtedy Linuksa i Windows. Nawet w tamtych czasach użycie strings
    zostałoby wyśmiane. Hoppke wyjaśnił czemu jest ono całkowicie nieskuteczne.\r\n\r\nPatrys
    zauważył swoją żenującą niewiedzę dopiero po kilku tygodniach i po przeczytanuiu
    kilkudziesięciu komentarzy. Dopiero w swoim ostatnim komentarzu, aby poprawić
    swój wizerunek, zaczyna wspominać o tym co wyczytał w poradach wyśmiewających
    go ludzi: o strace, ltrace itp.\r\n\r\nTylko po co brał się za analizę programu
    skoro nie ma o tym najmniejszego pojęcia?\r\n\r\nTekst o programie wyraźnie pokazuje
    brak elementarnej wiedzy.\r\nW swojej firmie nie zatrudniłbym takiej osoby nawet
    jakby chciał pracować za darmo.\r\n\r\nPotencjalni klienci Patrysa czytający jego
    blog pewnie wyrobią sobie taką samą opinię."
- id: 19415
  author: Patrys
  author_url: http://room-303.com/
  date: '2008-05-02 01:36:49 +0200'
  date_gmt: '2008-05-02 00:36:49 +0200'
  content: "Artur:\r\n\r\nMam dobry humor do karmienia trolli.\r\n\r\nArtur nie umie
    korzystać z wyszukiwarki, samo wpisanie \"strace\" w search box z prawej strony
    bloga zdradza choćby <a href=\"http://room-303.com/blog/2007/06/20/php-pcre-i-nagle-zgony/\"
    rel=\"nofollow\">tę notkę</a>.\r\n\r\nA <a href=\"http://cia.vc/stats/author/patrys\"
    rel=\"nofollow\">tutaj</a> możesz łatwo sprawdzić, że od ponad 4 lat pracuję przy
    PLD, co bez narzędzi typu gdb i strace jest raczej mało wykonalne.\r\n\r\nSerdecznie
    pozdrawiam pozbawionych elementarnej wiedzy na temat wyszukiwania :)"
- id: 19420
  author: Bartek
  author_url: ''
  date: '2008-05-02 09:12:39 +0200'
  date_gmt: '2008-05-02 08:12:39 +0200'
  content: "lol ja przecież wymieniłem narzędzia, które są dostępne w wersji unixowych,
    jak IDA czy htedit i są powszechnie wykorzystywane do analizy wszelkiego rodzaju
    oprogramowania, jak kiedyś przestaną cię utrzymywać rodzice i być może znajdziesz
    pracę w jakiejś firmie av, gdzie profesjonalnie analizuje się oprogramowanie,
    a nie czyta stringi, to cię oświeci i przestaniesz pieprzyć za przeproszeniem
    takie głupoty wprost ze wspomnianych przez kolegę Artura czasów średniowiecza...\r\n\r\nPS.
    a przy okazji, na Windowsach nie ma maszyn wirtualnych albo emulatorów? A słyszałeś
    o Sandboxie, VMware, VirtualPC, Parallels, VirtualBox (większość z nich jest wieloplatformowa)
    etc.? Czy może unixy mają wyłączność?"
- id: 19421
  author: Patrys
  author_url: http://room-303.com/
  date: '2008-05-02 12:46:56 +0200'
  date_gmt: '2008-05-02 11:46:56 +0200'
  content: "Bartek:\r\n\r\nPowszechnie wykorzystywane do jakiej analizy? Do reverse
    engineeringu? IDA do debugger/disassembler, chyba że coś się zmieniło od czasów,
    kiedy pracowałem na SoftIce.\r\n\r\nZ utrzymywania przez rodziców nawet nie chce
    mi się śmiać :)\r\n\r\nCo do twojego post scriptum: mylisz wirtualizację maszyny
    z wirtualizacją systemu. Idź, wygooglaj sobie kvm i vserver."
- id: 19909
  author: yaotzin
  author_url: http://www.ubuntu.linuxpl.com
  date: '2008-06-01 13:19:30 +0200'
  date_gmt: '2008-06-01 12:19:30 +0200'
  content: "Fajny tekst :)\r\nAle sam osobiście zamieściłem w jednym z topików na
    forum ubuntu spamerską wiadomość :)\r\nhttp://forum.ubuntu.pl/showthread.php?t=41865
    Więc nie do końca tylko ta osoba spamuje, zresztą jakby się nie patrzać to aplikacja
    pewnie niektórym przydatna, mnie osobiście nie udało za pomocą tego programu uruchomić
    neta :/ Szybciej skrypty napisałem... Nie wiem czy ta osoba nie jest również twórcą
    ubuDSL :), ale nie wnikam, Podkreślam, że nie znam autora ani tego programu ani
    tej strony i nie staram się bronić nikogo ani niczego :D"
- id: 20198
  author: B.
  author_url: ''
  date: '2008-06-20 10:00:47 +0200'
  date_gmt: '2008-06-20 09:00:47 +0200'
  content: Szczerze mnie rozbawiło wszystko co tu zostało napisane. Dziękuję Wam za
    tą radość, która pojawiła się na mych ustach gdy czytałem Wasze niesamowite wypowiedzi:)
- id: 20690
  author: krzemyk
  author_url: ''
  date: '2008-07-22 10:14:23 +0200'
  date_gmt: '2008-07-22 09:14:23 +0200'
  content: "wiem że odgrzebuje ale czy mógłby mi to ktoś przybliżyć \"\r\nDo zestawiania
    konfiguracji GPRS służy z powodzeniem pakiet NetworkManager"
---
<p>Są sobie takie dwa programy niejakiego Dariusza Rakowskiego. Nie podlinkuję, dopóki nie napiszę, dlaczego w ogóle o nich wspominam. <em>Bo osoba reklamująca je jest cholernym spamerem</em> i <em>nigdy nie należy ufać programom z niewiadomego źródła.</em></p>

<p>Pierwszy rzut oka na <a href="http://www.globalumts.strony.pl/" rel="nofollow">Global UMTS</a>: binarka bez źródeł. Nie dotykać, pomacać przez <code>ldd</code> i <code>strings</code>. Ten drugi pokazuje, że program szuka <code>gksu</code> albo <code>kdesu</code>. Po co? Pokazuje też, że autor jest słabym programistą i <em>szuka urządzeń przez <code>dmesg | grep</code></em>.</p>

<p>Więcej kwiatków nie chciało mi się szukać. Wygląda jednak na to, że wbrew naszym pierwszym skojarzeniom, program nie wysyła waszych danych do autora. <em>Wygląda</em> &mdash; nie poświęciliśmy mu więcej czasu, więc proszę nie brać tego za pewnik i najlepiej programu zwyczajnie unikać, zamiast tego posiłkując się najnowszym Network Managerem.</p>

<p>Dariuszowi zaś, jeśli <del>to prawdziwe imię i</del> ma faktycznie dobre zamiary, polecam skasować program, napisać od nowa po ludzku (z użyciem HALa, PolicyKit i bez sprawdzania, czy dystrybucja to czasem nie OpenSuSE) i udostępnić w postaci źródeł. Na licencji, która zezwala na dystrybucję. Aha, radziłbym się upewnić, czy rozprowadzanie loginów i haseł operatorów komórkowych z całego świata jest zgodne z ich wolą i prawem.</p>
