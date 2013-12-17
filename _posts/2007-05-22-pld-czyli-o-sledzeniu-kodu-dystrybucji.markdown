---
layout: post
status: publish
published: true
title: PLD, czyli o śledzeniu kodu dystrybucji
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 375
wordpress_url: http://room-303.com/blog/2007/05/22/pld-czyli-o-sledzeniu-kodu-dystrybucji/
date: 2007-05-22 19:04:24.000000000 +02:00
categories:
- linux
- software
tags: []
comments:
- id: 7962
  author: mb
  author_url: http://mb.jogger.pl/
  date: '2007-05-22 23:20:43 +0200'
  date_gmt: '2007-05-22 22:20:43 +0200'
  content: "Nie siedzę za bardzo w temacie, ale Mozilla brała jeszcze pod uwagę Bazaar:\r\nhttp://bazaar-vcs.org/\r\nhttp://weblogs.mozillazine.org/preed/2007/04/version_control_system_shootou_1.html"
- id: 7963
  author: mavx
  author_url: ''
  date: '2007-05-23 07:42:39 +0200'
  date_gmt: '2007-05-23 06:42:39 +0200'
  content: "mmazur ogłosił niedawno testowe wdrożenie układu podobnego do używanego
    przez Portage.\r\n\r\nNo żesz jego mać NARESZCIE! :)\r\nPróbowałem kilkukrotnie
    swoich sił z PLD, bardzo mi się podoba jako dystrybucja, ale jako zwykły Linux
    (L)user miałem poważny problem z instalacją i updejtem repozytoriów, kodu itp.,
    co z kolei zmusiło mnie do używania dystrybucji o bardziej ludzkim podejściu do
    tematu (ubuntu).\r\n\r\nMam nadzieję, że niedługo wyjdzie ten ficzer z fazy testowej
    i wrócę do PLD :)"
- id: 7964
  author: Liloo
  author_url: ''
  date: '2007-05-23 07:52:06 +0200'
  date_gmt: '2007-05-23 06:52:06 +0200'
  content: "W Bazaarze można zaimplementować cos takiego jak Review Board. Jest to
    PQM (patch queue manager) i coś takiego, co umozliwia glosowanie na nadsylane
    latki i jesli odpowiednia ilosc glosow jest zebrana, latka zostaje zaaplikowana:\r\nhttp://bundlebuggy.aaronbentley.com/"
- id: 7966
  author: Andrzej Dopierała
  author_url: http://andrzej.dopierala.name/
  date: '2007-05-23 16:15:44 +0200'
  date_gmt: '2007-05-23 15:15:44 +0200'
  content: 'mavx: repo to wewnętrzna sprawa pld. niedevelopera to raczej nie interesuje.
    Więc jak jako "niedeveloper" miałeś problemy z pld, to zmiana repo na svn, zmiana
    struktury w nim... albo cokolwiek innego Twoich problemów nie rozwiąże ;)'
---
<p>Od jakiegoś czasu na listach <abbr title="PLD Linux Distribution">PLD</abbr> toczy się dyskusja na temat zmiany układu repozytorium. mmazur <a href="http://mmazur.jogger.pl/2007/05/17/portage-like-repo-layout/">ogłosił niedawno testowe wdrożenie</a> układu podobnego do używanego przez Portage. Mam nadzieję, że to pierwszy krok na drodze do zmiany samego systemu wersjonowania kodu. A ma co śledzić, bo — wbrew pozorom — dystrybucja to dziesiątki tysięcy plików, nad którymi trzeba jakoś zapanować.</p>

<h4>CVS</h4>

<p>Obecnie do zarządzania repozytorium używamy CVS. Ma swoje wady i zalety. Przede wszystkim można w nim wiele rzeczy automatyzować, choćby ze względu na to, że pliki w repozytorium mają swoje przełożenie 1:1 na fizyczne pliki na dysku. Plik <code>foo.spec</code> ma wszystkie swoje dane w pliku <code>foo.spec,v</code> i można go sobie ręcznie backupować, edytować albo zmienić mu nazwę. No właśnie, CVS ma kilka wad:</p>

