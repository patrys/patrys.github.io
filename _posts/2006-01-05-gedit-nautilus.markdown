---
layout: post
status: publish
published: true
title: Gedit + Nautilus
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 207
wordpress_url: http://www.room-303.com/blog/2006/01/05/gedit-nautilus/
date: 2006-01-05 18:20:50.000000000 +01:00
categories:
- linux
- web
tags: []
comments:
- id: 2855
  author: Tomasz Staniak
  author_url: http://nbw.jogger.pl
  date: '2006-01-05 18:24:36 +0100'
  date_gmt: '2006-01-05 17:24:36 +0100'
  content: Tak się przyglądam - a czemu by nie Screem? Z tego co pamiętam ma wszystkie
    funkcje o których piszesz.
- id: 2856
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-01-05 18:31:32 +0100'
  date_gmt: '2006-01-05 17:31:32 +0100'
  content: Screem ma niewygodny bardzo układ drzewa - rozdzielony panel na pliki i
    foldery, poza tym w tej chwili nie oferuje mi wiele nad to, co daje gedit (nie
    krozystam z kreatorów, a snippety z gedita są znacznie wygodniejsze, niż makra
    ze Screema - można tam definiować pola do wypełnienia - patrz animowany screengrab
    z poprzedniego posta).
- id: 2858
  author: citizen
  author_url: http://citizen.jogger.pl
  date: '2006-01-05 20:21:39 +0100'
  date_gmt: '2006-01-05 19:21:39 +0100'
  content: Aż takim nazistą nie jesteś, ja koduję bardzo podobnie, tyle że wcinam
    już klamry. (nie mylić z wyjadaczem klamr ;)
- id: 2859
  author: Cthulhu
  author_url: ''
  date: '2006-01-05 20:39:12 +0100'
  date_gmt: '2006-01-05 19:39:12 +0100'
  content: ten bug gnome-vfs to jest jakiś potworek.. Problem zapisywania na ftpie
    istnieje od kiedy pamiętam i nikt tego nie poprawia.. Już nawet zapomniałem jakie
    było wytłumaczenia takiego stanu rzeczy. :/
- id: 2862
  author: Tomasz Staniak
  author_url: http://nbw.jogger.pl
  date: '2006-01-05 21:46:14 +0100'
  date_gmt: '2006-01-05 20:46:14 +0100'
  content: "Widziałem, widziałem. Skłoniło mnie to do zastanowienia się nad konfiguracją
    środowiska deweloperskiego pod Linuksem.\r\n\r\nDziś się prawie przesiadłem, ale
    wyskoczył BardzoPilnyProjektNaWczoraj i musiałem olać konfigurację wszystkiego.\r\n\r\nA
    Gedita zawsze lubiłem, dlatego cieszą mnie tego typu opisy :)"
- id: 2863
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-01-05 22:08:24 +0100'
  date_gmt: '2006-01-05 21:08:24 +0100'
  content: |
    Co jeszcze miłego jest w takim układzie:


    Można jednocześnie zarządzać plikami w lewym panelu. Potrzebuję coś skopiować na szybko? Ctrl C, Ctrl V
    Można mieć otwartych kilka paneli i przełączać się pomiędzy projektami. Często w biurze pracuję jednocześnie przy kilku-kilkunastu projektach
---
<p>Poprzednio pisałem, jak <a href="http://www.room-303.com/blog/2006/01/04/gedit-snippets/">dodać do gedita funkcjonalność <q>snippetów</q></a> i rozbudować jego działanie o znane z TextMate makra. Dziś dodałem do niego panel do wygodnego otwierania plików.</p>

<p>Jako wielki fan <a href="http://quanta.kdewebdev.org/">Quanty+</a>, marzyłem od dawna o wygodnym panelu, umożliwiającym w gedicie pracę z całymi projektami, a nie z pojedynczymi plikami. gedit jest idealnym edytorem do języków skryptowych i ma wygodne podświetlanie składni. Kod <abbr>HTML</abbr> piszę z palca, więc na nic nie przydają mi się całe paski narzędziowe, oferowane przez <a href="http://screem.org/">Screema</a>, <a href="http://bluefish.openoffice.nl/">Bluefisha</a> i Quantę. Lekkośc gedita jest jego zaletą. Jedynej niezbędnej funkcji — widoku struktury projektu — w samym gedicie nie ma. Dlaczego jej zatem nie zasymulować?</p>

<p>Instrukcja obsługi jest dość prosta:</p>

<ol>
<li>otwieramy okno gedita</li>
<li>otwieramy okno Nautilusa</li>
<li>przechodzimy w Nautilusie do katalogu z projektem</li>
<li>przełączamy widok Nautilusa na listę (<kbd>Ctrl</kbd>+<kbd>2</kbd>)</li>
<li>zmniejszamy okno Nautilusa i umieszczamy obok gedita</li>
</ol>

<p>Efekt końcowy wygląda tak:</p>

<p class="strip"><a href="http://www.flickr.com/photos/90175672@N00/82570335/" title="Photo Sharing"><img src="http://static.flickr.com/38/82570335_fe9f781906.jpg" alt="Making gedit work like TextMate" height="375" width="500" /></a></p>

<p>Pliki można w wygodny sposób otwierać przez przeciągnięcie z widoku drzewka do okna edytora. Po zakończeniu pracy z plikiem, wystarczy wcisnąć <kbd>Ctrl</kbd>+<kbd>W</kbd>, aby zamknąć zakładkę i kontynuować pracę. Działa także ze zdalnymi plikami, jedyny problem dotyczy <abbr>FTP</abbr> — stosowny <a href="http://bugzilla.gnome.org/show_bug.cgi?id=110191">bug czeka na rozwiązanie</a>.</p>

<p>Miłej pracy.</p>

Technorati Tags: <a href="http://technorati.com/tag/linux" rel="tag">linux</a>, <a href="http://technorati.com/tag/gedit" rel="tag">gedit</a>, <a href="http://technorati.com/tag/nautilus" rel="tag">nautilus</a>, <a href="http://technorati.com/tag/textmate" rel="tag">textmate</a>, <a href="http://technorati.com/tag/productivity" rel="tag">productivity</a>, <a href="http://technorati.com/tag/gnome" rel="tag">gnome</a>
