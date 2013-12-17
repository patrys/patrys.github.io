---
layout: post
status: publish
published: true
title: 'Django: zabawa z abstrakcją'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 879
wordpress_url: http://room-303.com/blog/?p=879
date: 2010-04-22 22:22:45.000000000 +02:00
categories:
- code
tags:
- django
- python
comments:
- id: 24986
  author: sowa
  author_url: ''
  date: '2010-04-23 05:06:48 +0200'
  date_gmt: '2010-04-23 03:06:48 +0200'
  content: Przestań się spuszczać nad modelami i abstrakcjami tylko napisz jakąś funkcjonalną
    aplikacje,
- id: 24987
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-04-23 09:46:16 +0200'
  date_gmt: '2010-04-23 07:46:16 +0200'
  content: "sowa:\r\n\r\nKim jesteś i jakimiż to dokonaniami chciałbyś się pochwalić
    zanim skrytykujesz notkę, której nie zrozumiałeś?"
- id: 24988
  author: forgems
  author_url: ''
  date: '2010-04-23 10:34:20 +0200'
  date_gmt: '2010-04-23 08:34:20 +0200'
  content: "a nie prościej tak ?\r\n\r\nclass MyProduct(models.Model):\r\n     ........\r\n
    \    category = models.ForeignKey(settings.PRODUCTS_MODEL)"
- id: 24989
  author: forgems
  author_url: ''
  date: '2010-04-23 10:36:53 +0200'
  date_gmt: '2010-04-23 08:36:53 +0200'
  content: "grr :)\r\nchodziło o : \r\ncategory = models.ForeignKey(settings.CATEGORY_MODEL)"
- id: 24990
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-04-23 10:38:37 +0200'
  date_gmt: '2010-04-23 08:38:37 +0200'
  content: "forgems:\r\n\r\nWtedy zawsze musi istnieć dokładnie jedna konkretyzacja
    każdej klasy. Cała idea była taka, żeby konkretyzować tylko potrzebne klasy i
    żeby można to było zrobić wielokrotnie.\r\n\r\nPoza tym, w settings raczej ciężko
    importować modele, bo plik jest przetwarzany jeszcze przed załadowaniem aplikacji."
- id: 24991
  author: forgems
  author_url: ''
  date: '2010-04-23 14:50:44 +0200'
  date_gmt: '2010-04-23 12:50:44 +0200'
  content: "a kto mówi o importowaniu modeli w settings ?\r\nw settings masz zdefiniowane
    tylko do jakiego konkretnego modelu ma się odwoływać inny model. I jest to napis."
- id: 24992
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-04-23 14:59:50 +0200'
  date_gmt: '2010-04-23 12:59:50 +0200'
  content: "forgems:\r\n\r\nNo możesz podać \"app.model\", ale dalej jesteś ograniczony
    do dokładnie jednej instancji każdego modelu.\r\n\r\nMoże ja ci tak na przykładzie:\r\n\r\n<pre>class
    MyFirstCategory(CategoryFactory()):\r\n    pass\r\n\r\nclass MyFirstProduct(ProductFactory(category=MyFirstCategory)):\r\n
    \   color = models.CharField(max_length=100)\r\n\r\nclass MyOtherCategory(CategoryFactory()):\r\n
    \   pass\r\n\r\nclass MyOtherProduct(ProductFactory(category=MyOtherCategory)):\r\n
    \   description = models.TextField(blank=True)</pre>"
- id: 24993
  author: forgems
  author_url: ''
  date: '2010-04-23 15:06:46 +0200'
  date_gmt: '2010-04-23 13:06:46 +0200'
  content: "Nadal nie wiem jaki to problem rozwiązuje ?\r\nDlaczego nie mozna tego
    tak zapisac?\r\n\r\n<pre>    class AbstractProduct(models.Model):\r\n        ....\r\n
    \       \r\n        abstract = True\r\n        \r\n    class MyFirstProduct(AbstractProduct):\r\n
    \       category=models.ForeignKey(MyCategory)\r\n        color = models.CharField(max_length=100)\r\n\r\n
    \   class MyOtherProduct(AbstractProduct):\r\n        category=models.ForeignKey(MyCategory)\r\n
    \       description = models.TextField(blank=True)</pre>"
- id: 24994
  author: forgems
  author_url: ''
  date: '2010-04-23 15:07:06 +0200'
  date_gmt: '2010-04-23 13:07:06 +0200'
  content: i jak tu włączyć formatowanie kodu ?:P
