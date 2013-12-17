---
layout: post
status: publish
published: true
title: 'Django: szybszy SQLite do testów'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 764
wordpress_url: http://room-303.com/blog/?p=764
date: 2010-01-22 13:18:37.000000000 +01:00
categories:
- web
- code
tags:
- django
- python
- sqlite
comments:
- id: 24786
  author: 'SQLite na partycji XFS &laquo; Mirumee Software: Let&#39;s keep geekin&#39;
    blog'
  author_url: http://mirumee.com/blog/2010/01/22/sqlite-na-partycji-xfs/
  date: '2010-01-22 14:07:37 +0100'
  date_gmt: '2010-01-22 13:07:37 +0100'
  content: '[...] znajdziecie na prywatnym blogu Patrysa       Delicious Wykop [...]'
---
<p>Domyślna konfiguracja SQLite każe mu synchronizować plik bazy po każdej operacji. W środowiskach testowych nie musimy się martwić o spójność danych w wypadku awarii, poniżej zamieszczam więc backend pozbawiony zbędnego narzutu:</p>

<pre><code class="python">from django.db.backends.sqlite3.base import (
    DatabaseWrapper as Sqlite3Wrapper,
    DatabaseError,
    IntegrityError,
    DatabaseFeatures,
    DatabaseOperations,
)

class DatabaseWrapper(Sqlite3Wrapper):
    def _cursor(self):
        new_conn = self.connection is None
        cursor = super(DatabaseWrapper, self)._cursor()
        if new_conn:
            cursor.execute('PRAGMA synchronous=OFF')
        return cursor</code></pre>

<p>W przypadku projektu, nad którym właśnie pracujemy, czas przebudowania bazy od nowa na partycji XFS <em>spadł z półtorej minuty do pięciu sekund</em>.</p>
