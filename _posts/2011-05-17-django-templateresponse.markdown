---
layout: post
status: publish
published: true
title: 'Django: TemplateResponse'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 1155
wordpress_url: http://room-303.com/blog/?p=1155
date: 2011-05-17 21:22:17.000000000 +02:00
categories:
- code
tags:
- django
- python
comments:
- id: 27768
  author: opi
  author_url: http://bronikowski.com
  date: '2011-05-17 21:28:48 +0200'
  date_gmt: '2011-05-17 19:28:48 +0200'
  content: Świetnie, jestem w połowie aplikacji i teraz muszę przepisać wszystkie
    widoki. Kiedy wypada render_to_response?
- id: 27769
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2011-05-17 21:42:50 +0200'
  date_gmt: '2011-05-17 19:42:50 +0200'
  content: Wypaść pewnie nie wypadnie przed 1.4 czy 1.5, ale TemplateResponse jest
    marzeniem jeśli chodzi o debugowanie i testy jednostkowe. Możesz już po odebraniu
    wyniku z widoku sprawdzić, który szablon został użyty to jego wyrenderowania i
    co dostał w kontekście.
- id: 27770
  author: Sharpek
  author_url: http://www.sharpek.net/blog
  date: '2011-05-17 21:43:16 +0200'
  date_gmt: '2011-05-17 19:43:16 +0200'
  content: '@opi, zobacz tutaj: http://docs.djangoproject.com/en/dev/releases/1.3/#deprecated-features-1-3'
- id: 27771
  author: opi
  author_url: http://bronikowski.com
  date: '2011-05-17 21:51:31 +0200'
  date_gmt: '2011-05-17 19:51:31 +0200'
  content: Dzięki Wam obu, czytałem tylko release notes od 1.3, nie czytałem deprecated.
    Nic, trzeba będzie zrobić zmiany póki nie jest tego za dużo.
- id: 27772
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2011-05-17 21:51:56 +0200'
  date_gmt: '2011-05-17 19:51:56 +0200'
  content: "@opi:\r\n\r\nTeraz przeczytałem twój komentarz jeszcze raz. Nikt nie mówił,
    że wylecieć ma <code>render_to_response</code>, chociaż to chyba najbardziej pracochłonna
    metoda osiągnięcia tego samego wyniku."
- id: 27773
  author: zwierzak
  author_url: http://zwierzak.info/
  date: '2011-05-17 22:04:56 +0200'
  date_gmt: '2011-05-17 20:04:56 +0200'
  content: "A to przypadkiem nie miało być render jako zastępstwo?\r\n\r\nPoza tym
    ja posiadam swój własny dekorator do funkcji, który wybiera template względem
    tego czy użytkownik pobierał zwykłą stronę czy AJAX (is_ajax z Django), a w funkcji
    zwracam tylko słownik z elementami, które mają się pojawić."
- id: 27774
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2011-05-17 22:12:23 +0200'
  date_gmt: '2011-05-17 20:12:23 +0200'
  content: "@zwierzak:\r\n\r\n\"Render jako zastępstwo\"?\r\n\r\nJa wolę jawnie zwracać
    odpowiedzi zamiast dekorować widoki. Zysk niewielki (zyskujesz jedną-dwie linie
    kodu kosztem czytelności), a w razie wystąpienia wyjątku w szablonie dostajesz
    bardzo średnio pomocny zrzut stosu.\r\n\r\nNie zmienia to faktu, że w samym dekoratorze
    też musisz coś zawołać."
- id: 27775
  author: kr
  author_url: ''
  date: '2011-05-18 04:05:14 +0200'
  date_gmt: '2011-05-18 02:05:14 +0200'
  content: „Ren­der jako zastępstwo”? render - http://docs.djangoproject.com/en/dev/topics/http/shortcuts/#render
- id: 27776
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2011-05-18 09:27:41 +0200'
  date_gmt: '2011-05-18 07:27:41 +0200'
  content: "@kr:\r\n\r\nTak, już domyśliłem się, o którą funkcję chodziło. Jak pisałem
    wyżej, <code>TemplateResponse</code> jest renderowany leniwie i nawet po fakcie
    pozwala ustalić, jakie przekazano do niego parametry."
- id: 27783
  author: crackcomm
  author_url: ''
  date: '2011-06-13 06:43:08 +0200'
  date_gmt: '2011-06-13 04:43:08 +0200'
  content: Jeżeli coś wyleci to pewnie wyleci w Django 1.5 - podejrzewam, że to będzie
    przeróbka a`la sf1.4 -&gt; Symfony 2
- id: 27959
  author: roymoss
  author_url: ''
  date: '2012-03-05 07:44:25 +0100'
  date_gmt: '2012-03-05 06:44:25 +0100'
  content: "Dzięki za wpis. Proszę o więcej wpisów na temat Django. Może jakiś kurs
    dla początkujących (z innymi tematami niż oficjalny tutorial), mało tego w polskiej
    sieci.\r\nPozdrawiam"
---
<p>Przyszło Django 1.3, pojawiła się paskudna implementacja class-based views, <a href="http://room-303.com/blog/2010/02/26/django-direct_to_template/"><code>direct_to_template</code></a> zostało oznaczone jako przestarzałe. Ale pojawił się też godny następca, choć z class-based views nie ma nic wspólnego.</p>

<p>Nie piszemy więc tak:</p>

<pre><code class="python">from django.shortcuts import render_to_response
from django.template import RequestContext

def foo(request):
    # ...
    return render_to_response('foo.html', {'bar': baz},
            context_instance=RequestContext(request))</code></pre>

<p>Nie piszemy też tak:</p>

<pre><code class="python">from django.views.generic.simple import direct_to_template

def foo(request):
    # ...
    return direct_to_template(request, 'foo.html', {'bar': baz})</code></pre>

<p>Ani ­— tym bardziej — tak:</p>

<pre><code class="python">from django.views.generic import TemplateView

def foo(request):
    # ...
    return TemplateView.as_view(template_name='foo.html')(request, bar=baz)</code></pre>

<p>Drodzy państwo, zamiast powyższych używamy:</p>

<pre><code class="python">from django.template.response import TemplateResponse

def foo(request):
    # ...
    return TemplateResponse(request, 'foo.html', {'bar': baz})</code></pre>
