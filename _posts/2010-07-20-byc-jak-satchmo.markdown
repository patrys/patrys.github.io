---
layout: post
status: publish
published: true
title: Być jak Satchmo
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 974
wordpress_url: http://room-303.com/blog/?p=974
date: 2010-07-20 17:20:30.000000000 +02:00
categories:
- code
tags:
- django
- python
- satchmo
comments:
- id: 25098
  author: trójkąt
  author_url: http://karbownicki.com/
  date: '2010-07-20 20:12:43 +0200'
  date_gmt: '2010-07-20 18:12:43 +0200'
  content: Zawsze jest jeszcze LFS - http://www.getlfs.com/
- id: 25099
  author: Remik
  author_url: ''
  date: '2010-07-21 00:42:52 +0200'
  date_gmt: '2010-07-20 22:42:52 +0200'
  content: "To naprawdę jest w satchmo? Ehh.\r\n\r\nJa mogę dodać jedno z czegoś innego:\r\n\r\n<pre>quantity
    = 0\r\nfor p in Products.objects.all():\r\n    quantity += p.quantity</pre>"
- id: 25100
  author: tas
  author_url: ''
  date: '2010-07-21 08:31:28 +0200'
  date_gmt: '2010-07-21 06:31:28 +0200'
  content: Tylko przy jednym projekcie próbowaliśmy zmusić satchmo do współpracy.
    Przy drugim już zabraliśmy się za pisanie własnego silnika sklepu - niesamowite
    jest, ile czasu udało się dzięki temu zaoszczędzić :)
- id: 25101
  author: DeeJay1
  author_url: http://princefool.blogspot.com/
  date: '2010-07-21 20:31:16 +0200'
  date_gmt: '2010-07-21 18:31:16 +0200'
  content: Aż boję się czytać ten kod, bo mi jeszcze wypali się w pamięci na zawsze…
- id: 25112
  author: slawek
  author_url: ''
  date: '2010-07-27 16:10:48 +0200'
  date_gmt: '2010-07-27 14:10:48 +0200'
  content: Bardzo fajne artykuly, ale przydaloby sie rownie wnikliwe spojrzenie w
    LFS z getlfs.com, bo wygląda sensowniej ale moze byc równie wielką miną co satchmo
- id: 25119
  author: owca
  author_url: ''
  date: '2010-08-03 01:45:06 +0200'
  date_gmt: '2010-08-02 23:45:06 +0200'
  content: uzywalem LFS w paru projektach i moge powiedziec,ze uruchomienie tego w
    porownaniu do satchmo jest pikusiem
- id: 27745
  author: Jaro
  author_url: http://techravings.com
  date: '2011-03-19 15:02:58 +0100'
  date_gmt: '2011-03-19 14:02:58 +0100'
  content: Korzystałem z LFS, nawet rozbudowałem go o kilka funkcjonalności (np. płatności
    przez platnosci.pl, promocje), poprawiłem też parę błędów i muszę przyznać, że
    funkcjonalność i kod są na prawdę w porządku. Minusem jest to, że rozbudowa wymaga
    ingerencji w kod projektu, co powoduje uciążliwe aktualizacje do kolejnych wersji
    lub nawet je uniemożliwia.
---
<p>Z pewnością naczytałeś się już, jakie to <a href="http://room-303.com/blog/2010/04/18/django-pinax-i-satchmo/">Satchmo nie jest doskonałe</a>, zazdrościsz i chciałbyś stworzyć coś równie wspaniałego. Dość jednak nieprzespanych nocy, albowiem przygotowałem krótki poradnik, który w kilku krokach pozwoli ci dorównać mistrzom.</p>

<h3>Sięgaj tam, gdzie import nie sięga</h3>

<p>Tak jest, zacznij od stworzenia modułu z myślnikiem w nazwie. Niestety, oczywista nazwa <code>email-auth.py</code> została już zajęta — musisz się bardziej wysilić. Znajomym oczy wypadną z zazdrości, gdy tylko pierwszy raz zobaczą:</p>

<pre><code class="python">hahaha = __import__('pokonalem-was', globals(), locals(), [], -1)</code></pre>

<h3>Uatrakcyjniaj pętle</h3>

<p>Od dawna wiadomo już, że przedwczesna optymalizacja jest złem, naszą odpowiedzią będzie zatem <q>przedwczesna dezoptymalizacja</q>! Oto przykład atrakcyjnego wyświetlenia listy:</p>

<pre><code class="django">{% raw %}{% for product in products %} 
    {% if forloop.first %} &lt;ul&gt;  {% endif %}
        &lt;li&gt;{% thumbnail product.main_image.picture 85x85 as image %}
        &lt;a href="{{ product.get_absolute_url }}">&lt;img src="{{ image }}" width="{{ image.width }}" height="{{ image.height }}" /&gt;&lt;/a&gt;
        &lt;a href="{{ product.get_absolute_url }}">{{ product.translated_name }}&lt;/a&gt;&lt;/li&gt;
    {% if forloop.last %} &lt;/ul&gt; {% endif %}
{% endfor %}{% endraw %}</code></pre>

