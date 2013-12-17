---
layout: post
status: publish
published: true
title: Reanimacja współczesnego systemu
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 1146
wordpress_url: http://room-303.com/blog/?p=1146
date: 2011-03-20 20:14:09.000000000 +01:00
categories:
- linux
tags: []
comments:
- id: 27746
  author: mazdac
  author_url: ''
  date: '2011-03-20 22:14:55 +0100'
  date_gmt: '2011-03-20 21:14:55 +0100'
  content: "\"ressurekcja\" w moim std wydaniu (niezależnie jaki linuch) wygląda następująco:\r\nmkdir
    /mnt/root\r\nmount -t extX /dev/sdXX /mnt/root\r\nmount -t extX /dev/sdXX /mnt/root/boot\r\nmount
    -t proc /proc /mnt/root/proc\r\nmount -t sysfs /sys /mnt/root/sysfs\r\nmount -o
    bind /dev /mnt/root/dev #czasami trzeba przywrócić gruba...\r\nchroot /mnt/root
    /bin/bash\r\nzależnie czy w systemie livecd ustawiliśmy sieć itd to w systemie
    ratowanym będzie lub nie, dns ustawiamy prostym skopiowaniem resolva do systemu
    ratowanego.\r\nJak widać wiedzę, niezależnie z jakiego linucha (akurat tego nauczułem
    się dzięki gentoo) można wykorzystać praktycznie w każdym (aby livecd miało taką
    samą architektrę)."
- id: 27747
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2011-03-20 22:29:07 +0100'
  date_gmt: '2011-03-20 21:29:07 +0100'
  content: "@mazdac:\r\n\r\nJa nie pisałem o livecd, tam wszystko jest proste, bo
    dostajesz gotowy, działający system."
- id: 27748
  author: arekm
  author_url: ''
  date: '2011-03-21 11:52:28 +0100'
  date_gmt: '2011-03-21 10:52:28 +0100'
  content: Jaki objaw upstartu z test? Po raporcie jednej z osób upstart 1.1 został
    usunięty z test tylko jestem ciekaw czy ten sam objaw czy inny.
- id: 27749
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2011-03-21 11:57:39 +0100'
  date_gmt: '2011-03-21 10:57:39 +0100'
  content: Próbuje zrobić coś głupiego z <code>/proc/self/fd/8</code> i na tym kończy.
- id: 27752
  author: arekm
  author_url: ''
  date: '2011-03-22 19:18:40 +0100'
  date_gmt: '2011-03-22 18:18:40 +0100'
  content: upstart 1.2 zawiera fixa - nietestowany.
- id: 27757
  author: wookash
  author_url: ''
  date: '2011-04-15 19:04:08 +0200'
  date_gmt: '2011-04-15 17:04:08 +0200'
  content: "Czesc,\r\n\r\nwidzialem, ze kminiles cos z plikiem z programu e-deklaracje
    http://room-303.com/blog/2010/04/25/pit-37/\r\n\r\nprzy update do najnowszej wersji
    wcielo mi kopie deklaracji z porzedniego roku. probuje odczytac plik settings2010.dat,
    jednak wyskakuje mi blad. znalazlem gdzies opis, ze plik ten byl w wersji 2.0.x
    szyfrowany. Jak udalo Ci sie go odczytac??\r\n\r\nPozdrawiam,\r\n\r\nLukasz"
- id: 27758
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2011-04-15 19:32:49 +0200'
  date_gmt: '2011-04-15 17:32:49 +0200'
  content: "@wookash:\r\n\r\nW mojej wersji (starszej) nic nie było szyfrowane, nie
    bardzo wiem, jak ci pomóc."
---
<p>Plotki na temat mojej śmierci były oczywiście grubo&hellip; aaruuaaaarrrghhhblargh. Niestety, równie dobrze poczuł się mój laptop po ostatniej aktualizacji pakietu <code>upstart</code> w PLD.</p>

<p>Ku pamięci potomnych przedstawiam zatem przepis na doprowadzenie do w miarę działającego stanu systemu wyposażonego we "wszystkie te niepotrzebne wodotryski¹".</p>

<p><small>¹ Tak niektórzy pieszczotliwie określają <code>udev</code>, a właściwie cokolwiek powstałego po statycznej strukturze <code>/dev</code>, może z wyjątkiem epoki lodowcowej.</small></p>

<p>Zaczynamy tradycyjnie, od pominięcia procesu <code>init</code> (przykład dla <code>grub2</code>):</p>

<pre>linux /boot/vmlinuz-2.6.37.4-1 root=/dev/sciezka/do-root init=/bin/sh</pre>

<p>Następnie odzyskujemy podstawowe funkcje życiowe:</p>

<pre>mount / -o remount,rw
mount /proc
mount /sys
export PATH=$PATH:/sbin:/usr/sbin
udevd &amp;
udevadm trigger
dbus-daemon --system &amp;
NetworkManager &amp;</pre>

<p>Uruchomiona w ten sposób konsola może odmawiać przerywania zadań przez <kbd>Ctrl+C</kbd>, ale zawsze można do tego celu użyć <kbd>Alt+SysRq+I</kbd>.</p>
