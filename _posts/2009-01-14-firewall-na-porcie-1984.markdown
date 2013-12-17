---
layout: post
status: publish
published: true
title: Firewall na porcie 1984
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 509
wordpress_url: http://room-303.com/blog/?p=509
date: 2009-01-14 12:11:53.000000000 +01:00
categories:
- varia
- software
tags: []
comments:
- id: 23746
  author: sprae
  author_url: ''
  date: '2009-01-14 13:36:17 +0100'
  date_gmt: '2009-01-14 12:36:17 +0100'
  content: Nie na darmo wcześniej w Niemczech powstała ustawa o zakazie używania "crackers-kiego"
    oprogramowania, a w Wielkiej Brytanii o zakazie szyfrowania poczty elektronicznej.
    Myślę ze w takich (niemieckich) warunkach przeszukiwanie jest ułatwione, to w
    reszcie krajów będzie to raczej prowadzone przez sniff i inne mitm.
- id: 23747
  author: Patrys
  author_url: http://room-303.com/
  date: '2009-01-14 13:49:44 +0100'
  date_gmt: '2009-01-14 12:49:44 +0100'
  content: "sprae:\r\n\r\nJeśli wystarczy ustawa, żeby ludzie nie używali softu do
    łamania zabezpieczeń, to może wystarczy ustawa, że nie wolno popełniać przestępstw?
    Chyba gdzieś już taką widziałem ;)\r\n\r\nA sniffing w czasie rzeczywistym jest
    dość trudny do uzyskania przy wykorzystaniu protokołów z szyfrowaniem niesymetrycznym."
- id: 23749
  author: GDR!
  author_url: http://gdr.geekhood.net/
  date: '2009-01-14 19:29:17 +0100'
  date_gmt: '2009-01-14 18:29:17 +0100'
  content: "Patrys:\r\n\r\nNo, ale kto używa szyfrowania, ten używa. A cała reszta
    pozostaje podatna na podsłuchiwanie."
- id: 23751
  author: Łukasz Adamczuk
  author_url: http://adamczuk.net.pl/
  date: '2009-01-15 00:07:12 +0100'
  date_gmt: '2009-01-14 23:07:12 +0100'
  content: "Twój wpis bardzo dobrze pokazuje próby ograniczenia wolności użytkowników
    przez wielkie korporacje. Używanie konkretnego sprzętu i oprogramowania daje dostęp
    do danych użytkownika.\r\n\r\nW aspekcie wolności jako podstawowego prawa człowieka
    nie powinniśmy się godzić na jej ograniczanie w jakikolwiek sposób."
- id: 23752
  author: qwiat
  author_url: ''
  date: '2009-01-15 00:17:20 +0100'
  date_gmt: '2009-01-14 23:17:20 +0100'
  content: bez problemu dam dostęp organom ścigania do jednej z kilku maszyn wirtualnych
    na moim desktopie, nawet z prawami roota :)
- id: 23755
  author: Marti
  author_url: http://marti.dimerge.net/
  date: '2009-01-15 09:55:17 +0100'
  date_gmt: '2009-01-15 08:55:17 +0100'
  content: "aktualnie:\r\n\r\nArt. 74. § 1. KPK Oskarżony nie ma obowiązku dowodzenia
    swej niewinności ani obowiązku dostarczania dowodów na swoją niekorzyść \r\n\r\nczyli
    w wolnym tłumaczeniu: \r\njeżeli mam założone hasło / szyfruje co mi się podoba
    i nie chcę go udostępnić Policji bo mam tam jakieś kradziejstwo czy \"bo tak mi
    się podoba\" to nikt nie może mi z tego powodu czynić zarzutu. Być może ustawodawcy
    chodzi o utrudnianie dostępu komuś do jego danych (czyli np. taki wredny hacking
    dla jaj) - no ale tego nie wiemy i to wyjdzie w praniu. Niemniej jednak uważam,
    że penalizowanie działań oskarżonego/podejrzanego mających na celu zaniechanie
    udzielenia organom ścigania uzyskanie dowodów popełnienia przestępstwa narusza
    powołany przepis kpk i jest niezgodne z Konstytucją."
- id: 23763
  author: anghan
  author_url: http://anghan.jogger.pl
  date: '2009-01-16 15:32:28 +0100'
  date_gmt: '2009-01-16 14:32:28 +0100'
  content: Ustawę napisali politycy, cieszyli się z tego rzecznicy prasowi policji
    i innych służb, a teraz będzie rozpoznanie rynku i stworzenie dokumentu wizji
    i innych pierdów, a na koniec wnioski, że system umożliwia wydajne sterowanie
    działaniem jednostek antyterrorystycznych.
