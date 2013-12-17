---
layout: post
status: publish
published: true
title: 'PLD Linux for Desktop: system-config-printer'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 376
wordpress_url: http://room-303.com/blog/2007/05/24/pld-linux-for-desktop-system-config-printer/
date: 2007-05-24 19:29:13.000000000 +02:00
categories:
- linux
- software
tags: []
comments:
- id: 7970
  author: yZZuF
  author_url: ''
  date: '2007-05-24 20:46:50 +0200'
  date_gmt: '2007-05-24 19:46:50 +0200'
  content: Hmm... mógłbyś gdzieś wystawić swoje fonts.conf? Czcionki masz niesamowite.
    :-)
- id: 7971
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-05-24 20:53:53 +0200'
  date_gmt: '2007-05-24 19:53:53 +0200'
  content: "yZZuF:\r\n\r\nKonfigi są z fontconfig, używam tych:\r\n\r\n<pre><code>[patrys@meaw
    ~]$ ls -1 /etc/fonts/conf.d/\r\n10-sub-pixel-rgb.conf\r\n20-fix-globaladvance.conf\r\n20-lohit-gujarati.conf\r\n20-unhint-small-vera.conf\r\n30-amt-aliases.conf\r\n30-urw-aliases.conf\r\n40-generic.conf\r\n49-sansserif.conf\r\n50-user.conf\r\n51-local.conf\r\n60-latin.conf\r\n65-fonts-persian.conf\r\n65-nonlatin.conf\r\n69-unifont.conf\r\n80-delicious.conf\r\n90-synthetic.conf</code></pre>"
- id: 7974
  author: urban
  author_url: http://bash.org.pl
  date: '2007-05-25 16:07:06 +0200'
  date_gmt: '2007-05-25 15:07:06 +0200'
  content: "Dostępne są gdzieś paczki z tym? Czy muszę sobie sam z cvsa budować?\r\nMoze
    są jakieś \"nieoficjalne\" repozytoria z takimi wynalazkami prosto z cvsa? Nie
    zawsze chce mi sie to wszystko budować. :)"
- id: 7975
  author: Hexe
  author_url: http://Hexe.openid.pl/
  date: '2007-05-25 16:10:26 +0200'
  date_gmt: '2007-05-25 15:10:26 +0200'
  content: "No tak, drukarki.. rychło w czas, nie powiem :].\r\nTo co się jeszcze
    szykuje?"
- id: 7978
  author: GDR!
  author_url: http://gdr.geekhood.net/
  date: '2007-05-29 00:01:18 +0200'
  date_gmt: '2007-05-28 23:01:18 +0200'
  content: Wlasnie wlasnie, gdzie szukac paczki?
- id: 22760
  author: ptiJo
  author_url: ''
  date: '2008-11-11 19:03:01 +0100'
  date_gmt: '2008-11-11 18:03:01 +0100'
  content: "That shot really looks great !\r\n\r\nCan you provide english steps (google
    translate is not much helpfull here ;) to achieve that ? What are the differences
    with a generic Xorg/fontconfig/cairo configuration ?"
---
<p>Prosto z Fedory przybywa do <abbr title="PLD Linux Distribution">PLD</abbr> pakiet o wdzięcznej nazwie <code>system-config-printer</code>. Napisałbym, że przybywa magicznie, ale spędziłem nad nim sporą część wczorajszego wieczoru.</p>

<p class="strip"><a href="http://www.flickr.com/photos/patrys/512408190/" title="Photo Sharing"><img src="http://farm1.static.flickr.com/215/512408190_606d8dc915.jpg" alt="GNOME Printer Configuration" height="313" width="500" /></a></p>

<p>Dzięki temu narzędziu można w końcu w wygodny sposób zarządzać drukarkami, także tymi zdalnymi (mam na myśli udostępniane przez Sambę). W obszarze powiadamiania pojawia się także ikona odpowiadająca za kolejkę wydruku. Nareszcie usuwanie niechcianych zadań nie wymaga dłubania w przeglądarce.</p>

<p>Miłej zabawy, a to dopiero początek zmian w <abbr>PLD</abbr> na lepsze ;)</p>
