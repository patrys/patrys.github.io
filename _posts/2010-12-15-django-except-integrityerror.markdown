---
layout: post
status: publish
published: true
title: Django, except IntegrityError
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 1136
wordpress_url: http://room-303.com/blog/?p=1136
date: 2010-12-15 21:01:09.000000000 +01:00
categories:
- code
tags:
- django
- python
comments:
- id: 25810
  author: jarek
  author_url: http://smiejczak.net
  date: '2010-12-15 21:59:39 +0100'
  date_gmt: '2010-12-15 20:59:39 +0100'
  content: "Bardziej ogólnie to except: pass i except Exception:pass to w 90% przypadków
    bardzo zły pomysł (ogólnie w programowaniu). Co do reszty się zgadzam (nawet sam
    w amoku coś takiego napisałem). Bez porządnego tdd praca z czymś takim to koszmar.
    Zastanawiałem się kiedyś z czego to wynika. W Java/C++ (śmiech na bok) w dokumentacjach
    api projektów częściej widziałem wyjątki jakie wypluwa dana metoda, a  w pythonie
    (projektach, środowisku) jest z tym słabo/średnio/bez spojrzenia w kod nie ustalisz.
    \r\nMimo tego że dokumentacja architektury/zachowań zazwyczaj jest naprawdę przystępna
    ;]\r\nbtw. dla mnie IntegrityError to taki Unicorn który pojawia się rzadko i
    zwiastuje że nie wykonałem migracji ;)"
- id: 25811
  author: jarek
  author_url: http://smiejczak.net
  date: '2010-12-15 22:06:17 +0100'
  date_gmt: '2010-12-15 21:06:17 +0100'
  content: "ps 1. Taki (częściowo powiązany) antywzorzec rzucania wyjątków to robienie
    biblioteki i na każdy błąd dawanie raise BigMothaFuckaException('opis bledu')
    bez podziału na konkretne przypadki. \r\nPotem użytkownicy się śmieją że dajesz
    Message \"wystąpił bliżej nieokreślony błąd\" ;) albo @fijal smieje się że łapiąc
    exception \"grepujesz\" po jego message  aby ustalić co się stało :)"
- id: 25889
  author: regisu
  author_url: http://blog.r3gi.net
  date: '2010-12-16 09:15:10 +0100'
  date_gmt: '2010-12-16 08:15:10 +0100'
  content: Mało nie padłem czytając "Wersje obrazową" :D Fajnie piszesz.
- id: 27723
  author: Nikow
  author_url: ''
  date: '2011-01-09 09:50:50 +0100'
  date_gmt: '2011-01-09 08:50:50 +0100'
  content: Dramatyzujesz. Prawda jest taka, że można reinicjować bazę. Nawiązać ponowne
    połączenie, ew. z opóźnieniem i nadpisać stary obiekt obsługi bazy. Trochę zabawy
    z tym jest, bo musisz wszystkie pierdółki od razu zresetować, ale to fajna zabawa.
    ;)
- id: 27730
  author: Majki
  author_url: ''
  date: '2011-01-30 08:40:58 +0100'
  date_gmt: '2011-01-30 07:40:58 +0100'
  content: "Cholera, zabiłem szczeniaczka... Nie możesz zmienić na 'kotka o maślanych
    oczkach', miałbym spokojniejsze sumienie!\r\n\r\nPozdro,\r\nmajki"
---
<p>Jeden mały, niewinny szczeniaczek o maślanych oczkach zostaje gdzieś na świecie żywcem przemielony na karmę dla kotów za każdym razem, kiedy piszesz coś takiego:</p>

<pre><code class="python">try:
    # ...
except IntegrityError:
    return None</code></pre>

<p>Łapanie <code>IntegrityError</code> jako metoda wykrywania problemów jest równie dobrym pomysłem, co wymiana czujników dymu na urządzenie wykrywające odgłos syreny nadjeżdżającej straży pożarnej.</p>

<p>Błąd na poziomie bazy danych jest nieodwracalny. Nie można nic naprawić. To jak pójść pośmiertnie do lekarza. Połknięcie wyjątku bez dalszej propagacji to tylko dodatkowe punkty za styl. Dzięki temu wszystkie otwarte transakcje (z izolującą włącznie) właśnie stały się bezużyteczne, a najbliższa operacja na bazie danych spowoduje spektakularny zgon całej aplikacji.</p>

<h3>Wersja obrazowa</h3>

<p>Twój kod próbuje dywanikiem z kibla gasić ogień w domu, w którym dawno złuszczyły się tapety i zniknęły meble. W domu, który sam podpalił. Niezbyt zadowolony z rezultatów wychodzi więc przed budynek i dusi strażaków wężem. Po wszystkim, gwiżdżąc, z rękoma w kieszeniach, odchodzi w stronę zachodzącego słońca, po drodze mijając sąsiada — powoli spopielającego się we własnym ogródku.</p>
