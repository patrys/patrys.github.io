---
layout: post
status: publish
published: true
title: PHP, PCRE i nagłe zgony
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 384
wordpress_url: http://room-303.com/blog/2007/06/20/php-pcre-i-nagle-zgony/
date: 2007-06-20 00:53:29.000000000 +02:00
categories:
- linux
- web
- software
- code
tags: []
comments:
- id: 8120
  author: Michał Górny
  author_url: http://mgorny.openid.pl/
  date: '2007-06-20 09:06:36 +0200'
  date_gmt: '2007-06-20 08:06:36 +0200'
  content: "Perl zdaje się być niewrażliwy na takie coś. No, chyba że źle przepisałem
    powyższy kawałek:\r\n\r\n#!/usr/bin/perl\r\nprint 'A teraz coś z zupełnie innej
    beczki: ';\r\n'a' x 10000 =~ /(.(?!b))*/;"
- id: 8121
  author: Max
  author_url: ''
  date: '2007-06-20 10:37:26 +0200'
  date_gmt: '2007-06-20 09:37:26 +0200'
  content: 'Witam, ciekawi mnie ten fragment: "Prawie wszystkie działające u nas aplikacje
    są zaimplementowane jako usługi FastCGI serwowane przez Lighttpd." Jakie to usługi,
    jeśli PHP jest obsługiwane przez Apache? I jak wykonuje sie takie rozdzielanie
    usług. No z tym ostatnim to może przesadziłem, bo ten blog to nie jakiś helpdesk
    ale bardzo mnie to zaciekawiło, a nie ma co ukrywać, jestem początkujący i póki
    co za bardzo nawet nie wiem jak zapytać google by grzecznie udzieliły mi odpowiedzi
    ;)'
- id: 8122
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-06-20 10:58:08 +0200'
  date_gmt: '2007-06-20 09:58:08 +0200'
  content: "Max:\r\n\r\nWiększość usług u nas to aplikacje Pythona (Django).\r\n\r\nPisząc
    o rozdzieleniu miałem na myśli stosowanie <code>suexec</code> albo <code>suPHP</code>
    i uruchamianie skryptów z prawami ich właścicieli zamiast użytkownika, na którym
    działa Apache."
- id: 8126
  author: nrm
  author_url: http://normanos.com
  date: '2007-06-20 11:34:29 +0200'
  date_gmt: '2007-06-20 10:34:29 +0200'
  content: "@Max: \"I jak wykonuje sie takie rozdzielanie usług.\" - jeżeli miałeś
    na myśli te php na apache, a reszta na lighttpd to jest to dosyć częsta praktyka
    (np. Youtube tak działa, serwis na apache, statyczne ciągniete z lightiego). Ustawiasz
    normalnie Apacha na :80, Lighttpd:nacosinnego, w Apache korzystasz z mod_proxy
    i definiujesz jaki ruch ma iść na ten inny port którym się zajmie lighty.\r\n\r\nPrzykład
    implementacji:\r\nhttp://www.linux.com/article.pl?sid=06/01/27/1813223"
- id: 8127
  author: Max
  author_url: ''
  date: '2007-06-20 11:57:38 +0200'
  date_gmt: '2007-06-20 10:57:38 +0200'
  content: Wielkie dzięki. To wydaje sie naprawdę świetne. Pozdrawiam :)
- id: 8128
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-06-20 13:08:37 +0200'
  date_gmt: '2007-06-20 12:08:37 +0200'
  content: "Michał Górny:\r\n\r\nPCRE to biblioteka, która naśladuje wyrażenia regularne
    Perla. Sam Perl z niej nie korzysta, używają jej za to Apache i PHP."
- id: 8130
  author: a
  author_url: ''
  date: '2007-06-21 01:31:23 +0200'
  date_gmt: '2007-06-21 00:31:23 +0200'
  content: W Perlu takich głupich błędów nie ma ;) I poprawia się je natychmiast.
    Natomiast PHP... ktoś coś chłapnie, a potem olewa. A inni na tym bazują i się
    wściekają.
