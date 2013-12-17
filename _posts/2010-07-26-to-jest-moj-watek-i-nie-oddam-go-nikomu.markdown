---
layout: post
status: publish
published: true
title: To jest mój wątek i nie oddam go nikomu
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 991
wordpress_url: http://room-303.com/blog/?p=991
date: 2010-07-26 16:53:26.000000000 +02:00
categories:
- code
tags:
- django
- python
- satchmo
comments:
- id: 25107
  author: Sayane
  author_url: ''
  date: '2010-07-26 17:15:57 +0200'
  date_gmt: '2010-07-26 15:15:57 +0200'
  content: Co do usera - nie ma się co czepiać. User i request z każdym zapytaniem
    ustawiane są na nowo przez middleware, więc nie ma problemu (znany trick w django).
    O wiele ciekawiej wygląda sprawa "taxer'a" właśnie. Prawdopodobnie jest to luka
    bezpieczeństwa. Co do tego skąd pochodzi, to wiem już z blipa, także pozostawię
    innym szansę :)
- id: 25108
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-07-26 17:29:03 +0200'
  date_gmt: '2010-07-26 15:29:03 +0200'
  content: Ja się nie czepiam usera i requesta, chociaż to potworne pogwałcenie separacji
    warstw aplikacji. Paskudztwo owo załączyłem dla pokazania kontekstu (taxer odwołuje
    się do tego kodu).
- id: 25109
  author: Sayane
  author_url: ''
  date: '2010-07-26 17:37:46 +0200'
  date_gmt: '2010-07-26 15:37:46 +0200'
  content: Zgłosiłeś im to chociaż? Kurcze, kilka sekund grzebania w kodzie i już
    następny kwiatek. Kurcze, jak oni to robią ...
- id: 25110
  author: Sayane
  author_url: ''
  date: '2010-07-26 17:43:11 +0200'
  date_gmt: '2010-07-26 15:43:11 +0200'
  content: Ano z tego co widzę, to zgłosiłeś. Wybacz, ale mam dzisiaj kiepski dzień
    i robię się upierdliwy :) Sorry za powtórzenie ("Kurcze").
- id: 25115
  author: Mekk
  author_url: http://notatnik.mekk.waw.pl
  date: '2010-07-30 14:36:41 +0200'
  date_gmt: '2010-07-30 12:36:41 +0200'
  content: "Te threadlocale ustawiane przez middleware to dość popularny idiom (np.
    pylonsy to mocno stosowały choć po troszku odchodzą), ma to pewne zalety (unika
    się wszechzaśmiecania api obiektami typu request czy session). taxer .... ech.\r\n\r\nCałe
    s*****o tak wygląda?"
- id: 25116
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-07-30 14:39:52 +0200'
  date_gmt: '2010-07-30 12:39:52 +0200'
  content: "Mekk:\r\n\r\nZ punktu widzenia architektury oprogramowania, threadlocal
    niczym nie różni się od zmiennej globalnej. Powiedziałbym, że to nie tyle popularne
    rozwiązanie, co częsty błąd w założeniach.\r\n\r\nCo do drugiego pytania: całe
    może nie, ale większość kodu autorstwa niejakiego Bruce'a."
- id: 25117
  author: Jakub Piotr Cłapa
  author_url: http://jpc.jogger.pl
  date: '2010-07-30 20:33:24 +0200'
  date_gmt: '2010-07-30 18:33:24 +0200'
  content: Tak jak mówisz threadlocal to jest zmienna globalna, ale bez wad zmiennej
    globalnej. Nie wydaje mi się, żeby (rozsądne) ich stosowanie było niewskazane.
---
<p>Bezstanowość protokołu HTTP jest faktem. Niezależnie od tego, czego chciałby autor danej aplikacji. Na przykład nie jest prawdą, że jeden proces lub wątek serwera jest przypisany jednemu, konkretnemu odwiedzającemu stronę. Wybaczcie zatem łzy, które zakręciły mi się w oczach na widok tego:</p>

<pre><code class="python">def _get_taxprocessor(request=None):
    taxprocessor = get_thread_variable('taxer', None)
    if not taxprocessor:
        if request:            
            user = request.user
            if user.is_authenticated():
                user = user
            else:
                user = None
        else:
            user = get_current_user()

        taxprocessor = get_tax_processor(user=user)    
        set_thread_variable('taxer', taxprocessor)
        
    return taxprocessor</code></pre>

<p>Dalej był już tylko płacz:</p>

<pre><code class="python">def get_current_user():
    user = get_thread_variable('user', None)
    if user != None: return user
    req = get_current_request()
    if req == None: return None
    return req.user</code></pre>

<p>I zgrzytanie zębów:</p>

<pre><code class="python">from threading import local

_threadlocals = local()

def set_current_user(user):
    set_thread_variable('user', user)

def set_thread_variable(key, var):
    setattr(_threadlocals, key, var)
    
def get_thread_variable(key, default=None):
    return getattr(_threadlocals, key, default)

def get_current_request():
    return get_thread_variable('request', None)</code></pre>

<pre><code class="python">class ThreadLocalMiddleware(object):
    """Middleware that gets various objects from the
    request object and saves them in thread local storage."""

    def process_request(self, request):
        set_thread_variable('request', request)
        set_current_user(request.user)</code></pre>

<p>Pytanie-zagadka: co się stanie z podatkiem, gdy ten sam wątek serwera obsłuży innego użytkownika? Pytanie pomocnicze: skąd może pochodzić ów kod?</p>

<p>Otrzymujesz <em>k3</em> Punkty Obłędu. Jeśli całkowita liczba zebranych punktów wynosi 6 lub więcej, rozpatrz test nabycia trwałej choroby psychicznej zgodnie z procedurą opisaną w rozdziale <em>Obłęd</em> podręcznika.</p>
