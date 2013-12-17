---
layout: post
status: publish
published: true
title: 'Django: alternatywa dla Form.as_table()'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 643
wordpress_url: http://room-303.com/blog/?p=643
date: 2009-08-21 15:54:58.000000000 +02:00
categories:
- web
- code
tags:
- django
- python
- forms
comments:
- id: 24501
  author: Jachu
  author_url: http://agiler.net
  date: '2009-08-21 16:58:26 +0200'
  date_gmt: '2009-08-21 15:58:26 +0200'
  content: Standardowo as_table jest metodą dlatego, że wszystkie sposoby na proste
    wyświetlanie forma są jego metodami. To natomiast jest wymagane, by {{ form }}
    wyświetlało zawartość forma - gdzieś w definicji jest zaszyte, że form.__str__
    to wywołanie as_table.
- id: 24502
  author: Marek
  author_url: ''
  date: '2009-08-22 10:06:45 +0200'
  date_gmt: '2009-08-22 09:06:45 +0200'
  content: "tak widze ze sie znowu zacząłęś o django rozpisywać więc mam dla Ciebie
    quiz:\r\n\r\n\r\ndef jakisview(request):\r\n    [blah blah...]\r\n    s = { \r\n
    \        'foo' : 'barbar',\r\n         'foo2' : 'bee'\r\n         'RefNo.' : 9320,\r\n
    \   }\r\n    return render_to_response(\"t.html\", s)\r\n\r\n\r\nPytanie brzmi
    - jak w samym templacie dostac sie do wartosci 9320 ?\r\nInaczej mówiąc jak zmusić
    django do potraktowania kropki za RefNo jako nazwy klucza zamiast akcji?"
---
<p>Domyślna struktura generowana przez metodę <code>django.forms.Form.as_table</code> pozostawia nieco do życzenia. Stąd nieco wygodniejsza i nieinwazyjna wersja w postaci filtra (zastanawiam się, czemu ta wbudowana w Django ma postać metody):</p>

<pre><code class="python">from django.template.loader import render_to_string

@register.filter
def as_table(form):
    return render_to_string('form_as_table.html', {'form': form})</code></pre>

<p>Do kompletu przykładowy szablon:</p>

<pre><code class="django">{% for f in form %}
{% if f.errors %}
    &lt;tr class="{{ f.name }} errors"&gt;
        &lt;td colspan="2"&gt;
            &lt;div class="error"&gt;{{ f.errors }}&lt;/div&gt;
        &lt;/td&gt;
    &lt;/tr&gt;
{% endif %}
    &lt;tr class="{{ f.name }} {% if f.errors %}errors{% endif %}"&gt;
        &lt;th&gt;{{ f.label_tag }}:&lt;/th&gt;
        &lt;td&gt;
{% if f.help_text %}
            &lt;span&gt;{{ f.help_text }}&lt;/span&gt;
{% endif %}
            {{ f }}
        &lt;/td&gt;
    &lt;/tr&gt;
{% endfor %}</code></pre>
