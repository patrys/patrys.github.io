---
layout: post
status: publish
published: true
title: 'Python: finanse'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 931
wordpress_url: http://room-303.com/blog/?p=931
date: 2010-05-20 22:36:56.000000000 +02:00
categories:
- code
tags:
- python
comments:
- id: 25045
  author: k3rni
  author_url: ''
  date: '2010-05-21 09:57:31 +0200'
  date_gmt: '2010-05-21 07:57:31 +0200'
  content: "Każdy jakkolwiek rozgarnięty programista uczy się tego drugiego dnia,
    kiedy próbuje dodać 0.1 do 0.2, a potem kiedy robi for z licznkiem typu float
    i nie chce mu się zatrzymać.\r\n\r\nNatomiast dlaczego nie używamy: łatwe wprowadzenie
    na http://floating-point-gui.de/, hardkor na http://docs.sun.com/source/806-3568/ncg_goldberg.html"
- id: 25046
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-05-21 10:17:44 +0200'
  date_gmt: '2010-05-21 08:17:44 +0200'
  content: "k3rni:\r\n\r\nWydaje mi się, że coraz więcej ludzi jest samoukami i coraz
    częściej dziwią się, że równość dla typu zmiennopozycyjnego określa się tak:\r\n\r\n<pre>abs(f2
    - f1) < EPSILON</pre>\r\n\r\nMinęły te piękne czasy, kiedy każdy programista grzebał
    w grafice (choć ze względu na wydajność każdy rozgarnięty programista do reprezentacji
    wektorów używał liczb całkowitych z przesunięciem bitowym)."
- id: 25047
  author: 3ED
  author_url: ''
  date: '2010-05-21 10:44:01 +0200'
  date_gmt: '2010-05-21 08:44:01 +0200'
  content: Ogólnie o decimal ciężko coś znaleść w google nie znając jego nazwy. Tutaj
    jest problem, że google tudzież strona pythona nie są dostatecznym narzędziem
    edukacyjnych dla samouków. Drugi powód to imho. ignorancja.. ;)
- id: 25048
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-05-21 11:01:06 +0200'
  date_gmt: '2010-05-21 09:01:06 +0200'
  content: "3ED:\r\n\r\nhttp://lmgtfy.com/?q=python+fixed+precision ;)"
- id: 25049
  author: 3ED
  author_url: ''
  date: '2010-05-21 11:24:47 +0200'
  date_gmt: '2010-05-21 09:24:47 +0200'
  content: 'Patrys: Jak przykładowo użytkownik szuka modułów do obliczeń finansowych?
    http://lmgtfy.com/?q=python+financial+math+module Ale chyba nie będziemy się licytować?
    ;) Wujek google w tym przypadku wyszukuje masę opisów pojedynczych modułów i książek
    traktujących o mathploitlib, itp. A co do "ignorancja", przydałoby się sprawdzić
    czy to działa jak powinno zanim się udostępni narzędzie do tak ważnych działań.'
- id: 25050
  author: 3ED
  author_url: ''
  date: '2010-05-21 11:27:23 +0200'
  date_gmt: '2010-05-21 09:27:23 +0200'
  content: I żeby nie było, że ja kogoś bronię lub nie. O deciaml wiem grubo ponad
    rok, a do pythona się nie dotykam (nie pasuje mi ale to kwestia gustu zapewne).
    :)
---
<p>Nie dalej jak wczoraj kolega podesłał mi łatkę do mojej <a href="http://github.com/patrys/python-number-to-words-pl">biblioteki do słownego zapisu liczb i kwot</a>. Nie zdradzę od kogo, by chronić niewinnego. Grunt, że łatka wyglądała tak:</p>

<pre>--- to_words_pl.py	(upstream)
+++ to_words_pl.py	(working copy)
@@ -82,7 +82,7 @@
         iteration += 1
     if unit:
         result.append(unit)
-    result.append(u'%d/100' % int(remainder * 100))
+    result.append(u'%d/100' % int(round(remainder * 100)))
     result = ' '.join(result)
     return result</pre>

<p>Zdziwiłem się bardzo, bo zwykłem kwoty odpowiednio zaokrąglać do dwóch miejsc po przecinku. Co się jednak okazało? <code>0.48</code> zamieniało się w <code>0.47</code>. A dokładniej? W <code>0.47999999999999998</code>. Tuś mi, ptaszku.</p>

<p>Patrząc na <code>0.48</code> tak naprawdę w głowie widziałem <code>decimal.Decimal('0.48')</code>. Jak się jednak okazuje, niektórzy próbują operacje finansowe przeprowadzać na liczbach zmiennopozycyjnych. <strong>Nie używamy typu <code>float</code> do operacji finansowych.</strong> Dlaczego?</p>

<pre>&gt;&gt;&gt; 0.48
0.47999999999999998
&gt;&gt;&gt; 0.82
0.81999999999999995</pre>

<p>Do operacji na liczbach o znanej precyzji używamy typu <code>decimal.Decimal</code> i jego kontrolowanego (i konfigurowalnego!) mechanizmu zaokrąglania:</p>

<pre>&gt;&gt;&gt; from decimal import Decimal
&gt;&gt;&gt; Decimal('0.48') + Decimal('0.12')
Decimal('0.60')
&gt;&gt;&gt; vat = Decimal('0.48') * Decimal('0.22')
&gt;&gt;&gt; vat.quantize(Decimal('0.01'))
Decimal('0.11')</pre>