- id: 8131
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-06-21 11:21:24 +0200'
  date_gmt: '2007-06-21 10:21:24 +0200'
  content: "a:\r\n\r\nTo nie błąd w PHP, tylko w PCRE.\r\n\r\nA swoje zdanie o PHP
    już kiedyś wyraziłem na łamach tego bloga."
---
<p>Jest wpół do drugiej w nocy. Siedzę w biurze. Serwer Apache wygląda na stabilny. Dokładnie, <q>wygląda.</q></p>

<p>Prawie wszystkie działające u nas aplikacje są zaimplementowane jako usługi FastCGI serwowane przez <a href="http://www.lighttpd.net/">Lighttpd</a>. Bazy danych działają w osobnych serwerach wirtualnych, podobnie odseparowany jest Apache, który dzierży brzemię mielenia <abbr title="PHP Hypertext Preprocessor">PHP</abbr> i przedzierania się przez gąszcze plików <code>.htaccess</code>.</p>

<p>Wszystko byłoby pięknie, gdyby Apache nie zaczął sobie chodzić na spacerek do krainy wiecznych łowów (jak to Indianie mają w zwyczaju czynić po <code>SIGSEGV</code>). Szybki (błyskawiczny rzekłbym, ale to nie prawda) <code>strace</code> i końcówka <code>gdb</code> pokazały, że ślad urywa się gdzieś w <abbr>PHP</abbr>.</p>

<p>Następny test — przestawienie <abbr>PHP</abbr> z <code>mod_php</code> (użytkownicy nie mają dostępu do kodu serwisów, więc nie bawiliśmy się w żadne separacje użytkowników) na <abbr title="Common Gateway Interface">CGI</abbr>. Tym razem dzielny serwer przetrwał, w przeciwieństwie do skryptu. Kolejny <code>strace</code> i <code>gdb</code> na symulowanym środowisku <abbr>CGI</abbr> (w bardzo wysublimowany sposób — <code>export QUERY_STRING=…</code> i tak dalej) i okazuje się, że zdycha jednak biblioteka implementująca <abbr title="Perl Compatible Regular Expressions">PCRE</abbr>.</p>

<p>Dużo Google. Bardzo dużo. W końcu pomaga <a href="http://qwiat.icenter.pl/">Qwiat</a>. Miał to samo, pomógł downgrade pakietu <code>pcre</code> do wersji 6.7. Przebudowa wspomnianego pakietu we wspomnianej wersji, upgrade w vserwerze, restart usług. Działa. Nieźle się maskuje.</p>

<p>Kod serwisów zdaje się działać bez zarzutu. Chciałem zarzucić temat, ale obiecałem znaleźć syntetyczny testcase. Więcej Google. Na liście błędów <code>pcre</code> jest znana podatność na przepełnienie stosu. Autorzy zdają się mieć ją w dużym poważaniu. Wersja 7.x zdycha, wersja 6.x działa. A takiego.</p>

<blockquote><pre><code>&lt;?php
print 'A teraz coś z zupełnie innej beczki: ';
preg_match('/(.(?!b))*/', str_repeat("a", 10000));
?&gt;</code></pre></blockquote>

<p>Powyższy kod położył mi każdą kombinację <abbr>PHP</abbr> i <abbr>PCRE</abbr>. Bardzo ładny sposób, żeby komuś zrobić <abbr title="Denial Of Service">DOS</abbr> na <abbr>PHP</abbr> działające w trybie FastCGI (po n-tym padzie usługi w krótkim czasie serwer słusznie uzna, że jest uszkodzona i przestanie ją wskrzeszać, przynajmniej na jakiś czas).</p>

<p>I tym optymistycznym akcentem zakończę swoje gadanie od rzeczy i udam się do domu spać.</p>
