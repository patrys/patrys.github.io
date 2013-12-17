---
layout: post
status: publish
published: true
title: Python + libchart = ładne wykresy
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 380
wordpress_url: http://room-303.com/blog/2007/06/06/python-libchart-ladne-wykresy/
date: 2007-06-06 12:36:01.000000000 +02:00
categories:
- software
- code
tags: []
comments:
- id: 8038
  author: kodz
  author_url: ''
  date: '2007-06-06 12:44:40 +0200'
  date_gmt: '2007-06-06 11:44:40 +0200'
  content: sprawdz xml/swf charts jeszcze.
- id: 8039
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-06-06 12:47:32 +0200'
  date_gmt: '2007-06-06 11:47:32 +0200'
  content: Nie zamierzam uzywać Flasha do wykresów i tłumaczyć klientom, dlaczego
    na którymś komputerze się nie pokazują (flashblock / adblock / brak flasha). Poza
    tym, wykresów flashowych nie osadzę sobie z poziomu Pythona w PDF.
- id: 8040
  author: Crash
  author_url: http://crash.jogger.pl
  date: '2007-06-06 13:14:15 +0200'
  date_gmt: '2007-06-06 12:14:15 +0200'
  content: Jakby były bardziej webdwazerowe jeszcze, lol ;D
- id: 8041
  author: sit0
  author_url: http://sit0.com
  date: '2007-06-06 13:37:14 +0200'
  date_gmt: '2007-06-06 12:37:14 +0200'
  content: "@Patrys: ty nie zamierzasz, ale ostatecznie na stronie i tak wyląduje
    pewnie xml/swf chart z maani.us (bo ma antyaliasing i się animuje, a to podoba
    sie end-userom ;) - twoja biblioteka przyda się(*) do wyczesanych wydruków, gdzie
    nie da się osadzić flasha, zresztą gadaliśmy o tym wczoraj. Co prawda wciąż nie
    wiem, kto potrzebowałby w tym projekcie drukowanych wykresów (a czy w ogóle miałyby
    sens to inna kwestia), ale i tak dostarczamy klientom pdf. Zważywszy masową klientelę,
    friki które by to chciały się znajdą.\r\nPogadaj z Lukiem o google gears (wprowadziłem
    go w temat wstępnie), jeśli uda nam się to przepchnąć przed release 1.0 to będzie
    przełom w aplikacjach tego typu ;)\r\n\r\n(*) - odpuście sobie polemikę, to jest
    wypowiedź związana z dość napiętym projektem który realizujemy."
- id: 8042
  author: byte
  author_url: http://byte.livenet.pl
  date: '2007-06-06 14:05:53 +0200'
  date_gmt: '2007-06-06 13:05:53 +0200'
  content: A tak zagaję przy okazji... 10p ma jakąś awarię od tygodnia?
- id: 8043
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-06-06 14:08:30 +0200'
  date_gmt: '2007-06-06 13:08:30 +0200'
  content: "byte:\r\n\r\nMa awarię, wygląda na to, że jeden skrypt PHP zdycha bez
    żadnego komunikatu w momencie wywoływania XML RPC. Ja za to od 1. marca nie mam
    dostępu do internetu w domu."
- id: 8044
  author: Lukasz Horodecki
  author_url: http://horodecki.net
  date: '2007-06-06 14:29:40 +0200'
  date_gmt: '2007-06-06 13:29:40 +0200'
  content: No prawie ładne, tylko żeby takie poszarpane te wykresy nie były...
- id: 8045
  author: jpc
  author_url: http://jpc.jogger.pl
  date: '2007-06-06 14:43:46 +0200'
  date_gmt: '2007-06-06 13:43:46 +0200'
  content: Właśnie, trochę AA brakuje. Może pycairo zamiast PIL?
- id: 8046
  author: Sebastian
  author_url: ''
  date: '2007-06-06 18:49:33 +0200'
  date_gmt: '2007-06-06 17:49:33 +0200'
  content: A tak w ogóle to dlaczego zdecydowaliście sie na Pythona + Django, a nie
    np na Railsy?
- id: 8047
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-06-06 18:53:48 +0200'
  date_gmt: '2007-06-06 17:53:48 +0200'
  content: "Sebastian:\r\n\r\nZ wszystkich języków, jakie znam, Python leży mi najbardziej
    (chociaż czasem zdarza mi się użyć podświadomie składni Rubiego i potem się dziwię,
    że nie działa)."
- id: 8048
  author: Sebastian
  author_url: ''
  date: '2007-06-06 20:00:51 +0200'
  date_gmt: '2007-06-06 19:00:51 +0200'
  content: "Rozumiem, tak pytam bo właśnie szukam czegoś czym mógłym zastąpić php
    \r\ni waham sie właśnie miedzy ruby (railsy) i pythonem (djanogo). Wiem ze Ty
    kiedyś robiłeś w php. Jakieś obserwacje po przejsciu na pythona?\r\nFaktycznie
    dużo lepiej/szybciej się pisze?"
