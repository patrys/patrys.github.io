---
layout: post
status: publish
published: true
title: Wyjątkowość PHP
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 402
wordpress_url: http://room-303.com/blog/2007/08/15/wyjatkowosc-php/
date: 2007-08-15 21:18:09.000000000 +02:00
categories:
- software
- code
tags: []
comments:
- id: 8385
  author: Wojtosz
  author_url: http://www.blaszkowski.com/
  date: '2007-08-16 00:29:49 +0200'
  date_gmt: '2007-08-15 23:29:49 +0200'
  content: "@Patrys\r\nOgólnie (rozpatrując sesn całego przesłania) nie powiedziałeś
    nic nowego :) Ot, kolejny \"niuans\" PHP jakim zostaliśmy uraczeni\r\n.\r\nKażdy,
    kto trochę więcej w PHP pisał i tknął prawdziwych języków (C++, Python) odniesie
    wrażenie, że PHP to bałaganiarski język. To, co dzieje się z PHP obecnie to próba
    jego ujednolicenia, uspójnienia (jeśli moge się wyrazić w ten sposób). \r\n\r\nPamiętasz
    zapewne wkroczenie na arenę PHP3 - rewolucja (rewolta ?) ;-)\r\nPHP tworzone było
    w chaotyczny sposób przez zbyt dużą grupę ludzi - a nie trudno w takich przypadkach
    zaprzeczyć, że prezentowali oni różne poziomy wiedzy. Efektem tego jest niekompatybilność
    PHP5 vs. PHP4 (że o trójce nie wspomnę).\r\n\r\nCo mamy dzisiaj ? \r\nPHP spogląda
    w stronę platformy .NET. Jedna po drugiej następują próby _odbadziewienia_ PHP
    (nie bójmy się tego sformuowania !), co widać np. czytając wzmianki o PHP6 (AFAIK
    chyba pisałem już kiedyś o tym na Twoim blogu). Tu będziemy mięli kolejne niekompatybilności
    z poprzednikami, ale w mojej opinii sytuacja zmieża w dobrą stronę i dobrze, że
    owa niekompatybilność z wcześniejszymi wersjami występuje.\r\n\r\nŻyczę dobrze
    przespanej nocy :)"
- id: 8387
  author: agaran
  author_url: ''
  date: '2007-08-16 08:08:20 +0200'
  date_gmt: '2007-08-16 07:08:20 +0200'
  content: "Nie masz pojecia o ornitologii? nie wiesz co to 'ptaszek'?\r\n\r\nps.
    nie moglem siepowstrzymac"
- id: 8388
  author: AdamK
  author_url: http://adamk.jogger.pl
  date: '2007-08-16 08:21:45 +0200'
  date_gmt: '2007-08-16 07:21:45 +0200'
  content: "To nie jest kwestia kompatybilności (tak mnie się przynajmniej wydaje).
    W PHP5 w porównaniu do PHP4 są duże zmiany które powodują niekompatybilność.\r\n\r\nTo
    o czym piszesz, to dodatkowe biblioteki. Jest ich w PHP całkiem sporo, i przepisanie
    wszystkiego od nowa 'po obiektowemu' zajmie trochę czasu. To się dzieje - zauważ
    że obecnie są np. dwa rodzaje współpracy z MYSQL - stara (nieobiektowa) i nowa
    (obiektowa).\r\n\r\nPo prostu PHP jest ofiarą swojej popularności - ma w tej chwili
    wielką inercję i nie da się wprowadzać zmian rewolucyjnie, trzeba to czynić ewolucyjnie."
