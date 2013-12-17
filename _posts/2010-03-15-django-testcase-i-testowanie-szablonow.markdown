---
layout: post
status: publish
published: true
title: 'Django: TestCase i testowanie szablonów'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 851
wordpress_url: http://room-303.com/blog/?p=851
date: 2010-03-15 18:03:55.000000000 +01:00
categories:
- web
- code
tags:
- django
- python
comments: []
---
<p>Bardzo brzydki hack, oparty o <a href="http://code.djangoproject.com/attachment/ticket/7611/7611.diff">załącznik do ticketu 7611</a>. Czyści wewnętrzny cache Django, ale pozwala testować działanie kodu opierającego się o renderowanie szablonów bez ryzyka, że aplikacja owe szablony nadpisze:</p>

<pre><code class="python">import os
import sys
from django.conf import settings
from django.template import loader
from django.test import TestCase

class TemplateTestCase(TestCase):
    def _pre_setup(self):
        self._template_setup()
        super(TemplateTestCase, self)._pre_setup()

    def _post_teardown(self):
        self._template_teardown()
        super(TemplateTestCase, self)._post_teardown()

    def _template_setup(self):
        if hasattr(self, 'template_loaders'):
            self._old_template_loaders = settings.TEMPLATE_LOADERS
            settings.TEMPLATE_LOADERS = self.template_loaders
            loader.template_source_loaders = None
        if hasattr(self, 'template_dirs'):
            self._old_template_dirs = settings.TEMPLATE_DIRS
            test_dir = os.path.dirname(sys.modules[self.__module__].__file__)
            settings.TEMPLATE_DIRS = [os.path.join(test_dir, dirname)
                                      for dirname in self.template_dirs]

    def _template_teardown(self):
        if hasattr(self, '_old_template_loaders'):
            settings.TEMPLATE_LOADERS = self._old_template_loaders
            loader.template_source_loaders = None
        if hasattr(self, '_old_template_dirs'):
            settings.TEMPLATE_DIRS = self._old_template_dirs</code></pre>

<p>Użycie:</p>

<pre><code class="python">class TestSomething(TemplateTestCase):
    template_loaders = ('django.template.loaders.app_directories.load_template_source',)

    def test_foo(self):
        pass</code></pre>
