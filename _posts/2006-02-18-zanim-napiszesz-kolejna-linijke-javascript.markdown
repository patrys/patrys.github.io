---
layout: post
status: publish
published: true
title: Zanim napiszesz kolejną linijkę JavaScript
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 234
wordpress_url: http://www.room-303.com/blog/2006/02/18/zanim-napiszesz-kolejna-linijke-javascript/
date: 2006-02-18 17:19:52.000000000 +01:00
categories:
- web
- software
- code
tags: []
comments:
- id: 3375
  author: mroq
  author_url: http://mroq.jogger.pl
  date: '2006-02-18 19:36:35 +0100'
  date_gmt: '2006-02-18 18:36:35 +0100'
  content: "<blockquote>\r\nNie próbuj nawet wykrywać przeglądarek. Zamiast tego wykrywaj
    obecnośc konkretnych funkcji.\r\n</blockquote>\r\n\r\nPewnie mam złe nawyki, ale
    czy nie lepiej wykrywać obiekty?"
- id: 3376
  author: bellois
  author_url: http://jabba.pl/bellois
  date: '2006-02-18 19:48:30 +0100'
  date_gmt: '2006-02-18 18:48:30 +0100'
  content: Ciekawe. Kiedyś trochę interesowałem się JavaScriptem. Co dziś warto przeczytać?
    Gdzie zajrzeć? Materiału jest dużo i trudno oddzielić wartościowy od bezwartościowego?
    Co byś polecił?
- id: 3377
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-02-18 19:54:14 +0100'
  date_gmt: '2006-02-18 18:54:14 +0100'
  content: "mroq:\r\n\r\nNa to samo wychodzi - czasem potrzebna ci funkcja, czasem
    obiekt, czasem metoda. Nigdy konkretna przeglądarka.\r\n\r\nbellois:\r\n\r\nPoleciłbym
    <a href=\"http://domscripting.com/book/\" rel=\"nofollow\">DOM Scripting</a>."
- id: 3378
  author: bellois
  author_url: http://jabba.pl/bellois
  date: '2006-02-18 20:26:46 +0100'
  date_gmt: '2006-02-18 19:26:46 +0100'
  content: Hmmm... a z materiałów darmowych? :-)
- id: 3379
  author: Riddle
  author_url: http://riddle.jogger.pl
  date: '2006-02-19 01:30:41 +0100'
  date_gmt: '2006-02-19 00:30:41 +0100'
  content: Tylko blogi.
- id: 3380
  author: bellois
  author_url: http://jabba.pl/bellois
  date: '2006-02-19 10:20:58 +0100'
  date_gmt: '2006-02-19 09:20:58 +0100'
  content: 'Riddle: masz na myśli jakieś konkretne?'
- id: 3381
  author: marcoos
  author_url: http://blog.marcoos.org/
  date: '2006-02-19 11:56:57 +0100'
  date_gmt: '2006-02-19 10:56:57 +0100'
  content: Behaviour - genialne. :)
- id: 3382
  author: blue
  author_url: ''
  date: '2006-02-19 15:41:18 +0100'
  date_gmt: '2006-02-19 14:41:18 +0100'
  content: "Coś mi tu nie pasuje:\r\n<blockquote cite=\"Patrys\">Pisząc proste onclick=\"return
    foo();\" oszczędzisz sobie kłopotu z propagacją zdarzeń, a mi oszczędzisz kilobajta
    kodu do pobrania.</blockquote><blockquote>\r\n</blockquote><blockquote cite=\"Patrys\">Jeśli
    chcesz to zrobić dobrze, użyj biblioteki takiej jak Behaviour.</blockquote><blockquote>\r\nPomijając
    fakt, iż uważam, że korzystanie z bibliotek, to w przypadku js jakaś pomyłka (cenny
    transfer marnowany na kod, z którego, w najbardziej optymalnym wypadku, potrzebna
    Ci będzie połowa), przeczysz sam sobie. To w końcu oszczędność kb, czy obszerne
    bilbioteki?</blockquote>"
- id: 3383
  author: blue
  author_url: ''
  date: '2006-02-19 15:46:22 +0100'
  date_gmt: '2006-02-19 14:46:22 +0100'
  content: Przepraszam, ale coś mi nie wyszło przy pisaniu komentarza :| Ostatni akapit
    nie powinien być cytatem.