- id: 8389
  author: smk
  author_url: http://staff.xiaoka.com/smoku/
  date: '2007-08-16 09:26:09 +0200'
  date_gmt: '2007-08-16 08:26:09 +0200'
  content: "Czepiasz się. Czepiasz się. Czepiasz się po trzykroć.\r\n\r\nPHP5 jest
    językiem obiektowym. Ma wsparcie dla wyjątków i to całkiem porządne.\r\n\r\nTo,
    że uparłeś się używać standardowej biblioteki PHP3, to już Twoja własna decyzja.
    Biblioteki tworzone dla PHP5 tej \"wady\" nie mają.\r\n\r\n\r\nTo tak jakbym ja,
    pisząc w D (który udostępnia dla wygody natywny interface do C), czepiałbym się,
    że stdlibc (glibc konkretnie), nie sygnalizuje mi błędów wyjątkami, nie wspiera
    programowania kontraktowego itd.\r\n\r\nŚwiadomie podjąłeś decyzję o używaniu
    prehistorycznej biblioteki, to świadomie licz się z tego konsekwencjami."
- id: 8391
  author: Wojtosz
  author_url: http://www.blaszkowski.com/
  date: '2007-08-16 10:33:31 +0200'
  date_gmt: '2007-08-16 09:33:31 +0200'
  content: "@smk\r\n\r\ne? przeczytaj raz jeszcze wpis by AdamK.\r\n\"przepisanie
    wszystkiego od nowa ‘po obiektowemu’ zajmie trochę czasu\" - wziąłeś pod uwagę,
    że w nowych rzeczach nie ma tych wszystkich funkcjonalności co w starych ?\r\n\r\nPrzypuszczam,
    że do tego pije Patrys."
- id: 8392
  author: Zisurrin
  author_url: ''
  date: '2007-08-16 11:11:07 +0200'
  date_gmt: '2007-08-16 10:11:07 +0200'
  content: Z drugiej strony są osoby, które uważają, że nic lepszego od PHP4 już nie
    może być. Wystarczy popatrzeć, jakie głosy pojawiły się po rozpoczęciu akcji http://gophp5.org/
    Także problemem mogą nie być tyle twórcy języka, co osoby, które go wykorzystują.
    To one będą hamowały przejście do nowych rozwiązań.
- id: 8393
  author: jarek .// wolnystrzelec.com
  author_url: http://wolnystrzelec.com
  date: '2007-08-16 11:15:45 +0200'
  date_gmt: '2007-08-16 10:15:45 +0200'
  content: 'Wojtosz : Chyba nawet nie chodzi o samo ''zajmie trochę czasu'' tylko
    o parcie społeczności w tym kierunku - tworzenia kodu łatwiejszego do utrzymania,
    zrozumienia. Jednak w części firm  oprogramowanie   jest tworzone na zasadzie
    : tworzymy stronę, dodajemy 2 formularze i nazywamy je cms-em, oddajemy klientowi
    i "zapominamy". Jednak gdy klient odezwie się po raz kolejny w celu dodania jakieś
    funkcjonalności , zaczynają się kłopoty ("hm... do czego to miało służyć...").
    Ale miejmy nadzieję że z czasem się to zmieni.'
- id: 8395
  author: mcv
  author_url: http://mcv.jogger.pl/
  date: '2007-08-16 15:25:47 +0200'
  date_gmt: '2007-08-16 14:25:47 +0200'
  content: "Ja mam chroniczny ból lewego małego palca od trzymania Shifta przy każdym
    znaku $. Muszę się „przezwyczaić” na wciskanie Shifta prawym małym palcem dla
    wszystkich znaków znajdujących się po lewej stronie klawiatury. ;-)\r\n\r\nPHP
    to właściwie jest nielogiczny. Nie mogę napisać:\r\n$x = $y-&gt;metoda()[0];\r\n\r\nMuszę:\r\n$z
    = $y-&gt;metoda();\r\n$x = $z[0];"
- id: 8396
  author: Wojtosz
  author_url: http://www.blaszkowski.com
  date: '2007-08-16 16:09:28 +0200'
  date_gmt: '2007-08-16 15:09:28 +0200'
  content: "@wolnystrzelec.com\r\nczy nie sadzisz, ze owo poparcie jest scisle z przeznaczonym
    na zmiany czasem powiazane ?\r\n\r\nodnosnie zapamietywania WTF funkcjonalnosci
    pozwole sobie zasugerowac prowadzenie dokumentacji. pomysl sprawdza sie od wielu
    lat :)"
