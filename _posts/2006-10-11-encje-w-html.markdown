---
layout: post
status: publish
published: true
title: Encje w HTML
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 295
alias: /blog/2006/10/11/encje-w-html/
date: 2006-10-11 22:34:12.000000000 +02:00
categories:
- web
- code
tags: []
comments:
- id: 4923
  author: Roy
  author_url: ''
  date: '2006-10-12 11:08:47 +0200'
  date_gmt: '2006-10-12 10:08:47 +0200'
  content: "Dzięki, to jest odpowiedź na nurtujące mnie ostatnio pytania!\r\n\r\nRoy"
- id: 4924
  author: medyk
  author_url: http://www.medikoo.com
  date: '2006-10-12 11:18:39 +0200'
  date_gmt: '2006-10-12 10:18:39 +0200'
  content: "Tak się zastanawiam nad polskimi nazwami. Po angielsku mamy DOMElement
    (element) i DOMNode (node) czyli w bezpośrednim tłumaczeniu element i węzeł..
    czy zatem mówienie element tekstowy jest poprawne? Ja staram się trzymać terminów
    węzeł i element ale sam sobie to przyjąłem, nie wiem jakie są tradycje w naszym
    światku - będę wdzięczny za jakiekolwiek spostrzeżenia na ten temat.\r\n\r\nInna
    sprawa w XML'u zapisywanym w utf-8 wystarczy, że zamienisz na encje '' oraz '&amp;'
    w węzłach tekstowych, oraz dodatkowo '\"' w wartościach atrybutów. \r\nZ tego
    co mi wiadomo nic więcej zamieniać nie trzeba i idealnie do tego nadaje się funkcja
    htmlspecialchars, która zmienia to i nic więcej, jeśli się ją o to ładnie poprosi:\r\nW
    pierwszym przypadku wywoływana tak:\r\nhtmlspecialchars($tekst, ENT_NOQUOTES,
    'utf-8')\r\nW drugim tak:\r\nhtmlspecialchars($tekst, 2, 'utf-8')"
- id: 4925
  author: medyk
  author_url: http://www.medikoo.com
  date: '2006-10-12 11:20:04 +0200'
  date_gmt: '2006-10-12 10:20:04 +0200'
  content: aha.. ucieło zacytowane znaki w komentarzu.. czy tutaj muszę wpisywać encje?
    :)
- id: 4926
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-10-12 11:26:47 +0200'
  date_gmt: '2006-10-12 10:26:47 +0200'
  content: "medyk:\r\n\r\nNapisałem na początku \"w skrócie,\" dlatego nie chciałem
    rozróżniać węzłów od elementów, bo musiałbym przy okazji całe drzewo DOM opisać.\r\n\r\nW
    XML z UTF-8 cytowania wymagają właściwie tylko wartości atrybutów, bo węzły można
    zamienić z typu PDATA w typ CDATA i nie wymagają wtedy absolutnie żadnego zabiegu.\r\n\r\nJa
    cytuję wszystkie encje XML dla czytelności kodu wynikowego - mogę np. gołym okiem
    w źródle wyłapać koniec elementu nawet bez kolorowania składni (czasem nieocenione
    przy debugowaniu wywołań RPC)."
- id: 4928
  author: neo
  author_url: http://neo.mlodzi.pl
  date: '2006-10-15 10:17:11 +0200'
  date_gmt: '2006-10-15 09:17:11 +0200'
  content: IMO syntax error. Nieładnie zamykać apostrof w apostrofach.
---
<p>Na prośbę Roya:</p>

<p><abbr title="(Extensible) HyperText Markup Language">(X)HTML</abbr> w skrócie definiuje dokument jako zestaw elementów. Każdy element to albo <code>textNode</code>, albo <q>kontener</q> — typowy element, jak nagłówek, paragraf, czy <code>span</code>, który zawiera kolejne elementy.</p>

<p>Elementy są czasem błędnie nazywane <q>tagami,</q> podczas gdy tagi to sposób tekstowego zapisu elementów — składają się wtedy z tagów otwierającego i zamykającego (albo jednego samozamykającego w przypadku elementów, które nie zawierają żadnych <q>dzieci</q>).</p>

<p>Wszytkie elementy, poza tekstowymi, posiadają różne atrybuty. Te ostatnie zapisuje się jako listę par <code>nazwa="wartość"</code> wewnątrz tagu otwierającego element. Teraz ważne: ponieważ <abbr>HTML</abbr> jest aplikacją <abbr title="Standard Generalized Markup Language">SGML</abbr> (trudne słowo), a <abbr>XHTML</abbr> jest aplikacją <abbr title="xtensible Markup Language">XML</abbr> (jeszcze trudniejsze słowo), <strong>wartości atrybutów w zapisie trzeba cytować za pomocą encji</strong>.</p>

<p>Ponieważ <abbr>HTML</abbr> definiuje encji masę, a <abbr>XHTML</abbr> dziedziczy ich po <abbr>XML</abbr> tylko pięć, to cytować powinno się tylko te ostatnie (inaczej nie można przetwarzać wyniku jako dokumentu <abbr>XML</abbr>).</p>

<p>Oto więc lista kandydatów: <code>&amp;amp;</code>, <code>&amp;lt;</code>, <code>&amp;gt;</code>, <code>&amp;quot;</code>, <code>&amp;apos;</code>.</p>

<p>Ponieważ w <abbr title="PHP Hypertext Preprocessor">PHP</abbr> funkcja <code>html_entities</code> jest mocno nadgorliwa, poniżej prosta implementacja poprawnej alternatywy:</p>

<blockquote><pre><code>function xmlentities($string)
{
	return str_replace(array
		(
			'&amp;', ''', '"', '&lt;', '&gt;'
		), array
		(
			'&amp;amp;', '&amp;#039;', '&amp;quot;', '&amp;lt;', '&amp;gt;'
		), $string);
}</code></pre></blockquote>

<p>Apostrof jest traktowany specjalnie, bo w <abbr>HTML</abbr> go… nie przewidzieli.</p>

Technorati Tags: <a href="http://technorati.com/tag/html" rel="tag">html</a>, <a href="http://technorati.com/tag/xhtml" rel="tag">xhtml</a>, <a href="http://technorati.com/tag/xml" rel="tag">xml</a>, <a href="http://technorati.com/tag/entities" rel="tag">entities</a>, <a href="http://technorati.com/tag/encoding" rel="tag">encoding</a>
