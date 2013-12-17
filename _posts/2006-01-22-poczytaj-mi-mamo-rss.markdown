---
layout: post
status: publish
published: true
title: Poczytaj mi mamo - RSS
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 216
wordpress_url: http://www.room-303.com/blog/2006/01/22/poczytaj-mi-mamo-rss/
date: 2006-01-22 18:17:02.000000000 +01:00
categories:
- web
tags: []
comments:
- id: 3102
  author: m
  author_url: ''
  date: '2006-01-22 19:08:13 +0100'
  date_gmt: '2006-01-22 18:08:13 +0100'
  content: "Niedawno też kleciłem mały kawałek kodu do odczytu feedów RSS na własne
    potrzeby i sporo gównianych tricków w tym było. Anyway, tak to jest jak ludzie
    zamiast pomyśleć, zaproponować i poczekać siądą od razu do standaryzacji... i
    tak oto mamy teraz generalnie RSS w dwóch wersjach i Atom, które z punktu widzenia
    końcowego usera niczym a niczym się nie różnią, służą w końcu do tego samego.
    Najweselsze jest to, że Atom dorobił się RFC (4287, \"The Atom Syndication Format\").
    \r\n\r\nNie zauważyłem za to, żeby na zachodzie, w szczególności za oceanem, było
    lepiej z przestrzeganiem tych \"standardów\" - nawet duże i bardzo duże serwisy
    niekoniecznie budują poprawne feedy RSS [1]. Pewnie dlatego, że liczba wejść na
    ich strony przez linki z RSS stanowi mniej niż 1%...\r\n\r\nbtw, może warto wskazać
    jakieś sprawdzone biblioteki do budowania feedów? Z jednej strony niby nie jest
    trudno samodzielnie sklecić kawałek XML, z drugiej, jak widać, diabeł tkwi w szczegółach.
    A to właśnie brak popularnych narzędzi sprawia, że ludzie po nocach potworki tworzą
    zamiast na becikowe pracować.\r\n\r\n[1] http://validator.w3.org/feed/check.cgi?url=http%3A%2F%2Fhealth.yahoo.com%2Fnews%2Frss%2Fhealth"
- id: 3103
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-01-22 19:50:01 +0100'
  date_gmt: '2006-01-22 18:50:01 +0100'
  content: Z technicznego punktu widzenia, ATOM jest dużo lepszym formatem od RSS.
    Problem w tym, że u nas daleko mu do popularności.
- id: 3104
  author: Maciej Łebkowski
  author_url: http://lebkowski.info
  date: '2006-01-22 20:13:35 +0100'
  date_gmt: '2006-01-22 19:13:35 +0100'
  content: "<blockquote>Nie, kanał RSS nie jest dokumentem HTML i stosowanie w nim
    encji HTML to raczej głupi pomysł — dokument przestaje być poprawny.</blockquote>\r\n\r\nOczywiście
    poza pięcioma podstawowymi:\r\nhttp://www.w3.org/TR/REC-xml/#sec-predefined-ent\r\n\r\nRozumiem,
    że w tym swoim rozpędzie mówileś również o moim blogu/kanale RSS? Bo ja nie widzę
    u siebie żadnych niepoprawnych danych.\r\n\r\n<blockquote>Gdyby 10przykazan miało
    przetwarzać tylko poprawne dokumenty, to musiałbym usunąć z serwisu wszystkie
    blogi, które nie są oparte o WordPressa.</blockquote>\r\nMówisz o tym samym WP,
    które potrafi podzelić stringa tak, że odcina jeden bajt z dwubajtowego znaku?
    :-)"
- id: 3105
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-01-22 21:56:24 +0100'
  date_gmt: '2006-01-22 20:56:24 +0100'
  content: "Maciej:\r\n\r\nNie, nie chodziło o ciebie akurat. Chodzi mi głównie o
    serwisy typu jogger.pl, blog.pl itp."
- id: 3106
  author: DeeJay1
  author_url: http://www.actus.org.pl/
  date: '2006-01-22 22:50:24 +0100'
  date_gmt: '2006-01-22 21:50:24 +0100'
  content: Nie tak dawno Google sporządziło stosowne statystyki odnośnie feedów, można
    sobie przejrzeć je <a href="http://googlereader.blogspot.com/2005/12/xml-errors-in-feeds.html"
    title="The Official Google Reader Blog - XML Errors in Feeds" rel="nofollow">tutaj</a>,
    jeśli ktoś nie miał okazji oglądać (aczkolwiek wartości są podane w procentach,
    to i tak daje w miarę dobry pogląd na zawartość feedów "blogosfery").
