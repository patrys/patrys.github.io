---
layout: post
status: publish
published: true
title: 'PLD Linux: Flash i działający dźwięk'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 515
wordpress_url: http://room-303.com/blog/?p=515
date: 2009-01-27 21:12:05.000000000 +01:00
categories:
- linux
tags: []
comments:
- id: 23878
  author: DeeJay1
  author_url: http://princefool.blogspot.com/
  date: '2009-01-28 07:27:53 +0100'
  date_gmt: '2009-01-28 06:27:53 +0100'
  content: Tja, tylko bardzo przypomina to ten link  http://www.pulseaudio.org/wiki/PerfectSetup
    ;&gt;
- id: 23879
  author: Patrys
  author_url: http://room-303.com/
  date: '2009-01-28 08:21:32 +0100'
  date_gmt: '2009-01-28 07:21:32 +0100'
  content: "Jakoś nie skojarzyłem nigdy, żeby rozwiązania problemu Flasha szukać na
    stronach PulseAudio :)\r\n\r\nU mnie problem nie dotyczył konfiguracji PulseAudio,
    bo wcześniej wcale go nie używałem. (W myśl zasady, że jak Flash nie radzi sobie
    z ALSĄ, to lepiej mu dodatkowo nie szkodzić.)"
- id: 23883
  author: princefool.blogspot.com/
  author_url: http://princefool.blogspot.com/
  date: '2009-01-28 18:19:46 +0100'
  date_gmt: '2009-01-28 17:19:46 +0100'
  content: Cóż, wiele osób nigdy tam nie zagląda a potem przeklina, że pulseaudio
    "zepsuło" aplikację X a to tylko alsa nawalała ;) Ostatnio przetoczyła się drobna
    dyskusja na ten temat przez planetosferę (ciekawe czy ten termin się przyjmie
    :P)
- id: 23884
  author: Klaudia
  author_url: ''
  date: '2009-01-28 19:35:47 +0100'
  date_gmt: '2009-01-28 18:35:47 +0100'
  content: Można też, wyrzucić alsę i pulseaudio i przejść na OSSv4, gdzie wszystko
    działa bez jakiejkolwiek konfiguracji.
- id: 23886
  author: Patrys
  author_url: http://room-303.com/
  date: '2009-01-28 21:06:50 +0100'
  date_gmt: '2009-01-28 20:06:50 +0100'
  content: "Klaudia:\r\n\r\nNie, nie, mój dźwięk nie miksuje się w kernelu i niech
    tak pozostanie :)"
---
<p>Ku pamięci (dotyczy również innych dystrybucji):</p>

<blockquote><pre><code>$ sudo lsmod | grep snd
snd_pcsp                9120  2 
snd_hda_intel         311948  5 
snd_pcm                58500  4 snd_pcsp,snd_hda_intel
snd_timer              18184  1 snd_pcm
snd_hwdep               7684  1 snd_hda_intel
snd_page_alloc          8072  2 snd_hda_intel,snd_pcm
snd                    41124  17 snd_pcsp,snd_hda_intel,snd_pcm,snd_timer,snd_hwdep
soundcore               6496  1 snd</code></pre>

<pre><code>$ rpm -q pulseaudio alsa-plugins-pulse gstreamer-pulseaudio
pulseaudio-0.9.14-1.i686
alsa-plugins-pulse-1.0.19-1.i686
gstreamer-pulseaudio-0.10.13-1.i686</code></pre>

<pre><code>$ cat ~/.asoundrc
pcm.!default {
    type pulse
}
ctl.!default {
    type pulse
}</code></pre></blockquote>

<p>Z takimi ustawieniami (i aktywnym daemonem PulseAudio) Flash w końcu przestaje kłócić się z resztą systemu o urządzenie ALSA, czego efektem jest dźwięk we Flashu, który nie znika po kilkunastu minutach od włączenia przeglądarki.</p>
