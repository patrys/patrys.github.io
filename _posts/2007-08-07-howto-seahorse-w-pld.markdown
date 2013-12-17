---
layout: post
status: publish
published: true
title: 'Howto: Seahorse w PLD'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 397
wordpress_url: http://room-303.com/blog/2007/08/07/howto-seahorse-w-pld/
date: 2007-08-07 14:59:12.000000000 +02:00
categories:
- linux
- software
tags: []
comments:
- id: 8352
  author: OJO
  author_url: ''
  date: '2007-08-11 16:51:05 +0200'
  date_gmt: '2007-08-11 15:51:05 +0200'
  content: 'u mnie coś nie chce to działać. jak próbuję się gdzieś logować po ssh
    to w trayu pojawia się ikonka kłódki z napisem "Warning: Your system is not configured
    to cache passphrases in secure memory."'
---
<p>Pakietu <a href="http://live.gnome.org/Seahorse">Seahorse</a> użytkownikom GNOME przedstawiać chyba nie trzeba. Ignorantom wystarczy powiedzieć, że Seahorse służy do zarządzania poufnymi informacjami. Potrafi edytować sekrety przechowywane w GNOME Keyring, zarządzać kluczami <abbr title="Secure Shell">SSH</abbr>, ale przede wszystkim jest najwygodniejszym interfejsem dla <a href="http://www.gnupg.org/">GnuPG</a>, jaki istnieje.</p>

<p>Problem polega na tym, że do wykorzystania pełni jego możliwości trzeba aktywować usługę <code>seahorse-agent</code>, która z kolei musi być uruchomiona przed resztą pulpitu. Do jej działania potrzebne są:</p>

<ul>
<li><code>seahorse</code></li>
<li><code>gnupg-agent</code> &gt;= 2.0.5-2</li>
</ul>

<p>Dalsze kroki wyglądają następująco:</p>

<ol>
<li><code>echo "pinentry-program seahorse-agent" &gt; ~/.gnupg/gpg-agent.conf</code></li>
<li><code>vim ~/.gnupg/gpg.conf</code> i usuwamy znak komentarza na początku linii <code>use-agent</code></li>
<li>wylogowujemy się i logujemy ponownie</li>
</ol>

<p>Od tego momentu o hasło powinien nas prosić już agent Seahorse, oferując czasowe przechowywanie odblokowanych kluczy w pamięci. Bardzo wygodne w przypadku wysyłaniu zleceń na buildery <abbr title="PLD Linux Distribution">PLD</abbr>.</p>
