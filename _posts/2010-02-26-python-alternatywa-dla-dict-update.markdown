---
layout: post
status: publish
published: true
title: 'Python: alternatywa dla dict.update'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 835
wordpress_url: http://room-303.com/blog/?p=835
date: 2010-02-26 16:42:15.000000000 +01:00
categories:
- code
tags:
- python
comments:
- id: 24852
  author: maniel
  author_url: ''
  date: '2010-02-26 22:01:19 +0100'
  date_gmt: '2010-02-26 21:01:19 +0100'
  content: "ładne, magia pythona, w ruby tak się nie da, ale jest mniej wyszukana,
    ale IMHO bardziej elegancka metoda:\r\nbar.merge(baz)"
- id: 24858
  author: damcyk
  author_url: ''
  date: '2010-03-01 09:00:49 +0100'
  date_gmt: '2010-03-01 08:00:49 +0100'
  content: yyy, a co jest nie tak z dict(bar, **baz) ?
- id: 24859
  author: Norbert
  author_url: http://pithyless.com
  date: '2010-03-01 17:05:52 +0100'
  date_gmt: '2010-03-01 16:05:52 +0100'
  content: "&gt; Korzystając ze skrótów zawsze upew nij się, że na \r\n&gt; pierw
    szy rzut oka wiadomo, co dany kod robi.\r\n\r\nHaha! Podoba mi się uwaga. :-)"
---
<p>Kolejny skrót. Dość regularny przypadek zwrócenia sumy słowników bez niszczenia któregokolwiek z nich:</p>

<pre><code class="python">def foo(bar, baz):
    tmpdict = dict(bar)
    tmpdict.update(baz)
    return tmpdict</code></pre>

<p>Można również rozwiązać inaczej, korzystając z faktu, że <code>dict</code> akceptuje nazwane parametry:</p>

<pre><code class="python">def foo(bar, baz):
    return dict(bar, **baz)</code></pre>

<p>Korzystając ze skrótów zawsze upewnij się, że na pierwszy rzut oka wiadomo, co dany kod robi.</p>
