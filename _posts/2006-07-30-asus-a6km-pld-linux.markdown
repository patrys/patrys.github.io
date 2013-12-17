---
layout: post
status: publish
published: true
title: ASUS A6KM + PLD Linux
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 279
alias: /blog/2006/07/30/asus-a6km-pld-linux/
date: 2006-07-30 13:06:08.000000000 +02:00
categories:
- linux
tags: []
comments:
- id: 4388
  author: ehh
  author_url: ''
  date: '2006-07-30 13:32:42 +0200'
  date_gmt: '2006-07-30 12:32:42 +0200'
  content: Dobry wybór:)
- id: 4389
  author: arekm
  author_url: ''
  date: '2006-07-30 14:03:17 +0200'
  date_gmt: '2006-07-30 13:03:17 +0200'
  content: "14:00.3 System peripheral: Ricoh Co Ltd R5C592 Memory Stick Bus Host Adapter
    (rev 08)\r\n\r\ndziała znakomicie z sterownikiem sdhci."
- id: 4390
  author: Elus
  author_url: ''
  date: '2006-07-30 14:03:48 +0200'
  date_gmt: '2006-07-30 13:03:48 +0200'
  content: "Moment... Turion 64 i 32-bitowy system.\r\nMoże sie nie znam, ale czemu
    architektura i686 a nie k-7?"
- id: 4391
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-07-30 14:14:27 +0200'
  date_gmt: '2006-07-30 13:14:27 +0200'
  content: "arekm:\r\n\r\nDziała tylko z kartami SD, ja używam głównie MMC.\r\n\r\nElus:\r\n\r\nPotrzebuję
    mieć natychmiast sprawny builder dla i686, nie mam czasu na zabawy w chroot teraz
    ani na walkę z rzeczami które nie obsługują innych architektur (np. flash). Turion
    w trybie 32-bitowym i tak jest znacznie szybszy od poprzedniego laptopa - ASUS
    A2500D."
- id: 4392
  author: vox populi
  author_url: ''
  date: '2006-07-30 14:23:04 +0200'
  date_gmt: '2006-07-30 13:23:04 +0200'
  content: (0.12 czy 1.0.12?)
