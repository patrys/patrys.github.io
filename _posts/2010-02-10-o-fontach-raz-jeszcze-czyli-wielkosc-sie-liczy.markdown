---
layout: post
status: publish
published: true
title: O fontach raz jeszcze, czyli wielkość się liczy
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 787
wordpress_url: http://room-303.com/blog/?p=787
date: 2010-02-10 16:04:31.000000000 +01:00
categories:
- web
tags: []
comments:
- id: 24829
  author: pawel
  author_url: ''
  date: '2010-02-10 18:18:38 +0100'
  date_gmt: '2010-02-10 17:18:38 +0100'
  content: "Warto także nadmienić, że piksel w CSS nie musi być równy fizycznemu pikselowi
    ekranowemu. Przeglądarka przelicza te wartości tak, jakby ekran miał 96dpi, dlatego
    np. na monitorze o rozdzielczości 72dpi, 1px w CSS jest równy 1.33 ekranowego
    piksela :)\r\nhttp://www.emdpi.com/csspixel.html\r\nhttp://webkit.org/blog/57/css-units/"
- id: 24830
  author: wariat
  author_url: http://wariat.jogger.pl
  date: '2010-02-11 11:32:37 +0100'
  date_gmt: '2010-02-11 10:32:37 +0100'
  content: Jak już przy fontach i stopniach i pikselach ... to co to jest za ustrojstwo
    co robi ten bur^W bałagan z litektami tutaj, bo to co się wyświetla po przejściu
    huraganu aka jakiegoś przedurnego skryptu jest porażająco nieczytelne, przynajmniej
    gdzieniegdzie, jeśli nie wszędzie. O głupim efekcie kiedy wszystko się zmienia
    kiedy człowiek zaczyna czytać trzecie zdanie nie wspominając nawet.
- id: 24831
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-02-11 11:39:49 +0100'
  date_gmt: '2010-02-11 10:39:49 +0100'
  content: "wariat:\r\n\r\nObawiam się, że ten \"głupi skrypt\" to twoja przeglądarka.
    Winna tak za zmianę tekstu w czasie czytania trzeciego zdania, jak za nieczytelny
    tekst."
- id: 24832
  author: wariat
  author_url: http://wariat.jogger.pl
  date: '2010-02-11 11:50:43 +0100'
  date_gmt: '2010-02-11 10:50:43 +0100'
  content: I dlatego dzieje się to tylko na room-303? To jakaś dziwna ta moja przeglądarka
    (Mozilla/5.0 (X11; U; Linux i686; en-US; rv:1.9.2) Gecko/20100130 Gentoo Firefox/3.6).
- id: 24833
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-02-11 11:54:00 +0100'
  date_gmt: '2010-02-11 10:54:00 +0100'
  content: "wariat:\r\n\r\nA ile odwiedzasz stron, które używają <code>@font-face</code>?"
- id: 24834
  author: Ajnsztajn
  author_url: ''
  date: '2010-02-11 13:25:51 +0100'
  date_gmt: '2010-02-11 12:25:51 +0100'
  content: "To nie przeglądarka. Mam dokładnie niemal dokładnie to samo co Wariat:
    Mozilla/5.0 (X11; U; Linux x86_64; pl-PL; rv:1.9.2) Gecko/20100209 Gentoo Firefox/3.6\r\ni
    nie mam żadnych dziwnych efektów. Może poza dziwnym wygładzaniem fontu ;). Ale
    to da się przeżyć."
- id: 24835
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-02-11 13:28:07 +0100'
  date_gmt: '2010-02-11 12:28:07 +0100'
  content: "Ajnsztajn:\r\n\r\nA Firefox to nie przeglądarka? Jeśli przeszkadza wam
    podmiana fontu w trakcie czytania, to błędy można zgłaszać w trackerze Mozilli
    :)"
- id: 24836
  author: Ajnsztajn
  author_url: ''
  date: '2010-02-11 13:49:01 +0100'
  date_gmt: '2010-02-11 12:49:01 +0100'
  content: Nie zrozumiałeś mnie. To nie wina przeglądarki, bo u mnie wygląda nieźle
    :P.
- id: 24837
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-02-11 13:56:55 +0100'
  date_gmt: '2010-02-11 12:56:55 +0100'
  content: "Ajnsztajn:\r\n\r\nWygląda nieźle, bo po zobaczeniu, jak wyświetla to Firefox,
    zmieniłem ciężar fontów na nieco większy."
- id: 28135
  author: aaas
  author_url: http://asd
  date: '2012-05-16 14:34:41 +0200'
  date_gmt: '2012-05-16 12:34:41 +0200'
  content: 'dpi jest parametrem ekranu... litosci, podstawy: co to jest DPI a co to
    jest PPI, zenada'
---
<p>Z powodu występującego dzisiaj u mnie przesilenia kataru, zostałem zmuszony (dosłownie ze łzami w oczach) do zmiany wielkości fontów z 10 na 12 punktów. Później wspomniałem o tym kilku osobom, dodając, że nie rozróżniam liter poniżej 16 pikseli, co w dwóch przypadkach wywołało konsternację. Punkty i piksele to nie to samo.</p>

<p>Punkt jest jednostką typograficzną pochodzącą ze standardu pica, który to stworzyli Amerykanie by zemścić się za nasz system metryczny. Według standardu okrągłe¹ dwanaście punktów (<code>pt</code>) równe jest tytułowemu pica (<code>pc</code>). Z kolei sześć pica równe jest jednemu calowi (<code>in</code>). Jak wiemy cal to 2,54 centymetra (<code>cm</code>), ale w tym przypadku nie jest to wiedza istotna.</p>

<p><small>¹ Tak, bezczelnie naśmiewam się z systemu zbudowanego na wielokrotnościach liczby 6.</small></p>

<p>Co wiemy do tej pory: <code>72pt = 6pc = 1in = 2.54cm = 25.4mm</code>.</p>

<p>Na szczęście rozdzielczość sprzętową (DPI) również zdefiniowali Amerykanie i liczymy ją w punktach na cal. W punktach ekranowych, czyli pikselach (nie w punktach typograficznych, o których mówiliśmy wcześniej). DPI jest parametrem konkretnego ekranu² i mówi nam, ile kolejnych pikseli (<code>px</code>) ekranu należy zapalić, żeby długość powstałej linii wynosiła dokładnie jeden cal. Dla przykładu: rozdzielczość sprzętowa mojego laptopa wynosi 96 pikseli na cal, a mojego telefonu 260 pikseli na cal.</p>

<p><small>² Oczywiście zakładając poprawną konfigurację systemu operacyjnego, nic nie stoi bowiem na przeszkodzie do wmówienia komputerowi, że jego ekran jest wielkości biurka czy stadionu.</small></p>

<p>Posiadając tę wiedzę, możemy zacząć przeliczać: <code>12pt = 12 × 1/72in = 12/72in × 96px/in = 16px</code>. <em>Voilà!</em> Teraz mogę spokojnie poumierać dalej.</p>