- id: 24995
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-04-23 15:16:47 +0200'
  date_gmt: '2010-04-23 13:16:47 +0200'
  content: "forgems:\r\n\r\nPrzeczytaj pierwszy akapit. Twoja propozycja to dokładnie
    jego ostatnie zdanie.\r\n\r\nCel jest taki, żeby uniwersalna aplikacja mogła polegać
    na tym, że istnieje pole \"category\" i że jest kluczem obcym. Właśnie dlatego
    nie chcę, żeby ktoś używając aplikacji musiał zdefiniować za każdym razem wszystkie
    brakujące pola z odpowiednimi nazwami i typami.\r\n\r\nHint: aplikacje oprócz
    modeli dostarczają widoków i te widoki zwykle chcą z pól korzystać."
- id: 25013
  author: 'Django: abstrakcji ciąg dalszy &laquo; Room 303'
  author_url: http://room-303.com/blog/2010/04/27/django-abstrakcji-ciag-dalszy/
  date: '2010-04-27 11:33:45 +0200'
  date_gmt: '2010-04-27 09:33:45 +0200'
  content: '[...] prze­ci­wień­stwie do poprzed­niego przy­kładu, pozwala uży­wać
    super() w abs­trak­cyj­nych kla­sach [...]'
---
<p>Zastanawialiśmy się ostatnimi czasy, w jaki sposób zbudować aplikację tak, by z jednej strony była uniwersalna (abstrakcyjne modele bazowe), a z drugiej zawierała całą niezbędną logikę. Problem polega na tym, że — z oczywistych względów — klucza obcego do modelu abstrakcyjnego stworzyć się nie da. Pozostaje więc zwalić pracę na programistę, który konkretyzuje abstrakcyjne prototypy, prawda?</p>

<p>Dzisiaj do głowy przyszło mi rozwiązanie może nie do końca ładne, ale na pewno działające. Fabryka abstrakcyjnych modeli:</p>

<pre><code class="python">from django.db import models

class AbstractModelMetaclass(type):
    def __new__(cls, name, bases, attrs):
        super_new = super(AbstractModelMetaclass, cls).__new__
        if bases == (object, ):
            return super_new(cls, name, bases, attrs)
        new_attrs = attrs.copy()
        module = attrs['__module__']
        new_cls = super_new(cls, name, bases, {'__module__': module})
        fields = getattr(new_cls, '_fields', {}).copy()
        for key, val in attrs.items():
            if key not in ['construct', '__new__']:
                fields[key] = val
        new_attrs['_fields'] = fields
        return super_new(cls, name, bases, new_attrs)

class AbstractModelFactory(object):
    __metaclass__ = AbstractModelMetaclass

    @staticmethod
    def construct():
        return {}

    def __new__(cls, *args, **kwargs):
        attrs = cls._fields.copy()
        attrs.update(cls.construct(*args, **kwargs))
        attrs['__module__'] = cls.__module__
        attrs['Meta'] = type('Meta', (), {'abstract': True})
        return type(cls.__name__, (models.Model, ), attrs)</code></pre>

<p>Idea jest taka, że implementując swoją podklasę fabryki modeli mamy możliwość zadecydować o polach, jakie trafią do ostatecznego modelu. Dla lepszego zrozumienia, rozważmy abstrakcyjne klasy produktu i kategorii:</p>

<pre><code class="python">class CategoryFactory(AbstractModelFactory):
    name = models.CharField(max_length=100)

    def __unicode__(self):
        return self.name

class ProductFactory(AbstractModelFactory):
    name = models.CharField(max_length=100)

    @staticmethod
    def construct(category):
        return {'category': models.ForeignKey(category)}

    def __unicode__(self):
        return u'%s / %s' % (self.category, self.name)</code></pre>

<p>Skonkretyzujmy klasy własną implementacją:</p>

<pre><code class="python">class MyCategory(CategoryFactory()):
    pass

class MyProduct(ProductFactory(category=MyCategory)):
    pass</code></pre>

<p>Upewnijmy się, że zależności działają prawidłowo:</p>

<pre><code class="python">from . import models

c = models.MyCategory(name='cat')
p = models.MyProduct(name='prod', category=c)
print p # 'cat / prod'</code></pre>

<p>Oczywiście — ktoś zaraz powie — to samo można uzyskać tworząc funkcję zwracającą klasę zdefiniowaną w jej ciele. Można, ale nie da się po niej wygodnie dziedziczyć (rozszerzenie istniejącej fabryki).</p>
