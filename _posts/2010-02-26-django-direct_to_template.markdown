---
layout: post
status: publish
published: true
title: 'Django: direct_to_template'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 830
wordpress_url: http://room-303.com/blog/?p=830
date: 2010-02-26 00:36:23.000000000 +01:00
categories:
- web
- code
tags:
- django
- python
comments:
- id: 24847
  author: nickers
  author_url: ''
  date: '2010-02-26 01:00:55 +0100'
  date_gmt: '2010-02-26 00:00:55 +0100'
  content: "Może wynika to z obecności tej funkcji w tutorialu? ;)\r\n\r\nhttp://docs.djangoproject.com/en/1.1/intro/tutorial03/#intro-tutorial03\r\n\r\nW
    każdym razie ja jako nowy człowiek w pythonie i django nawet nie wpadłem na to,
    że można używać widoku jak zwykłej funkcji(wspomniane direct_to_template). Dziękuję
    za trick :)"
- id: 24849
  author: http-blog.jajcus.net-
  author_url: http://blog.jajcus.net/
  date: '2010-02-26 09:49:43 +0100'
  date_gmt: '2010-02-26 08:49:43 +0100'
  content: render_to_response() jest bardziej uniwersalne, bo można mu podać coś innego
    niż RequestContext(request). Oczywiście w prostych przypadkach wystarcza direct_to_template()
    i IIRC tutorial o takiej możliwości wykorzystania widoków też wspomina (ale pewnie
    nie dość wyraźnie).
- id: 24850
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-02-26 09:55:08 +0100'
  date_gmt: '2010-02-26 08:55:08 +0100'
  content: "jajcus:\r\n\r\nOczywiście chodzi mi o trywialny przypadek, kiedy przekazać
    trzeba pełny kontekst."
- id: 24855
  author: zwierzak
  author_url: http://zwierzak.jogger.pl/
  date: '2010-02-28 11:30:06 +0100'
  date_gmt: '2010-02-28 10:30:06 +0100'
  content: "Dlatego osobiście korzystam z tego rozwiązania:\r\nhttp://www.djangosnippets.org/snippets/596/\r\nJedyne
    co zwracam to dane do template. Bardzo przyjemne rozwiązanie, a osobiście jeszcze
    korzystam z lekko zmodyfikowanej wersji w której mogę określić dodatkowy szablon
    dla ajax'a (wtedy wszystkie żądania są wykonywane pod 1 url więc zmniejsza mi
    się ilość widoków."
- id: 24860
  author: Norbert
  author_url: http://pithyless.com
  date: '2010-03-01 17:12:37 +0100'
  date_gmt: '2010-03-01 16:12:37 +0100'
  content: "from annoying.decorators import render_to\r\n\r\n@render_to('foo.html')\r\ndef
    foo(request):\r\n    # ...\r\n    return {'bar': baz}\r\n\r\n# django-annoying
    ma również inne skróty:\r\n# http://bitbucket.org/offline/django-annoying/"
- id: 27767
  author: 'Django: TemplateResponse - Room 303'
  author_url: http://room-303.com/blog/2011/05/17/django-templateresponse/
  date: '2011-05-17 21:22:24 +0200'
  date_gmt: '2011-05-17 19:22:24 +0200'
  content: '[...] Django 1.3, poja­wiła się paskudna imple­men­ta­cja class-based
    views, direct_to_template zostało ozna­czone jako prze­sta­rzałe. Ale poja­wił
    się też godny następca, choć z [...]'
---
<p>Nie wiem, czemu niektórzy tak uparcie korzystają z funkcji <code>render_to_response</code>, by za każdym razem przekazać do niej ręcznie stworzony obiekt kontekstu. Zresztą, sami oceńcie, która wersja jest ładniejsza:</p>

<pre><code class="python">from django.shortcuts import render_to_response
from django.template import RequestContext

def foo(request):
    # ...
    return render_to_response('foo.html', {'bar': baz},
                              context_instance=RequestContext(request))</code></pre>

<p>Czy może:</p>

<pre><code class="python">from django.views.generic.simple import direct_to_template

def foo(request):
    # ...
    return direct_to_template(request, 'foo.html', {'bar': baz})</code></pre>

<p>A teraz pomnóżcie to przez liczbę widoków w aplikacji.</p>
