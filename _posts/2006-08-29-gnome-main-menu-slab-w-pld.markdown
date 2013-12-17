---
layout: post
status: publish
published: true
title: GNOME Main Menu (SLAB) w PLD
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 288
wordpress_url: http://www.room-303.com/blog/2006/08/29/gnome-main-menu-slab-w-pld/
date: 2006-08-29 23:11:13.000000000 +02:00
categories:
- linux
- usability
- software
tags: []
comments:
- id: 4528
  author: AvantaR
  author_url: http://avantar.jogger.pl
  date: '2006-08-29 23:13:30 +0200'
  date_gmt: '2006-08-29 22:13:30 +0200'
  content: Jak tam sie w ogole ma PLD, bo troche czasu minelo jak porzucilem to distro
    ;) Dalej sie tak psuje?
- id: 4529
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-08-29 23:19:40 +0200'
  date_gmt: '2006-08-29 22:19:40 +0200'
  content: Undefined constant <code>psuje</code>, assumed <code>NULL</code> ;)
- id: 4534
  author: bazyl
  author_url: ''
  date: '2006-08-30 07:38:57 +0200'
  date_gmt: '2006-08-30 06:38:57 +0200'
  content: No, nieźle. Ale i tak najfajniejsze jest tełko :) Boli Blog rzondzi :P
- id: 4535
  author: MiKom
  author_url: ''
  date: '2006-08-30 09:06:28 +0200'
  date_gmt: '2006-08-30 08:06:28 +0200'
  content: Można dostać jakoś to tło pulpitu?
- id: 4536
  author: MiKom
  author_url: ''
  date: '2006-08-30 09:15:11 +0200'
  date_gmt: '2006-08-30 08:15:11 +0200'
  content: A przepraszam, już znalazłem
- id: 4538
  author: marcolphus
  author_url: http://www.markolf.org
  date: '2006-08-30 11:32:01 +0200'
  date_gmt: '2006-08-30 10:32:01 +0200'
  content: MiKom -&gt; to podziel się wiedzą, bo ja nie mogę znaleźć.
- id: 4539
  author: OJO
  author_url: ''
  date: '2006-08-30 11:39:43 +0200'
  date_gmt: '2006-08-30 10:39:43 +0200'
  content: szkoda tylko że nie działa (na th). wywala się zaraz po dodaniu do panela,
    a uruchomienie wymaganego przez menu NetworkManagera wyłącza sieć. No ale to nie
    miejsce na biadolenie, co? :)
- id: 4540
  author: cli3nt
  author_url: http://techlebak.blogspot.com
  date: '2006-08-30 11:52:38 +0200'
  date_gmt: '2006-08-30 10:52:38 +0200'
  content: 'marcolphus: http://www.flickr.com/photos/patrys/223133961/in/photostream/'
- id: 4541
  author: luo
  author_url: http://quest-88.jogger.pl
  date: '2006-08-30 12:10:43 +0200'
  date_gmt: '2006-08-30 11:10:43 +0200'
  content: "\"Sprawuje się bardzo wygodnie i choć nie zastąpi raczej standardowego
    menu GNOME, jest bardzo miłym do niego dodatkiem.\"\r\n\r\nA czy przypadkiem nie
    będzie to domyślne menu w GNOME3?"
- id: 4542
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-08-30 14:40:43 +0200'
  date_gmt: '2006-08-30 13:40:43 +0200'
  content: "OJO:\r\n\r\nDziała (screeny są właśnie z Th, Ac nie mam), przeloguj się
    do sesji GNOME, żeby GConf wciągnął schemy konfiguracji, a dopiero potem dodaj
    do panelu.\r\n\r\nNetworkManager wcale nie jest potrzebny, potrzebne jest tylko
    NetworkManager-devel do zbudowania pakietu (stamtąd bierze nagłówki dla komunikacji
    po DBUS).\r\n\r\nluo:\r\n\r\nTopaz póki co jest kilkoma zdaniami na kartce papieru
    (a dokładniej w wiki), więc to ciekawy wniosek."
