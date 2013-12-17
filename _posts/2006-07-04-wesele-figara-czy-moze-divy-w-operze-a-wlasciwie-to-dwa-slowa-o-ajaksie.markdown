---
layout: post
status: publish
published: true
title: Wesele Figara, czy może DIVy w Operze, a właściwie to dwa słowa o Ajaksie
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 272
wordpress_url: http://www.room-303.com/blog/2006/07/04/wesele-figara-czy-moze-divy-w-operze-a-wlasciwie-to-dwa-slowa-o-ajaksie/
date: 2006-07-04 15:38:52.000000000 +02:00
categories:
- web
- software
- code
tags: []
comments:
- id: 4075
  author: quiris
  author_url: http://operapl.net
  date: '2006-07-04 17:10:46 +0200'
  date_gmt: '2006-07-04 16:10:46 +0200'
  content: A gdzie test case z demonstracją problemu? Wydaje mi się, że kto, jak kto,
    ale profesjonalista powinien mieć profesjonalne podejście do tematu. Ile ja się
    naużeram z różnymi "webmasterami", którzy twierdzą, że w ich mniemaniu, coś tam
    Opera źle obsługuje. Jednocześnie, prośba o przedstawienie stosownego dowodu,
    w postaci demonstracji problemu, spotyka się z w odpowiedzi z ciszą. Powtórzę
    jeszcze raz. Możesz przedstawić stosowny dowód?
- id: 4076
  author: quiris
  author_url: http://operapl.net
  date: '2006-07-04 17:13:50 +0200'
  date_gmt: '2006-07-04 16:13:50 +0200'
  content: 'Aha, a gdybyś nie wiedział jak przygotować dobrą demonstrację błędu to
    służę stosownym dokumentem: http://www.w3.org/Style/CSS/Test/guidelines.html'
- id: 4077
  author: medyk
  author_url: http://www.medikoo.com
  date: '2006-07-04 17:42:47 +0200'
  date_gmt: '2006-07-04 16:42:47 +0200'
  content: A to ciekawa informacja.. choć nie sądzę bym kiedykolwiek miał potrzebę
    przekierowywania  wywołań ajaxa.
- id: 4078
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-07-04 19:39:42 +0200'
  date_gmt: '2006-07-04 18:39:42 +0200'
  content: "quiris:\r\n\r\nNie trzeba mnie uczyć pisania test case, jestem programistą
    z zawodu i siedzę w OS ze względu na hobby. Poza tym nikt nie napisał, że coś
    jest zepsute i nie widzę powodu, żeby coś demonstrować. Opera zwyczajnie jako
    wynik XmlHttpRequest zwraca pierwszy dokument, który dostanie (czyli jako status
    podaje 302 i kończy zapytanie), podczas gdy Fx podąża za nagłówkiem przekierowania
    i zwraca dopiero tamten dokument (ze statusem 200). Opera 9, buga tu nie widzę,
    bo raczej rzadko używa się przekierowań w powiązaniu z Ajaksem (tu wynikało akurat
    ze specyfiki skryptu, który każdy POST automatycznie przekierowywał, żeby zapobiec
    zmianie danych przez \"refresh\")."
- id: 4079
  author: quiris
  author_url: http://operapl.net
  date: '2006-07-04 20:04:39 +0200'
  date_gmt: '2006-07-04 19:04:39 +0200'
  content: "<blockquote>Nie trzeba mnie uczyć pisania test case, jestem programistą
    z zawodu i siedzę w OS ze względu na hobby.</blockquote>Wiem kim jesteś i dlatego
    napisałem, to co napisałem. Władzia, który napisał pierwszą stronę w życiu, nie
    prosiłbym o zademonstrowanie zachowania. Od Ciebie, jako profesjonalisty, wymagam
    profesjonalnego podejścia do sprawy ;)\r\n\r\n<blockquote> Opera zwyczajnie jako
    wynik XmlHttpRequest zwraca pierwszy dokument, który dostanie (czyli jako status
    podaje 302 i kończy zapytanie), podczas gdy Fx podąża za nagłówkiem przekierowania
    i zwraca dopiero tamten dokument (ze statusem 200).</blockquote>Wiem na czym polegają
    przekierowania. Jednak przy wszelkich zgłoszeniach o błędach (nieprawidłowych
    zachowaniach) krytycznie ważny jest poprawnie zbudowany test case. I dalej będę
    Cię prosił o przedstawienie takiego, ponieważ wypadałoby do końca wyjaśnić, czy
    to jest zachowanie prawidłowe, czy nie.\r\nWg roboczej specyfikacji http://www.w3.org/TR/XMLHttpRequest/#xmlhttprequest
    UA MUSI jednak podążać za przekierowaniem:\r\n\r\n\"If the response is an HTTP
    redirect (status code 301, 302, 303 or 307), then it MUST be transparently followed
    (unless it violates security, infinite loop precautions or the scheme isn't supported).
    Note that HTTP [RFC2616] places requirements on UAs regarding the preservation
    of the request method during redirects, and also requires users to be notified
    of certain kinds of automatic redirections.\"\r\n\r\nChoć z pewnymi wyjatkami.
    Pytanie: Czy taki wyjątek zachodził w Twoim przypadku, czy nie? Ad vocem: Opera
    \ ma niezwykle drakońskie zabezpieczenia przeciw XSS, więc może istnieć podejrzenie
    takiego działania, dlatego, znowu, potrzebna jest strona demonstrująca zachowanie
    ;)\r\n\r\nI nawet, jeśli stwierdzimy, że standardu jako takiego jeszcze nie ma,
    to Opera w imię zachowania interoperacyjności z innymi przeglądarkami, powinna
    podążać ze przekierowaniami i to należy zgłosić jako niedoróbkę, a do tego potrzebny
    jest... już wiesz... test case ;)"
