---
layout: post
status: publish
published: true
title: 'Python: wyjątkowo głupi pomysł'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 926
wordpress_url: http://room-303.com/blog/?p=926
date: 2010-05-13 18:12:38.000000000 +02:00
categories:
- code
tags:
- python
comments:
- id: 25037
  author: mrk
  author_url: ''
  date: '2010-05-13 18:45:23 +0200'
  date_gmt: '2010-05-13 16:45:23 +0200'
  content: Dzięki, cenna uwaga. Myślałem, że te dwie notacje są równoważne :)
- id: 25039
  author: Name
  author_url: ''
  date: '2010-05-14 10:13:01 +0200'
  date_gmt: '2010-05-14 08:13:01 +0200'
  content: ot/ 10przykazan -&gt; 500 Internal Server Error
- id: 25040
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-05-14 10:24:06 +0200'
  date_gmt: '2010-05-14 08:24:06 +0200'
  content: "Name:\r\n\r\nDobre zgłoszenie, ale nie do mnie. :)"
- id: 25041
  author: kazam
  author_url: ''
  date: '2010-05-15 00:58:52 +0200'
  date_gmt: '2010-05-14 22:58:52 +0200'
  content: do czego przydaje sie 'raise' ?
- id: 25042
  author: mynthon
  author_url: http://mynthon.net/
  date: '2010-05-17 20:49:54 +0200'
  date_gmt: '2010-05-17 18:49:54 +0200'
  content: samo raise wyrzuca jeszcze raz ostatni wyjątek.
- id: 25160
  author: demikaze
  author_url: ''
  date: '2010-09-01 21:28:21 +0200'
  date_gmt: '2010-09-01 19:28:21 +0200'
  content: A wydawało mi się że to taka oczywista oczywistość - przynajmniej w C++/C#
    tak jest to traktowane
- id: 25161
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-09-01 21:34:46 +0200'
  date_gmt: '2010-09-01 19:34:46 +0200'
  content: "demikaze:\r\n\r\nOczywiste dla tego, kto wie, jak działają wyjątki. Dla
    ciebie oczywista jest też różnica między \"x++\" i \"++x\", a popatrz, ile osób
    się na tym nacina."
- id: 25162
  author: demikaze
  author_url: ''
  date: '2010-09-02 08:12:13 +0200'
  date_gmt: '2010-09-02 06:12:13 +0200'
  content: Niestety jest masa *programistów* których *prawie* żadna konstrukcja języka
    nie zaskoczy i których programy potem *prawie* działają :)
---
<p>Nigdy nie róbcie tak:</p>

<pre><code class="python">try:
    # ...
except FooException, e:
    # ...
    raise e</code></pre>

<p>Wyjątki przepuszcza się tak:</p>

<pre><code class="python">try:
    # ...
except FooException:
    # ...
    raise</code></pre>

<p>Istotna różnica polega na niezniszczeniu całego stosu wywołań. Z góry dziękuję.</p>