- id: 4393
  author: Elus
  author_url: ''
  date: '2006-07-30 14:29:07 +0200'
  date_gmt: '2006-07-30 13:29:07 +0200'
  content: "@Patrys:\r\nTak, w zupełności to rozumiem. Sam mam 64-bitowy procesor
    i 32-bitowy system desktopowy. Mówiłem o czym innym. \r\n\r\nArchitektura k-7
    to o ile mi wiadomo 32-bitowa architektura AMD dla procesorów siódmej generacji
    (jeden \"poziom niżej\" od twojego procka), jakby odpowiednik Intelowskiej i686.
    Sam jadę na jądrze kompilowanym pod tę architekturę (paczki niestety w Ubuntu
    zdaje się są domyślnie kompilowane pod i386) i myślę że to najbardziej optymalne
    rozwiązanie. Ale mogę się mylić."
- id: 4394
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-07-30 14:36:44 +0200'
  date_gmt: '2006-07-30 13:36:44 +0200'
  content: "Elus:\r\n\r\nJeśli o to chodzi to tak, mógłbym używać paczek budowanych
    dla architektur athlon albo p4, z tym, że zysk wydajności nie jest wart zabawy
    w zmnianę architektury systemu. PLD prowadzi specjalną architekturę optymalizowaną
    dla procesorów K7 AMD."
- id: 4395
  author: zdzichu
  author_url: http://zdzichubg.jogger.pl
  date: '2006-07-30 15:22:28 +0200'
  date_gmt: '2006-07-30 14:22:28 +0200'
  content: ',,Matryca GLARE''''... Fuj!'
- id: 4397
  author: mcv
  author_url: http://mcv.jogger.pl/
  date: '2006-07-30 19:32:48 +0200'
  date_gmt: '2006-07-30 18:32:48 +0200'
  content: O, a poprzedni Ci się nie rozleciał w kawałki? ;-) Mam A2532 i tandetna
    budowa dała o sobie znać już dawno… Zwłaszcza przy „zawieszeniu” matrycy.
- id: 4400
  author: delphiak
  author_url: ''
  date: '2006-07-31 09:05:32 +0200'
  date_gmt: '2006-07-31 08:05:32 +0200'
  content: mozesz powiedziec czym sie kierowales wybierajac amd a nie pentiuma? z
    ciekawosci pytam..
- id: 4401
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-07-31 15:58:49 +0200'
  date_gmt: '2006-07-31 14:58:49 +0200'
  content: "delphiak:\r\n\r\nStosunkiem jakości do ceny. Nie tylko wybierając AMD
    przed Pentiumem, ale też wybierając nVidię przed ATI."
- id: 7020
  author: szpila
  author_url: ''
  date: '2007-03-04 22:10:45 +0100'
  date_gmt: '2007-03-04 21:10:45 +0100'
  content: Patryku, mam Linuxa Ubuntu i potrzebuje zrobić downgrade BIOS do wersji
    202. nie mogę jednak namierzyć tej wersji. masz może jakieś namiary? będę zobowiązany.
- id: 7023
  author: evil_core (Krzysztof Krakowiak)
  author_url: ''
  date: '2007-03-05 00:44:47 +0100'
  date_gmt: '2007-03-04 23:44:47 +0100'
  content: Teraz mozna wziasc core2duo + grafika intela gma x3000. Otwarte sterowniki
    = mniej problemow(mam 7300GT, i nieraz modul do jadra sie wywala, szczegolnie
    przy berylu wlaczonym). Jak sterowniki rozwina to w dooma3 na tym mozliwe ze bedzie
    sie dalo grac, nie pwosminajac juz o tym ile karty intela zra proadu.
- id: 7636
  author: Rafał
  author_url: ''
  date: '2007-04-12 15:50:05 +0200'
  date_gmt: '2007-04-12 14:50:05 +0200'
  content: Witam. Mam podobnego laptopa i za nic w świece nie mogę odpalić porządnie
    wifi. Jeśli możęsz to prześlij mi na maila rafal.kondrat@gmail.com te sterowniki
    pod ktorymi ndiswrapper działa OK. Link który podałeś niestety jest juz nieaktualny
    :(
---
<p>Zmieniam laptopa na <a href="http://www.notebooki.wroc.pl/konf_note.php?id=215">nowszy model</a> i od czwartku w, wolnym czasie, powoli stawiam na nim system. Z powodu różnych zawirowań i kłopotów z oprogramowaniem zdecydowałem się, póki co, przenieść tam architekturę i686, choć jest to Turion 64. Z tym problemów nie było, okazało się jednak, że są inne:</p>

<dl>
<dt><abbr title="Advanced Configuration and Power Interface">ACPI</abbr></dt>
<dd>Wadliwy <abbr title="Basic Input/Output System">BIOS</abbr> w laptopie uszkadza tablicę <abbr>ACPI</abbr>, jeśli w czasie <abbr title="Power-On Self Test">POST</abbr> do komputer podłączone są jakiekolwiek urządzenia <abbr title="Universal Serial Bus">USB</abbr>. Rozwiązania są trzy, odłączyć urządzenia <abbr>USB</abbr> do momentu uruchomienia bootloadera, naprawić DSDT, albo wykonać downgrade <abbr>BIOS</abbr> do wersji 202.</dd>

<dt>Dźwięk</dt>
<dd>Karta jest zgodna z intel8x0 i taki sterownik jest dla niej ładowany. Wymaga jednak specjalnej inicjalizacji (a raczej braku inicjalizacji) i załadowanie modułu kończy się… brakiem dźwięku. Specjalny <a href="https://bugtrack.alsa-project.org/alsa-bug/view.php?id=1898">patch czeka już w bugtrackerze <abbr title="Advanced Linux Sound Architecture">ALSA</abbr></a>, zdaje się, że został także włączony do wersji 1.0.12.</dd>

<dt><abbr title="Wireless Local Area Network">WLAN</abbr></dt>
<dd><p>Komputer ma wbudowaną kartę opartą o chipset 802.11g Broadcom, ten sam, który znajduje się w AirportExtreme. Sterownik bcm43xx został włączony do jądra dopiero od wersji 2.6.17 i wciąż jest w fazie rozwoju. Cały czas mam z nim problemy, a sieć udało mi się podnieść dopiero dwa razy i nie jest to działanie deterministyczne. Jak tylko zwalczę kaprysy radiówki, postaram się uaktualnić notkę. Dodam tylko, że próba skorzystania z ndiswrappera zakończyła się komunikatem o niemożliwości rezerwacji obszaru pamięci przez sterownik.</p>

<p><strong>Update:</strong> zgodnie z poradą ehh, użyłem ndiswrappera w połączeniu ze sterownikiem bcmwl5a, który można sobie unzipem wypakować z <a href="ftp://ftp.gateway.com/pub/hardware_support/drivers/win_xp/portable/m360/D00268-001-002.exe">paczki windowsowej</a>. Wszystko działa, jak należy (poza wskaźnikiem siły sygnału, ale do tego się przyzwyczaiłem).</p></dd>

<dt>Kamera</dt>
<dd>Teoretycznie, laptop ma wbudowaną kamerę wysokiej rozdzielczości, opartą o Ali M5602 z matrycą 1,3Mpix. Stosowny <a href="http://m560x.x3ng.com/">sterownik jest już w budowie</a>, ale nadal nie nadaje się do zwykłego użytku.</dd>

<dt>Czytnik kart pamięci</dt>
<dd><p>Podobnie jak wszystkie notebooki ASUS, A6KM ma wbudowany czytnik combo oparty na chipsecie Ricoh. Te ostatnie słyną z braku wsparcia dla Linuksa, więc o urządzeniu można spokojnie zapomnieć.</p>

<p><strong>Update:</strong> to trochę taki skrót myślowy, jak słusznie zauważył arekm, karty SD oczywiście działają, problemy są z kartami MMC.</p></dd>
</dl>

Technorati Tags: <a href="http://technorati.com/tag/asus" rel="tag">asus</a>, <a href="http://technorati.com/tag/laptop" rel="tag">laptop</a>, <a href="http://technorati.com/tag/linux" rel="tag">linux</a>, <a href="http://technorati.com/tag/a6km" rel="tag">a6km</a>