- id: 3108
  author: m
  author_url: ''
  date: '2006-01-23 00:08:57 +0100'
  date_gmt: '2006-01-22 23:08:57 +0100'
  content: "Patrys:\r\n\r\n<blockquote>Z technicznego punktu widzenia, ATOM jest dużo
    lepszym formatem od RSS. Problem w tym, że u nas daleko mu do popularności.\r\n</blockquote>\r\n\r\nHmm,
    ale o co chodzi? Nie przyglądałem się z lupą, ale nie widzę w Atom tych ekstra
    ficzerów rewolucjonizujących ideę RSS ;). Sęk w tym, żeby chociaż dla jednego
    z tych \"standardów\" popularyzować bibliote(cz)ki, które pozwalają na wygodne
    i poprawne tworzenie feedów. Nie wiem, jak to wygląda np. z punktu widzenia programisty
    php, ale generalnie jest trochę kiepsko. A za granicą taki sam śmietnik jak u
    nas.\r\n\r\ni jeszcze:\r\n\r\n<blockquote>\r\nGdyby 10przykazan miało przetwarzać
    tylko poprawne dokumenty, to musiałbym usunąć z serwisu wszystkie blogi, które
    nie są oparte o WordPressa.\r\n</blockquote>\r\n\r\nHej, no skąd to rozżalenie!
    Tak to już jest, że real world nigdy nie będzie idealny, dopóki nie wymrą ludzie,
    poza tym Szef Projektu (TM) nie powinien się martwić takimi pierdołami ;)."
- id: 3109
  author: m
  author_url: ''
  date: '2006-01-23 00:12:36 +0100'
  date_gmt: '2006-01-22 23:12:36 +0100'
  content: "DeeJay1:\r\n\r\n<blockquote>\r\naczkolwiek wartości są podane w procentach,
    to i tak daje w miarę dobry pogląd na zawartość feedów “blogosfery”\r\n</blockquote>\r\n\r\nA
    w Google Readerze to ludzie niby najczęściej blogaski subskrybują? Not so sure
    ;)\r\nSam nie śledzę przez RSS żadnego bloga, bo informacje w interesujących serwisach
    aktualizowane są dużo częściej niż najciekawsze blogi, które mogę sobie wieczorkiem
    przejrzeć sam."
---
<p>Jako programista, stoczyłem ponad miesiąc na polu walki pomiędzy standardami, a wdrożeniami. Chodzi mi oczywiście o technologiczne podłoże <a href="http://10przykazan.com/">10przykazan</a>. Z przykrością stwierdzam, że <em>żaden</em> z agregowanych przez nas serwisów blogowych nie generuje poprawnego kanału <abbr title="Really Simple Syndication">RSS</abbr>.</p>

<p>Piszę to w nawiązaniu do analizy polskiej blogosfery, <a href="http://riddle.jogger.pl/comment.php?eid=183217">napisanej przez Riddle'a</a>, a do której <a href="http://lebkowski.info/arch/2006/01/dokad_idziemy_blogu_moj">nawiązał też Maciej Łebkowski</a>. Poziom techniczny naszego kawałka Internetu przypomina bardziej chałupy zbudowane z powiązanych drutem łodyg bambusa, niż domy. Niby wszystko działa, niby wszystko mamy to samo, ale wystarczy zajrzeć pod śliczny papierek z kokardką, żeby okazało się, że pod spodem mamy pęk drutów posklejanych taśmą klejącą.</p>

<p>Drodzy panowie administratorzy serwisów — kanał <abbr>RSS</abbr> jest aplikacją <abbr title="Extensible Markup Language">XML</abbr> i wymaga kodowania encji w standardzie <abbr>XML</abbr>. Tak, oznacza to dokładnie tyle, że ampersand i znak mniejszości powinny być zamienione na ich odpowiedniki (w praktyce, dla czytelności, zamienia się też znaki większości). Nie, kanał <abbr>RSS</abbr> nie jest dokumentem <abbr title="HyperText Markup Language">HTML</abbr> i stosowanie w nim encji <abbr>HTML</abbr> to raczej głupi pomysł — dokument przestaje być poprawny.</p>

<p>RSS przewiduje dwa formaty podawania dat. Wersja 1.0 i wcześniejsze stosowały kosmiczne kodowanie <abbr title="World Wide Web Consortium">W3C</abbr>, wersja 2.0 podaje czas w standardzie <abbr title="Request For Comments">RFC</abbr> 822. Używanie pierwszego wariantu w <abbr>RSS</abbr> 2.0 jest błędem.</p>

<p>Gdyby 10przykazan miało przetwarzać tylko poprawne dokumenty, to musiałbym usunąć z serwisu wszystkie blogi, które nie są oparte o <a href="http://wordpress.org/">WordPressa</a>.</p>

Technorati Tags: <a href="http://technorati.com/tag/wordpress" rel="tag">wordpress</a>, <a href="http://technorati.com/tag/rss" rel="tag">rss</a>, <a href="http://technorati.com/tag/blog" rel="tag">blog</a>, <a href="http://technorati.com/tag/xml" rel="tag">xml</a>
