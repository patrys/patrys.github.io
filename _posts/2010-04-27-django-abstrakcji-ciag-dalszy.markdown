---
layout: post
status: publish
published: true
title: 'Django: abstrakcji ciąg dalszy'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 901
wordpress_url: http://room-303.com/blog/?p=901
date: 2010-04-27 11:33:38.000000000 +02:00
categories:
- code
tags:
- django
- python
comments:
- id: 25015
  author: emes
  author_url: ''
  date: '2010-04-27 23:21:05 +0200'
  date_gmt: '2010-04-27 21:21:05 +0200'
  content: 'Tak intensywne prace mogą wskazywać tylko na jedno: w Mirumee piszecie
    własny sklep. Tak jest?'
---
<p>Tym razem inne podejście, naturalne dziedziczenie abstrakcyjnych modeli z dwoma dodatkowymi metodami.</p>

<p>W przeciwieństwie do <a href="http://room-303.com/blog/2010/04/22/django-zabawa-z-abstrakcja/">poprzedniego przykładu</a>, pozwala używać <code>super()</code> w abstrakcyjnych klasach pośrednich.</p>

<pre><code class="python">from django.db import models

class AbstractMixin(object):
    _classcache = {}

    @classmethod
    def contribute(cls):
        return {}

    @classmethod
    def construct(cls, *args, **kwargs):
        attrs = cls.contribute(*args, **kwargs)
        attrs.update({
            '__module__': cls.__module__,
            'Meta': type('Meta', (), {'abstract': True}),
        })
        key = (args, tuple(kwargs.items()))
        if not key in cls._classcache:
            clsname = (('%s%x' % (cls.__name__, hash(key)))
                       .replace('-', '_'))
            cls._classcache[key] = type(clsname, (cls, ), attrs)
        return cls._classcache[key]</code></pre>

<p>Przykład użycia:</p>

<pre><code class="python">class CategoryFactory(models.Model, AbstractMixin):
    name = models.CharField(max_length=100)

    class Meta:
        abstract = True

    def __unicode__(self):
        return self.name

class ProductFactory(models.Model, AbstractMixin):
    name = models.CharField(max_length=100)

    class Meta:
        abstract = True

    @classmethod
    def contribute(cls, category):
        return {'category': models.ForeignKey(category)}

    def __unicode__(self):
        return u'%s / %s' % (self.category, self.name)</code></pre>

<p>Konkretyzacja klas:</p>

<pre><code class="python">class MyCategory(CategoryFactory.construct()):
    pass
 
class MyProduct(ProductFactory.construct(category=MyCategory)):
    pass</code></pre>

<p>Działa również nasz test:</p>

<pre><code class="python">from . import models

c = models.MyCategory(name='cat')
p = models.MyProduct(name='prod', category=c)
print p # 'cat / prod'</code></pre>
