---
layout: post
status: publish
published: true
title: Blog powrócił
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 410
wordpress_url: http://room-303.com/blog/2007/10/08/blog-powrocil/
date: 2007-10-08 15:33:43.000000000 +02:00
categories:
- varia
tags: []
comments:
- id: 8555
  author: byte
  author_url: http://bytowisko.pl
  date: '2007-10-08 16:40:10 +0200'
  date_gmt: '2007-10-08 15:40:10 +0200'
  content: A jak tam 10p?
- id: 8556
  author: reod
  author_url: http://reod.jogger.pl
  date: '2007-10-08 17:37:51 +0200'
  date_gmt: '2007-10-08 16:37:51 +0200'
  content: byte++
- id: 8557
  author: Łukasz Wójcik
  author_url: http://lukem.net/
  date: '2007-10-08 17:38:41 +0200'
  date_gmt: '2007-10-08 16:38:41 +0200'
  content: Przyznam, że przez RSS nie zauważyłem problemów...
- id: 8558
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-10-08 17:42:25 +0200'
  date_gmt: '2007-10-08 16:42:25 +0200'
  content: 10p nadejdzie Niedługo&trade;, musimy wcześniej zamknąć kilka komercyjnych
    rzeczy.
- id: 11782
  author: wojtek_germ
  author_url: ''
  date: '2007-12-12 20:35:36 +0100'
  date_gmt: '2007-12-12 19:35:36 +0100'
  content: "WordPress database error: [Table 'room303.wp_post2cat' doesn't exist]\r\nSELECT
    DISTINCT YEAR(p.post_date) AS `year` FROM wp_posts p INNER JOIN wp_post2cat p2c
    ON (p.ID = p2c.post_id) WHERE p.post_date &gt; 0 ORDER By p.post_date DESC"
---
<p>Pewnie sporo z was zauważyło, że wizyty na moim blogu kończyły się ostatnio przepięknym komunikatem <q>500 Internal Server Error.</q> Okazało się, że po którymś upgradzie na serwerze, wtyczka OpenID przestała działać i razem ze sobą do grobu pociągnęła cały serwis.</p>

<p>Dzisiaj zebrałem się i zrobiłem upgrade tak wtyczki, jak i całego WordPressa. Wszystko powinno już działać bez zarzutu.</p>
