---
layout: post
status: publish
published: true
title: 'Python: Utop sierotki w zupie'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 636
wordpress_url: http://room-303.com/blog/?p=636
date: 2009-08-12 19:16:40.000000000 +02:00
categories:
- web
- code
tags:
- django
- python
comments:
- id: 24492
  author: Tomasz Elendt
  author_url: http://geekspace.pl
  date: '2009-08-12 20:51:02 +0200'
  date_gmt: '2009-08-12 19:51:02 +0200'
  content: Czemu u'\\b(a|i|o|u|w|z)\\b\\s+' a nie r'\b([aiouwz])\b\s+'? Wersja przyjmująca
    HTML na wejściu powinna chyba robić reg.sub(r'\1&nbsp;', val) i pomijać niektóre
    tagi (jak np. ).
- id: 24493
  author: Patrys
  author_url: http://room-303.com/
  date: '2009-08-12 20:54:58 +0200'
  date_gmt: '2009-08-12 19:54:58 +0200'
  content: "1) Po to, żeby sobie móc prosto dopisać dwuliterowe wersje w miarę potrzeb.\r\n2)
    Sugerujesz, że &amp;nbsp; jest krótsze, czy bardziej przenośne (tekst, HTML, XML)?\r\n3)
    Co to znaczy <q>pomijać niektóre tagi</q>?"
- id: 24494
  author: Tomasz Elendt
  author_url: http://geekspace.pl
  date: '2009-08-12 20:57:44 +0200'
  date_gmt: '2009-08-12 19:57:44 +0200'
  content: "Ha. Do sub-a podajesz jednak dobry argument, co jednak (podobnie jak w
    moim poprzednim komentarzu) zostało zinterpretowane przez przeglądarkę (encja
    &amp;nbsp; nie została „wyeskejpowana”).\r\n\r\nNie wiedziałem, że pozwalasz w
    komentarzach na niektóre tagi HTML.\r\n\r\nMówiąc o tagach miałem na myśli m.in.
    <code>&lt;pre&gt;</code>."
- id: 24495
  author: Patrys
  author_url: http://room-303.com/
  date: '2009-08-12 21:04:59 +0200'
  date_gmt: '2009-08-12 20:04:59 +0200'
  content: "Do <code>sub</code> podaję <code>u'\\u00a0'</code>, co oznacza niełamliwą
    spację (wcześniej faktycznie niechcący została rozwinięta). <code>&amp;nbsp;</code>
    to jej bardzo długi, nieprzenośny zapis.\r\n\r\nPonieważ nie podmieniam białych
    znaków na encje HTML, nie miałem dotąd problemów z żadnymi znacznikami. Jedyny
    problem, jaki mogę sobie wyobrazić, to spójnik poprzedzający znak końca wiersza
    w elementach z <code>white-space: pre</code>."
- id: 24496
  author: Tomasz Elendt
  author_url: http://geekspace.pl
  date: '2009-08-12 21:18:33 +0200'
  date_gmt: '2009-08-12 20:18:33 +0200'
  content: "Tak, wiem jaki kod ma niełamliwa spacja w unikodzie. Wcześniejsze moje
    „czepialstwa” wynikały z tego, że przeglądarka zintepretowała część kodu.\r\n\r\nZamiana
    ta może być problematyczna faktycznie wewnątrz znaczków z <code>white-space: pre</code>
    jeśli np. po spójniku występuje znak tabulacja (który łapie się pod <code>\\s</code>)."
- id: 24497
  author: Ludwik C. Siadlak
  author_url: http://www.personaldevelopment.pl
  date: '2009-08-12 23:33:21 +0200'
  date_gmt: '2009-08-12 22:33:21 +0200'
  content: A SynPrezesa się nie odzywał?
- id: 24498
  author: gshegosh
  author_url: http://acogitosis.krop.pl/
  date: '2009-08-13 07:16:44 +0200'
  date_gmt: '2009-08-13 06:16:44 +0200'
  content: Chyba jestem zboczony, bo "do_sierotki" śmierdzi mi więzieniem.
---
<p>Ot, taki znak, że nie umarłem. Dziś w programie dość popularny błąd składu, choć wielu uważa, że internetu reguły nie dotyczą. A <a href="http://pl.wikipedia.org/wiki/Wisz%C4%85cy_sp%C3%B3jnik">sierotki</a> wykończymy tak:</p>

<pre><code class="python">import re

def sierotki(text):
    reg = re.compile(u'\\b(a|i|o|u|w|z)\\b\\s+')
    return reg.sub(u'\\1\u00a0', text)</code></pre>

<p>Niestety, na ogół mamy do czynienia z tekstem zawierającym znaczniki:</p>

<pre><code class="python">import re
from BeautifulSoup import BeautifulSoup

def sierotki(text):
    soup = BeautifulSoup(text)
    reg = re.compile(u'\\b(a|i|o|u|w|z)\\b\\s+')
    for val in soup.findAll(text=reg):
        val.replaceWith(reg.sub(u'\\1\u00a0', val))
    return unicode(soup)</code></pre>

<p>I na koniec bonus, blok dla Django:</p>

<pre><code class="python">from django import template
register = template.Library()

@register.tag(name='sierotki')
def do_sierotki(parser, token):
    nodelist = parser.parse(('endsierotki',))
    parser.delete_first_token()
    return SierotkiNode(nodelist)

class SierotkiNode(template.Node):
    def __init__(self, nodelist):
        self.nodelist = nodelist
    def render(self, context):
        output = self.nodelist.render(context)
        return sierotki(output)</code></pre>
