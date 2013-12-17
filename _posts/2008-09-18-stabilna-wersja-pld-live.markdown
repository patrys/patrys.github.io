---
layout: post
status: publish
published: true
title: Stabilna wersja PLD Live
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 486
wordpress_url: http://room-303.com/blog/?p=486
date: 2008-09-18 12:31:11.000000000 +02:00
categories:
- linux
- software
tags: []
comments:
- id: 21597
  author: grizz
  author_url: http://grizz.pl
  date: '2008-09-18 13:42:48 +0200'
  date_gmt: '2008-09-18 12:42:48 +0200'
  content: Świetna robota :&gt;
- id: 21601
  author: sl3dziu
  author_url: http://sl3dziu.jogger.pl
  date: '2008-09-18 15:15:47 +0200'
  date_gmt: '2008-09-18 14:15:47 +0200'
  content: To już wiem co będę robił wieczorem ;)
- id: 21606
  author: 3ED
  author_url: ''
  date: '2008-09-18 21:19:20 +0200'
  date_gmt: '2008-09-18 20:19:20 +0200'
  content: PLD w końcu nabiera prawdziwych rumieńców, jak miło.
- id: 21608
  author: Joseph
  author_url: ''
  date: '2008-09-18 23:49:30 +0200'
  date_gmt: '2008-09-18 22:49:30 +0200'
  content: Jakby ktoś chciał i nie mógł się dopchać to umieściłem tą płytkę tutaj
    ftp://zs.zdzieszowice.pl. Mam nadzieje, że antyspam mi tego nie zje.
- id: 21615
  author: nightman
  author_url: http://www.ubuntustory.com
  date: '2008-09-19 10:38:40 +0200'
  date_gmt: '2008-09-19 09:38:40 +0200'
  content: Być może to głupie pytanie ale zadam - Jest PLD z KDE 4 lub choćby z 3.5?
- id: 21624
  author: cactus
  author_url: ''
  date: '2008-09-19 22:51:02 +0200'
  date_gmt: '2008-09-19 21:51:02 +0200'
  content: "nightman: chodzi ci o PLD live ? Jesli tak, to nie ma \r\nale z pewnoscia
    powstanie :)"
- id: 21741
  author: martinez
  author_url: http://marcin.af.gliwice.pl/
  date: '2008-09-29 17:24:08 +0200'
  date_gmt: '2008-09-29 16:24:08 +0200'
  content: 'Instalacja wyrzuciła błąd (AttributeError: ''module'' object has no attribute
    ''makeDevInode''), ale... dam szansę i będę próbował kolejnych wersji.'
- id: 21742
  author: Patrys
  author_url: http://room-303.com/
  date: '2008-09-29 18:14:07 +0200'
  date_gmt: '2008-09-29 17:14:07 +0200'
  content: "martinez:\r\n\r\nZ błędami proszę na Launchpad, a nie do komentarzy. Bez
    pełnego zrzutu stosu wywołań (traceback) nie będziemy w stanie tego znaleźć i
    poprawić."
- id: 22472
  author: Listwa
  author_url: ''
  date: '2008-11-01 22:08:37 +0100'
  date_gmt: '2008-11-01 21:08:37 +0100'
  content: Ja mam pytanie odnośnie działania PLD na laptopie Asus A6km (kiedyś miałeś
    takowego). Czy któryś z kerneli przystosowany jest do uruchomienia laptopa z podłączonymi
    urządzeniami USB?
- id: 22487
  author: Patrys
  author_url: http://room-303.com/
  date: '2008-11-02 11:27:56 +0100'
  date_gmt: '2008-11-02 10:27:56 +0100'
  content: 'Listwa: nie, to błąd w biosie, najprościej cofnąć bios do działającej
    wersji.'
---
Trochę musieliśmy poczekać, ale chyba było warto. Wczoraj <a href="http://pozar-w-burdelu.blogspot.com/">qwiat</a> zdecydował się wydać stabilną wersję PLD Live w wersji <em>th.2008.09</em>. A trzeba powiedzieć, że nie było to łatwe zadanie — trudna ścieżka stabilizacji okupiona była wieloma mękami i torturami w postaci rozlicznych butelek tequili, kilku flaszek szkockiej i walających się po kątach butelek po piwie.

O oprogramowaniu rozpisywać się nie będę, zainteresowanych szczegółami zapraszam na <a href="http://ep09.pld-linux.org/~qwiat/">stronę projektu</a>. Mam nadzieję, że niedługo uda się przenieść projekt do stosownej subdomeny pld-linux.org (trwa jeszcze sezon urlopowy i część władnych tego świata jest zwyczajnie nieosiągalna).

Kolejne kroki naszej drogi do władzy nad światem to dopracowanie instalatora i dostosowanie do potrzeb PLD usługi <code>firstboot</code>. Ta ostatnia pozwala skonfigurować świeżo zainstalowany system, włącznie z założeniem konta pierwszego użytkownika.

Jak zwykle, serdecznie zapraszamy do testowania. Wszelkie błędy i problemy powinny trafiać <a href="https://bugs.launchpad.net/pld-linux">na Launchpad</a>.

<p><strong>Update:</strong> hawk zlitował się nad nami i strona ma już <a href="http://livecd.pld-linux.org/">bardziej oficjalny adres</a>. Wielkie dzięki!</p>
