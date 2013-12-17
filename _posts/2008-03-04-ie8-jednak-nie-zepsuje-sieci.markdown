---
layout: post
status: publish
published: true
title: IE8 jednak nie zepsuje sieci
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 432
wordpress_url: http://room-303.com/blog/2008/03/04/ie8-jednak-nie-zepsuje-sieci/
date: 2008-03-04 10:49:45.000000000 +01:00
categories:
- web
tags: []
comments:
- id: 17625
  author: Roberto
  author_url: http://roberto.ovh.org
  date: '2008-03-04 11:15:06 +0100'
  date_gmt: '2008-03-04 10:15:06 +0100'
  content: "To jest bardzo pozytywna wiadomość :D\r\ncoś przynajmniej zaczyna się
    dziać\r\n\r\naż trudno mi jest wyobrazić sobie, że IE będzie zgodny ze standardami"
- id: 17627
  author: wojtosz
  author_url: http://www.blaszkowski.com
  date: '2008-03-04 11:40:07 +0100'
  date_gmt: '2008-03-04 10:40:07 +0100'
  content: "bosz.. jak by nie można było od razu zrobić poprawnej interpretacji ?!
    ciekawi mnie kto stał za pomysłem odstępstwa od trzymania się standardów dla ie.
    \r\n\r\ncóż, kolejny powód dla którego produktu z redmont używam do grania CoD
    i CS :&gt;"
- id: 17629
  author: cezio
  author_url: http://thelirium.net
  date: '2008-03-04 12:35:13 +0100'
  date_gmt: '2008-03-04 11:35:13 +0100'
  content: Nie chwal dnia przed zachodem. Chyba, że chcesz potem MS rozliczać za obietnice
    wyborcze ;)
- id: 17635
  author: Mike
  author_url: http://michal.osmenda.com
  date: '2008-03-04 18:11:57 +0100'
  date_gmt: '2008-03-04 17:11:57 +0100'
  content: Amen!
- id: 17636
  author: jpc
  author_url: http://jpc.jogger.pl
  date: '2008-03-04 18:22:03 +0100'
  date_gmt: '2008-03-04 17:22:03 +0100'
  content: "wojtosz: Większość ,,błędów'' popełnili nim powstały standardy, lub na
    swój sposób intepretując drafty. A potem byli zwyczajnie aroganccy i nie chciało
    im się ich poprawiać.\r\n\r\nPatrys: A czy faktycznie tak powinno być? Negocjacja
    features powinna być chyba opt-in, a nie opt-out. Tzn. teraz każdy winien napisać,
    że strona jest zgodna max. z IE8, bo kto wie co wymyślą w nowej wersji. Przy odwrotnym
    (tym, który proponowali) systemie nie piszesz nic, to strona chodzi przez najbliższe
    10 lat tak samo. Chyba, że znajdziesz czas, zmodyfikujesz i dostosujesz do nowej
    wersji.\r\n\r\nAFAIK biblioteki linkowane dynamicznie linkuje się do konkretnego
    ABI, a nie do ABI &gt;= cośtam."
- id: 17637
  author: Patrys
  author_url: http://room-303.com/
  date: '2008-03-04 20:44:16 +0100'
  date_gmt: '2008-03-04 19:44:16 +0100'
  content: "jpc:\r\n\r\nStandardy są zgodne wstecz. Przeglądarki nie implementują
    nowego API/ABI, tylko ulepszają wsparcie dla istniejących standardów. Jeśli ktoś
    polega na błędach w konkretnej implementacji, to jest sam sobie winien. Pozostałe
    przeglądarki będą interpretować kod poprawnie i już dziś efekt będzie daleki od
    oczekiwanego, nie trzeba czekać na nową wersję IE."
- id: 23703
  author: IE8 Beta - Paweł Rabinek blog
  author_url: http://blog.rabinek.pl/2008/03/05/ie8-beta/
  date: '2009-01-09 15:31:29 +0100'
  date_gmt: '2009-01-09 14:31:29 +0100'
  content: '[...] niewtajemniczonych, IE8 ma być sporym krokiem na przód w doścignięciu
    Opery i Firefoxa, pod względem zgodności ze standardami [...]'
---
<p>Z <a href="http://blogs.msdn.com/ie/archive/2008/03/03/microsoft-s-interoperability-principles-and-ie8.aspx">ostatniej notki na IEBlogu</a> wynika, że <abbr title="Internet Explorer">IE</abbr>8 domyślnie będzie wspierał tryb zgodny ze standardami:</p>

<blockquote>We’ve decided that <abbr>IE</abbr>8 will, by default, interpret web content in the most standards compliant way it can. This decision is a change from what we’ve posted previously.</blockquote>

<p>Wcześniejsze zapowiedzi sugerowały konieczność umieszczenia w kodzie specjalnego znacznika, który potwierdzałby, że autor faktycznie życzy sobie taki sposób interpretacji dokumentu. Dlaczego? Przez wersję siódmą przeglądarki, której wydanie okazało się sporym ciosem dla firmy z Redmond. Wiele serwisów (w tym prowadzone przez partnerów Microsoftu) przygotowanych było tylko i wyłącznie dla <q>quirks mode</q> wersji szóstej, tymczasem wersja siódma nauczyła się poprawnie składać dokumenty, co zaowocowało rychłym <q>zepsuciem</q> wadliwych stron.</p>

<p>Microsoft &mdash; w obawie przed kolejnymi próbami linczu &mdash; postanowił dodać do przyszłych wersji przeglądarek funkcję <q>zamrażania</q> zachowania przeglądarki na poziomie konkretnej wersji, a domyślnym poziomem zgodności dla wszystkich przyszłych wydań miał być właśnie <abbr>IE</abbr>7. Oznaczało to dokładnie tyle, że <abbr>IE</abbr>8 zachowywałby się dokładnie jak <abbr>IE</abbr>7 dopóty, dopóki autor strony wyraźnie nie zaznaczył, że życzy sobie wykorzystać możliwości i poprawki wprowadzone w wersji ósmej.</p>

<p>Na szczęście (po wielkiej burzy, jaka wybuchła pomiędzy autorytetami w dziedzinie standardów) zespół zdecydował się nie psuć Sieci i odwrócić działanie mechanizmu. Jak czytamy na blogu przeglądarki, to autorzy wadliwych serwisów zyskają możliwość zaznaczenia <q>przetwarzaj ten dokument tak, jakbyś był wersją X.</q> W efekcie modyfikacji będą musiały ulec tylko te serwisy, których treść i tak może nie być dostępna dla użytkowników innych agentów (przeglądarek biurkowych i urządzeń do przeglądania służących). Mówiąc krótko &mdash; Microsoft sprząta po sobie swoje śmieci i aktywnie wspiera standardy tam, gdzie jest to możliwe.</p>
