---
layout: post
status: publish
published: true
title: Pięć setek szaleństwa
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 1159
wordpress_url: http://room-303.com/blog/?p=1159
date: 2011-11-05 00:08:09.000000000 +01:00
categories:
- code
tags:
- python
comments:
- id: 27848
  author: tomek
  author_url: ''
  date: '2011-11-05 11:17:16 +0100'
  date_gmt: '2011-11-05 10:17:16 +0100'
  content: A jak w pythonie 3 nie wyglądało by to podobnie? Składnia wyjątków chyba
    jest podobna, czy czegoś nie złapałem?
- id: 27849
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2011-11-05 12:21:04 +0100'
  date_gmt: '2011-11-05 11:21:04 +0100'
  content: http://www.python.org/dev/peps/pep-3110/
- id: 27850
  author: PiotrB
  author_url: http://piotrbla.blogspot.com/
  date: '2011-11-05 14:45:06 +0100'
  date_gmt: '2011-11-05 13:45:06 +0100'
  content: Ja bym przede wszystkim nie łączył obsługi takich dwóch wyjątków. To są
    jednak odmienne sytuacje, inne są ich przyczyny, waga i inne powinno być zachowanie
    programu (przynajmniej w środku).
- id: 27851
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2011-11-05 15:22:30 +0100'
  date_gmt: '2011-11-05 14:22:30 +0100'
  content: "@PiotrB:\r\n\r\nA gdyby to były dwa inne wyjątki, to wpłynęłoby to w jakimś
    znaczącym stopniu na 500 na drugim końcu serwisu? Jakość tego kodu to problem
    zupełnie prostopadły do opisywanego."
---
<p>Wtem!</p>

<p>— Leży!</p>

<p>Produkcja? Ale tutaj?</p>

<pre>Traceback (most recent call last):
  File "/var/www/foo/catalogue/views.py", line 252, in get
    product = Product.objects.get(upc=tokens[0])
  File "/usr/lib/python2.6/site-packages/django/db/models/manager.py", line 132, in get
    return self.get_query_set().get(*args, **kwargs)
  File "/usr/lib/python2.6/site-packages/django/db/models/query.py", line 351, in get
    % (self.model._meta.object_name, num, kwargs))
TypeError: 'DoesNotExist' object is not callable</pre>

<p>Odśwież. Działa. Ki czort? Odśwież. Leży. Działa — działa — leży — działa. Wynik zdaje się zależeć od procesu, który akurat obsłuży zapytanie.</p>

<p>No dobrze, zobaczmy, co…</p>

<pre><code class="python">        raise self.model.MultipleObjectsReturned("get() returned more than one %s -- it returned %s! Lookup parameters were %s"
                % (self.model._meta.object_name, num, kwargs))</code></pre>

<p>Wyjątek. W trakcie rzucania wyjątku. Wbudowanego w klasę modelu.</p>

<p>Wdech, wydech. Drugi <i>worker</i> dostał. Dziwacznie poskręcane fragmenty jego wnętrzności zasypują mi skrzynkę.</p>

<p>Wdech, wydech, <code>grep</code>.</p>

<p>Zanim się przedarłem, straciliśmy jeszcze trzech. W sumie połowa zwijała się tam i charczała wewnętrznymi błędami. Wytrzymajcie, jeszcze tylko kilka plików. I jest.</p>

<pre><code class="python">        try:
            product = Product.objects.get(upc=product_upc)
        except Product.DoesNotExist, Product.MultipleObjectsReturned:
            # …</code></pre>

<p>Zasadzka — sztuk trzy w projekcie — ładnie nas urządzili. Jeden koniec kodu powoli kopie dołek pod drugim. Pułapki udało się usunąć, ale tamtym już nikt nie pomoże. Przysłanie na produkcję posiłków zajmie minimum trzy dni. Pozostaje tylko patrzeć, jak jeden po drugim toną w tym dziwacznym morzu bezradności, serwując skomplikowane dokumenty, jednak dławiąc się na najprostszych rzeczach. Zostali sami. Oni i pięć setek szaleństwa.</p>

<p>Kurtyna. Niestosowne słowa cisną mi się na usta, ubliżać chcę składni, albowiem łaknę Pythona trzeciej inkarnacji.</p>