<p>Tylko wyobraź sobie ich miny! Jeśli chcesz przeskoczyć mistrza, spróbuj przenieść kod do Pythona:</p>

<pre><code class="python">for counter, product in enumerate(products):
    if counter == 0:
        print '&lt;ul&gt;'
    # ...i tak dalej</code></pre>

<h3>Nie daj się zaszufladkować</h3>

<p>Nie łudźmy się — przestrzenie nazw są dla frajerów. Bez ceregieli pakuj wszystko w ścieżkę Pythona i upewnij się, że tak właśnie importujesz swoje moduły. Pokaż, że jesteś ważniakiem i twórz moduły o jak najogólniejszych nazwach. Naucz fajansów pokory, tych kilka dodatkowych wpisów w <code>PYTHONPATH</code> ich nie zabije. Mogą to zrobić konflikty, ale jeśli chcą używać czegoś ponad twój framework, to sami są sobie winni i zasłużyli na karę.</p>

<pre>export PYTHONPATH=~/web/satchmo/satchmo/apps</pre>

<h3>Unikaj biurokracji</h3>

<p>Po co męczyć się z formularzami, gdy do wszystkiego sięgnąć można już w widoku? Niezwykle istotne jest tu unikanie <code>request.REQUEST</code>.</p>

<pre><code class="python">if request.method=="POST":
    reqdata = request.POST
else:
    reqdata = request.GET

if reqdata.has_key('quantity'):
    try:
        quantity = round_decimal(reqdata['quantity'], places=2, roundfactor=.25)
    except RoundedDecimalError:
        quantity = Decimal('1.0')
        log.warn("Could not parse a decimal from '%s', returning '1.0'", reqdata['quantity'])
else:
    quantity = Decimal('1.0')</code></pre>

<p>Jeśli już musisz użyć formularza, upewnij się, że upakujesz wszystkie, niezwiązane ze sobą grupy pól w jednej dużej klasie. Dzięki temu zaoszczędzisz sobie kilka wywołań <code>is_valid()</code> i jednocześnie udaremnisz wszelkie próby innego wykorzystania poszczególnych części przez te niedorozwoje, które mają czelność importować twoje klasy.</p>

<h3>Wyznaczaj nowe trendy</h3>

<p>Przez takich jak oni, programowanie obiektowe stoi praktycznie w miejscu. Pokaż im nowe sztuczki, takie jak zastąpienie rozszerzania klas nadpisywaniem funkcji w locie¹:</p>

<pre><code class="python">def confirm_info(request, template='shop/checkout/protx/confirm.html', extra_context={}):
    payment_module = config_get_group('PAYMENT_PROTX')
    controller = confirm.ConfirmController(request, payment_module)
    controller.templates['CONFIRM'] = template
    controller.extra_context = extra_context
    controller.onForm = secure3d_form_handler
    controller.confirm()
    return controller.response</code></pre>

<p><small>¹ W rzeczywistości <code>ConfirmController.onForm</code> jest w konstruktorze klasy ustawiany na <code>ConfirmController._onForm</code>, co można uznać za architekturę po dwakroć lepszą.</small></p>

<h3>Parametry dobieraj z rozmachem</h3>

<p>Piękno tkwi w różnorodności. Upewnij się zatem, że wyczerpiesz wszelkie metody osiągnięcia tego samego celu.</p>

<pre><code class="python">class ProductImage(models.Model):
    # ...
    picture = ImageWithThumbnailField(verbose_name=_('Picture'),
        upload_to="__DYNAMIC__",
        name_field="_filename",
        max_length=200)
    # ...


class ImageWithThumbnailField(ImageField):
    # ...
    def __init__(self, verbose_name=None, name=None,
                 width_field=None, height_field=None,
                 auto_rename=NOTSET, name_field=None, 
                 upload_to=upload_dir, **kwargs):
        # ...
        if upload_to == "__DYNAMIC__":
            upload_to = upload_dir
        # ...</code></pre>

<h3>Bądź elastyczny</h3>

<p>Teraz twój sklep znajduje się w Polsce, ale kto wie, co będzie <em>po</em> obiedzie? Upewnij się, że cała konfiguracja może być edytowana w locie. Zwłaszcza te jej fragmenty, które wymagają restartu aplikacji. To jedna z wielu sztuczek, które zapewnią ci popularność w branży. Co prawda dawni przyjaciele zazdroszczą ci już do tego stopnia, że przestali się do ciebie odzywać, ale i tak nie tęsknisz po tych prostakach. Od teraz twoim jedynym przyjacielem jest aplikacja <a href="http://bitbucket.org/bkroeze/django-livesettings/">django-livesettings</a>. Na innych nie masz szans, bo przyjaciół poznaje się w biedzie, a ty przecież właśnie zyskałeś umiejętności, dzięki którym praktycznie już jesteś bogaty.</p>