- id: 4550
  author: matipl
  author_url: ''
  date: '2006-08-31 07:44:54 +0200'
  date_gmt: '2006-08-31 06:44:54 +0200'
  content: "Polecałbym do SPEC-a dodać w zależnościach fam-devel, ponieważ wysypuje
    się builder:\r\n/bin/sh ../../libtool --tag=CC --mode=link gcc  -g -O2   -o libslab.la
    -rpath /usr/lib  nld-marshal.lo app-resizer.lo app-shell.lo app-shell-startup.lo
    double-click-detector.lo search-bar.lo search-context-picker.lo search-entry.lo
    shell-window.lo slab-gnome-util.lo slab-section.lo tile.lo tile-action.lo nameplate-tile.lo
    application-tile.lo -pthread -L/usr/X11R6/lib -lgnome-desktop-2 -lgnomeui-2 -lSM
    -lICE -lstartup-notification-1 -lbonoboui-2 -lgnome-keyring -lxml2 -lgnomecanvas-2
    -lgnome-2 -lpopt -lart_lgpl_2 -lgtk-x11-2.0 -lgdk-x11-2.0 -lXrandr -lXi -lXinerama
    -latk-1.0 -lpangocairo-1.0 -lXcursor -lXfixes -lcairo -lpangoft2-1.0 -lfontconfig
    -lfreetype -lz -lXrender -lX11 -lXext -lgnomevfs-2 -lbonobo-2 -lgconf-2 -lbonobo-activation
    -lORBit-2 -lgthread-2.0 -lrsvg-2 -lgdk_pixbuf-2.0 -lgnome-menu -lpango-1.0 -lm
    -lgobject-2.0 -lgmodule-2.0 -ldl -lglib-2.0   ../../utils/libutils.la\r\ngrep:
    /usr/lib/libfam.la: No such file or directory\r\n/bin/sed: can't read /usr/lib/libfam.la:
    No such file or directory"
- id: 4591
  author: gregl
  author_url: ''
  date: '2006-09-10 00:04:34 +0200'
  date_gmt: '2006-09-09 23:04:34 +0200'
  content: W AC działa bez najmniejszych problemów. Całkiem ciekawe rozwiązanie.
---
<p>Znane dobrze użytkownikom SUSE menu, opracowane przez specjalistów użyteczności Novella, trafiło dziś do PLD. Dodałem dziś <a href="http://cvs.pld-linux.org/cgi-bin/cvsweb/SPECS/gnome-main-menu.spec">plik SPEC dla apletu</a> i stosownego patcha dla pakietu <code>gnome-desktop</code>, który dodaje obsługę ostatnio używanych aplikacji.</p>

<p class="strip"><a href="http://www.flickr.com/photos/patrys/228570497/" title="Photo Sharing"><img src="http://static.flickr.com/66/228570497_fa752169c5.jpg" alt="GNOME Main Menu (SLAB) - Favorite Apps" height="313" width="500" /></a></p>

<p>Górną część menu zajmuje pasek wyszukiwania Beagle, który pozwala w łatwy sposób dotrzeć do plików, bez potrzeby majstrowania w systemie plików. Wpisanie tam dowolnego ciągu i wciśnięcie <kbd>Enter</kbd> uruchamia aplikację <code>beagle-search</code>. Prawa część to typowe zadania i stan komputera — połączenie sieciowe i dostępne miejsce na dyskach. Środkową zaś część okupuje standardowo lista ulubionych aplikacji, lista ta ma jednak trzy możliwe funkcje, za pomocą przełącznika można zmienić ją w listę ostatnio otwieranych dokumentów albo w listę ostatnio uruchamianych aplikacji:</p>

<p class="strip"><a href="http://www.flickr.com/photos/patrys/228570492/" title="Photo Sharing"><img src="http://static.flickr.com/87/228570492_d37b6ee395.jpg" alt="GNOME Main Menu (SLAB) - Recently Used Apps" height="313" width="500" /></a></p>

<p>Pod listą znajduje się dodatkowy przycisk, uruchamiający wyszukiwarkę aplikacji zainstalowanych na komputerze:</p>

<p class="strip"><a href="http://www.flickr.com/photos/patrys/228570495/" title="Photo Sharing"><img src="http://static.flickr.com/63/228570495_ca52f68c12.jpg" alt="GNOME Main Menu (SLAB) - Application Browser" height="313" width="500" /></a></p>

<p>Sprawuje się bardzo wygodnie i choć nie zastąpi raczej standardowego menu GNOME, jest bardzo miłym do niego dodatkiem.</p>

Technorati Tags: <a href="http://technorati.com/tag/slab" rel="tag">slab</a>, <a href="http://technorati.com/tag/gnome" rel="tag">gnome</a>, <a href="http://technorati.com/tag/applet" rel="tag">applet</a>, <a href="http://technorati.com/tag/menu" rel="tag">menu</a>, <a href="http://technorati.com/tag/novell" rel="tag">novell</a>, <a href="http://technorati.com/tag/suse" rel="tag">suse</a>, <a href="http://technorati.com/tag/pld" rel="tag">pld</a>
