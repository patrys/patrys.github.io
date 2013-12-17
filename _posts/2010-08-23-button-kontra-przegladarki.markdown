---
layout: post
status: publish
published: true
title: Button kontra przeglądarki
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 1038
wordpress_url: http://room-303.com/blog/?p=1038
date: 2010-08-23 16:45:24.000000000 +02:00
categories:
- web
- software
tags: []
comments:
- id: 25131
  author: Przyciski w przeglądarkach
  author_url: http://iworks.pl/przyciski-w-przegladarkach/
  date: '2010-08-23 18:18:03 +0200'
  date_gmt: '2010-08-23 16:18:03 +0200'
  content: '[...] Button kontra przeglądarki [...]'
- id: 25132
  author: Wasacz
  author_url: http://wasacz.net/
  date: '2010-08-24 10:53:36 +0200'
  date_gmt: '2010-08-24 08:53:36 +0200'
  content: "W trzecim punkcie vendor prefiksy powinny być przed standardową właściwością.\r\n\r\nJakieś
    to częste ostatnio ;)"
- id: 25133
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-08-24 11:09:45 +0200'
  date_gmt: '2010-08-24 09:09:45 +0200'
  content: "Wasacz:\r\n\r\nDopóki wartości i interpretacja pozostają takie same, kolejność
    nie gra roli."
- id: 25134
  author: Wasacz
  author_url: http://wasacz.net/
  date: '2010-08-24 11:21:24 +0200'
  date_gmt: '2010-08-24 09:21:24 +0200'
  content: Dlatego kolejność to zabezpieczenie na przyszłość.
- id: 25135
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-08-24 11:55:47 +0200'
  date_gmt: '2010-08-24 09:55:47 +0200'
  content: Na jaką przyszłość? Spodziewasz się, że któregoś dnia po zatwierdzeniu
    standardu te same nazwy powrócą w wersji z prefiksami? To byłoby wbrew zasadzie
    zachowywania wstecznej zgodności w CSS.
- id: 25159
  author: Paweł Ludwiczak
  author_url: http://blog.ludwiczakpawel.com
  date: '2010-09-01 21:13:13 +0200'
  date_gmt: '2010-09-01 19:13:13 +0200'
  content: Do IE polecam też dodać white-space:nowrap; bo gdy button ma kilkuwyrazową
    wartość, to każdy z wyrazów jest w osobnej linii, co oczywiście rozsypuje takowego
    :)
---
<p>Ku pamięci:</p>

<ul>
<li><p>Firefox¹ ignoruje <code>line-height</code>.</p></li>
<li><p>Firefox¹ dodaje własny element z dwupikselowym paddingiem i pikselowym borderem:</p>
<pre><code lang="css">button::-moz-focus-inner {
    border: 0 none;
    padding: 0;
}</code></pre></li>
<li><p>Wszystkie przeglądarki domyślnie wliczają ramki i padding do rozmiarów elementu:</p>
<pre><code lang="css">button {
    box-sizing: content-box;
    -moz-box-sizing: content-box;
    -ms-box-sizing: content-box;
    -webkit-box-sizing: content-box;
}</code></pre></li>
<li><p><abbr title="Internet Explorer 7">IE7</abbr> i starsze nie radzą sobie z automatyczną szerokością przycisków:</p>
<pre><code lang="css">button {
    overflow: visible;
    width: 0;
}
button[type] {
    width: auto;
}</code></pre></li>
</ul>

<p><small>¹ Dotyczy ogólnie produktów Mozilli.</small></p>
