---
layout: post
status: publish
published: true
title: GStreamer 0.10 i obsługa WMV w PLD
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 239
wordpress_url: http://www.room-303.com/blog/2006/03/30/gstreamer-010-i-obsluga-wmv-w-pld/
date: 2006-03-30 13:53:56.000000000 +02:00
categories:
- linux
- software
tags: []
comments:
- id: 3508
  author: Mork
  author_url: ''
  date: '2006-03-31 08:24:50 +0200'
  date_gmt: '2006-03-31 07:24:50 +0200'
  content: "Nice! Tego mi brakowało.\r\n\r\nCzy oprócz WMV jest możliwość obsługi
    RealMedia i QuickTime?\r\n\r\nTak czy inaczej, czekam na Ubuntu 6.06..."
- id: 3509
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-03-31 08:28:24 +0200'
  date_gmt: '2006-03-31 07:28:24 +0200'
  content: Jest obsługa wszystkiego, do czego masz pliki DLL z Windowsa.
- id: 3521
  author: jpc
  author_url: http://jpc.jogger.pl
  date: '2006-04-04 22:22:00 +0200'
  date_gmt: '2006-04-04 21:22:00 +0200'
  content: A co z plikami WMV9 z DRM, których nie rusza nawet mplayer (czyli z 90%
    plikow WMV9)? ;]
- id: 24655
  author: Tomasz
  author_url: ''
  date: '2009-12-20 11:49:07 +0100'
  date_gmt: '2009-12-20 10:49:07 +0100'
  content: "-&gt; A co z plikami WMV9 z DRM, których nie rusza nawet mplayer (czyli
    z 90% plikow WMV9)? ;] &lt;-\r\npozostało bez odpowiedzi"
---
<p>Jeśli kogoś to interesuje, to właśnie zmusiłem GStreamer do obsługi formatów zamkniętych. Skutkiem tego jest natualnie ich obsługa przez Totem, najwygodniejszy z odtwarzaczy.</p>

<p>Do działania potrzebne są:</p>

<ul>
<li><code>gstreamer-0.10</code></li>
<li><code>gstreamer-pitfdll</code> zbudowany z HEAD w <abbr title="Concurrent Versioning System">CVS</abbr></li>
<li><code>w32codec</code> przebudowany z akceptacją licencji</li>
</ul>

<p>Po instalacji powyższych, Totem bez słowa zająknięcia odtworzy nawet pliki <abbr title="Windows Media Video 9">WMV9</abbr>. Tym samym, jestem już całkowicie niezależny od Xine.</p>

Technorati Tags: <a href="http://technorati.com/tag/totem" rel="tag">totem</a>, <a href="http://technorati.com/tag/gstreamer" rel="tag">gstreamer</a>, <a href="http://technorati.com/tag/wmv" rel="tag">wmv</a>, <a href="http://technorati.com/tag/pitfdll" rel="tag">pitfdll</a>, <a href="http://technorati.com/tag/pld" rel="tag">pld</a>, <a href="http://technorati.com/tag/linux" rel="tag">linux</a>
