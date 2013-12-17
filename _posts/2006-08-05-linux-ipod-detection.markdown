---
layout: post
status: publish
published: true
title: 'Linux: iPod detection'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 282
alias: /blog/2006/08/05/linux-ipod-detection/
date: 2006-08-05 09:36:32.000000000 +02:00
categories:
- linux
- software
- code
tags: []
comments:
- id: 4425
  author: byte
  author_url: http://byte.livenet.pl
  date: '2006-08-05 11:05:48 +0200'
  date_gmt: '2006-08-05 10:05:48 +0200'
  content: Działa, podaje nazwę urządzenia i punkt montowania. Testowane na iPodzie
    Shuffle, pod Ubuntu Dapper 6.06.
- id: 4426
  author: krzak
  author_url: http://www.hakore.com
  date: '2006-08-05 14:07:17 +0200'
  date_gmt: '2006-08-05 13:07:17 +0200'
  content: ja nie wiem ale iPod "poprostu działa" w Ubuntu. Podłączyłem i poprostu
    zadziałało bez cudów.
- id: 4427
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-08-05 14:11:26 +0200'
  date_gmt: '2006-08-05 13:11:26 +0200'
  content: "krzak:\r\n\r\nU mnie też działa jako dysk. Chodzi mi o konkretne programy
    do synchronizacji muzyki."
- id: 4484
  author: steamm
  author_url: http://www.steamm.net
  date: '2006-08-19 23:35:26 +0200'
  date_gmt: '2006-08-19 22:35:26 +0200'
  content: 'zgadza sie byte ubunciak wszystko ladnie wykrywa, offtopic : Patrys jedziesz
    na xgl''u ?'
- id: 4485
  author: steamm
  author_url: http://www.steamm.net
  date: '2006-08-19 23:36:30 +0200'
  date_gmt: '2006-08-19 22:36:30 +0200'
  content: "zgadza sie byte ubunciak wszystko ladnie wykrywa, a nie wiecie czy jest
    cos podobnego (chodzi mi o wtyczke do synchronizacji) do odtwarzaczy creativa
    ?\r\nofftopic : Patrys jedziesz na xgl'u ?"
---
<p>Kolejny raz prosty skrypt, tym razem z prośbą o przetestowanie. Chodzi o automatyczne wykrywanie podłączonego <a href="http://www.apple.com.pl/ipod/index.html">iPoda</a>. Zależy mi dodaniu automatycznej obsługi tych urządzeń do programów, które w tej chwili wymagają ręcznego podania nazwy urządzenia i punktu montowania (<a href="http://www.gtkpod.org/about.html">gtkpod</a>, <a href="http://www.sacredchao.net/quodlibet/">Quod Libet</a> z <a href="http://www.sacredchao.net/quodlibet/wiki/Plugins/iPod">wtyczką do iPoda</a>). W tym celu muszę się upewnić, że wykrywanie działa prawidłowo.</p>

<h4>Wymagania</h4>

<ul>
<li>dbus</li>
<li>hal</li>
<li>python</li>
<li>python-dbus</li>
</ul>

<h4>Skrypt</h4>

<blockquote><pre>#!/usr/bin/python
import dbus

class IPodSeek (object):
	def findPod(self):
		bus = dbus.SystemBus()
		try:
			hal_manager_obj = bus.get_object('org.freedesktop.Hal', 
				'/org/freedesktop/Hal/Manager')
			hal_manager = dbus.Interface(hal_manager_obj,
				'org.freedesktop.Hal.Manager')
			dev_udi_list = hal_manager.FindDeviceStringMatch ('portable_audio_player.type', 'ipod')
			for udi in dev_udi_list:
				vol_udi_list = hal_manager.FindDeviceStringMatch ('info.parent', udi)

				for vol_udi in vol_udi_list:
					vol_obj = bus.get_object ('org.freedesktop.Hal', vol_udi)
					vol = dbus.Interface (vol_obj, 'org.freedesktop.Hal.Device')

					if not vol.GetProperty('volume.is_mounted'):
						continue;

					return (vol.GetProperty('block.device'), vol.GetProperty('volume.mount_point'))
		except None:
			print 'HAL is down.'

		return ('', '')

	def __init__(self):
		(dev, mount) = self.findPod()
		print 'dev = %s; mount = %s' % (dev, mount)

IPodSeek()</pre></blockquote>

<h4>Instrukcja obsługi</h4>

<p>Wystarczy zapisać plik jako <code>ipodseek.py</code> i nadać mu prawa do wykonania (<code>chmod +x ipodseek.py</code>).</p>

<p>Prosiłbym o podanie w komentarzach, czy skrypt działa prawidłowo (iPod musi być zamontowany), konkretnego modelu iPoda i dystrybucji użytej do testowania. Jeśli wszystko pójdzie zgodnie z planem, przygotuję patche na źródła programów. Zgodnie z filozofią Apple, chciałbym żeby iPod <q>po prostu działał.</q></p>

<h4>Sprawdzone urządzenia</h4>

<ul>
<li>iPod Nano (PLD 3.0; Gentoo &mdash; Maciej <q>Tas</q> Litwiniuk)</li>
<li>iPod Shuffle (Ubuntu Dapper 6.06 &mdash; Maciej <q>byte</q> Chojnacki)</li>
</ul>

<h4>Implementacja</h4>

<p>Na początek, przygotowałem patch dla wtyczki do Quod Libeta, jest do pobrania na stronie z wtyczką.</p>

<p class="strip"><a href="http://www.flickr.com/photos/patrys/207227802/" title="Photo Sharing"><img src="http://static.flickr.com/64/207227802_40abfbdc57.jpg" width="500" height="313" alt="iPod detection actually works" /></a></p>

<p>Autor wtyczki poinformował mnie przy okazji, że planowane jest jej włączenie do podstawowego kodu Quod Libet.</p>

Technorati Tags: <a href="http://technorati.com/tag/ipod" rel="tag">ipod</a>, <a href="http://technorati.com/tag/detection" rel="tag">detection</a>, <a href="http://technorati.com/tag/linux" rel="tag">linux</a>, <a href="http://technorati.com/tag/python" rel="tag">python</a>, <a href="http://technorati.com/tag/dbus" rel="tag">dbus</a>, <a href="http://technorati.com/tag/hal" rel="tag">hal</a>
