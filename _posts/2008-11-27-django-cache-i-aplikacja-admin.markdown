---
layout: post
status: publish
published: true
title: 'Django: cache i aplikacja Admin'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 498
wordpress_url: http://room-303.com/blog/?p=498
date: 2008-11-27 12:32:50.000000000 +01:00
categories:
- web
- code
tags: []
comments:
- id: 23146
  author: Dominik Porada
  author_url: http://dominikporada.com
  date: '2008-11-27 16:34:16 +0100'
  date_gmt: '2008-11-27 15:34:16 +0100'
  content: O, dzięki za tipa. ;-)
- id: 24500
  author: Janusz
  author_url: http://skonieczny.pl
  date: '2009-08-18 11:17:05 +0200'
  date_gmt: '2009-08-18 10:17:05 +0200'
  content: Thx :D
- id: 24532
  author: Kaja
  author_url: ''
  date: '2009-10-06 12:23:19 +0200'
  date_gmt: '2009-10-06 10:23:19 +0200'
  content: Thx :)
---
<p>Wczoraj na Blipie pojawiła się dyskusja na temat obsługi cache w Django i domyślnego przechowywania w nim wszystkich widoków, z panelem administracyjnym włącznie. Koncepcji pojawiło się kilka, z łataniem kodu Django włącznie. Na szczęście rozwiązanie jest bardzo proste.</p>

<p>Aby zblokować pamięć podręczną dla panelu administracyjnego (oglądanie nieaktualnych danych przez administratora to raczej średni pomysł), wystarczy udekorować go funkcją <code>never_cache</code> tak, jak robi się to z każdym innym widokiem:</p>

<blockquote><pre><code>from django.conf.urls.defaults import *
from django.contrib import admin
from django.views.decorators.cache import never_cache

admin.autodiscover()

urlpatterns = patterns('',
    ('^admin/(.*)', never_cache(admin.site.root)),
)</code></pre></blockquote>

<p>emes przygotował nawet stosowną <a href="http://code.djangoproject.com/ticket/9709">łatkę na dokumentację</a>.</p>
