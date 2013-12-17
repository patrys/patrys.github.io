---
layout: post
status: publish
published: true
title: 'Django hack: wiele domen i jedna instancja'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 599
wordpress_url: http://room-303.com/blog/?p=599
date: 2009-05-05 23:40:16.000000000 +02:00
categories:
- web
- software
- code
tags:
- django
- python
comments: []
---
<p>Pozwala serwować wiele domen za pomocą jednego tylko projektu Django. Inspiracją był <a href="http://www.djangosnippets.org/snippets/1099/">ten snippet</a>.</p>

<p>Zmiany w <code>settings.py</code>:</p>

<blockquote><pre><code>from threading import local

SITE_THREAD_INFO = local()
SITE_THREAD_INFO.SITE_ID = 1

class SiteIDHook(object):
    def __int__(self):
        return SITE_THREAD_INFO.SITE_ID
    def __hash__(self):
        return SITE_THREAD_INFO.SITE_ID

SITE_ID = SiteIDHook()</code></pre></blockquote>

<p>Nowa klasa middleware:</p>

<blockquote><pre><code>from django.conf import settings
from django.contrib.sites.models import Site
from django.http import HttpResponseRedirect

class MultiSiteMiddleware(object):
    def process_request(self, request):       
        settings.SITE_THREAD_INFO.SITE_ID = 0 # Fail by default

        host = request.META.get('HTTP_HOST').split(':')[0]
        if host:
            try:
                site = Site.objects.get(domain = host)
                settings.SITE_THREAD_INFO.SITE_ID = site.id
            except Site.DoesNotExist:
                return HttpResponseRedirect('http://example.com/')</code></pre></blockquote>

<p>Bonus &mdash; automatyczne fitrowanie obiektów:</p>

<blockquote><pre><code>from django.contrib.sites.models import Site
from django.db import models

def create_custom_manager(*args, **kwargs):
    class CustomManager(models.Manager):
        def get_query_set(self):
            return super(CustomManager, self).get_query_set().filter(*args, **kwargs)
    return CustomManager()

class Product(models.Model):
    site = models.ForeignKey(Site, default = Site.objects.get_current)
    # ...
    objects = create_custom_manager(site = Site.objects.get_current)</code></pre></blockquote>
