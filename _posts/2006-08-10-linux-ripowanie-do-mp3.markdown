---
layout: post
status: publish
published: true
title: 'Linux: ripowanie do mp3'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 284
alias: /blog/2006/08/10/linux-ripowanie-do-mp3/
date: 2006-08-10 23:30:37.000000000 +02:00
categories:
- linux
- software
tags: []
comments:
- id: 4435
  author: Michał Moroz
  author_url: http://dragonee.jogger.pl
  date: '2006-08-11 00:50:40 +0200'
  date_gmt: '2006-08-10 23:50:40 +0200'
  content: abcde potrafi załatwić całe ripowanie, tagowanie poprzez CDDB, enkodowanie
    i normalizację jednym poleceniem. Po co klikać, shell Cię wyręczy. ;)
- id: 4436
  author: Elus
  author_url: ''
  date: '2006-08-11 00:51:05 +0200'
  date_gmt: '2006-08-10 23:51:05 +0200'
  content: "To ja może dodam że Ubuntowcy (Ubunciarze?) korzystający z gstreamera
    0.10 będą potrzebować pakietów gstreamer0.10-plugins-bad-multiverse i liblame0.
    W przeciwnym razie tracki bedę jedynie ripowane a nie encodowane o czym sound-juicer
    nawet nas nie poinformuje (można sie zorientować dopiero po wielkości wyplutego
    pliku).\r\n\r\nDo bardziej zaawansowanych zabaw polecam grip-a."
- id: 4437
  author: salvadhor
  author_url: http://404.g-net.pl
  date: '2006-08-11 07:19:26 +0200'
  date_gmt: '2006-08-11 06:19:26 +0200'
  content: Wszystko to ładnie wygląda, ale jaki jest sens korzystania z takiego kompromisu
    ( brak możliwości zmiany parametrów ripiowanych plików, brak uzupełniania nazw
    plików i tagów wpisami z CDDB ( ? ) ), jeżeli są takie programy jak grip, ripperx,
    goobox itp itd.
- id: 4438
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-08-11 08:26:20 +0200'
  date_gmt: '2006-08-11 07:26:20 +0200'
  content: "salvadhor:\r\n\r\nPrzecież sound-juicer pobiera wszystkie metadane z CDDB,
    zakłada dowolną praktycznie strukturę katalogów (u mnie Artysta/Album), nazywa
    i otagowuje pliki, korzystając z danych z CDDB? Bez FUDowania."
- id: 4439
  author: Krzysztof Rosiński
  author_url: http://kr.livenet.pl
  date: '2006-08-11 09:15:19 +0200'
  date_gmt: '2006-08-11 08:15:19 +0200'
  content: "Patrys:\r\n\r\nAFAIR Sound Juicer pobiera metadane z MusicBrainz."
- id: 4440
  author: Azrael Nightwalker
  author_url: http://metal.eu.org/techblog/
  date: '2006-08-11 10:33:20 +0200'
  date_gmt: '2006-08-11 09:33:20 +0200'
  content: Wolę Gripa.
- id: 4441
  author: rasheed
  author_url: http://mklimek.org
  date: '2006-08-11 10:34:09 +0200'
  date_gmt: '2006-08-11 09:34:09 +0200'
  content: Dla informacji, jezeli ktos chce aplikacje pod KDE to niech zwroci uwage
    na KAudioCreator.
- id: 4442
  author: wolf
  author_url: ''
  date: '2006-08-11 16:22:17 +0200'
  date_gmt: '2006-08-11 15:22:17 +0200'
  content: Pod KDE wystarczy mieć zainstalowane k3b i włożyć płytkę. Potem tylko kliknąć,
    że chce się zripować płytę, wybrać format i gotowe.
- id: 4443
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-08-11 16:32:52 +0200'
  date_gmt: '2006-08-11 15:32:52 +0200'
  content: "wolf:\r\n\r\nPod GNOME tak samo działa Sound Juicer, ale domyślnie ma
    tylko obsługę OGG (co jest świetną opcją, jeśli się nie używa iPoda)."
- id: 4555
  author: Bartini
  author_url: http://bartini.jogger.pl/
  date: '2006-08-31 20:25:33 +0200'
  date_gmt: '2006-08-31 19:25:33 +0200'
  content: A jak można poprawić jakość zgrywania takim sposobem? Bo wyjściowy plik
    ma tylko 128 kbps...
- id: 4856
  author: Paladine
  author_url: http://palanthas.net
  date: '2006-09-26 23:59:48 +0200'
  date_gmt: '2006-09-26 22:59:48 +0200'
  content: "Tagów Ci nie gubi to rozwiązanie? ;-)\r\nProponuję:\r\naudio/x-raw-int,rate=44100,channels=2
    ! lame name=enc ! id3mux v1-tag=1\r\n\r\nBartini:\r\n\r\nhint: gst-inspect lame"
---
<p>Tym razem bez skryptu.</p>

<h4>Wymagania</h4>

<ul>
<li>gnome-media</li>
<li>gstreamer-lame</li>
<li>sound-juicer</li>
</ul>

<h4>Konfiguracja</h4>

<ol>
<li>odpalamy Sound Juicera</li>
<li>wybieramy <q>Preferencje,</q> <q>Modyfikuj profile…</q></li>
<li>w nowootwartym okienku wbyieramy <q>Nowy</q></li>
<li>wybieramy nazwę dla profilu, na przykład <q>MP3</q></li>
<li>zaznaczamy nowy profil i klikamy <q>Edycja</q></li>
<li>w pole <q>Potok GStreamer</q> wpisujemy <code>audio/x-raw-int,rate=44100,channels=2 ! lame name=enc</code></li>
<li>w pole <q>Rozszerzenie pliku</q> wpisujemy <code>mp3</code></li>
<li>zaznaczamy <q>Aktywny?</q></li>
<li>klikamy OK, zamykamy preferencje i cieszymy się obsługą mp3</li>
</ol>

Technorati Tags: <a href="http://technorati.com/tag/sound-juicer" rel="tag">sound-juicer</a>, <a href="http://technorati.com/tag/mp3" rel="tag">mp3</a>, <a href="http://technorati.com/tag/lame" rel="tag">lame</a>, <a href="http://technorati.com/tag/gnome" rel="tag">gnome</a>, <a href="http://technorati.com/tag/cd" rel="tag">cd</a>, <a href="http://technorati.com/tag/music" rel="tag">music</a>, <a href="http://technorati.com/tag/rip" rel="tag">rip</a>
