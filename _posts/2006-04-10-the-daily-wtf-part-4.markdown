---
layout: post
status: publish
published: true
title: The Daily WTF, part 4
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 242
wordpress_url: http://www.room-303.com/blog/2006/04/10/the-daily-wtf-part-4/
date: 2006-04-10 15:01:49.000000000 +02:00
categories:
- software
- code
tags: []
comments:
- id: 3533
  author: byte
  author_url: http://byte.livenet.pl
  date: '2006-04-10 15:22:34 +0200'
  date_gmt: '2006-04-10 14:22:34 +0200'
  content: Banzaiiiiiiii! Piękne :)
- id: 3534
  author: medyk
  author_url: http://www.medikoo.com
  date: '2006-04-10 15:46:48 +0200'
  date_gmt: '2006-04-10 14:46:48 +0200'
  content: A propos host'ów. Jakiś czas temu pamiętam pisałeś, że zarejstrowałeś się
    na dreamhost.com. Cały czas jesteś z nimi? Wszystko jest ok? Obok dosyć dużych
    możliwości jakie dają (jak na dzielony hosting) to słyszałem o nich różne zdania.
- id: 3535
  author: normanos
  author_url: http://normanos.com
  date: '2006-04-10 16:55:31 +0200'
  date_gmt: '2006-04-10 15:55:31 +0200'
  content: "szkoda gadac...\r\ntez cos na ten temat pisalem :(\r\n\r\nhttp://normanos.com/linux/exploit-na-vhcs2/"
- id: 3538
  author: qwiat
  author_url: ''
  date: '2006-04-10 23:13:24 +0200'
  date_gmt: '2006-04-10 22:13:24 +0200'
  content: Do tego sam panel VHCS-a wymaga <em>register_globals</em> - rotfl
- id: 3540
  author: Michał Kwiatkowski
  author_url: http://joker.linuxstuff.pl
  date: '2006-04-10 23:47:29 +0200'
  date_gmt: '2006-04-10 22:47:29 +0200'
  content: "Bug już dość stary, powinien dostać nagrodę sprzed dwóch miesięcy. Ale
    cały kod vhcsa to jeden wielki żart, więc czego byś tu nie przytoczył nadawałoby
    się na WTF.\r\n\r\nA <em>register_globals</em> wymagany jest tylko dla filemanagera."
- id: 3542
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-04-11 10:44:09 +0200'
  date_gmt: '2006-04-11 09:44:09 +0200'
  content: "medyk:\r\n\r\nTak, dalej korzystamy z Dreamhosta i jesteśmy nader zadowoleni.
    To duży hosting, więc i zdania będą podzielone, a najgłośniej słychać tych, co
    narzekają. Jeśli tylko jest jakiś problem, to helpdesk reaguje natychmiast i są
    bardzo pomocni (w przeciwieństwie do kilku innych firm hostingowych, z którymi
    miałem nieprzyjemność współpracować). Ceny mają rewelacyjne, a polski hosting
    w porównianiu z nimi wypada blado.\r\n\r\nMichał:\r\n\r\nBug stary, ale oficjalny
    patch go nie poprawia (a raczej nie poprawiał, bo autorzy VHCS bez jakiejkolwiek
    informacji podmienili plik z patchem na serwerze)."
- id: 8305
  author: Wojtosz
  author_url: http://www.blaszkowski.com
  date: '2007-07-28 18:33:27 +0200'
  date_gmt: '2007-07-28 17:33:27 +0200'
  content: "właśnie przeglądałem sobie opinie n/t paneli hostingowych.\r\nten projekt
    (VHCS) jest jeszcze w ogóle w konkretny sposób rozwijany ?"
---
<p>Dzisiejszą nagrodę zdobywają autorzy <a href="http://www.vhcs.net/">najgorzej napisanego systemu hostingowego</a>. Tylko prawdziwy geniusz mógł coś takiego wymyślić. Każda strona <abbr>VHCS</abbr> jest <q>zabezpieczona</q> wywołaniem specjalnej funkcji. Kod poniżej:</p>

<blockquote><pre>function check_login () {
	if (isset($_SESSION['user_logged'])) {
		if (!check_user_login($_SESSION['user_logged'],
			$_SESSION['user_type'],
			$_SESSION['user_id'])) {
			header("Location: ../index.php");
		}
	} else {
		header("Location: ../index.php");
	}
}</pre></blockquote>

<p>Oto, moi drodzy, nowy sposób zabezpieczania systemów. Jeśli użytkownik nie jest zalogowany, to wysyłamy mu nagłówek przekierowania do strony logowania, po czym… Po czym nie przerywamy wykonania skryptu przez <code>die();</code> albo <code>exit();</code>, tylko pozwalamy mu się normalnie wykonać.</p>

<p>Tym panom już podziękujemy, serwisy przywrócone z backupów, z <abbr>VHCS</abbr> się chyba pożegnamy — bezpieczeństwo mają wyraźnie w dużym poważaniu i nie czują się zobowiązani do publikowania informacji o krytycznych błędach (a kolejne poprawki udostępniają przez nadpisanie pliku z poprzednim patchem, bez informacji o zmianach).</p>

Technorati Tags: <a href="http://technorati.com/tag/vhcs" rel="tag">vhcs</a>, <a href="http://technorati.com/tag/security" rel="tag">security</a>, <a href="http://technorati.com/tag/hosting" rel="tag">hosting</a>, <a href="http://technorati.com/tag/wtf" rel="tag">wtf</a>, <a href="http://technorati.com/tag/code" rel="tag">code</a>, <a href="http://technorati.com/tag/software" rel="tag">software</a>
