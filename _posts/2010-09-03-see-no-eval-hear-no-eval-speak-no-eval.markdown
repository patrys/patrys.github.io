---
layout: post
status: publish
published: true
title: See no eval, hear no eval, speak no eval
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 1060
wordpress_url: http://room-303.com/blog/?p=1060
date: 2010-09-03 17:51:31.000000000 +02:00
categories:
- web
- code
tags:
- python
- facebook
comments:
- id: 25166
  author: Głupi
  author_url: ''
  date: '2010-09-04 15:01:35 +0200'
  date_gmt: '2010-09-04 13:01:35 +0200'
  content: A mógłbyś troche wyjaśnić tak żeby ci głupsi mogli sie też czegos nauczyc?
- id: 25167
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-09-04 15:13:33 +0200'
  date_gmt: '2010-09-04 13:13:33 +0200'
  content: "Wyjaśniam:\r\n\r\nEwaluacja jest zła i powinno się jej unikać jak ognia."
- id: 25168
  author: crackcomm
  author_url: http://www.lukaszkurowski.pl
  date: '2010-09-04 19:29:30 +0200'
  date_gmt: '2010-09-04 17:29:30 +0200'
  content: Rozumiem, że eval jest zły dlatego, że łatwo jest wstrzyknąć 'złośliwy'
    kod ?
- id: 25169
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-09-04 19:33:56 +0200'
  date_gmt: '2010-09-04 17:33:56 +0200'
  content: eval jest zły, bo nigdy nie jest właściwym rozwiązaniem, uczy potencjalnie
    niebezpiecznych praktyk (stąd rodzą się potworki w rodzaju JSONP) i nie pozwala
    na podstawie kodu określić, jak zachowuje się program.
- id: 25218
  author: owca
  author_url: ''
  date: '2010-10-22 12:32:10 +0200'
  date_gmt: '2010-10-22 10:32:10 +0200'
  content: Ostatnio udalo mi sie uniknac implementacji fejsbukowego api, ale poszukiwania
    czegos dzialajacego tez zajely mi wczesniej dluzsza chwile. A sprawdzales te django-facebookconnect,
    django-facebook-oauth i django-socialauth ?
- id: 25219
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-10-22 12:39:44 +0200'
  date_gmt: '2010-10-22 10:39:44 +0200'
  content: "owca:\r\n\r\nNie sprawdzałem, bo potrzebowałem korzystać z pełnego API,
    nie samego logowania."
- id: 25249
  author: trunk
  author_url: ''
  date: '2010-11-21 23:58:20 +0100'
  date_gmt: '2010-11-21 22:58:20 +0100'
  content: niby wszystko fajnie, tylko zniknela polowa kodu m.in "get_facebook_client"
    i bez tutoriala ciezko teraz tego uzywac
- id: 25250
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-11-22 00:01:36 +0100'
  date_gmt: '2010-11-21 23:01:36 +0100'
  content: "trunk:\r\n\r\nKlienta dostajesz z obiektem <code>request</code>. Nie potrzeba
    do tego żadnych specjalnych funkcji. Jeśli nie masz requesta, użyj konstruktora
    klasy <code>Facebook</code>. Używanie thread locals to zło."
- id: 25251
  author: trunk
  author_url: ''
  date: '2010-11-22 18:28:40 +0100'
  date_gmt: '2010-11-22 17:28:40 +0100'
  content: cool :) A czy moglbys jeszcze sie podzielic jak uzywac tego jako samodzielnej
    a nie fejsbukowej aplikacji ? facebook.login_required automatycznie przenosi na
    strone fb a po zalogowaniu przerzuca do callback url. Czy nalezy sprawdzic sobie
    'zalogowanie' w sesji i kierowac do templejta z logowaniem czy jeszcze jakos inaczej
    ?
