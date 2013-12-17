---
layout: post
status: publish
published: true
title: Rhythmbox i trzeszcząca muzyka
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 426
wordpress_url: http://room-303.com/blog/2008/02/13/rhythmbox-i-trzeszczaca-muzyka/
date: 2008-02-13 13:48:56.000000000 +01:00
categories:
- linux
- software
tags: []
comments:
- id: 17163
  author: Fluxid
  author_url: ''
  date: '2008-02-13 20:05:38 +0100'
  date_gmt: '2008-02-13 19:05:38 +0100'
  content: "Ooo, nareszcie! (Mimo że nie używam PLD a Gentoo... Ale mam ten sam problem.)\r\nA
    wiesz może coś o zużywaniu 100% CPU przy odtwarzaniu plików m4a z włączonym crossfade?
    (Którego włączenie, oprócz wyciszenia dźwięku o 1%, usuwało problem trzeszczenia
    :) )"
- id: 17164
  author: Patrys
  author_url: http://room-303.com/
  date: '2008-02-13 20:12:24 +0100'
  date_gmt: '2008-02-13 19:12:24 +0100'
  content: "Fluxid:\r\n\r\nZnany problem, dlatego między innymi crossfader nie jest
    domyślnie aktywny. Po upgradzie możesz go spokojnie wyłączyć ;)"
- id: 17317
  author: mareviq
  author_url: ''
  date: '2008-02-18 18:00:25 +0100'
  date_gmt: '2008-02-18 17:00:25 +0100'
  content: A ja poszukując rozwiązania przesiadłem się na OSS v4.0 ;)
---
<p>W <abbr title="PLD Linux Distribution">PLD</abbr> przez dłuższy czas ludzie skarżyli się na artefakty przy odtwarzaniu muzyki przez Rhythmboksa. Problem rozwiązany został dopiero wczoraj.</p>

<p>Zacznę może od rozwiązania, trzeba <strong>zaktualizować pakiet <code>alsa-lib</code> do wersji 1.0.16</strong>.</p>

<p>Jeśli kogoś ciekawi przyczyna problemu, to służę informacjami. Rhythmbox do odtwarzania dźwięku używa szkieletu GStreamer. GStreamer odpowiada za dekodowanie strumieni i nakładanie efektów, sam jednak do komunikacji z urządzeniem wyjściowym wykorzystuje jedną z bibliotek audio. Najczęściej używana jest w tym przypadku wspomniana ALSA.</p>

<p>Na każdym styku elementów następuje negocjacja obsługiwanych formatów danych. Rhythmbox przed otwarciem pliku sprawdza, czy GStreamer potrafi go obsłużyć. Następnie tworzony jest <q>łańcuszek</q> elementów GStreamera. Każde dwa elementy w kolejce ustalają między sobą preferowany format przekazywanych danych. Ostatnim elementem w łańcuchu odtwarzania jest <q>odpływ</q> (<em>sink</em>), przekazujący dane do biblioteki ALSA.</p>

<p>Również tutaj odbywa się negocjacja i tu pojawia się problem trzeszczenia. GStreamer od niedawna oferuje wsparcie dla 32-bitowych próbek dźwięku. Zapewnia to większą precyzję przy przetwarzaniu, a w przypadku droższego sprzętu także wyższą jakość dźwięku kierowanego na głośniki. Oczywiście, większość z nas słucha muzyki w formatach kompresowanych i nie usłyszymy raczej różnicy, ale GStreamer robi WłaściwąRzecz&trade;.</p>

<p>Problemem jest jednak ALSA, która również od niedawna zmieniła sposób skalowania próbek w przypadku 16-bitowych kart muzycznych. Do niedawna operacja ta polegała na obcięciu 16 mniej znaczących bitów. Zastąpił go nieco bardziej skomplikowany wzór, który &mdash; w przypadku dużej siły sygnału &mdash; podatny był na przepełnienie arytmetyczne. Ten właśnie <q>drobny szczegół</q> poprawiono w wersji 1.0.16.</p>

<p>Miłego słuchania muzyki zatem, <strong>Rhythmbox jest niewinny</strong> ;)</p>
