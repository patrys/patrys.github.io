---
layout: post
status: publish
published: true
title: 'Internet Explorer: Pomocy!'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 297
wordpress_url: http://www.room-303.com/blog/2006/10/20/internet-explorer-pomocy/
date: 2006-10-20 14:07:46.000000000 +02:00
categories:
- web
- software
- code
tags: []
comments:
- id: 4978
  author: dominik
  author_url: http://www.ekstenso.com/blog
  date: '2006-10-20 15:51:37 +0200'
  date_gmt: '2006-10-20 14:51:37 +0200'
  content: Miałem kiedyś coś podobnego ale to było dawno i nieprawda i really nie
    umiem sobie przypomnieć :( jak zwalczyłem tego rodzaju odjazdy ie6. Rozumiem,
    że kod nie bardzo można zobaczyć. Rozumiem, że wywaliliście wszystkie *.js na
    próbę?
- id: 4979
  author: nightman
  author_url: ''
  date: '2006-10-20 16:47:03 +0200'
  date_gmt: '2006-10-20 15:47:03 +0200'
  content: "Miałem kiedyś podobny problem przy dość skomplikowanej stronie, opartej
    na przeogromiastym szablonie. \r\n\r\nAby dojść do tego co powodowało problem
    musiałem rozebrać projekt \"wstecz\" kawałek po kawałku. Niestety nie pamiętam
    co było dokładnie nie tak - chyba coś z wysokościami elementów (dokładnie height
    100%). Robione to było jeszcze za czasów tabelek więc nie wiem czy to się w ogóle
    ima do Twojego problemu. Podobnie jednak jak u Ciebie, na innych przeglądarkach
    strona wyświetlała się poprawnie. Tylko IE 6 \"gubił\" część strony.\r\n\r\nCo
    mogę Ci polecić to:\r\n\r\n1. Sprawdź elementy z height 100% zagnieżdzone w innych.
    Właśnie z wyświetlaniem tego typu rzeczy, w pewnych specyficznych przypadkach
    IE6 u mnie sobie nie radził.\r\n\r\n2. Rozłóż kod strony na kawałki - wycinaj
    na początku dużymi kęsami aż do momentu dojścia do momentu gdy problem zniknie
    - wtedy skup się na wyciętym kawałku - pracochłonne ale przy odpowiednim zacięciu
    masz duże szanse dojścia do tego co powoduje problemy. Jeśli nie to podeślę Ci
    gratis miecz samurajski abyś popełnił rytualne harakiri.\r\n\r\nNie mam pojęcia
    czy to problem kodu strony ale jest to bardzo możliwe (inne przeglądarki przecież
    wyświetlają stronę poprawnie).\r\n\r\nSzczerze życzę Ci powodzenia w rozwiązaniu
    problemu."
- id: 4980
  author: opi
  author_url: http://bronikowski.com
  date: '2006-10-20 18:27:42 +0200'
  date_gmt: '2006-10-20 17:27:42 +0200'
  content: Zupełnie z głupia franc. Weź te obrazki przepuść przez jakiś server-side,
    np. PHP i przed wysłaniem ich mime-type puść, że się zmieniły. Ciekawe, czy tak
    obszadzone będą się wyświetlać.
- id: 4990
  author: ludwikc
  author_url: http://blog.ludwikc.net
  date: '2006-10-21 08:46:29 +0200'
  date_gmt: '2006-10-21 07:46:29 +0200'
  content: "U mnie z kolei, (też w IE6) nie da się zarejestrować (zni nawet zobaczyć)
    szkoleń microsoftu na na microsoftelearning.com. A w firefoksie działa bez zarzutu
    :)\r\n\r\nlink: https://www.microsoftelearning.com/catalog/itproDev.aspx :)"
- id: 5016
  author: Nina
  author_url: http://blog.monoverse.net
  date: '2006-10-25 07:54:19 +0200'
  date_gmt: '2006-10-25 06:54:19 +0200'
  content: "Electric shiver cross my skin...it´s like a fever, and you´re my only
    medicine ;)\r\n\r\nWybacz, ale nie mogłam się powstrzymać, od razu mi się przypomniała
    ta reklama :&gt;"
- id: 5017
  author: Nina
  author_url: http://blog.monoverse.net
  date: '2006-10-25 07:57:06 +0200'
  date_gmt: '2006-10-25 06:57:06 +0200'
  content: boże, nie ten wpis ;) ale wstyd... :&gt;
- id: 5294
  author: dalmacja
  author_url: ''
  date: '2006-11-26 20:22:42 +0100'
  date_gmt: '2006-11-26 19:22:42 +0100'
  content: "Witajcie!\r\n\r\nA ja mam taki problem z Explorerem.Cokolwiek bym nie
    chciała ściągnąc z netu ,wyskakuje informacja \" Internet Explorer nie może otworzyć
    lub nie znalazł żądanej witryny \".I tak jest z każdą rzeczą jaką próbuje ściągnąć
    i obojętnie z jakiej stronki.Nie mam pojęcia co się dzieje.Wprawdzie jestem laikiem
    w sprawach komputerowych ale zawsze dawałam sobie rade.Teraz siedze nad tym 2
    dni i nic.R a t u n ku !!!!"
---
<p>Kolejny dzień spędzamy na poszukiwaniu przyczyny chorego zachowania <abbr title="Internet Explorera">IE</abbr>6.</p>

<p>Efekt jest taki, że losowo przerywa przetwarzanie dokumentu, a efektem jest jedynie fragment drzewa <abbr title="Document Object Model">DOM</abbr>. Co ciekawe, przy każdym odświeżeniu strony, utyka gdzie indziej. Próbowałem to rozdłubać nawet <a href="http://www.fiddlertool.com/">Fiddlerem</a>. Ten ostatni pokazuje też, że <abbr>IE</abbr> pyta serwera, czy grafiki się zmieniły, otrzymuje odpowiedź 304, po czym dziarsko uznaje, że grafiki nie da się załadować.</p>

<p>W każdej innej przeglądarce, z <abbr>IE</abbr>7 włącznie, serwis działa poprawnie.</p>

<p>W życiu takiego cyrku nie widziałem. Pomoże nam ktoś?</p>

<p><strong>Update:</strong> chłopaki z <a href="http://janmedia.com/">Janmedia</a> zdiagnozowali problem &mdash; winnym okazał się serwis <a href="http://video.google.pl/">Google Video</a> i wtyczka do Flasha. Otóż po załadowaniu odtwarzacza googlowego, <abbr>IE</abbr> przestawał ładować cokolwiek więcej. Czekamy jeszcze na potwierdzenie, czy to jedyna przyczyna.</p>
