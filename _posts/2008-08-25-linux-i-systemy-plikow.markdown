---
layout: post
status: publish
published: true
title: Linux i systemy plików
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 460
wordpress_url: http://room-303.com/blog/?p=460
date: 2008-08-25 16:45:43.000000000 +02:00
categories:
- linux
tags: []
comments:
- id: 21143
  author: opi
  author_url: http://bronikowski.com
  date: '2008-08-25 16:52:31 +0200'
  date_gmt: '2008-08-25 15:52:31 +0200'
  content: To sztuczka dla wszystkich systemów plików, czy tylko tych z journalingiem?
- id: 21144
  author: Patrys
  author_url: http://room-303.com/
  date: '2008-08-25 17:15:31 +0200'
  date_gmt: '2008-08-25 16:15:31 +0200'
  content: "Dla wszystkich z fizycznymi urządzeniami (dla takiego procfs nie ma sensu).\r\n\r\nrelatime
    powoduje, że atime jest zapisywany tylko jeśli jest starszy od ctime albo mtime.
    noatime wyłącza go całkiem. atime to taka durnota odziedziczona po Uniksie i w
    implementacji jest jeszcze głupszy, niż windowsowy atrybut \"archive\". Powoduje
    mianowicie zapis danych przy odczycie (taki wierszyk)."
- id: 21145
  author: mt3o
  author_url: ''
  date: '2008-08-25 18:18:34 +0200'
  date_gmt: '2008-08-25 17:18:34 +0200'
  content: "Także dla vfat i ntfs? O swap się już pytać nie będę ;)\r\natime, mtime
    i ctime to są daty dostępu, modyfikacji i utworzenia pliku, tak?"
- id: 21146
  author: Patrys
  author_url: http://room-303.com/
  date: '2008-08-25 18:36:14 +0200'
  date_gmt: '2008-08-25 17:36:14 +0200'
  content: "mt3o:\r\n\r\nTak, atime to czas ostatniego dostępu i tak, dotyczy to też
    systemów vfat. W przypadku ntfs nie wiem, dwa lata temu ntfs pod Linuksem nie
    obsługiwał w ogóle modyfikacji czasów w atrybutach plików. W przypadku vfat atime,
    mtime i ctime zapisywane są w tym samym polu (vfat nie powstał na potrzeby Uniksa
    i ma tylko jeden atrybut czasu).\r\n\r\nSwap nie jest systemem plików sensu stricte,
    bo nie operuje na plikach :)"
- id: 21156
  author: wojtosz
  author_url: http://www.blaszkowski.com
  date: '2008-08-26 18:27:32 +0200'
  date_gmt: '2008-08-26 17:27:32 +0200'
  content: 'jeśli już o systemach plików mowa: ext4 testował ktoś ?'
---
<p>Glen (Elan Ruusamäe z PLD) spytał mnie dziś o system plików, jaki polecałbym na serwer pocztowy. Chodziło o jego serwer, na którym zdechł był właśnie reiserfs. Zaproponowałem ext3 z journalingiem albo xfs ze zmniejszonym rozmiarem bloku (poczta = dużo małych plików).</p>

<p>Przy okazji przypomniało mi się, o czym miałem tu napisać dawno temu. Początkowo dla własnej pamięci, ale jakoś uleciało mi to z głowy. Spóźnione o jakieś dwa lata, bo mniej więcej dwa lata temu przypadkiem odkryłem powód powolności jednego z serwerów.</p>

<blockquote><p><em>Zawsze</em> (zawsze!) po instalacji systemu należy upewnić się, że <em>wszystkie fizyczne systemy plików</em> montowane są z parametrami <strong><code>noatime,nodiratime</code></strong> albo przynajmniej <code>relatime</code>. Dla xfs dodatkowo pomoże <code>logbufs=8</code>.</p></blockquote>

<p>Ku pamięci i takie tam. Wydrukować i oprawić w ramki albo więcej nie dziwić się, kiedy maszyna z minimalnym ruchem http doświadcza load na poziomie 5.</p>

<p><strong>Update:</strong> okazuje się, że w sierpniu zeszłego roku <a href="http://kerneltrap.org/node/14148">podobny wątek</a> pojawił się na kerneltrapie. Upewniłem się też (wczoraj zastanawialiśmy się nad tym z qwiatem w drodze na piwo, więc z dala od kerneli), że <code>noatime</code> dotyczy zarówno plików, jak katalogów, przez co podawanie dodatkowo <code>nodiratime</code> jest zbędne. Czas się odzwyczaić.</p>