- id: 25252
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-11-22 22:38:18 +0100'
  date_gmt: '2010-11-22 21:38:18 +0100'
  content: Dekoratory dedykowane są dla aplikacji webowych, ale nic nie stoi na przeszkodzie,
    żeby sprawdzać <code>request.facebook.uid</code> i odpowiednio oferować własne
    logowanie. Można też użyć <code>require_oauth</code> (zakładam, że używasz aktualnego
    kodu z https://github.com/mirumee/pyfacebook).
---
<p>Choć sam konta w <a href="http://www.facebook.com/">Książeczce Maryja</a> nie posiadam, przyszło mi ostatnio ścierać się z ichnim API, coby dla klienta wdrożenia poczynić. Po przejrzeniu dostępnych bibliotek (w tym dość żałosnego <a href="http://github.com/facebook/python-sdk/">python-sdk</a>), stanęło na dość popularnym projekcie <em>pyfacebook</em>.</p>

<p>Oryginalne repozytorium było wybrakowane pod względem funkcjonalności, wybraliśmy więc fork, który z pewnością stworzył fan Władcy Pierścieni. Jak się miało później okazać, "jeden, by wszystkie zgromadzić i w ciemności związać" dość wiernie oddaje uzyskany efekt.</p>

<p>Człowiek głupi, to przy pierwszym problemie zajrzał w bebechy ofiary. Po tym stanął jak wryty i całe Satchmo przeleciało mu przed oczami. Na początek tradycyjny problem — przejście się w glanach po separacji warstw:</p>

<pre><code class="python">from threading import local

_thread_locals = local()</code></pre>

<pre><code class="python">def get_facebook_client():
    """
    Get the current Facebook object for the calling thread.

    """
    try:
        return _thread_locals.facebook
    except AttributeError:
        raise ImproperlyConfigured('Make sure you have the Facebook middleware installed.')</code></pre>

<pre><code class="python">class FacebookMiddleware(object):
    """
    Middleware that attaches a Facebook object to every incoming request.
    The Facebook object created can also be accessed from models for the
    current thread by using get_facebook_client().

    callback_path can be a string or a callable.  Using a callable lets us
    pass in something like lambda reverse('our_canvas_view') so we can follow
    the DRY principle.
    """
    # ...

    def process_request(self, request):
        # ...
        _thread_locals.facebook = request.facebook = Facebook(self.api_key,
                self.secret_key, app_name=self.app_name,
                callback_path=callback_path, internal=self.internal,
                proxy=self.proxy, app_id=self.app_id, oauth2=self.oauth2)</code></pre>

<p>Przerażające konstrukcje zaczęły się jednak później:</p>

<pre><code class="python"># generate the Facebook proxies
def __generate_proxies():
    for namespace in METHODS:
        methods = {}

        for method, param_data in METHODS[namespace].iteritems():
            methods[method] = __generate_facebook_method(namespace, method, param_data)

        proxy = type('%sProxy' % namespace.title(), (Proxy,), methods)

        globals()[proxy.__name__] = proxy

__generate_proxies()</code></pre>

<pre><code class="python">class Facebook(object):
    """
    Provides access to the Facebook API.

    ...
    """

    def __init__(self, api_key, secret_key, auth_token=None, app_name=None,
                 callback_path=None, internal=None, proxy=None,
                 facebook_url=None, facebook_secure_url=None,
                 generate_session_secret=0, app_id=None, oauth2=False):
        # ...
        for namespace in METHODS:
            self.__dict__[namespace] = eval('%sProxy(self, \'%s\')' % (namespace.title(), 'facebook.%s' % namespace))</code></pre>

<p>Skończyło się na własnym forku i refaktoryzacji tych i wielu innych fragmentów kodu. Poprawioną wersję można znaleźć <a href="http://github.com/mirumee/pyfacebook">na GitHubie</a>.</p>

<p>Na koniec stare powiedzenie ludowe:</p>

<blockquote><p>Gdy bowiem zoczysz, iż jest coś narzeczy, a za cwanego masz się i uważasz <code>__globals__</code> i <code>eval()</code> za sprawy rozwiązanie, mylisz się wielce, przeto idź przypudrować nos¹.</p></blockquote>

<p><small>¹ <cite><a href="http://pl.wikiquote.org/wiki/Cia%C5%82o_(film)">Ciało</a></cite>, 2003</small></p>
