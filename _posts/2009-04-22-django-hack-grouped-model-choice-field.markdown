---
layout: post
status: publish
published: true
title: 'Django hack: Grouped Model Choice Field'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 592
wordpress_url: http://room-303.com/blog/?p=592
date: 2009-04-22 11:05:40.000000000 +02:00
categories:
- web
- software
- code
tags:
- django
- python
comments:
- id: 24431
  author: tamok
  author_url: ''
  date: '2009-04-22 12:55:51 +0200'
  date_gmt: '2009-04-22 11:55:51 +0200'
  content: "Ciekawe, ale efekt końcowy - przynajmniej w przykładzie niezbyt czytelny
    w praktyce, bo nie widać, co zostało wybrane (jaki rozmiar). No i przy większej
    ilości opcji zrobi się bałagan. \r\nBardziej elegancko byłoby coś mieszanego (niekoniecznie
    dwa selecty) w tym stylu (radio - drodown): http://tinyurl.com/c43t9a gdzie po
    wybraniu rozmiaru ujawniałby się dropdown z jemu przynależnymi kolorami (ale to
    już chyba bardziej ajaksowe rozwiązanie)"
- id: 24432
  author: Patrys
  author_url: http://room-303.com/
  date: '2009-04-22 13:00:29 +0200'
  date_gmt: '2009-04-22 12:00:29 +0200'
  content: "tamok:\r\n\r\nMylisz AJAX z JavaScriptem. JS nie powinien być wymagany
    do działania aplikacji."
- id: 24434
  author: riddle
  author_url: http://riddle.pl
  date: '2009-04-22 15:07:19 +0200'
  date_gmt: '2009-04-22 14:07:19 +0200'
  content: "No i teraz to Twoje rozwiązanie najlepiej w JS rozdzielić na radiobutton
    (względnie coś selectable) i select. Bądź zbudować jeszcze inny interfejs, a wszystko
    wysyłać przez Twój formularz.\r\n\r\nProgressive enhancement FTW."
- id: 24435
  author: tamok
  author_url: ''
  date: '2009-04-22 15:13:23 +0200'
  date_gmt: '2009-04-22 14:13:23 +0200'
  content: "Oczywiście ferszteje, chodziło mi o to, że to takie ajaksowe zadziałanie
    byłoby. \"Wyberam opcję i na stronie pojawiają mi się schowane elementy bez potrzeby
    odświeżania\". Bez JS się nie da.\r\nDlatego twoja metoda jest jedyną dobrą, tyle,
    że znika (z oczu) rozmiar po wybraniu koloru, ewentualnie w praktyce potrzebny
    byłby jakiś def, który uzupełniałby nazwy kolorów w stylu \"niebieski(XXL). \r\nBo
    jak rozmiarów i kolorów zrobi się więcej to potencjalna klientka-dziunia już cała
    głupia będzie jakiego wypasionego szerta wybrała dla swojego fakola..."
---
<p>Przypuśćmy, że nasza aplikacja pozwala kupić koszulkę. Dostępne kolory zależą od rozmiaru i trzeba pozwolić je jakoś wybrać. Dwa <code>select</code>y? Będzie się dało wybrać nieistniejącą kombinację. Łączony select? Nieczytelnie, chyba że&hellip;</p>

<blockquote><label>To tylko przykład: <select><optgroup label="M"><option>biały</option><option>niebieski</option></optgroup><optgroup label="XL"><option>czerwony</option><option>niebieski</option><option>żółty</option></optgroup></select></label></blockquote>

<p>Poniższe rozwiązanie używa klasy <code>GroupedSelect</code> <a href="http://www.djangosnippets.org/snippets/200/">pochodzącej z Django Snippets</a>.</p>

<blockquote><pre><code>from django.forms import ModelChoiceField, ValidationError
from django.forms.util import smart_unicode
from django.utils.itercompat import groupby
from operator import attrgetter

class GroupedModelChoiceIterator(object):
    def __init__(self, field, grouper):
		self.field = field
		self.queryset = field.queryset
		self.grouper = grouper

    def __iter__(self):
		if self.field.empty_label is not None:
			yield (None, ((u'', self.field.empty_label), ))
		for grouper, items in groupby(self.queryset.all(), attrgetter(self.grouper)):
			yield (unicode(grouper), tuple((o.pk, unicode(o)) for o in items))

class GroupedModelChoiceField(ModelChoiceField):
	def __init__(self, field, widget = GroupedSelect, *args, **kwargs):
		self._field = field
		super(GroupedModelChoiceField, self).__init__(widget = widget, *args, **kwargs)

	def _get_choices(self):
		return GroupedModelChoiceIterator(self, self._field)

	choices = property(_get_choices, None)
		
	def clean(self, value):
		"""
		Validates that the input is in self.choices.
		"""
		if value in (None, ''):
			value = u''
		value = smart_unicode(value)
		valid_values = \[\]
		for group_label, group in self.choices:
			valid_values += [str(k) for k, v in group]
		if value not in valid_values:
			raise ValidationError(u'Select a valid choice. That choice is not one of the available choices.')
		return super(GroupedModelChoiceField, self).clean(value)</code></pre></blockquote>

<p>Przykład (zakładając, że <code>color</code> jest referencją na obiekt, który posiada pole <code>size</code>):</p>

<blockquote><code><pre>class SizeAndColorForm(forms.ModelForm):
	class Meta:
		model = Product
		fields = ['color']
	color = GroupedModelChoiceField(field = 'size', label = u'size/color')</pre></code></blockquote>
