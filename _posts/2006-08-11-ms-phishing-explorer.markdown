---
layout: post
status: publish
published: true
title: MS Phishing Explorer
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 285
alias: /blog/2006/08/11/ms-phishing-explorer/
date: 2006-08-11 15:29:05.000000000 +02:00
categories:
- web
- software
- code
tags: []
comments:
- id: 4444
  author: Piotr Konieczny
  author_url: http://blog.konieczny.be
  date: '2006-08-11 16:35:43 +0200'
  date_gmt: '2006-08-11 15:35:43 +0200'
  content: A ja w Operze, korzystając z Twojego przykładu, potrafie przejść na stronę
    i Google i 7thguarda. (Pewna strefa w okolicach obrazka pozwala "złapać pod kursorem"
    href=google)
- id: 4445
  author: Robert Drózd
  author_url: http://www.webaudit.pl/blog/
  date: '2006-08-11 17:59:10 +0200'
  date_gmt: '2006-08-11 16:59:10 +0200'
  content: "Wystarczy podpiąć pod onclick prosty javascript, aby firefox też pokazywał
    w pasku google, a przechodził do yahoo.  http://www.webaudit.pl/temp/explode2.html\r\n\r\nzachowanie
    IE w Twoim przykladzie to rzeczywiscie błąd, ale pasek statusu jest i tak mało
    wiarygodny."
- id: 4446
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-08-11 20:48:00 +0200'
  date_gmt: '2006-08-11 19:48:00 +0200'
  content: "Robert:\r\n\r\nTyle, że tego nie zablokuje ci żaden produkt Symanteca,
    czy inny Internet Guard, bo to całkiem poprawny kod."
- id: 4447
  author: jpc
  author_url: http://jpc.jogger.pl
  date: '2006-08-12 13:46:14 +0200'
  date_gmt: '2006-08-12 12:46:15 +0200'
  content: Tak samo jest z Operą. Generalnie to chyba trudne do obejścia. Chyba, źe
    wywoływany byłby kod w sandboksie i wyświetlany rezultat odpalenia tego kodu.
    Super rowiązanie, ale chyba nierealne w obecnych przeglądarkach...
- id: 4448
  author: smoku
  author_url: http://staff.xiaoka.com/smoku/
  date: '2006-08-12 17:23:49 +0200'
  date_gmt: '2006-08-12 16:23:49 +0200'
  content: "Widzę obrazek Google. Najeżdżam myszą w pasku stanu jest http://google.com/.
    Klikam i zostaję przekierowany na http://www.google.pl/.\r\nFUDujesz... Nie jest
    tak źle jak to przedstawiasz.\r\n\r\nPrzeglądarka: Epiphany 2.15.91 (Powered by
    Gecko 1.8)."
- id: 4449
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-08-12 19:34:22 +0200'
  date_gmt: '2006-08-12 18:34:22 +0200'
  content: "smoku:\r\n\r\nDo kogo to?"
- id: 4454
  author: Bartini
  author_url: http://bartini.jogger.pl/
  date: '2006-08-13 21:03:56 +0200'
  date_gmt: '2006-08-13 20:03:56 +0200'
  content: "Dziwne, w Operze kiedy\r\nkopiuje link - jest google\r\npatrze w pasek
    stanu - 7thguard.net i tyle\r\npo kliknięciu- 7th guard ze wspolrzednymi punktu
    ktory klikłem :p"
- id: 4456
  author: nigerianscams.info&raquo; Blog Archive &raquo; MS Phishing Explorer
  author_url: http://nigerianscams.info/?p=195
  date: '2006-08-14 03:06:06 +0200'
  date_gmt: '2006-08-14 02:06:06 +0200'
  content: '[...] Original post by Patrys and software by Elliott Back [...]'
- id: 4457
  author: 'nigerianscams.info&raquo; Blog Archive &raquo; Patryk Zawadzki: MS Phishing
    Explorer'
  author_url: http://nigerianscams.info/?p=208
  date: '2006-08-14 03:06:44 +0200'
  date_gmt: '2006-08-14 02:06:44 +0200'
  content: '[...] Original post by Patrys and software by Elliott Back [...]'
- id: 4469
  author: '{o}'
  author_url: http://www.roswell.pl
  date: '2006-08-17 18:35:01 +0200'
  date_gmt: '2006-08-17 17:35:01 +0200'
  content: W IE7 na pasku stanu widać http://7thguard.net/
- id: 4470
  author: oom
  author_url: ''
  date: '2006-08-18 01:45:41 +0200'
  date_gmt: '2006-08-18 00:45:41 +0200'
  content: 'robert: nie dziala.'
---
<p>Taka drobna ciekawostka dla fanów Domyślnej Przeglądarki. Znaleziona w raporcie dotyczącym błędu z 2005. roku. Okazuje się, że to, co pojawia się w pasku stanu <abbr title="Internet Explorera">IE</abbr>, nie ma nic wspólnego z tym, dokąd trafisz po kliknięciu odnośnika.</p>

<p>Prosty przykład:</p>

<blockquote><pre><code>&lt;form action="http://7thguard.net/" method="get"&gt;
	&lt;a href="http://google.com/"&gt;&lt;input type="image" src="http://www.google.com/intl/en/images/logo.gif" alt="google.com" /&gt;&lt;/a&gt;
&lt;/form&gt;</code></pre></blockquote>

<p>Do pobawienia się <a href="http://patrys.icenter.pl/test/2006-08-11-ms-phishing-explorer/">przykład phishingu w <abbr>IE</abbr>. Tak, działa z każdym Service Packiem</a>.</p>

Technorati Tags: <a href="http://technorati.com/tag/ie" rel="tag">ie</a>, <a href="http://technorati.com/tag/phishing" rel="tag">phishing</a>, <a href="http://technorati.com/tag/bug" rel="tag">bug</a>, <a href="http://technorati.com/tag/exploit" rel="tag">exploit</a>
