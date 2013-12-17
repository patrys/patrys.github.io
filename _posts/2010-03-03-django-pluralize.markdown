---
layout: post
status: publish
published: true
title: 'Django: pluralize'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 841
wordpress_url: http://room-303.com/blog/?p=841
date: 2010-03-03 18:18:57.000000000 +01:00
categories:
- web
- code
tags:
- django
- python
- gettext
comments:
- id: 24863
  author: zwierzak
  author_url: http://zwierzak.jogger.pl/
  date: '2010-03-04 17:09:15 +0100'
  date_gmt: '2010-03-04 16:09:15 +0100'
  content: "Bardzo dobra informacja, nie wiedziałem, że można tak wykorzystać blocktrans'a.\r\n\r\nOdnośnie
    pytania kto to stosuje. Nie zawsze robi się międzynarodowe aplikację, czasami
    jest potrzeba na szybko napisania jakiegoś serwisu, który ma tylko działać i nie
    będzie rozwijany. Wtedy można stosować takie nie do końca poprawne znaczki."
- id: 24864
  author: DeeJay1
  author_url: ''
  date: '2010-03-05 10:43:10 +0100'
  date_gmt: '2010-03-05 09:43:10 +0100'
  content: IMHO duża część serwisów, która ma "tylko" działać, zazwyczaj po jakimś
    czase musi zostać przepisana od zera, bo wychodzi szybciej niż rozwinięcie istniejącej,
    szczególnie jeśli chodzi o i18n (debugowanie działania gettextu w wielowątkowych
    aplikacjach nie jest fajne...)
---
<p>Najważniejszą rzeczą, jaką powinniście wiedzieć na temat filtra <code>pluralize</code> jest ta, żeby go nigdy nie używać. <em>Nigdy</em>. Jego istnienie wynika z lenistwa ludzi, którzy nigdy w życiu nie przygotowywali aplikacji do tłumaczenia. Jeśli nie wyraziłem się dość jasno, używanie filtra <code>pluralize</code> wywoła u ciebie raka, stereoporoże i zatwardzenie rozsiane.</p>

<p>Jakkolwiek sprytnie by nie wyglądał, ten kod nie nadaje się do niczego:</p>

<pre><code class="django">&lt;p&gt;
    There {{ item_count|pluralize:"is,are" }}
    {{ item_count }} thing{{ item_count|pluralize:"s" }}.
&lt;/p&gt;</code></pre>

<p>Dlaczego się nie nadaje? Spróbujcie go przetłumaczyć na kilka języków. Niektórzy chwytają się <a href="http://code.google.com/p/django-pluralize-pl/">brzydkich obejść</a>, inni wolą zrobić to zgodnie ze sztuką. Jeśli kiedykolwiek pracowaliście przy lokalizacji oprogramowania, doskonale wiecie, że tłumaczenie jednego słowa jest tak samo sensowne, jak tłumaczenie każdej litery z osobna.</p>

<p>Poprawna wersja jest przy okazji czytelna:</p>

<pre><code class="django">{% raw %}&lt;p&gt;
{% blocktrans count item_count as items %}
    There is {{ items }} thing.
{% plural %}
    There are {{ items }} things.
{% endblocktrans %}
&lt;/p&gt;{% endraw %}</code></pre>

{% raw %}<p><code>{% blocktrans %}</code> z <code>{% plural %}</code> używają <code>ungettext</code>, dzięki czemu bez konieczności odprawiania czarów radzą sobie z polskimi liczebnikami (<q>jeden tysiąc, dwa tysiące, pięć tysięcy</q>).</p>{% endraw %}
