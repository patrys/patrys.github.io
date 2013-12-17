---
layout: post
status: publish
published: true
title: 'Religijnie: 10 przykazań i władza nad demonami'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 382
wordpress_url: http://room-303.com/blog/2007/06/10/religijnie-10-przykazan-i-wladza-nad-demonami/
date: 2007-06-10 21:51:30.000000000 +02:00
categories:
- linux
- web
- software
- code
tags: []
comments:
- id: 8063
  author: http-marcinj.openid.pl-
  author_url: http://marcinj.openid.pl/
  date: '2007-06-10 22:59:35 +0200'
  date_gmt: '2007-06-10 21:59:35 +0200'
  content: 'a ja myślałem, żeś przeportował to: http://www.daemon-tools.cc/  na pajtona
    :)'
- id: 8064
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-06-10 23:22:15 +0200'
  date_gmt: '2007-06-10 22:22:15 +0200'
  content: "Marcin:\r\n\r\nDo tego wystarczy <code>mount -o loop</code> ;)"
- id: 8066
  author: http-blog.jajcus.net-
  author_url: http://blog.jajcus.net/
  date: '2007-06-11 07:59:29 +0200'
  date_gmt: '2007-06-11 06:59:29 +0200'
  content: To która to już będzie reimplementacja daemontools?
- id: 8067
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-06-11 09:12:18 +0200'
  date_gmt: '2007-06-11 08:12:18 +0200'
  content: "Jajcus:\r\n\r\nNie wiem, czy liczyć różne minity itp. wynalazki. Mi nie
    zależy na zastępowaniu całego SystemV jak najmniejszym procesem napisanym w C,
    chcę mieć tylko wygodne narzędzie do zarządzania usługami, łącznie z możliwością
    ich ubicia od czasu do czasu :)\r\n\r\nNajbliżej naszych potrzeb jest daemontools,
    ale djb w dzieciństwie uderzył się w głowę i jego paczka jest nierozwijalna (zakaz
    dystrybucji zmodyfikowanego kodu i wersji binarnych), a niedługo będzie całkiem
    niezdatna do dystrybucji (2007-07-01 wygasa licencja)."
- id: 8082
  author: Marcin
  author_url: http://www.ktos.info
  date: '2007-06-13 17:49:04 +0200'
  date_gmt: '2007-06-13 16:49:04 +0200'
  content: Mała uwaga - w tym &lt;abbr&gt; od FCGI masz href zamiast title i się nie
    wyświetla co to właściwie jest ;-)
---
<p>Ostatnie dni stanowiły dla mnie nieprzerwane pasmo imprez&hellip; wróć! Nieprzerwane pasmo pracy z kodem. A właściwie to jedno i drugie, Python jest tak wygodny, że nawet przy kilku projektach pozostaje czas na imprezy.</p>

<p>O Pythonie za chwilę, najpierw jednak o <abbr title="PHP Hypertext Preprocessor">PHP</abbr>. Wróciło <a href="http://10przykazan.com/">10przykazan</a>, po 9 dniach awarii. Długa przerwa, ale głównym problemem był dostęp do internetu. Trzeba wam bowiem wiedzieć, że 1. <del>marca</del> <ins>kwietnia</ins> (więcej kawy) przeprowadziłem się do nowego mieszkania i do dziś nie udało się nam podpisać umowy z żadnym dostawcą. Ale nie o tym chciałem pisać, okazało się, że przyczyną problemu jest <a href="http://bugs.php.net/bug.php?id=41293"><abbr>PHP</abbr> w wersji 5.2.2, które psuje biblioteki <abbr title="Remote Procedure Call">RPC</abbr></a>.</p>

<p>W wolnym czasie zacząłem też eksperymentować z własną implementacją niesławnego pakietu <a href="http://cr.yp.to/daemontools.html">daemontools</a>. O działalności <a href="http://cr.yp.to/djb.html">djb</a> słyszeli chyba wszyscy, a niezorientowanych pozostawię na pastwę Google, bo i szukać nie trzeba długo.</p>

<p>W <a href="http://itsltd.eu/">ITS Ltd.</a> używamy daemontools do zarządzania usługami <abbr title="Fast Common Gateway Interface">FCGI</abbr>. Wszystko byłoby dobrze, gdyby nie fakt, że od czasu do czasu (po zmianie kodu na serwerze) trzeba taką usługę zrestartować, a czasem i zatrzymać na dłużej. Cóż, daemontools pozwala to zrobić tylko rootowi z poziomu konsoli.</p>

<p>Pakiet wygląda na martwy, za trzy tygodnie kończy się jego <a href="http://cr.yp.to/distributors.html">licencja redystrybucji</a>. Mój nowy projekt poboczny to próba odtworzenia schematu działania oryginału za pomocą odrobiny Pythona. Przy okazji dodałem nieco interfejsów <a href="http://www.freedesktop.org/Software/dbus">D-Bus</a>. Zainteresowanych wczesnymi testami zapraszam na <a href="http://code.google.com/p/daemontools-ng/">stronę daemontools-ng</a>.</p>