- id: 8049
  author: x
  author_url: ''
  date: '2007-06-06 21:19:56 +0200'
  date_gmt: '2007-06-06 20:19:56 +0200'
  content: http://www.mps.mpg.de/dislin/
- id: 8056
  author: jpc
  author_url: http://jpc.jogger.pl
  date: '2007-06-07 13:15:49 +0200'
  date_gmt: '2007-06-07 12:15:49 +0200'
  content: Ale DISLIN jest paskudny. ;]
- id: 8057
  author: sprae
  author_url: http://sprae.openid.pl/
  date: '2007-06-07 14:38:48 +0200'
  date_gmt: '2007-06-07 13:38:48 +0200'
  content: Ja też optowałbym za cairo, szczególnie że takie rozwiązania wyglądają
    tam estetyczniej dzieki aa.
- id: 8059
  author: Brut[all]
  author_url: ''
  date: '2007-06-08 12:31:55 +0200'
  date_gmt: '2007-06-08 11:31:55 +0200'
  content: W PIL'u można to wygladzić, tworząc początkową grafikę o większych rozmiarach,
    a potem resamplując ją z AA do wyjściowej. Ale takie rozmiarowanie w PIL'u zżera
    trochę mocy.
- id: 8062
  author: jpc
  author_url: http://jpc.jogger.pl
  date: '2007-06-08 21:53:29 +0200'
  date_gmt: '2007-06-08 20:53:29 +0200'
  content: 'Brut[all]: Zdaje się też, że ta metoda nie zadziała najlepiej dla tekstu
    (ale ok dla grafiki), więc trzeba by opisy dokładać po skalowaniu.'
- id: 8065
  author: Brut[all]
  author_url: ''
  date: '2007-06-11 00:49:06 +0200'
  date_gmt: '2007-06-10 23:49:06 +0200'
  content: "\")...) więc trzeba by opisy dokładać po skalowaniu.\"\r\n\r\nCo chyba
    nie jest wielkim problemem.\r\n\r\nOczywiście nie jest też chyba dla nikogo żadną
    tajemnicą, że to rozwiązanie bardzo na około i generalnie do dupy :-)"
- id: 8068
  author: jpc
  author_url: http://jpc.jogger.pl
  date: '2007-06-11 10:49:38 +0200'
  date_gmt: '2007-06-11 09:49:38 +0200'
  content: Eeee... AA poprzez oversampling jest całkiem niezłym pomysłem i dla grafiki
    działą dość dobrze. :)
- id: 8072
  author: L Grad
  author_url: ''
  date: '2007-06-12 10:40:04 +0200'
  date_gmt: '2007-06-12 09:40:04 +0200'
  content: Mi sie sama idea podoba. Ktos kiedys powiedzial, ze Rzym (czy Krakow jak
    kto woli) wasn't built in one day. Stad zdecydowanie za wczesnie by porownywac
    to z czymkolwiek, jednak... ilosc projektow w jakich potrzebna jest takowa biblioteka
    moze przyczynic sie do jej rozwoju :-)
- id: 8156
  author: 'Python: libchart 0.0.3 at Room 303'
  author_url: http://room-303.com/blog/2007/06/21/python-libchart-003/
  date: '2007-06-21 20:42:35 +0200'
  date_gmt: '2007-06-21 19:42:35 +0200'
  content: '[...] pojawiła się obiecana potrzeba i tak powstała trzecia wersja biblioteki
    do generowania wykresów. Tym razem nie wymaga PIL i [...]'
---
<p>Długo szukaliśmy sensownej biblioteki, która pozwoli nam narysować prosty wykres kołowy, nie zajmuje pół mega i w trakcie działania nie uruchamia zewnętrznego konwertera PostScriptu. Idealny kandydat powinien do tego mieć sensowne <abbr title="Application Programming Interface">API</abbr>.</p>

<p>W końcu znudziło mi się szukanie i siadłem do klawiatury. Przypomniałem sobie o świetnej bibliotece <a href="http://naku.dohcrew.com/libchart/pages/introduction/">libchart</a>, której używamy w <a href="http://wego.pl/">Wego CMS</a> i postanowiłem ją odtworzyć w Pythonie.</p>

<p class="strip"><a href="http://www.flickr.com/photos/patrys/533108759/" title="Photo Sharing"><img src="http://farm2.static.flickr.com/1256/533108759_51b59c469b.jpg" width="500" height="300" alt="Charting in python with libchart" /></a></p>

<p>Powyżej widać efekt 3 godzin mojej pracy. Kod do działania wymaga <a href="http://www.pythonware.com/products/pil/">Python Imaging Library</a> i jest objęty licencją <a href="http://www.gnu.org/licenses/lgpl.html">LGPL</a>.</p>

<p>Pobierz <a href="http://code.google.com/p/python-libchart/">ze strony projektu</a> i podziękuj firmie <a href="http://itsltd.eu/">ITS Ltd.</a> za jego sfinansowanie ;). Wersja 0.0.1 oferuje tylko wykresy kołowe, pozostałe typy pojawią się w miarę potrzeb naszych klientów.</p>
