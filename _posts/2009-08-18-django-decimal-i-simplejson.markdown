---
layout: post
status: publish
published: true
title: 'Django: Decimal i simplejson'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 640
wordpress_url: http://room-303.com/blog/?p=640
date: 2009-08-18 12:01:37.000000000 +02:00
categories:
- web
- code
tags:
- django
- python
- json
comments: []
---
<p>Moduł <code>django.utils.simplejson</code> nie obsługuje domyślnie typu <code>decimal.Decimal</code>. Na szczęście da się podać własny mechanizm kodowania nieznanych typów:</p>

<pre><code class="python">import decimal

def json_encoder(value):
    if isinstance(value, decimal.Decimal):
        return float(str(value))
    else:
        raise TypeError

from django.utils import simplejson

print simplejson.dumps([decimal.Decimal('1.2')], default=json_encoder)</code></pre>
