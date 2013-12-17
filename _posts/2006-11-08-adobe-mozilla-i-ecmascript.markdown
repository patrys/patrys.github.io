---
layout: post
status: publish
published: true
title: Adobe, Mozilla i ECMAScript
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 306
wordpress_url: http://www.room-303.com/blog/2006/11/08/adobe-mozilla-i-ecmascript/
date: 2006-11-08 23:25:25.000000000 +01:00
categories:
- web
- software
tags: []
comments:
- id: 5150
  author: mcv
  author_url: http://mcv.jogger.pl
  date: '2006-11-08 23:40:33 +0100'
  date_gmt: '2006-11-08 22:40:33 +0100'
  content: Ale będzie wypas… To może i sam Fx (interfejs) zacznie się „rysować” zdeczko
    szybciej? ;-)
- id: 5151
  author: jpc
  author_url: http://jpc.jogger.pl
  date: '2006-11-09 00:45:42 +0100'
  date_gmt: '2006-11-08 23:45:42 +0100'
  content: Prawdopodobnie powinien, aczkolwiek tu jeszcze potrzeba rozwoju Cairo do
    pełni sukcesu. :)
- id: 5157
  author: zdzichu
  author_url: http:///zdzichubg.jogger.pl
  date: '2006-11-09 19:49:01 +0100'
  date_gmt: '2006-11-09 18:49:01 +0100'
  content: "Raczej nieprędko, w tym tempie rozwoju co ma Firefox teraz to zobaczymy
    to w okolicach wersji 5.0.\r\nAle do tej pory mam nadzieje wydzielą już Xulrunnera
    i Firefox będzie po prostu jednym z interfejsów do Gecko. A szybki JS będzie w
    każdym Kazahase czy Epiphany."
- id: 5159
  author: zdzichu
  author_url: http:///zdzichubg.jogger.pl
  date: '2006-11-09 20:54:29 +0100'
  date_gmt: '2006-11-09 19:54:29 +0100'
  content: "O, z dzisiejszego LWN:\r\n,,It will take a while before Tamarin is incorporated
    into Firefox, the current plan is for a release in 2008.''"
---
<p>Dla tych, którzy przegapili, Adobe <a href="http://www.adobe.com/aboutadobe/pressroom/pressreleases/200611/110706Mozilla.html">przekazało</a> fundacji Mozilla swój najnowszy silnik ActionScript, zbudowany dla Flash Playera 9.</p>

<p>Co to oznacza? Nie, w Firefoksie 3.0 nie będzie wbudowanego Flasha. W niezdefiniowanej bliżej przyszłości pojawi się za to nowy silnik JavaScript. Jako że oba języki oparte są na tym samym standardzie, wirtualna maszyna JavaScript może zostać z powodzeniem zastąpiona wydajnym silnikiem produkcji Adobe. Ichnia implementacja maszyny wirtualnej ma jedną szczególnie interesującą zaletę — kompilator <q>Just In Time,</q> który w locie kompiluje język skryptowy do postaci kodu natywnego dla procesora, na którym jest uruchomiony silnik.</p>

<p>W skrócie: możemy oczekiwać, że w ciągu najbliższego roku pojawi się Firefox z najwydajniejszą na rynku przeglądarek implementacją JavaScriptu.</p>