---
<p>VaGla w swojej notce zatytułowanej <q><a href="http://prawo.vagla.pl/node/8305">Firmy antywirusowe w rozkroku wobec wizji policyjnych włamań</a></q> zwraca uwagę na coś, co wygląda na oczywiste niedopatrzenie ze strony orwellowców lobbujących na rzecz dopuszczenia tak zwanych <q>zdalnych przeszukań</q> ze strony policji. Wydaje się, że nikt nie wziął pod uwagę, że to administrator komputera decyduje o tym, jakie usługi i komu komputer ów będzie świadczył.</p>

<p>Nawet jeśli prawo w którymś momencie zezwoli policji na zdalne przeszukanie moich maszyn, będą najpierw musieli w jakiś sposób połączyć się z komputerem. Tu opcje są dwie &mdash; ustawowo wymagany interfejs lub włamanie z wykorzystaniem luk bądź słabości w mechanizmach działającego oprogramowania. W obu przypadkach pojawia się bariera zgodności oprogramowania, każdy system wymaga dedykowanej implementacji interfejsu, każdy ma też inne zabezpieczenia i błędy.</p>

<p>Naturalny kolejny krok to delegalizacja systemów, które nie będą podatne na taki zdalny dostęp. Czy to ze względu na fakt, że ustawodawca nie dostarczył stosownego oprogramowania, czy ze względu na nadmierne bezpieczeństwo (brak dostatecznie długiej listy znanych luk w zabezpieczeniach). Może któregoś dnia doczytamy się w konstytucji zapisu o tym, że wolność obywatela ogranicza się do wyboru między Windows Vista Home Basic z dodatkiem Service Pack 1 i Windows Vista Business?</p>

<p>Interesuje mnie też, w jaki sposób organy uprawnione do takich przeszukań określałyby &mdash; przed przystąpieniem do czynności &mdash; czy mają do czynienia ze sprzętem prywatnym pana Kowalskiego, czy z maszyną służbową, znajdującą się w jego biurze bądź serwerem w kolokacji? Jeśli bowiem wolno byłoby przeszukiwać każdy komputer bez wyjątku, to co z zagranicznymi firmami, które część sprzętu posiadają w Polsce i co z obywatelami Polski, którzy wykorzystują komputery poza naszymi granicami? Naturalnym skutkiem będzie masowa emigracja usług IT na wschód.</p>

<p>I w jaki sposób &mdash; bez czynnej współpracy ze strony przeszukiwanego &mdash; oprogramowanie takie miałoby spenetrować bramki NAT i maskarady, powszechnie stosowane w sieciach domowych?</p>

<p>Dla mnie cały pomysł zdalnego przeszukania jest jak scenariusz do ekranizacji <q>1984.</q> Mam spore wątpliwości co do technicznej wykonalności i możliwości egzekwowania takich przepisów.</p>

<p>Z jednej strony pewnych zabezpieczeń nie da się łatwo przełamać. Nie może być tak, że zdalne obejrzenie listy plików na dysku jest droższe (a pamiętajmy, że czas również jest kosztem) od wysłania tam jednostki antyterrorystycznej, otoczenia budynku i przywiezienia komputera na komendę.</p>

<p>Z drugiej strony nie można ustawowo nakazać obywatelowi współpracy. Przyczyna jest prosta - który sąd podejmie się rozstrzygać, czy dany sprzęt jest "komputerem" w rozumieniu tej ustawy? W czasach, gdy telefony, kuchenki mikrofalowe i tostery posiadają własne systemy operacyjne, może się okazać koniecznym zaimplementowanie stosownych interfejsów w piekarnikach, samochodach i pralkach.</p>

<p>Na koniec pozostaje najtrywialniejsza kwestia &mdash; wszyscy związani z branżą IT wiedzą, że żadne zabezpieczenia nie są od uniemożliwiania, ich celem jest utrudnienie powyżej granicy opłacalności. Gdyby jednak powstała specjalna usługa, pozwalająca na pełny, zdalny dostęp do dowolnego komputera w kraju (albo na kontynencie czy wręcz planecie), to kto nie skusi się na przełamanie jej mechanizmów i wykorzystanie ich do własnych celów? Mieliśmy już sytuacje, kiedy oprogramowanie DRM było sprytnie wykorzystywane do ukrywania wirusów i trojanów przed oprogramowaniem antywirusowym, czy tak trudno wyobrazić sobie sytuację, gdy globalny projekt <q>Wielki Brat</q> staje się tylko ustawowym fundamentem dla zupełnie nowej sieci usług szpiegowskich?</p>

<p>PS: Z niecierpliwością czekam na projekt mający na celu umożliwienie przeprowadzania zdalnej kolonoskopii bez wiedzy pacjenta.</p>