- id: 8397
  author: qwiat
  author_url: ''
  date: '2007-08-17 01:42:13 +0200'
  date_gmt: '2007-08-17 00:42:13 +0200'
  content: Patrys, najpierw chwalisz Pythona a potem ganisz PHP. To mi zalatuje hipokryzją.
    ;]
- id: 8398
  author: jarek .// wolnystrzelec.com
  author_url: http://wolnystrzelec.com
  date: '2007-08-17 08:05:31 +0200'
  date_gmt: '2007-08-17 07:05:31 +0200'
  content: "@Wojtosz:\r\nJednak sam czas nie sprawi że Ci ludzie  zaczną tworzyć projekty
    inaczej.\r\nMiejmy nadzieje że  z czasem zmusi ich do tego jakiś zamach stanu
    w php.net albo wymagania rynku :). \r\n\r\n\"odnosnie zapamietywania WTF funkcjonalnosci....\"\r\nTeż
    tak uważam. Czego nie mogę powiedzieć o niektórych osobach których projekty muszę
    poszerzać/poprawiać :)."
- id: 8399
  author: Atrakcyjny Wlodzimierz
  author_url: ''
  date: '2007-08-17 11:12:58 +0200'
  date_gmt: '2007-08-17 10:12:58 +0200'
  content: "Lubię oświecać początkujących, więc dodam swoje dwa gr.\r\nJak ktoś już
    wspomniał - wyjątki pojawiły się w PHP5, natomiast większość API pamięta wersje
    dużo starsze - nie zostało ono dostosowane do rzucania wyjątkami. Ale MOŻESZ,
    pisząc własny kod\r\ntymi wyjątkami rzucać. Dodatkowo, nowe biblioteki stawiają
    na Exceptions (chociażby To naprawdę proste.\r\nZgodność wsteczna, wrappery. Nie
    rozumiesz ideii wyjątków.\r\nMapowanie return false z throw Ex?\r\nTo jest kwestia
    zaprojektowania nowej filozofii wykonywania pewnych czynnosci w ramach języka.
    Nikt tego nie obiecywał,\r\nza to klikacze mogą z powodzeniem używać wyjątków
    w ramach własnych klas. To bardzo użyteczne.\r\n\r\n\r\nTak zupełnie gratis podpowiem,
    że chociażby w C++ bez rzutu wyjątkiem wewnątrz wywoływanej funkcji/metody twój
    kod będzie nadal sieczką if if if if if.\r\n\r\nZ początkiem postu oczywiście
    się zgodzę, bo PHP oczywiście obsysa, tyle że nocą jest księżyc, w dzień słońce,
    a spice girls są znowu razem. Czyt. \"STARE\" / \"BYŁO\" / \"ZNOWU\" / \"DOBRY
    MELANŻ BYŁ?\""
- id: 8400
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-08-17 11:18:32 +0200'
  date_gmt: '2007-08-17 10:18:32 +0200'
  content: "Atrakcyjny:\r\n\r\nProblemem nie jest to, że core pamięta czasy PHP3.
    Problemem jest to, że co i rusz na listach deweloperskich PHP czytam o tym, że
    \"X się nie zmieni na model obiektowy, bo PHP ma mieć niski próg wejścia i łagodną
    krzywą nauki.\" Z takim podejściem, to i w PHP7 nie będzie obiektowego dostępu
    do IO, gdzie wyjątki przydają się najbardziej, bo i najwięcej błędów tam się może
    pojawić."
- id: 8404
  author: acd
  author_url: http://acdbddh.openid.pl/
  date: '2007-08-19 22:21:21 +0200'
  date_gmt: '2007-08-19 21:21:21 +0200'
  content: "Czy może mi ktoś powiedzieć co trzyma ludzi (developerów, managerów) przy
    PHP'ie, gdy dostępne sa platformy takie jak .Net albo RoR ?\r\n\r\nCos w tym na
    pewno jest. Giganci tacy jak allegro nie mogli sie mylić."
- id: 8405
  author: mcv
  author_url: http://mcv.jogger.pl/
  date: '2007-08-20 09:22:59 +0200'
  date_gmt: '2007-08-20 08:22:59 +0200'
  content: "acd: Np. dostępność hostingu, z czego pokrętnymi drogami wynika liczba
    dostępnych programistów, z czego niekoniecznie pokrętnymi drogami wynika koszt
    zatrudnienia takiego programisty.\r\n\r\nA giganci zawsze się mogą mylić.\r\n\r\nPS:
    .NET ze swoim Yellow-screen-of-death to chyba też do szczęśliwych nie należy?
    ;-)"
