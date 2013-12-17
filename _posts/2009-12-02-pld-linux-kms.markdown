---
layout: post
status: publish
published: true
title: 'PLD Linux: KMS'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 667
wordpress_url: http://room-303.com/blog/?p=667
date: 2009-12-02 14:02:46.000000000 +01:00
categories:
- linux
- software
tags:
- pld
- kms
- nouveau
- nvidia
comments:
- id: 24584
  author: danim
  author_url: ''
  date: '2009-12-02 15:36:37 +0100'
  date_gmt: '2009-12-02 14:36:37 +0100'
  content: Tak przy okazji posta o PLD ciekawy jestem co sądzisz na temat systemu
    intrux - który notabene oparty jest właśnie o PLD - ja jakoś szczerze mówiąc nie
    mam zaufania do tego typu wynalazków a linux na serwerze kojarzy mi się jakoś
    wyłącznie z debianem ;)
- id: 24585
  author: Patrys
  author_url: http://room-303.com/
  date: '2009-12-02 15:42:05 +0100'
  date_gmt: '2009-12-02 14:42:05 +0100'
  content: Nie znam, ja na serwerach od lat trzymam PLD, Debiana kiedyś używałem a
    dziś serdecznie nie trawię.
- id: 24586
  author: specnaz
  author_url: ''
  date: '2009-12-02 22:54:58 +0100'
  date_gmt: '2009-12-02 21:54:58 +0100'
  content: 'Hmmm... tak sobie chodze po tej stronie inrtuxa i jak rozumiem jest to
    zmodyfikowany PLD - "Zestaw oprogramowania INTRUX Firewall &amp; QoS działa w
    środowisku specjalnie przygotowanej dystrybucji PLD " blablabla. Moze troche panikuje,
    ale: NIE MA ZRODEL, nie moge znalezc kodu zrodlowego ich modyfikacji, sa tylko
    dostepne binaria za ktore trzeba placic. Wydaje mi sie, ze zapomnieli udostepnic
    source code - a jezeli mam racje - jest to naruszenie GPLv2+ jak w pysk strzelil.'
- id: 24667
  author: Wojciech Błaszkowski
  author_url: http://www.blaszkowski.com
  date: '2009-12-27 14:39:32 +0100'
  date_gmt: '2009-12-27 13:39:32 +0100'
  content: Bez nouveau nie da rady ?
- id: 24671
  author: Patrys
  author_url: http://room-303.com/
  date: '2009-12-28 13:34:14 +0100'
  date_gmt: '2009-12-28 12:34:14 +0100'
  content: "Wojciech:\r\n\r\nJeśli masz nVidię, to nie ;)\r\n\r\nNa nowych kernelach
    nie potrzeba za to fbcon, bo jest u nas wbudowane."
- id: 24753
  author: DeeJay1
  author_url: ''
  date: '2010-01-14 15:21:50 +0100'
  date_gmt: '2010-01-14 14:21:50 +0100'
  content: Na swoim inetlu musiałem w PREMODS dać "intel-agp", inaczej nawet X'y nie
    wstawały, ale teraz śmiga :)
---
<p>Jeśli każda próba użycia <abbr title="Kernel Mode Setting">KMS</abbr> kończy się czarnym ekranem, prawdopodobnie potrzebujesz tego samego, co ja.</p>

<p>Na początek na warsztat bierzemy plik <code>/etc/sysconfig/geninitrd</code>. Tam istotne są dwa wiersze:</p>

<blockquote><code><pre>PREMODS="fbcon"
FBMODULE="nouveau"</pre></code></blockquote>

<p>Oczywiście, <code>nouveau</code> należy zastąpić modułem adekwatnym do posiadanego sprzętu.</p>

<p>Następnie tworzymy plik <code>/etc/modprobe.d/kms.conf</code> o treści:</p>

<blockquote><code><pre>options nouveau modeset=1</pre></code></blockquote>

<p>Oczywiście, tu również podstawiamy stosowny moduł.</p>

<p>Na koniec generujemy za pomocą <code>geninitrd</code> nowy obraz startowy i uruchamiamy ponownie komputer. Voilà!</p>
