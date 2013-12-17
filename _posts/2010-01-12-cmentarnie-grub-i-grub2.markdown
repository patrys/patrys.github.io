---
layout: post
status: publish
published: true
title: 'Cmentarnie: GRUB i GRUB2'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 725
wordpress_url: http://room-303.com/blog/?p=725
date: 2010-01-12 22:49:56.000000000 +01:00
categories:
- linux
- software
tags:
- pld
- grub
comments:
- id: 24737
  author: Piotr Budny
  author_url: http://coffee3.org
  date: '2010-01-13 01:08:10 +0100'
  date_gmt: '2010-01-13 00:08:10 +0100'
  content: Mnie grub bez problemu działał z xfs (bez lvm). Grub2 działa fajnie (choć
    wykrywanie wszystkiego i generowanie konfiga trochę trwa), no i pewnie będzie
    wyglądać sympatyczniej od poprzednika, o ile się uda ustawić tryb graficzny, czcionki,
    obrazek w tle itp (mnie się nie udało).
- id: 24739
  author: Hadret
  author_url: http://hadret.com/
  date: '2010-01-13 07:48:06 +0100'
  date_gmt: '2010-01-13 06:48:06 +0100'
  content: Grub2 nadal nie radzi sobie z software'owym RAID-em, a właściwie nie współpracuje
    z dmraidem, przez co mój nvraid nie współpracuje z wersją 2 Gruba i muszę używać
    wersji legacy. Tyle, że jest to też moja wina -- kto w Linuksie ustawia software
    RAID? No właśnie.
- id: 24740
  author: arekm
  author_url: ''
  date: '2010-01-13 08:22:33 +0100'
  date_gmt: '2010-01-13 07:22:33 +0100'
  content: 2 nie radzi też sobie z znajdowaniem initrd skompresowanego lzma.
- id: 24741
  author: Patrys
  author_url: http://room-303.com/
  date: '2010-01-13 09:22:35 +0100'
  date_gmt: '2010-01-13 08:22:35 +0100'
  content: "arekm:\r\n\r\nKwestia dopisania odpowiedniego kodu - inne dystrybucje
    nie mają takich szalonych pomysłów (a ja odwagi - po tym, jak peeldowe geninitrd
    wygenerowało mi initram w lzma dla kernela bez jego obsługi)."
- id: 24743
  author: qwiat
  author_url: ''
  date: '2010-01-13 10:46:36 +0100'
  date_gmt: '2010-01-13 09:46:36 +0100'
  content: "@Hadret:\r\n\r\nDziała z raidem softwarowym (a przynajmniej pod qemu),
    tyle że wersja superbloku musi sie zgadzać: 0.90. Działa wyśmienicie z RAID5 i
    nawet z uszkodzonym (bez jednego dysku)."
- id: 24747
  author: arekm
  author_url: ''
  date: '2010-01-13 14:00:57 +0100'
  date_gmt: '2010-01-13 13:00:57 +0100'
  content: '@Patrys: coś nie wierzę. Problem jaki był to bug w kernelu powodujący
    stworzenie błędnego vmlinuz kompresowanego lzma i tyle. geninitrd patrzy po System.map
    szukając unlzma... więc naprawdę ciężko uwierzyć.'
- id: 24748
  author: Patrys
  author_url: http://room-303.com/
  date: '2010-01-13 14:48:27 +0100'
  date_gmt: '2010-01-13 13:48:27 +0100'
  content: "arekm:\r\n\r\nNie wiem, w czym to był bug, ale system nie wstał, od tego
    czasu mam na sztywno gzip :)"
- id: 25114
  author: Rafał
  author_url: ''
  date: '2010-07-29 17:37:01 +0200'
  date_gmt: '2010-07-29 15:37:01 +0200'
  content: Wkurza w grub2 brak obsługi bootowania po sieci.
---
<p>Wczoraj, za namową <a href="http://pozar-w-burdelu.blogspot.com/">qwiata</a>, zrobiłem kolejną przymiarkę do drugiego wcielenia <a href="http://www.gnu.org/software/grub/">GRUBa</a>. Tym razem zakochałem się niemal i nie chcę za nic wracać.</p>

<p>Automatyka wykrywająca konfigurację PLD działa znakomicie, a po napotkanych dawniej błędach w okolicach obsługi LVM nie pozostał nawet ślad. Na poparcie swojego stanowiska wspomnę tylko, że dziś rano, pierwszy raz od lat, pozbyłem się partycji <code>/boot</code>. Dotąd musiałem trzymać osobną, 30-megabajtową partycję na <code>ext2</code>, gdyż pierwsze wcielenie GRUBa nie radziło sobie ani z <code>xfs</code>, ani z LVM.</p>

<h4>Howto</h4>

<p>Instalacja:</p>

<pre># grub-install /dev/sda
# grub-setup '(hd0)'
# update-grub</pre>

<p>Po zmianie jądra:</p>

<pre># update-grub</pre>

<p>Ten ostatni krok już niedługo stanie się zbędny.</p>

<p>Jeśli ktoś jeszcze zwleka, to naprawdę nie ma na co czekać. Oczywiście, są jeszcze użytkownicy LILO, ale ich szanujemy. Jeśli pozostałe projekty GNU będą rozwijać się tak prężnie, to są szanse na używalną wersję HURD jeszcze zanim przepełni się 32-bitowy znacznik czasu ;)</p>
