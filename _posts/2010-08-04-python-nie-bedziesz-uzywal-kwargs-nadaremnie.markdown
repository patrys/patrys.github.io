---
layout: post
status: publish
published: true
title: 'Python: Nie będziesz używał **kwargs nadaremnie'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 1001
wordpress_url: http://room-303.com/blog/?p=1001
date: 2010-08-04 16:16:52.000000000 +02:00
categories:
- code
tags:
- python
comments:
- id: 25121
  author: salmon
  author_url: ''
  date: '2010-08-04 19:36:53 +0200'
  date_gmt: '2010-08-04 17:36:53 +0200'
  content: Kurwica mnie bierze jak widzę coś takiego w kodzie. Oczywiście dokumentacji
    do tego nigdy nie ma...
- id: 25122
  author: MySZ
  author_url: http://urzenia.net/
  date: '2010-08-04 21:02:52 +0200'
  date_gmt: '2010-08-04 19:02:52 +0200'
  content: Moje BlipAPi.py tak robi ;) Za często dochodziły kolejne parametry które
    trzeba było sensownie obsłużyć, i miałem do wyboru albo tak jak w wersji PHP (czyli
    tworzę obiekt, przypisuję mu właściwości, etc - trochę nadmiarowe) albo użycie
    samych parametrów nazwanych (ale tutaj czasem zmieni się kolejność dla spójności
    jednych metod z innymi etc), albo właśnie użycie kwargs. Ew. jeszcze mogłem użyć
    jawnych słowników, ale to dla mnie było najgorsze rozwiązanie.
---
<p>Prawidłowe użycie:</p>

<pre><code class="python">def foo(bar, *args, **kwargs):
    frobnicate(bar)
    baz(*args, **kwargs)</code></pre>

<p>Nigdy tak¹:</p>

<pre><code class="python">def foo(bar, *args, **kwargs):
    frobnicate(bar)
    baz()</code></pre>

<p><small>¹  Z wyjątkiem kilku API, które wyraźnie rezerwują sobie możliwość wprowadzenia dodatkowych parametrów. Działają tak np. wbudowane sygnały w Django.</small></p>

<p>Ciche połykanie śmieci w parametrach w malowniczy sposób zemści się przy pierwszej literówce w kodzie. I będzie ci się należało.</p>

<p>Jeśli wydaje ci się, że w ten sposób skracasz sobie kod, to przypomnij sobie starą zasadę: utrzymywanie kodu wymaga dwa razy więcej inteligencji i sprytu, niż jego napisanie. Jeśli cały swój spryt włożysz w stworzenie kodu, to z definicji jesteś za głupi, by go potem debugować.</p>
