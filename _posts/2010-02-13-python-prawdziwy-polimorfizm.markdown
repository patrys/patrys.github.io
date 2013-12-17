---
layout: post
status: publish
published: true
title: 'Python: prawdziwy polimorfizm'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 799
wordpress_url: http://room-303.com/blog/?p=799
date: 2010-02-13 16:47:50.000000000 +01:00
categories:
- code
tags:
- python
comments: []
---
<p>Taki weekendowy żarcik:</p>

<pre><code class="python">#!/usr/bin/env python
import random

class Foo(random.choice([int, str, unicode, Exception])):
    pass

f = Foo('1')
print `f`</code></pre>
