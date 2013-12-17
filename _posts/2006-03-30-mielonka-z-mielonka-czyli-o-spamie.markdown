---
layout: post
status: publish
published: true
title: Mielonka z mielonką, czyli o spamie
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 240
wordpress_url: http://www.room-303.com/blog/2006/03/30/mielonka-z-mielonka-czyli-o-spamie/
date: 2006-03-30 15:47:00.000000000 +02:00
categories:
- software
tags: []
comments:
- id: 3504
  author: opi
  author_url: http://bronikowski.com
  date: '2006-03-30 16:02:29 +0200'
  date_gmt: '2006-03-30 15:02:29 +0200'
  content: Ciekawe, kiedyś przy piwie wymyśliliśmy podobny sposób. :-)
- id: 3505
  author: pjf
  author_url: http://pjf.jogger.pl/
  date: '2006-03-30 17:17:32 +0200'
  date_gmt: '2006-03-30 16:17:32 +0200'
  content: "Właśnie wymyśliłeś http://en.wikipedia.org/wiki/Domainkeys\r\n\r\nA to
    co Tomek Nidecki próbuje wymyślić to połączenie zasad działania greylistingu dla
    adresów IP w systemem RBLi (nota bene takie whitelisty działają w Internecie).\r\n\r\nO
    pomyśle tej wspomnianej firmy nawet słowa nie powiem, bo ręce mi opadły jak usłyszałem
    o ich \"innowacyjności\". Ech..."
- id: 3506
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-03-30 18:10:02 +0200'
  date_gmt: '2006-03-30 17:10:02 +0200'
  content: "pjf:\r\n\r\nNo nie, bo DomainKeys podpisuje treść wiadomości, a nie nagłówki."
- id: 3531
  author: tonid
  author_url: http://spam.jogger.pl
  date: '2006-04-09 22:43:02 +0200'
  date_gmt: '2006-04-09 21:43:02 +0200'
  content: "Patrys: OIDP, DKIM (czyli wersja rozwojowa DomainKeys) podpisuje także
    wybrane nagłówki.\r\n\r\nPJF: Dokładniej, to ja chcę połączyć więcej mechanizmów
    na etapie sesji tak, żeby zwiększyć skuteczność, zmniejszyć opóźnienia i false
    positives. No, ale to temat mojej pracy magisterskiej 8D."
---
<p>Poniższy tekst oryginalnie był moim komentarzem do <a href="http://spam.jogger.pl/2006/03/27/mujica-mdash-monopol-na-reputacje-nadawcy/">postu na temat systemu antyspamowego Mujica</a>, ale uznałem, że pomysł może nie jest taki zły i warto go sobie zostawić pod ręką.</p>

<p>Byłoby o niebo wygodniej, gdyby serwer wysyłający pocztę podpisywał nagłówki swoim kluczem <abbr title="Pretty Good Privacy">PGP</abbr> i udostępniał w strefie <abbr title="Domain Name Server">DNS</abbr> klucz publiczny (jako pole <code>TXT</code>), umożliwiający sprawdzenie, czy podpis jest prawidłowy.</p>

<p>Teraz mamy trzy możliwe sytuacje odbierania poczty:</p>

<ul>
<li>list pochodzi od nadawcy, którego MX nie posiada publicznego klucza - list zostaje sprawdzony normalnie, za pomocą spamassassina i trafia do kolejki</li>

<li>list pochodzi od nadawcy, którego MX posiada publiczny klucz, a list jest prawidłowo podpisany przez serwer - list trafia do kolejki bez sprawdzania</li>

<li>list pochodzi od nadawcy, którego MX posiada publiczny klucz, ale list nie jest podpisany prawidłowo lub nie jest podpisany wcale - list zostaje odrzucony przed przyjęciem</li>
</ul>

<p>Łatwe w konfiguracji (wystarczy skopiować klucz publiczny na wszystkie maszyny służące za MX w danej sieci) i łatwo zapobiegnie wysyłaniu spamu z fikcyjnych kont typu <code>user@hotmail.com</code> (zakładając, że taki Hotmail by to zainstalował). Przy okazji skuteczniejsze od <abbr title="Sender Policy Framework">SPF</abbr>, gdzie spora część adminów dla wygody wpisała sobie <q>all.</q></p>

Technorati Tags: <a href="http://technorati.com/tag/spam" rel="tag">spam</a>, <a href="http://technorati.com/tag/pgp" rel="tag">pgp</a>, <a href="http://technorati.com/tag/mail" rel="tag">mail</a>