<ul>
<li>Nie ma możliwości przeniesienia czegokolwiek w repozytorium. Można usunąć plik i dodać go pod nową nazwą, ale w tym momencie tracimy jakąkolwiek historię. Jedyna opcja to fizyczna zmiana nazwy pliku kontroli wersji przez osobę z uprawnieniami administratora na serwerze.</li>
<li>Gałęzie i tagi są przywiązane do poszczególnych plików kopiowanie, scalanie i przenoszenie plików pomiędzy gałęziami to prawdziwy wrzód na dupie.</li>
<li>Z powyższego powodu, praca na kilku gałęziach jednocześnie jest bardzo męcząca. Każdą gałąź trzeba pobrać z repozytorium do osobnego katalogu. Każdy nowy plik odpowiednio oznaczyć, bo w przeciwym wypadku trafi w najmniej pożądane miejsce. Do tego musimy spierać się z serwerem o to, że wiemy, że plik o identycznej nazwie już istnieje na innej gałęzi, ale nie ma nic wspólnego z naszym.</li>
<li>Nie istnieją zestawy zmian, każda zmiana w repozytorium jest pojedynczą operacją i nie ma po niej śladu w żadnym pliku poza aktualnie modyfikowanymi.</li>
</ul>

<h4>Mercurial</h4>

<p>Świeżutka zabawka, łatwo rozwijalna, ale jeszcze nie spełnia oczekiwań dużej dystrybucji:</p>

<ul>
<li>Każda kopia robocza jest pełnym odbiciem lustrzanym głównego repozytorium. Nie ma możliwości pobrania jednego pliku, dokonania w nim zmian i wysłania z powrotem.</li>
<li>Rozbicie na rewizje i kody zestawów zmian jest bardzo nieintuicyjne ze względu na fakt, że tylko kod szesnastkowy jest unikalny.</li>
<li>Zaśmieca kopię roboczą, tworząc w niej katalogi z metadanymi, co utrudnia pracę z narządziami operującymi na plikach rekursywnie (<code>diff</code>, <code>find</code>, <code>grep</code>).</li>
</ul>

<h4>GIT</h4>

<p>Rozproszony system kontroli wersji zaprojektowany przez Linusa Torvaldsa. Nadawałby się świetnie, gdyby nie to, że ma intuicyjność składni zbliżoną do Emacsa. W związku z tym, nikt nie zmusi deweloperów, żeby z dnia na dzień nauczyli się nowego narzędzia i przepisali wszystkie swoje skrypty. Zwłaszcza, że z opcji pracy offline skorzysta góra kilka osób (w przypadku dystrybucji, ciężko bez dostępu do sieci zbudować jakikolwiek pakiet).</p>

<h4>Subversion</h4>

<p>Narzędzie sprawdzone, oferuje to samo, co CVS, jednocześnie poprawiając jego niedociągnięcia. Nie oferuje pracy na rozproszonych kopiach repozytorium. Ma za to jedną wadę Mercuriala:</p>

<ul>
<li>Zaśmieca kopię roboczą, tworząc w niej katalogi z metadanymi.</li>
<li>Kod pobrany z repozytorium zajmuje dwa razy więcej miejsca niż powinien, bo trzymana jest lokalna kopia pliku (co pozwala na częściową pracę offline).</li>
</ul>

<h4>Subversion + SVK</h4>

<p>Wyobraźcie sobie Subversion, ale bez wspomnianych problemów. Z pełnym wsparciem dla pracy offline. To właśnie jest SVK — pełni rolę klienta Subversion, zarządzając jednocześnie kopią roboczą i klonami repozytorium. Kopie robocze nie są wzbogacane o żadne magiczne katalogi z metadanymi, nie mają narzutu w postaci trzymania kopii plików, a do tego system potrafi śledzić lokalne scalenia i automatycznie podpowiada komentarz przy upychaniu swoich zmian z powrotem do głównego repozytorium Subversion.</p>

<p>Rozwiązanie niemal idealne — miłośnicy GIT mają swoje ulubione funkcje, a reszta może używać tradycyjnego klienta Subversion. Bez żadnej magii shellowej.</p>

<h4>Review Board</h4>

<p>A skoro już mowa o Subversion, to kilka dni temu <a href="http://www.chipx86.com/blog/?p=222">chipX86 ogłosił projekt</a>, który stworzyli wewnętrznie na potrzeby VMware. <a href="http://code.google.com/p/reviewboard/">Review Board</a>, bo tak się nazywa, to aplikacja Django, która pozwala wygodnie przechowywać nadsyłane łatki. Na listach <abbr>PLD</abbr> pojawia się ich sporo i często giną w czeluściach skrzynek pocztowych. Coś takiego z pewnością by nam się przydało — miejsce, gdzie każdy z uczestników listy może zaproponować swoje zmiany i otrzymać komentarze jeszcze przed włączeniem ich do samej dystrybucji. Miejsce, gdzie łatki nie giną.</p>
