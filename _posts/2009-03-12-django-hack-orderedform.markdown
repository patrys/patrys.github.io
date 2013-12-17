---
layout: post
status: publish
published: true
title: 'Django hack: OrderedForm'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 559
wordpress_url: http://room-303.com/blog/?p=559
date: 2009-03-12 13:35:41.000000000 +01:00
categories:
- web
- software
- code
tags:
- django
- python
comments: []
---
<p>Ile razy ręcznie składałem formularz w szablonie tylko po to, żeby pola były we właściwej kolejności? Nie mam pojęcia, ale od jakiegoś czasu stosuję poniższe rozwiązanie. Tak, to jest jedna z tych notek <em>ku własnej pamięci</em>.</p>

<blockquote><pre><code>class OrderedForm(object):
	def __init__(self, *args, **kwargs):
		super(OrderedForm, self).__init__(*args, **kwargs)
		if hasattr(self.Meta, 'fields_order'):
			self.fields.keyOrder = self.Meta.fields_order</code></pre></blockquote>

<p>Po umieszczeniu powyższego w jakimś ustronnym wspólnym module można zabrać się za używanie:</p>

<blockquote><pre><code>from django.contrib.auth.models import User
from django import forms
from core.forms import OrderedForm

class UserNewForm(OrderedForm, forms.ModelForm):
	class Meta:
		model = User
		fields = ('first_name', 'last_name', 'username', 'password', 'email')
		fields_order = ('username', 'password', 'first_name', 'last_name', 'email')
	password = forms.CharField(label = u'Password', required = True, widget = forms.PasswordInput(attrs = {'autocomplete': 'off'}))</code></pre></blockquote>

<p>Trzeba zauważyć, że <code>OrderedForm</code> celowo nie dziedziczy po żadnej innej klasie Django, dzięki czemu równie dobrze działa z <code>forms.ModelForm</code>, co z <code>forms.Form</code>, jak i z dowolną własną (zgodną) implementacją.</p>
