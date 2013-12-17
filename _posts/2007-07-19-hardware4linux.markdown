---
layout: post
status: publish
published: true
title: Hardware4Linux
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 390
wordpress_url: http://room-303.com/blog/2007/07/19/hardware4linux/
date: 2007-07-19 19:32:24.000000000 +02:00
categories:
- linux
- software
tags: []
comments:
- id: 8250
  author: University Update - Linux - Hardware4Linux
  author_url: http://www.universityupdate.com/Technology/linux/3979486.aspx
  date: '2007-07-19 20:50:04 +0200'
  date_gmt: '2007-07-19 19:50:04 +0200'
  content: '[...]                       Link to Article                linux Hardware4Linux
    &#187;  Posted at  Room 303 on Thursday, July 19, 2007   Jest [...]'
- id: 8251
  author: nrm
  author_url: http://normanos.com
  date: '2007-07-19 22:10:00 +0200'
  date_gmt: '2007-07-19 21:10:00 +0200'
  content: dzięki za info, dokonałem dobrego uczynku :D chwali sie, ze sajt jest na
    django hehe, szkoda tylko, że po uploadzie nie było pytań o wszystkie wykryte
    komponenty bo bym dopisał, że kamerka w moim asusie nie działa i prawdopodobnie
    nikomu nie działa pod linuksem :(
- id: 8252
  author: Stef
  author_url: http://jabba.pl/stef
  date: '2007-07-19 23:38:48 +0200'
  date_gmt: '2007-07-19 22:38:48 +0200'
  content: Fedora/Red Hat ma swojego <a href="http://smolt.fedoraproject.org/" rel="nofollow">Smolt</a>a,
    w dodatku <a href="https://www.redhat.com/archives/fedora-announce-list/2007-July/msg00007.html"
    rel="nofollow">chcą się rozwinąć w coś większego</a>, w każdym razie również przydatne.
- id: 8253
  author: Wojtosz
  author_url: http://www.blaszkowski.com
  date: '2007-07-20 07:35:20 +0200'
  date_gmt: '2007-07-20 06:35:20 +0200'
  content: "@nrm\r\nna chwilę obecną mam A3E 5018H, powerd by Ac - u mnie również
    problem z kamerą. VIP <a href=\"http://coffee3.org/2007/02/02/syntek-webcam-linux-05e10501/\"
    rel=\"nofollow\">chwalił się</a> działającą kamerą, ale inny model kamery i asusa.\r\n\r\nNiniejszym
    sugeruję, aby w/w kolega poczuł się w obowiązku złożenia swojego zeznania sprzętowego
    w możliwie najkrótszym terminie, o ile jeszcze czynności tej nie wykonał :)"
- id: 8254
  author: byte
  author_url: http://bytowisko.pl
  date: '2007-07-20 10:55:47 +0200'
  date_gmt: '2007-07-20 09:55:47 +0200'
  content: Canonical również prowadzi swoją bazę sprzętu kompatybilnego (lub nie)
    z Linuksem (odpowiednie narzędzie do wysyłania raportów jest dostępne od ręki
    po instalacji Ubuntu). Kurcze, wystarczyłoby gdyby po prostu wymieniono się bazami
    danych.
- id: 8255
  author: S.
  author_url: ''
  date: '2007-07-20 23:22:46 +0200'
  date_gmt: '2007-07-20 22:22:46 +0200'
  content: Taka uwaga dotycząca interpunkcji. Przed 'lub' nie stawia się przecinka.
- id: 8257
  author: Andrzej Dopierała
  author_url: http://andrzej.dopierala.name/
  date: '2007-07-22 11:15:45 +0200'
  date_gmt: '2007-07-22 10:15:45 +0200'
  content: "ee... idea fajna, ino... po rejestracji przysłał mi maila z aktywacją,
    zaktywowałem.. i uświadomiłem sobie że nie pamiętam hasła :(\r\n\r\nA w systemie
    oczywiście brak opcji przypomnienia/resetu hasła :/"
- id: 8260
  author: Maciej Delmanowski
  author_url: http://harnir.net/
  date: '2007-07-23 22:48:06 +0200'
  date_gmt: '2007-07-23 21:48:06 +0200'
  content: Trzeba będzie dodać swojego laptopa :)
- id: 8280
  author: Hawk
  author_url: ''
  date: '2007-07-26 08:11:17 +0200'
  date_gmt: '2007-07-26 07:11:17 +0200'
  content: "Szkoda, że nie używa usbutils do gromadzenia info o podpiętym sprzęcie
    USB. Mogło by również korzystać z hdparm/sdparm/smartmontools czy czegoś tam do
    zbierania informacji o dyskach. Jak już gromadzić info to kompleksowo, a obecnie
    jest IMO po łebkach. Poza tym wiem z doświadczenia, że takie dmidecode _bardzo_
    często daje wyniki tak sobie pokrywające się z rzeczywistością.\r\n\r\nBTW: wolę
    swoją bazę sprzętu, niestety jest niepubliczna :("
---
<p>Jest sobie taki skromny projekt, którego jedynym zadaniem jest zbieranie informacji o twoich komputerach. <a href="http://hardware4linux.info/">Hardware4Linux</a>, bo o nim mowa, to centralna baza informacji o kompatybilności przeróżnego sprzętu z Linuksem.</p>

<p>W tej chwili jest jeszcze na etapie gromadzenia informacji, ale można sobie wyobrazić, że już niedługo może stać się nieocenionym źródłem informacji dla takich projektów, jak <abbr title="Hardware Abstraction Layer">HAL</abbr>, czy poszczególne dystrybucje.</p>

<p>Jeśli używasz Linuksa i masz chwilę czasu, to zachęcam do zbudowania sobie pakietu <code>hwreport</code> i wysłania wyników jego działania na stronę, gdzie następnie można dodatkowo ocenić i skomentować najważniejsze (i potencjalnie sprawiające najwięcej kłopotów) składniki maszyny.</p>

<p>Cała procedura wygląda tak:</p>

<ol>
<li>Budujemy (lub pobieramy) pakiet <code>hwreport</code></li>
<li>Z prawami roota wykonujemy <code>hwreport /tmp/report</code></li>
<li>Zakładamy konto w serwisie</li>
<li>Uploadujemy plik <code>/tmp/report.tar.bz2</code></li>
<li>Oceniamy wybrane składniki</li>
<li>Cieszymy się z dobrego uczynku i liczymy na sławę, kobiety lub wygraną w totka</li>
</ol>
