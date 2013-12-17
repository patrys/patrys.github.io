---
layout: post
status: publish
published: true
title: Pierwszy z demonów
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 436
wordpress_url: http://room-303.com/blog/2008/03/20/pierwszy-z-demonow/
date: 2008-03-20 14:59:14.000000000 +01:00
categories:
- linux
- software
tags: []
comments:
- id: 18776
  author: tomek
  author_url: ''
  date: '2008-03-20 16:32:51 +0100'
  date_gmt: '2008-03-20 15:32:51 +0100'
  content: myślę, że do postu powinieneś też dodać krótki opis einit, moim zdaniem
    też dość ciekawa alternatywa, która się teraz rozwija.
- id: 18777
  author: Fluxid
  author_url: ''
  date: '2008-03-20 17:21:25 +0100'
  date_gmt: '2008-03-20 16:21:25 +0100'
  content: "Bardzo-bardzo lubię twój styl pisania.\r\nMoże kiedyś się skuszę na PLD,
    ale na razie jestem zadowolony z Gentoo, więc..."
- id: 18778
  author: Andrzej Dopierała
  author_url: http://andrzej.dopierala.name/Blog
  date: '2008-03-20 20:47:27 +0100'
  date_gmt: '2008-03-20 19:47:27 +0100'
  content: Buu... a dla AC nie ma :(
- id: 18797
  author: woo
  author_url: ''
  date: '2008-03-21 22:29:32 +0100'
  date_gmt: '2008-03-21 21:29:32 +0100'
  content: "Pomarańczowy. Pasek postępu jest pomarańczoy.\r\n\r\nCo do upstart to
    Ubuntu folks obiecywali, że wraz ze stopniową konwersją skryptów na nowy mechanizm
    znacznie zmaleje czas uruchamiania systemu. Albo dorzucają cały czas nowe uslugi
    startowe, albo konwersja idzie im nieskładnie albo bezczelnie kłamali. Kolejne
    Ubuntu ślimaczą się tak samo jak stare w tym aspekcie.\r\n\r\nNie żeby mnie to
    ruszało specjalnie - na laptopie i tak używam suspenda a desktop włączam raz dziennie
    i idę podrażnić się z kobietą w międzyczasie.\r\n\r\nFajnie piszesz BTW :s"
- id: 18827
  author: Fluxid
  author_url: ''
  date: '2008-03-24 11:05:42 +0100'
  date_gmt: '2008-03-24 10:05:42 +0100'
  content: "Hehe... Zainstalowałem usptart z ichniego overlaya, okazało się że zastąpił
    mi sysvinit, ale wszystko działało tak jak wcześniej. Grzebałem przy event.d,
    ale nic, kiła. Poza tym widzę nieprzyjemny brak wsparcia.\r\nInitng: nieźle, po
    skonfigurowaniu usług system wstaje 20 sekund szybciej, czyli w ~40. Problemy?
    Mnóstwo. Zawsze segfaultuje przy odpalaniu wifi, czasem przy kablowym necie, co
    trzeci przypadek próby wyłączenia komputera kończy się sefaultem i potrzebą użycia
    jakiegoś \"ostrego narzędzia\" żeby wreszcie zgasł. sulogin się zawiesza, w sensie
    wypisuje mi symbol zachęty, że jestem zalogowany, ale jakiekolwiek polecenie powoduje
    zwis, z którego nie mogę wyjść i znowu muszę użyć ostrego narzędzia, bo init też
    leży przez to.\r\nJeszcze jest einit, tak? eee... Poczekam aż będzie to w miarę
    stabilne..."
- id: 18856
  author: cactus
  author_url: ''
  date: '2008-03-26 23:52:23 +0100'
  date_gmt: '2008-03-26 22:52:23 +0100'
  content: "Dla tych co wola einit przygotowalem spec :\r\neinit i einit-modules-xml\r\nPewnie
    cos tam trzeba jeszcze dopiescic ...\r\n\r\nNie testowalem tego jeszcze - wersja
    0.40.0\r\n(wyglada stabilnie)\r\n\r\ninitng tez mi sprawial problemy ...\r\nupstarta
    bedzie trzeba sprawdzic."
---
<p>Na każdym zebraniu jest taka sytuacja, że ktoś musi zacząć. Przy komputerze nikt kogo pod pistoletem nie trzyma, a skoro pan nie mówi o przyrodzie, możemy przejść do spraw ciekawszych. Jeśli wiesz, czym jest dæmon <code>init</code> i jaka jest jego rola w systemie uniksowym, możesz śmiało przeskoczyć nad płytkim, powierzchownym i łopatologicznym wprowadzeniem, którego się nie spodziewasz, a którym za chwilę uraczę całą resztę. Wpadliście w zasadzkę, marny wasz los.</p>

<h4>Głupi kaowiec</h4>

<p><code>init</code> nie jest wielki, ale lekceważyć go nie wolno. Jest alfą i omegą, krótkie starcie z nim szybko upewni cię, że może to oznacząć początek twojego końca. <q>Jak to?</q> &mdash; pytasz ze zdziwieniem w oczach, gdy ja przypominam ci radosny komunikat:</p>

<blockquote><pre>Kernel panic: Attempted to kill init</pre></blockquote>

<p><code>init</code> jest nieśmiertelny. Rodzi się jako pierwszy i, niczym dobry kapitan, pozostaje na pokładzie do samego końca. Inne procesy traktują go jako dobrotliwego wujka, który przygarnia zbłąkane sieroty, bądź jako wielkiego przedwiecznego, który wszelkie nieposłuszeństwo karze globalną zagładą.</p>

<p><q>Czy powinienem się go bać?</q> &mdash; zapytujesz, a twarz twą oblewa rumieniec. <q>Nie</q> &mdash; odpowiadam, wzbudzając tym większą ciekawość. <code>init</code> to bardzo specyficzna bestia. Uruchamiany jest jako pierwszy proces przestrzeni użytkownika (nie licząc tak zwanego <q>early userspace</q> zawartego w <code>initramfs</code>, odpowiadającego za przygotowanie urządzeń do właściwego uruchomienia systemu) i zawsze jest numerem jeden (chodzi oczywiście o <abbr title="Process ID">PID</abbr>, czyli identyfikator procesu). Przygarnia również sieroty, czyli procesy, które wyrzekają się rodziców. Jądro systemu operacyjnego automatycznie przypisuje wszystkim bezpańskim procesom zastępczego opiekuna w postaci procesu <code>init</code> właśnie.</p>

<p>Mało tego, to właśnie biografia <code>init</code>a zawierać mogłaby <q>i rzekł "niech staną się inne procesy"; i poczęły się uruchamiać usługi; i zobaczył, że było to dobre.</q> Dæmon <code>init</code> pełni rolę nadzorcy całego systemu i troszczy się o to, by uruchomione zostały wszystkie niezbędne do działania komputera usługi (oczywiście mówię o działaniu w pojęciu użytkownika, komputer w pełni zadowoli się samym jądrem i użytkownika do szczęścia nie potrzebuje).</p>

<h4>SysVinit</h4>

<p>Dawno, dawno temu, gdy SCO nie straszyło świata patentami, a głównym zajęciem AT&amp;T nie było sprzedawanie iPhonów stadom amerykańskich nastoletek, ci ostatni, znani jako Laboratoria Bella, opracowywali standard systemu Unix. W owych mrocznych czasach, poprzedzających erę komputera łupanego (gdy komputer zajmuje sporą część budynku, nikomu nie przychodzi do głowy naprawianie go poprzez walenie pięścią w monitor), pojawiła się koncepcja głównego nadzorcy. Sposób jego działania pozostał przez lata właściwie niezmieniony, różniąc się tylko nieco implementacją pomiędzy architekturami i pokoleniami uniksowej rodziny.</p>

<p>Do dziś za wzorcową implementację uznaje się ponad dwudziestoletnią skamielinę, pochodzącą ze standardu System V (właścicielom cyfowych zegarków spieszę wyjaśnić, że tak wygląda rzymska piątka). Obsługuje start usług i przypisywanie ich do różnych profili (System V posiada system siedmiu profili nazywanych poziomami i numerowanych od 0 do 6), potrafi dodatkowo wskrzeszać swoje dzieci, jeśli taka jest wola administratora.</p>

<p>Dlaczego zatem usługi uruchamiane są poza nadzorem systemu? Problemem jest ich elastyczna konfiguracja, możliwość zatrzymywania i uruchamiania w dowolnym momencie, a także fakt, że w przypadku problemów <code>init</code> z System V zupełnie nie interesuje się przyczyną nagłego zgonu.</p>

<h4>W pozostałych rolach</h4>

<p>Konkurencja nie spała. Pomijam systemy oparte o szkielet BSD, który jako model systemu powstał jeszcze przed System V, więc informacja o używaniu innego nadzorcy nie powinna cię zdziwić.</p>

<p>Najszerzej kojarzoną jest z pewnością implementacja <code>daemontools</code>. Jedni twierdzą, że to ze względu na kontrowersyjną postać autora, inni, że jest to wynik radykalnego podejścia do procesu nadzorcy. Rewolucyjnych zmian nie ma tam co szukać, podstawową różnicą jest większa konfigurowalność nadzorowanych usług i rezygnacja z profili uruchomieniowych. O sukcesie podejścia wystarczy powiedzieć tyle, że w 90% przypadków <code>daemontools</code> uruchamiane jest przez&hellip; <code>SysVinit</code>.</p>

<p>Nieco inne podejście zastosowali autorzy <code>initng</code>, rozwijanego przez deweloperów Gentoo. Do tradycyjnego nadzorcy dodano możliwość równoległego uruchamiania wielu usług i wprowadzono prosty system zależności. Zaowocowało to skróceniem czasu startu systemu &mdash; usługi nie musiały stać gęsiego w kolejce i uruchamiane były, gdy tylko zaspokojone zostały ich podstawowe wymagania (zaznaczyć wypada, że większość usług zadowala się działającą siecią bądź samym faktem włączenia komputera, tylko nieliczni domagają się prywatnego apartamentu z widokiem na morze).</p>

<p>Apple z kolei stworzyło <code>launchd</code>, który jest hybrydą pomiędzy tradycyjnym procesem <code>init</code>, dæmonem <code>inetd</code> i usługą <code>cron</code>. Podstawowym udogodnieniem dla użytkowników była tu wprowadzona możliwość uruchamiania usług <q>na żądanie,</q> rozszerzona później przez grupę freedesktop.org i zintegrowana z zarządcą magistrali DBus.</p>

<h4>upstart already!</h4>

<p>Mamy wreszcie projekt <code>upstart</code>, o którym krótko opowiem. <q>Myślałem, że nigdy do tego nie dojdziesz</q> &mdash; wzdychasz pod nosem, sprawdzając, czy mikrofon laptopa na pewno jest wyłączony. Pamiętaj jednak, że dla niektórych Linux to żółty pasek postępu z napisem <q>Loading Ubuntu</q> i każda okazja do postraszenia ich bebechami systemu jest dobra.</p>

<p><code>upstart</code> łączy zalety większości wspomnianych wyżej implementacji. Potrafi emulować zachowanie System V, uruchamiać usługi równolegle, wspiera zależności, a autorzy obiecują, że niedługo może też zastąpić dæmona <code>inetd</code>. Przejście na niego jest bezproblemowe, bo usługi ze starego do nowego formatu przenosić można stopniowo, z każdym krokiem zyskując pełen nadzór nad ich działaniem, automatyczny restart w przypadku awarii i powiadamianie administratora o występujących problemach.</p>

<p><code>upstart</code> dodaje też unikalny system reakcji na zdarzenia, nowe procesy mogą więc zostać uruchomione lub zakończone w odpowiedzi na zmiany zachodzące w działającym systemie. Chcesz, aby system obsługi wydruku działał tylko, jeśli do komputera podłączona jest drukarka? Nie ma problemu. Zatrzymać mniej krytyczne usługi, gdy serwer korzysta z zasilania awaryjnego? Proszę bardzo. Wszystko w automatycznie i z pełnym wglądem w listę tego, co aktualnie działa, co nie działa i dlaczego.</p>

<p>Oczywiście, nie piszę tego wszystkiego bez przyczyny. Wczoraj <code>upstart</code> pojawił się w <a href="http://pld-linux.org/">PLD</a> i skutecznie zastąpił swego pradziadka na wszystkich moich komputerach. Daj mu szansę i zainstaluj pakiet <code>upstart-SysVinit</code>, a jeśli ktoś spyta cię, jaki jest cel projektu, odpowiesz spokojnie:</p>

<blockquote><pre>Attempting to kill init</pre></blockquote>