- id: 3386
  author: jpc
  author_url: http://jpc.jogger.pl
  date: '2006-02-19 20:44:36 +0100'
  date_gmt: '2006-02-19 19:44:36 +0100'
  content: "copy and paste to często najlepsze reuse jakie można sobie wyobrazić...\r\n\r\nCzęsto
    nie warto się męczyć nad tworzeniem wyższej abstrakcji, bo to strata czasu, a
    i tak nie mamy szans, źeby dobrze uchwycić sedno problemu póki nie napiszemy podobnej
    funkcji 4 raz. A wtedy wyodrębnienie tego kodu stanie się oczywistym rozwiązaniem
    bez potrzeby nadmiernej ewangelizacji. ;]"
- id: 3388
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-02-19 23:14:14 +0100'
  date_gmt: '2006-02-19 22:14:14 +0100'
  content: "blue:\r\n\r\nJa się zajmuję budowaniem nie tylko stron, ale i aplikacji
    internetowych. W przypadku tych ostatnich spora część znajduje się w warstwie
    JS, więc nie ma strachu, że połowa dołączonego kodu jest bezużyteczna.\r\n\r\nCo
    do oszczędzania transferu -- przeleć się po stronach. Często na dole dokumentu
    jest wynalazek w stylu:\r\n\r\n<pre>window.onload = [...]</pre>\r\n\r\nDokładnie
    o to mi chodziło w pierszym cytowanym punkcie."
- id: 14717
  author: Aldona
  author_url: ''
  date: '2008-01-31 12:06:12 +0100'
  date_gmt: '2008-01-31 11:06:12 +0100'
  content: "Czesc wszystkim!\r\nChce sie nauczyc porzadnie JavaScript, przegladnelam
    kilka ksiazek, ale   nie wiem, ktora jest najlepsza, moglibyscie cos zarekomendowac.
    Z matematyka nie mam klopotow, ale JavaScript nie znam prawie wcale.\r\nDzieki!"
---
<p>Nie próbuj nawet wykrywać przeglądarek. Zamiast tego wykrywaj obecność konkretnych funkcji. Dlaczego? Pełna lista przeglądarek byłaby kilkanaście razy dłuższa niż cały twój skrypt i przestanie być aktualna w przeciągu kilku dni. Jeśli obetniesz ją do kilku najpopularniejszych, to odcinasz się od tych, które działałyby poprawnie, ale nigdy o nich nie słyszałeś. Sieć polega na zgodności.</p>

<p>Poznaj drzewo <abbr title="Document Object Model">DOM</abbr> i naucz się z niego korzystać. <code>document.write()</code> porównać można do malowania kodu farbą z liści. Na ścianach jaskiń.</p>

<p>Zanim skopiujesz i wkleisz jakiś kawałek kodu w drugie miejsce w skrypcie, zastanów się dobrze, co robisz. Skoro wystarczy skopiowanie i wklejenie, to prawdopodobnie łamiesz właśnie zasadę wydzielania redundantnego kodu do osobnych funkcji. Tyczy się to każdego języka programowania.</p>

<p>Zanim napiszesz 20 linii kodu, które podłączą obsługę <code>onclick</code> do jednego jedynego elementu na stronie, zastanów się, czy nie uprawiasz właśnie sztuki dla sztuki. Pisząc proste <code>onclick="return foo();"</code> oszczędzisz sobie kłopotu z propagacją zdarzeń, a mi oszczędzisz kilobajta kodu do pobrania. Jeśli chcesz to zrobić dobrze, użyj biblioteki takiej jak <a href="http://bennolan.com/behaviour/">Behaviour</a>.</p>

<p>Upraszczaj kod — oszczędzisz sobie pracy i zwiększysz jego czytelność. Polecam biblioteki wrapujące istniejące funkcje i zapewniające komfort pracy w każdej przeglądarce. Sprawdź <a href="http://prototype.conio.net/">Prototype</a> - jego używanie jest <a href="http://www.sergiopereira.com/articles/prototype.js.html">naprawdę proste</a>.</p>

<p>Wyłączaj wspólny i często używany kod do zewnętrznych plików. Nie każ wszystkim pobierać go za każdym razem.</p>

Technorati Tags: <a href="http://technorati.com/tag/javascript" rel="tag">javascript</a>, <a href="http://technorati.com/tag/dom" rel="tag">dom</a>, <a href="http://technorati.com/tag/prototype" rel="tag">prototype</a>, <a href="http://technorati.com/tag/behaviour" rel="tag">behaviour</a>, <a href="http://technorati.com/tag/code" rel="tag">code</a>
