---
layout: post
status: publish
published: true
title: Python, Whoosh i błędy
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 609
wordpress_url: http://room-303.com/blog/?p=609
date: 2009-05-08 14:46:15.000000000 +02:00
categories:
- web
- software
- code
tags:
- django
- python
- whoosh
- haystack
comments:
- id: 24444
  author: paluh
  author_url: ''
  date: '2009-05-08 17:01:46 +0200'
  date_gmt: '2009-05-08 16:01:46 +0200'
  content: "mam wrażenie, że w patchu brakuje prefixów: '@@' w liniach określających
    zakresy patch'owania.\r\n\r\nDziki za wpis - bardzo sie przydal!"
- id: 24445
  author: Patrys
  author_url: http://room-303.com/
  date: '2009-05-08 17:11:04 +0200'
  date_gmt: '2009-05-08 16:11:04 +0200'
  content: "paluh:\r\n\r\nDzięki, kopiowałem go z serwera przez pastebin i ten je
    zjadł. Poprawione."
- id: 24448
  author: Ryszard Szopa
  author_url: http://gryziemy.net/
  date: '2009-05-08 22:52:54 +0200'
  date_gmt: '2009-05-08 21:52:54 +0200'
  content: "Dzięki wielkie! BTW odważyłeś się kiedykolwiek puścić Haytacka z Whooshem
    na produkcję? O ile Haystack wydaje się fajnie zaprojektowany, o tyle Whoosh wydaje
    się jakiś taki... nie do końca godny zaufania. Obawiam się, że podobnych problemów
    wyjdzie na jaw jeszcze sporo. A szkoda, bo idea wyszukiwarki pełnotekstowej w
    Pythonie jest kusząca.\r\n\r\n(PS. Jakbyś stworzył na Githubie forka Haytacka
    ze swoim patchem, świat byłby o jedno repozytorium lepszy ;-)"
- id: 24449
  author: Patrys
  author_url: http://room-303.com/
  date: '2009-05-10 13:50:19 +0200'
  date_gmt: '2009-05-10 12:50:19 +0200'
  content: "Ryszard Szopa:\r\n\r\nhttp://github.com/patrys/django-haystack/tree/master"
---
<p>Tytułem wstępu: <a href="http://whoosh.ca/">Whoosh</a> to bardzo przyjemny silnik indeksujący i wyszukujący dokumenty w trybie <q>full-text</q>. Niestety, masa ludzi ma problemy z jego wdrożeniem.</p>

<h4>Objawy</h4>

<p>Główne objawy to:</p>

<blockquote><pre>OSError: [Errno 17] File exists: '/path/to/index/cache/_MAIN_LOCK'</pre></blockquote>

<p>oraz:</p>

<blockquote><pre>IOError: [Errno 2] No such file or directory: '/path/to/index/cache/_MAIN_123.tiz'</pre></blockquote>

<p>Oba z nich są na ogół różnymi objawami faktu, że więcej niż jeden proces próbuje używać tego samego indeksu w tym samym czasie. Główną przyczyną jest nieświadomość tego, że <strong>Whoosh nie gwarantuje bezpieczeństwa wątków</strong>.</p>

<h4>Rozwiązanie pierwsze: gdy używasz Haystack</h4>

<p>Ponieważ zdecydowana większość użytkowników nie odwołuje się bezpośrednio do <abbr>API</abbr> Whoosh, a korzysta z niego za pośrednictwem modułu <a href="http://haystacksearch.org/">Haystack</a>, najpierw przedstawię rozwiązanie dla nich.</p>

<p>Jak <a href="http://groups.google.com/group/django-haystack/browse_thread/thread/97109b65a6d725f3">ustaliliśmy</a> przedwczoraj z autorem Haystack, przykładowy backend dostarczany dla Whoosh błędnie zakłada bezpieczeństwo wątków tego ostatniego.</p>

<p>Dodatkowo, Haystack używa <q>leniwych obiektów</q> (obiektów z odwleczoną inicjalizacją) do ładowania indeksów, co powoduje, że nawet przy zachowaniu bezpieczeństwa wątków, <em>aplikacja nie będzie działać prawidłowo w środowisku typu <q>prefork</q></em>.

</p><p>Najprawdopodobniej w przyszłości Haystack będzie uruchamiał Whoosh w postaci usługi systemowej, co pozwoli na wielodostęp do tego samego indeksu i tym samym zlikwiduje problemy związane z rozgałęzianiem procesów i wątkowaniem. Póki co, rozwiązanie składa się z dwóch kroków:</p>

<ol>
<li><p>Nałożenie na Haystack mojej łatki, która zapewnia bezpieczeństwo wątków: <a href='http://room-303.com/blog/wp-content/uploads/2009/05/haystack-whoosh.patch'>haystack-whoosh.patch</a></p></li>
<li>Upewnienie się, że Django działa w serwerze wątkowanym, a nie forkowanym. Dla używających <code>manage.py</code> sprowadza się to do dopisania parametru <code>method</code>:
<blockquote><pre>python manage.py runfcgi method=threaded ...</pre></blockquote></li>
</ol>

<h4>Rozwiązanie drugie: gdy bezpośrednio wołasz Whoosh</h4>

<p>Tutaj gotowej łatki podać nie mogę, bo każdy pisze kod po swojemu. Wystarczy jednak &mdash; podobnie jak zrobiłem to w łatce dla Haystack &mdash; użyć mechanizmu <code>threading.Lock</code> i ogrodzić wszystkie wywołania API wspólną blokadą (czy może ryglem, jak czasem jest to słowo tłumaczone). Na przykład:</p>

<blockquote><pre><code>import threading

whoosh_api = threading.Lock()

def do_something():
	whoosh_api.acquire()
	try:
		# use API
	finally:
		whoosh_api.release()</code></pre></blockquote>

<p>Należy się również upewnić, że w danej chwili istnieje tylko jeden obiekt typu <code>whoosh.index.Index</code> na każdy katalog indeksu, a także maksymalnie jedna instancja <code>whoosh.writing.IndexWriter</code>. Pierwszy przypadek rozwiązuje implementacja singletona, drugi &mdash; ogrodzenie całego cyklu życia obiektu (aż do pomyślnego wywołania metody <code>commit</code> lub <code>cancel</code>) wewnątrz tej samej blokady, co reszta wywołań <abbr>API</abbr>.</p>
