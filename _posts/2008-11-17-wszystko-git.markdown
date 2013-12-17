---
layout: post
status: publish
published: true
title: Wszystko git
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 494
wordpress_url: http://room-303.com/blog/?p=494
date: 2008-11-17 17:28:59.000000000 +01:00
categories:
- code
tags: []
comments:
- id: 22913
  author: CoSTa
  author_url: http://costa.kofeina.net
  date: '2008-11-17 19:56:58 +0100'
  date_gmt: '2008-11-17 18:56:58 +0100'
  content: Patrys, z tego wszystkiego mnie zainteresowały wzmianki o LBP :). Warte
    wydanych na to pieniędzy?
- id: 22915
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2008-11-17 21:14:07 +0100'
  date_gmt: '2008-11-17 20:14:07 +0100'
  content: Pewnie, że warte. Chociaż ja nic nie wydałem, bo moja lepsza podarowała
    mi LBP na urodziny (oboje się śliniliśmy do tej gry jeszcze jak grałem w wersję
    beta).
- id: 22919
  author: krzysio
  author_url: ''
  date: '2008-11-18 00:25:17 +0100'
  date_gmt: '2008-11-17 23:25:17 +0100'
  content: "git rządzi, nawet gdy cała reszta firmy pracuje na SVN. Przykład z życia
    wzięty, raz czy dwa w tygodniu tak bywa:\r\nPrzybiega ktoś z bugiem do naprawienia
    w projekcie który mam aktualnie rozdłubany maksymalnie. Zakładając, że nie zrobiłem
    sobie (lokalnego) brancha wcześniej mogę na chwilę odłoźyć sobie zmiany na bok
    (git stash), zrobić up z svn (git svn rebase), poprawić buga, wrzucić do svn (git
    commit; git svn dcommit) i wrócić do swojego burdeliku (git stash pop).\r\n\r\nGdy
    używałem svn było niby tak samo, ale jednak inaczej:\r\nsvn diff &gt; ~/tmp-diff;
    svn up; zmiany; svn commit; patch -p0 &lt; ~/tmp-diff. Efekt ten sam, ale o ile
    wygodniej robi się to gitem ;)"
- id: 22920
  author: jpc
  author_url: http://jpc.jogger.pl
  date: '2008-11-18 01:23:43 +0100'
  date_gmt: '2008-11-18 00:23:43 +0100'
  content: "svn vs. git. ok.\r\na co z git vs. np. mercurial?\r\n\r\nPS. Ja rozumiem,
    że ewangelizacja ciemnej masy, ale co z tymi co się oświecili już wcześniej tyle,
    że na inny kolor? ;-)"
- id: 22921
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2008-11-18 01:29:10 +0100'
  date_gmt: '2008-11-18 00:29:10 +0100'
  content: "jpc:\r\n\r\nKolor nie gra roli tak długo, jak długo narzędzia są łatwo
    dostępne - tzn. da się je zbudować w obcym systemie bez roota i da się je odpalić
    pod Windows, Linuksem i OS X :)"
- id: 22926
  author: jpc
  author_url: http://jpc.jogger.pl
  date: '2008-11-18 03:56:45 +0100'
  date_gmt: '2008-11-18 02:56:45 +0100'
  content: Ładnie tak naśmiewać się z darcs-a i Haskella? ;]
- id: 22930
  author: GDR!
  author_url: ''
  date: '2008-11-18 07:24:53 +0100'
  date_gmt: '2008-11-18 06:24:53 +0100'
  content: Niestety wiem o którym z projektów mówisz, i żałuję że nie wpadłem na ten
    pomysł kiedy męczyłem się z nim wcześniej.
- id: 22933
  author: Patrys
  author_url: http://room-303.com/
  date: '2008-11-18 10:08:39 +0100'
  date_gmt: '2008-11-18 09:08:39 +0100'
  content: "GDR:\r\n\r\nNie ty jeden, połowę znajomych tam w komentarzach znalazłem
    ;)"
- id: 22979
  author: offtza
  author_url: ''
  date: '2008-11-20 10:15:58 +0100'
  date_gmt: '2008-11-20 09:15:58 +0100'
  content: "\"[...] Wyobraźcie sobie, że dostajecie serwis w spadku po tragicznie
    znikniętym deweloperze (tragicznie wykonal pracę i zniknął). Kilka giga śmiecia
    — pliki pe-ha-pe wymieszane z szablonami, grafiką, plikami do pobrania. [...]\"\r\n\r\nŁa!
    Dlaczego przypominasz mi stare dzieje?! Łaaaa!"
---
<p>Ha, jeszcze żyję! Nie miałem ostatnio zbyt dużo czasu na prowadzenie bloga. Powodów było wiele &mdash; Little Big Planet, pomoc przy serwisie <a href="http://www.e-lady.pl/">e-Lady</a>, Little Big Planet, duży projekt dla <a href="http://zurich.com/main/home/welcome.htm">Zurichu</a> i impreza z okazji mojego upgrade'u do wersji 0.26. Chyba dobrze, bo parzyste wydania są stabilne.</p>

<p>Skoro jestem już staruchem, to pozwólcie, że udzielę wam rady, przez którą przemawiają dziesięciolecia doświadczenia. <strong>Nauczcie się używać Gita, warto.</strong> Zwłaszcza, jeśli w tym momencie pomyśleliście sobie <q>a po co &mdash; znam ci ja wszak Subversion?</q></p>

<p>Ciężko byłoby mi wymienić, ile razy git uratował moje szanowne cztery litery w ciągu tylko tego roku. Najprostszy przykład mam jednak na wyciągnięcie ręki. Wyobraźcie sobie, że dostajecie serwis w spadku po tragicznie znikniętym deweloperze (tragicznie wykonal pracę i zniknął). Kilka giga śmiecia &mdash; pliki pe-ha-pe wymieszane z szablonami, grafiką, plikami do pobrania.</p>

<p>Cały ten bajzel bez ładu i składu poupychany w dziesiątki katalogów o dźwięcznych nazwach: <q>includes</q>, <q>modules</q>, <q>files</q>, <q>pliki</q>, <q>integracja.</q> Kopiować przez <abbr title="Secure Shell">SSH</abbr> nie ma sensu, bo życia by nie starczyło, wrzucić całość do kontroli wersji? Narzędzie importu SVN ubiłem po godzinie, gdy nadal czekałem na prośbę o komentarz do zmian.</p>

<p>Skończyło się na lokalnej kompilacji Gita, zainicjowaniu repozytorium w katalogu z projektem i dodaniu tylko sensownych plików (html, php, css). Całość trwała w sumie z pięć minut i świat znów stał się kolorowy (dłuższa styczność z <abbr title="PHP Hypertext Preprocessor">PHP</abbr> oprócz kolorowych wizji może być również powodem halucynacji, przed użyciem skontaktuj się z lekarzem lub farmaceutą).</p>

<p>Jeśli więc i ty trafisz kiedyś na projekt, który jest wzorcową implementacją specyfikacji z The Daily WTF i nigdy nie widział systemu kontroli wersji, przypomnij sobie o Gicie i uczyń świat lepszym miejscem dla naszych dzieci.</p>