---
<p>Podobno <abbr title="PHP Hypertext Preprocessor">PHP</abbr>5 jest językiem obiektowym, niektórzy twierdzą nawet, że językiem czwartej generacji. Ja bym go nazwał językiem <q>obiektowalnym,</q> bo zaiste, można w nim programować obiektowo, jednak sam język ani do tego nie zachęca, ani procesu nie ułatwia. Znakomita większość funkcji bibliotecznych obiektowości zwyczajnie nie obsługuje. Ciekawsze jednak są wyjątki, które w <abbr>PHP</abbr> są… niemal bezużyteczne.</p>

<p>Autorzy języka uznali, że najważniejsza jest zgodność wstecz za wszelką cenę. Zamiast jednak przygotować moduł, który dostarczałby <abbr title="Application Programming Interface">API</abbr> zgodnego ze starszymi wydaniami i zmodernizować rdzeń funkcjonalności bibliotecznej, postanowili ciągnąć za sobą brzemię średniowiecznych początków języka. Złośliwi mówią, że wystarczy zamienić część znaków dolara na małpki i otrzymamy poprawny kod Perla, a usuwając dolary w liniach deklaracji otrzymamy zgodność ze skryptami powłoki. Trudno się dziwić, bo <q>szerokie możliwości</q> języka to głównie posklejane kawałki bibliotek standardowych Perla i C, pomieszane z możliwościami powłoki. Faktycznie, jeśliby dodać do siebie procentowy udział języków pomnożony przez ich generację, to <abbr>PHP</abbr> okazuje się stać na czele i już tylko krok dzieli go od interpretacji języka naturalnego.</p>

<p>Nie o tym jednak chciałem pisać. Jedną z konsekwencji zachowania zgodności jest wyjątkowość języka, przejawiające się w braku wbudowanych wyjątków. Nie mam tu na myśli klasy <code>Exception</code>, mówię o tym, że żadna z funkcji bibliotecznych wyjątkami nie rzuca. Zwracają magiczne wartości, ustawiają liczniki błędów, ale wyjątków unikają jak ognia. Dlaczego? Może dlatego, że przeciętny konsument <abbr>API</abbr> o obiektowości, wyjątkach i wzorcach projektowych ma takie samo pojęcia, jak ja o ornitologii. Dlatego właśnie uważam, że wyjątki w <abbr>PHP</abbr> są niemal bezużyteczne.</p>

<blockquote><pre><code>$f = foo();
if (foo_error())
	return false;
if (!foo_write($f, 'bar'))
	return false;
if (!foo_write($f, 'baz'))
	return false;
foo_flush($f);
if (foo_error())
	return false;
foo_close($f);
if (foo_error())
	return false;
</code></pre></blockquote>

<p>Czy tak powinien wyglądać kod? A może tak:</p>

<blockquote><pre><code>$result = true;
try
{
	$f = foo();
	$f-&gt;write('bar');
	$f-&gt;write('baz');
	$f-&gt;flush();
}
catch (FooException $e)
{
	$result = false;
}
finally
{
	if ($f)
		$f-&gt;close();
}
return $result;</code></pre></blockquote>

<p>Żeby móc osiągnąć czytelność drugiej wersji kodu, programista musi poświęcić kilka godzin na napisanie wrapperów dla większości bibliotecznych wywołań. W przeciwnym wypadku używanie wyjątków jest bezcelowe, bo i tak na każdym kroku trzeba kontrolować zwracane wartości. Czy jest tu zaszyta jakaś głębsza logika, czy słusznie wydaje mi się, że <abbr>PHP</abbr>5 wygląda na zaprojektowany na kolanie?</p>
