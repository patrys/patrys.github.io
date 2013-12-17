---
layout: post
status: publish
published: true
title: 'Internet Explorer: System error -1072896658'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 300
alias: /blog/2006/10/24/internet-explorer-system-error-1072896658/
date: 2006-10-24 12:39:45.000000000 +02:00
categories:
- web
- code
tags: []
comments:
- id: 5008
  author: sit0
  author_url: http://sit0.com/biba/
  date: '2006-10-24 12:53:29 +0200'
  date_gmt: '2006-10-24 11:53:29 +0200'
  content: nie napisałeś, że złapanie tego wyjątku wymagało dopisania obsługi onException
    bo domyślnie ginie on w czeluściach prototype ;)
---
<p>Właśnie z <a href="http://sitnick.blogspot.com/">sit0</a> zabieraliśmy się za spędzenie drugiego dnia nad kolejnym dziwadełkiem, które występowało w naszej ukochanej przeglądarce. Spora część ajaksowej funkcjonalności naszych zabawek zaprzestała pełnienia swych funkcji w <abbr title="Internet Explorerze">IE</abbr>.</p>

<p>Zaczęliśmy tradycyjnie, od zabawy z Fiddlerem i upewnienia się, że zapytanie trafia do serwera prawidłowo i że serwer generuje prawidłową odpowiedź. Pudło, trzeba pobawić się z <abbr title="JavaScriptem">JS</abbr>. Debugowanie tego ostatniego w <abbr>IE</abbr> jest zabawą tyle niewdzięczną, co czasami graniczącą z absurdem. Po kilku godzinach zabawy z wstawianiem kodu kontrolnego w różne etapy przetwarzania odpowiedzi (rozoraliśmy całą bibliotekę <a href="http://script.aculo.us/">script.aculo.us</a>), zostaliśmy dalej z niczym. Mieliśmy tylko jeden wyjątek, który nie miał kompletnie sensu. Cała jego zawartość to <code>System error -1072896658</code>.</p>

<p>Zbawienie przyszło z Google: <a href="http://www.panoramio.com/blog/explorer-system-error-1072896658/">ktoś miał już identyczny problem</a> i okazało się, że rozwiązanie stosuje się także w naszym przypadku. Jeśli więc <abbr>IE</abbr> zachowuje się dziwnie i nie działają w nim wywołania <abbr title="Asynchronous JavaScript And XML">AJAX</abbr>, sprawdź zawsze nagłówki. <abbr>IE</abbr> jest bardzo wybredny i bardzo małomówny.</p>

Technorati Tags: <a href="http://technorati.com/tag/internet explorer" rel="tag">internet explorer</a>, <a href="http://technorati.com/tag/ie" rel="tag">ie</a>, <a href="http://technorati.com/tag/exception" rel="tag">exception</a>, <a href="http://technorati.com/tag/ajax" rel="tag">ajax</a>
