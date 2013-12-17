---
layout: post
status: publish
published: true
title: Xgl + compiz dla PLD
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 241
wordpress_url: http://www.room-303.com/blog/2006/03/30/xgl-compiz-dla-pld/
date: 2006-03-30 23:11:41.000000000 +02:00
categories:
- linux
- software
tags: []
comments:
- id: 3511
  author: wolf
  author_url: ''
  date: '2006-03-31 14:01:04 +0200'
  date_gmt: '2006-03-31 13:01:04 +0200'
  content: Umieszczenie move za rotate jest błędęm - ctrl-alt nie dotrze do rotate,
    bo już move obsłuży alt.
- id: 3512
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-03-31 14:09:33 +0200'
  date_gmt: '2006-03-31 13:09:33 +0200'
  content: Racja, poprawiłem, dzięki.
- id: 3515
  author: mmazur
  author_url: ''
  date: '2006-03-31 23:02:54 +0200'
  date_gmt: '2006-03-31 22:02:54 +0200'
  content: Gdzie zgubiłeś noarcha w tym th?
- id: 3516
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-03-31 23:04:10 +0200'
  date_gmt: '2006-03-31 22:04:10 +0200'
  content: "mmazur:\r\n\r\nDo instalacji Xgl nie jest potrzebny żaden pakiet z noarch."
- id: 5276
  author: wolvverine
  author_url: http://www.linkomp.pl
  date: '2006-11-22 16:02:31 +0100'
  date_gmt: '2006-11-22 15:02:31 +0100'
  content: a co z kartami innymi niz ATI/NVIDIA?
- id: 8204
  author: Giertych
  author_url: http://giertychszyce.pl
  date: '2007-06-28 11:12:59 +0200'
  date_gmt: '2007-06-28 10:12:59 +0200'
  content: Co to za pedał ten przebrany ;-)))
- id: 23842
  author: XGL nie dzia
  author_url: http://www.hilpers.pl/449727-xgl-nie-dzia-a
  date: '2009-01-23 05:31:14 +0100'
  date_gmt: '2009-01-23 04:31:14 +0100'
  content: '[...] &gt; XOrg wraz z OpenGL dzia'
---
<p>Zbierałem się od dłuższego czasu, to może w końcu napiszę, jak to uruchomić bez psucia systemu. Poniższy opis jest przeznaczony dla użytkowników GNOME. Z KDE nie korzystam, więc nie pomogę.</p>

<h4>Wymagania</h4>

<p>Na początek warto przejść na <abbr title="PLD Linux Distribution">PLD</abbr> Th (3.0). Nie jest to konieczne, ale i tak trzeba skorzystać z tamtejszych źródeł pakietów. W tym celu podłączamy je do poldka w <code>/etc/poldek/pld-source.conf</code>:</p>

<blockquote><pre>[source]
type  = pndir
name  = th
path  = ftp://ftp.th.pld-linux.org/dists/th/PLD/%{_pld_arch}/RPMS/
noauto  = yes</pre></blockquote>

<blockquote><pre>[source]
type  = pndir
name  = th-test
path  = ftp://ftp.th.pld-linux.org/dists/th/test/%{_pld_arch}/RPMS/
noauto  = yes</pre></blockquote>

