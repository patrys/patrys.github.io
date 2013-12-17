---
layout: post
status: publish
published: true
title: Faktury przez API
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 913
wordpress_url: http://room-303.com/blog/?p=913
date: 2010-04-29 15:56:14.000000000 +02:00
categories:
- web
- software
tags:
- centrumfaktur
comments:
- id: 25020
  author: emes
  author_url: ''
  date: '2010-04-30 21:01:52 +0200'
  date_gmt: '2010-04-30 19:01:52 +0200'
  content: Gulasz z serc z kaszą rządzi. Szczególnie ten z Mewy. Aż zaczynam tęsknić
    za Wrockiem...
- id: 25022
  author: fghgf
  author_url: ''
  date: '2010-05-03 14:26:13 +0200'
  date_gmt: '2010-05-03 12:26:13 +0200'
  content: Będzie XML z przestrzenią nazw jako format danych?
- id: 25027
  author: zientus
  author_url: ''
  date: '2010-05-08 01:46:38 +0200'
  date_gmt: '2010-05-07 23:46:38 +0200'
  content: Ktos to kupuje? Chyba trudno mi sobie wyobrazić gorszy model biznesowy...
    No bo jaki ma sens tworzenie po raz n-ty  kolejnego typu "fakturka pro". Nie te
    czasy, takich rozwiązań(także darmowych) jest kazylion i to, że tym razem będzie
    to działało przez przeglądarkę nieczego nie zmieni.
- id: 25028
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-05-08 02:30:45 +0200'
  date_gmt: '2010-05-08 00:30:45 +0200'
  content: "zientus:\r\n\r\nPorada: nie używaj."
- id: 25029
  author: zientus
  author_url: ''
  date: '2010-05-08 11:12:38 +0200'
  date_gmt: '2010-05-08 09:12:38 +0200'
  content: Przecież tylko pytam. I miałem nadzieje na jakieś uzasadnienie, próbę obrony,
    a nie argumentacje na poziomie ekspedientki w mięsnym w czasach głebokiego PRLu.
- id: 25030
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-05-08 11:52:03 +0200'
  date_gmt: '2010-05-08 09:52:03 +0200'
  content: "zientus:\r\n\r\nNie widzę powodu, dla którego miałbym się tłumaczyć z
    wykonywania pracy, za którą ktoś mi płaci."
- id: 25031
  author: zientus
  author_url: ''
  date: '2010-05-08 19:49:39 +0200'
  date_gmt: '2010-05-08 17:49:40 +0200'
  content: No nieładnie tak nie identyfikować się ze swoją pracą/firmą. Widzę, że
    sam siebie redukujesz do roli kółka w machinie. "Zapłacili - zrobiłem i wuj mnie
    interesuje na to co komu." Tylko nie płacz za rok, że znowu trafił Ci się niewypłacalny
    pracodawca. Wiesz co to syndrom ofiary?
- id: 25032
  author: Patrys
  author_url: http://room-303.com/blog/
  date: '2010-05-08 20:50:56 +0200'
  date_gmt: '2010-05-08 18:50:56 +0200'
  content: "zientus:\r\n\r\nWidzę tu raczej syndrom prowokatora. Nie wiesz, do czego
    może służyć aplikacja do wystawiania faktur? Wiesz. Nie wiesz czym się różni od
    innych? Jest opis na stronie, konta są darmowe. Do czego ja ci jestem potrzebny?"
---
<p>Odkąd rozpocząłem współpracę z <a href="http://mirumee.com/blog/">Mirumee</a>, w listach od moich czytelniczek wciąż powtarzało się jedno pytanie — <q>kiedy?</q> W końcu zrobiłem jednak te badania, a blog to nie miejsce na dyskusje o moim życiu łóżkowym, dlatego dziś pomówimy o <a href="http://centrumfaktur.pl/">CentrumFaktur</a>.</p>

<p><strong>Co wybrałbyś zatem, gdyby zaoferowano ci body shot z ciała dowolnie wskazanej przez siebie kobiety¹ lub nieskrępowany dostęp do API pozwalającego szybko, łatwo i bezpiecznie wystawiać faktury z poziomu twojego programu?</strong></p>

<p><small>¹ Chciałem tu napisać, że panie mogą sobie wybrać mężczyznę, ale w ten sposób zmniejszyłbym szanse na to, że ktokolwiek wybierze API.</small></p>

<p>Mamy cholerną nadzieję, że nie lubisz tequili, bo w stworzenie tego API zainwestowaliśmy już sporo czasu. Nie owijając w bawełnę, przechodząc do meritum, bez ogródek i zbędnych ceregieli, waląc prosto z mostu i nie lejąc wody przedstawiam <a href="http://centrumfaktur.pl/api/">dokumentację API CentrumFaktur</a>.</p>

<p>Zdradzę przy okazji, że odnośnikiem tym dzielę się z wami nieprzypadkowo. Wiem bowiem, że przeczytacie, bez wyjątku, wszystko, co tylko napiszę. I będzie się wam podobało. To moja strona i ja tu ustalam zasady.</p>