- id: 4080
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-07-04 20:13:56 +0200'
  date_gmt: '2006-07-04 19:13:57 +0200'
  content: "Ok, nie jestem w tej chwili w stanie (nie jestem w domu) zbudować proof-of-concept,
    a kod serwisu już nie używa przekierowań, ale mogę powiedzieć, jak to działało:\r\n\r\n-
    /plik1 zawiera DIV, do którego jest wołany Ajax.Updater ze script.aculo.us, jako
    URI podana jest ścieżka absolutna /plik2 i typ zapytania POST\r\n- /plik2 obsługuje
    post i zwraca status 302 z nagłówkiem Location: /plik3 (ścieżka absolutna, bez
    podania hosta, więc nie zachodzi niebezpieczeństwo XSS)\r\n- /plik3 dowolny, niepusty\r\n\r\nOczekiwane
    zachowanie: DIV zostaje wypełniony zawartością /plik3\r\n\r\nFaktyczne zachowanie:
    DIV zostaje wyczyszczony, bo /plik2 zwraca puste ciało dokumentu (zgodnie z zasadą
    budowania przekierowania)."
- id: 4082
  author: diz
  author_url: ''
  date: '2006-07-04 21:17:51 +0200'
  date_gmt: '2006-07-04 20:17:51 +0200'
  content: "Można to było rozwiązać przez dodanie obsługi statusu 302.\r\n\r\nCzyli
    sprawdzić nagłówek \"Location\" przez getResponseHeader i puścić drugie zapytanie.\r\n\r\nWidziałem
    jakąś dyskusję na ten temat na forum Opery, ale nie pamiętam czy zostało to uznane
    jako bug czy też nie."
- id: 4083
  author: quiris
  author_url: http://operapl.net
  date: '2006-07-04 22:12:28 +0200'
  date_gmt: '2006-07-04 21:12:28 +0200'
  content: "Hmm... To wszystko wygląda mi na błąd w Operze. \r\nhttp://my.opera.com/community/forums/topic.dml?id=133680\r\nhttp://my.opera.com/community/forums/topic.dml?id=140253\r\n\r\nBTW.
    Znalazłem ciekawy zestaw testów pokazujący różnice w implementacjach XMLHttpRequest:
    http://www.mnot.net/javascript/xmlhttprequest/"
- id: 4086
  author: Tomash
  author_url: http://tomash.jogger.pl
  date: '2006-07-05 14:55:54 +0200'
  date_gmt: '2006-07-05 13:55:54 +0200'
  content: "Tak z tej okazji - mistrzostwo świata:\r\nhttp://www.yatblog.com/wp-content/uploads/2006/06/pm20060621.png"
- id: 4088
  author: BartekB
  author_url: ''
  date: '2006-07-05 20:14:48 +0200'
  date_gmt: '2006-07-05 19:14:48 +0200'
  content: "Tak a propos, to oczywiście wiecie, że wg RFC2616 po Location: ma być
    absoluteURI, czyli np. Location: http://www.w3.org/pub/WWW/People.html\r\nTak,
    wiem, że większość chyba implementacji obsługuje też formę  typu  /pub/WWW/People.html
    \ , bez protokołu i serwera, kierując request do serwera, który zwrócił dane Location:..."
---
<p>Wczoraj i dziś straciliśmy kilka godzin na diagnozowanie bardzo dziwnego zachowania Opery — okazało się bowiem, że przeciąganie produktu do koszyka i odświeżenie tego ostatniego po Ajaksie istotnie zwiększało liczbę zamówionych sztuk, jednak sam koszyk nagle znikał w bliżej nieokreślonych okolicznościach. W Operze. Firefox i Internet Explorer nie pokazywały nic dziwnego. Sama konsola błędów Opery też milczała, co irytowało mnie jeszcze bardziej.</p>

<p>W końcu sprawdziłem wszystkie możliwości i okazało się, co następuje: <strong>Opera nie obsługuje przekierowań <q>temporarily moved</q> i <q>permanently moved</q> w przypadku treści wołanej przez <code>XmlHttpRequest</code></strong>. Mam nadzieję, że zaoszczędzi to komuś kłopotu w przyszłości.</p>

Technorati Tags: <a href="http://technorati.com/tag/opera" rel="tag">opera</a>, <a href="http://technorati.com/tag/ajax" rel="tag">ajax</a>, <a href="http://technorati.com/tag/redirect" rel="tag">redirect</a>