<p>Następnie uruchamiamy poldka z nowymi źródłami (<code>poldek -n th -n th-test</code>) i instalujemy paczki (dla chcących pozostać przy PLD Ac, polecam przełącznik <code>-I</code>, który zapobiegnie upgrade'owi):</p>

<ul>
<li><code>xorg-xserver-xgl</code></li>
<li><code>xorg-xserver-xgl-libGL</code></li>
<li><code>compiz</code></li>
<li><code>compiz-gnome-settings</code></li>
<li><code>compiz-gnome-decorator</code></li>
</ul>

<p>Do pełnej konfiguracji będzie jeszcze potrzebny <code>gconf-editor</code>, ale ten można zainstalować z dowolnego źródła.</p>

<h4>Konfiguracja</h4>

<p>Zanim przejdziesz dalej, upewnij się, że korzystasz z binarnych sterowników ATI lub nVidii i że Iksy poprawnie obsługują akcelerację (<q>Direct rendering: yes</q> w <code>glxinfo</code>).</p>

<p>Przystępujemy do edycji pliku <code>/usr/share/gdm/defaults.conf</code> z pakietu <code>gdm</code>. W okolicach linii 517. powinien znajdować się wpis:</p>

<blockquote><pre>[servers]
0=Standard</pre></blockquote>

<p>Zmieniamy go na następujący:</p>

<blockquote><pre>[servers]
1=Standard</pre></blockquote>

<p>Następnie przechodzimy do majstrowania we wnętrznościach <code>/etc/gdm/custom.conf</code>. Sekcję <code>[servers]</code> uzupełniamy o poniższy wpis:</p>

<blockquote><pre>[servers]
1=Xgl</pre></blockquote>

<p>Na końcu pliku dodajemy jeszcze jedną sekcję:</p>

<blockquote><pre>[server-Xgl]
name=Xgl server
command=/usr/bin/Xgl :1 -ac -accel xv:pbuffer -accel glx:pbuffer -fullscreen
flexible=true</pre></blockquote>

<p><strong>Uwaga:</strong> powyższa linijka <q>command</q> stosuje się <em>tylko do kart ATI</em>, użytkownicy nVidii powinni zamiast niej użyć:</p>

<blockquote><pre>[server-Xgl] 
name=Xgl server 
command=/usr/bin/Xgl :1 -ac -accel xv:fbo -accel glx:pbuffer -fullscreen
flexible=true</pre></blockquote>

<p>Następnie tworzymy nowy plik, <code>/usr/bin/compiz-start</code>:</p>

<blockquote><pre>#!/bin/bash
DISPLAY=:1 LD_PRELOAD=/usr/lib/xgl/libGL.so.1.2 compiz --replace gconf &amp;
DISPLAY=:1 gnome-window-decorator &amp;
DISPLAY=:1 setxkbmap -model pc105 -layout pl</pre></blockquote>

<p>I nadajemy mu prawo wykonania:</p>

<blockquote><pre># chmod a+x /usr/bin/compiz-start</pre></blockquote>

<h4>Uruchomienie</h4>

<p>Na początek restartujemy daemona GDM. Jeśli wszystko pójdzie dobrze, to Iksy powinny uruchomić się normalnie. Logujemy się na swojego użytkownika i wybieramy <em>Środowisko / Preferencje / Sesje</em>. Na zakładce <q>Programy startowe</q> klikamy <q>Dodaj</q> i wpisujemy jako polecenie <code>compiz-start</code>. Od tego momentu, compiz będzie startował automatycznie z każdym logowaniem.</p>

<p>Uruchamiamy ręcznie compiz — wciskamy <kbd>Alt</kbd> + <kbd>F2</kbd> i wpisujemy <code>compiz-start</code>. Nie przejmujemy się faktem, że pulpit wygląda nieco dziwnie i uruchamiamy z menu <em>Aplikacje / Narzędzia systemowe / Edytor konfiguracji</em>.</p>

<p>Po uruchomieniu <code>gconf-editor</code>, przechodzimy do gałęzi <code>/apps/compiz/general/allscreens/options</code> i edytujemy wartość <code>active_plugins</code>. Jest to lista i powinna zawierać następujące elementy:</p>

<ul>
<li><code>gconf</code></li>
<li><code>decoration</code></li>
<li><code>wobbly</code></li>
<li><code>fade</code></li>
<li><code>minimize</code></li>
<li><code>cube</code></li>
<li><code>place</code></li>
<li><code>resize</code></li>
<li><code>move</code></li>
<li><code>rotate</code></li>
<li><code>zoom</code></li>
<li><code>scale</code></li>
<li><code>switcher</code></li>
</ul>

<p><strong>Uwaga:</strong> wszystkie powyższe wartości trzeba dodać za jednym razem (bez zamykania okna edycji listy), bo compiz przeładowuje wtyczki w locie i zwyczajnie usunie z listy te, dla których nie zostały spełnione zależności (niektóre wtyczki wymagają innych).</p>

<h4>Tuning</h4>

<p>Po zapisaniu zmian, wtyczki powinny załadować się automatycznie i compiz powinien uzyskać pełną sprawność bojową. Powyższych czynności nie trzeba powtarzać w przyszłości (chyba, że nowe wersje compiz dostarczą nowych wtyczek).</p>

<p>Ciekawscy mogą jeszcze pogrzebać w trzewiach klucza <code>/apps/compiz/plugins</code> — każdy z jego elementów odpowiada za konfigurację jednej wtyczki i można tam zmienić całkiem sporo rzeczy.</p>

Technorati Tags: <a href="http://technorati.com/tag/linux" rel="tag">linux</a>, <a href="http://technorati.com/tag/pld" rel="tag">pld</a>, <a href="http://technorati.com/tag/compiz" rel="tag">compiz</a>, <a href="http://technorati.com/tag/xgl" rel="tag">xgl</a>, <a href="http://technorati.com/tag/gnome" rel="tag">gnome</a>
