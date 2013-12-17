---
layout: post
status: publish
published: true
title: 'Wstęp do kultury: ten komentarz ewentualnie wyjebać'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 580
wordpress_url: http://room-303.com/blog/?p=580
date: 2009-04-02 16:13:37.000000000 +02:00
categories:
- web
- code
tags: []
comments:
- id: 24403
  author: Hansa
  author_url: ''
  date: '2009-04-02 17:58:11 +0200'
  date_gmt: '2009-04-02 16:58:11 +0200'
  content: Wyjebać mój komentarz... ups! Aaa zapomniałem :)
- id: 24407
  author: Filthy
  author_url: ''
  date: '2009-04-02 21:15:33 +0200'
  date_gmt: '2009-04-02 20:15:33 +0200'
  content: Ten document.write to się na CodingHorror, DailyWTF i Eatliver nadaje jak
    nic...
- id: 24412
  author: mls
  author_url: http://mls.jogger.pl
  date: '2009-04-05 17:24:30 +0200'
  date_gmt: '2009-04-05 16:24:30 +0200'
  content: '"chujotest"? tego nie znam, my w firmie często robiliśmy (w php) prosty
    zapis: die(''dupy'');'
- id: 24430
  author: finally
  author_url: http://finally.blox.pl
  date: '2009-04-22 12:45:25 +0200'
  date_gmt: '2009-04-22 11:45:25 +0200'
  content: (Ale czego się spodziewać po http://opzsgu.pl...)
- id: 24433
  author: Patrys
  author_url: http://room-303.com/
  date: '2009-04-22 13:02:53 +0200'
  date_gmt: '2009-04-22 12:02:53 +0200'
  content: 'No tak, faktycznie, bloga mają frontem do klienta: http://opzsgu.pl/?p=140'
- id: 24476
  author: tosiek
  author_url: http://tosiek.pl
  date: '2009-06-28 07:29:27 +0200'
  date_gmt: '2009-06-28 06:29:27 +0200'
  content: "ale czy to ma znaczenie iż tematyka serwisu jest religijna ? :)\r\n\r\nraczej
    żaden ksiądz z siostrą zakonną u boku tej strony nie pisał ;P"
---
<p>Jeśli ktoś przegapił <a href="http://blip.pl/s/8524980">dyskusję na Blipie</a>, to z pewnością powinien nadrobić i zapoznać się ze startupem <a href="http://wieczne-odpoczywanie.pl/">Wieczne Odpoczywanie</a>.</p>

<p><strong>Uwaga:</strong> notka zawiera słownictwo nieodpowiednie dla osób, które nie sięgają brodą do klawiatury.</p>

<p class="strip"><a href="http://www.flickr.com/photos/patrys/3407151684/" title="Wieczne odpoczywanie by patrys, on Flickr"><img src="http://farm4.static.flickr.com/3610/3407151684_82224c2079_o.png" width="560" height="323" alt="Wieczne odpoczywanie" /></a></p>

<p>Tu właściwie mógłbym zakończyć.</p>

<p>Jaka mądrość płynie z powyższego fragmentu kodu? <em>Nie ma żadnego powodu, żeby komentarze przeznaczone dla ekipy opuszczały serwer</em>. Ładnie, ale to się nie sprawdza. Podejrzewam wręcz, że autorowi w ogóle do głowy nie przyszło, że da się to odczytać poza serwerem.</p>

<p>Bardziej ogólna wersja tego przypadku wygląda tak:</p>

<blockquote><pre><code>if impossible:
    print 'FUCK!!1!' # ← this will never happen</code></pre></blockquote>

<p>Prawdziwy wniosek jest taki: <em><strong>nigdy</strong> nie umieszczaj w programie kodu, którego efekt działania jest kompromitujący</em>. I nie dotyczy to tylko komentarzy w <abbr>HTML</abbr>. Główni podejrzani to przede wszystkim różnego rodzaju <q>niemożliwe</q> asercje (błędy typu <q>wyjebało się połączenie do bazy</q> okazują się całkiem możliwe po telefonie od klienta).</p>

<p>Nie zapominajmy też o jednej z najpopularniejszych metod debugowania, żartobliwie ochrzczonej przeze mnie <em>chujotestem</em> (polega na wstawianiu w różne miejsca w kodzie właściwej dla danego języka instrukcji drukującej nazwę pewnej popularnej wśród pań części ciała; choć brzmi całkiem niepoważnie, jest bardzo skuteczną metodą śledzenia przepływu sterowania w programowaniu wielowątkowym).</p>

<p>Chcę też zastrzec, że o ile to właśnie religijna tematyka serwisu sprawia, że komentarze w kodzie stają się tak zabawne, to nie chcę, żeby ktoś odebrał to jako nagonkę na jakikolwiek kościół (w sensie organizacji, nie budynku). Miejsce na dyskusje religijne jest pod <a href="http://room-303.com/blog/2009/04/01/wstep-do-kultury-ateizm/">wczorajszą notką</a>.</p>

<p>PS: Kod <abbr>HTML</abbr> wspomnianego wyżej serwisu nadaje się na całą serię notek, celowo na zrzucie ekranu pozostawiłem niezwykle interesującą metodę ukrywania elementów. Ktoś umie zrobić to bardziej absurdalnie? Aż prosi się o <abbr>XML</abbr>.</p>
