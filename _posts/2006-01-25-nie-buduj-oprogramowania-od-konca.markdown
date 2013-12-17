---
layout: post
status: publish
published: true
title: Nie buduj oprogramowania od końca
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 218
wordpress_url: http://www.room-303.com/blog/2006/01/25/nie-buduj-oprogramowania-od-konca/
date: 2006-01-25 19:43:04.000000000 +01:00
categories:
- web
- usability
- software
tags: []
comments:
- id: 3139
  author: Cthulhu
  author_url: ''
  date: '2006-01-25 20:02:31 +0100'
  date_gmt: '2006-01-25 19:02:31 +0100'
  content: Zgadywanie w jakim formacie wpisać jakieś dane to moja ulubiona zabawa
    ale z tymi numerami to już przegięcie. Ja zawsze jak wpiszę numer karty/konta
    to sprawdzam czy jest poprawny - dostałbym cholery jakby to wszystko zlało się
    w jednego inta..
- id: 3142
  author: mcv
  author_url: http://mcv.jogger.pl/
  date: '2006-01-25 22:47:35 +0100'
  date_gmt: '2006-01-25 21:47:35 +0100'
  content: Może nie znają podziału na warstwy prezentacji, logiki i źródła informacji?
- id: 3161
  author: Tomash
  author_url: ''
  date: '2006-01-27 17:25:44 +0100'
  date_gmt: '2006-01-27 16:25:44 +0100'
  content: Aplikacji nie buduje się od interfejsu - ten zazwyczaj zostawia się na
    koniec. Aplikację buduje się od zaprojektowania, najpierw warstwy logicznej, a
    potem interfejsu przyciętego do tej warstwy logicznej. Że ktoś jest palant i ominął
    etap projektowania albo zrzuca większość pracy na użytkownika - no jasne, do kanału
    z nim. Ale proszę bez odważnych, wywrotowych tekstów w stylu "zaczynaj aplikację
    od interfejsu", bo wtedy dopiero zacznie się tragedia ;)
- id: 3162
  author: Patrys
  author_url: http://room-303.com/
  date: '2006-01-27 17:36:37 +0100'
  date_gmt: '2006-01-27 16:36:37 +0100'
  content: "Interfejst to nie tylko przyciski i inputy, to cały schemat interakcji
    z użytkownikiem.\r\n\r\nPowtórzę przykład z kalkulatorem:\r\n\r\nProgramując kalkulator
    nie zaczynasz od implementacji wydajnego algorytmu ONP, a potem nie mówisz użytkownikowi,
    że znak się wciska po parametrach. Najpierw projektujesz schemat interakcji (co
    użytkownik może zrobić, w jakich okolicznościach, w jakim formacie), a dopiero
    potem dostosowujesz do tego warstwę logiki.\r\n\r\nLogika to warstwa, która ma
    za zadanie tylko połączyć model z widokiem, do jej prawidłowego stworzenia potrzebne
    są makiety tych ostatnich."
- id: 3184
  author: lu
  author_url: ''
  date: '2006-01-30 23:58:28 +0100'
  date_gmt: '2006-01-30 22:58:28 +0100'
  content: "\"Aplikacji nie buduje się od interfejsu - ten zazwyczaj zostawia się
    na koniec.\" - zalezy w jaki sposob tworzona jest aplikacja, jesli masz dobrze
    \"uchwycone\" wymagania interfejs moze powstawac rownolegle. \r\n\r\n\"Że ktoś
    jest palant i ominął etap projektowania albo zrzuca większość pracy na użytkownika
    - no jasne, do kanału z nim.\" - a to jest juz mala przesada z tym palantem.  Pokaz
    swoje I komercyjne projekty kolego, od razu byles geniuszem??? Moze poprostu klient
    nie szanuje uzytkownika, i nie zalezy mu na jego wygodzie, moze mu spieszylo sie
    z oddaniem systemu?"
---
<p>Programiści są leniwi, klienci też — nie chce im się skarżyć na interfejs. Zaczynaj budowanie aplikacji od interfejsu, a nie od warstwy funkcjonalnej. I rób to z głową.</p>

<p>Przykładem jest system płatności online <a href="http://www.protx.com/">Protx</a>, który podłączamy właśnie do serwisu jednego z klientów. Po przejściu do formularza dokonywania płatności, naszym oczom ukazuje się okienko z napisem <q>credit card number, enter without the spaces.</q> Jeśli projektant tego systemu wiedział doskonale, że wszystkie numery kart kredytowych posiadają separatory w postaci spacji lub myślników, to czemu kazać je usuwać użytkownikowi, zamiast wyczyścić je po stronie serwisu?</p>

<p>To wzorcowy przypadek zwalania pracy na użytkownika w sytuacji, w której komputer poradziłby sobie znacznie lepiej. Wpisywanie numeru karty bez separatorów powoduje też, że łatwiej o błąd — cyfry nie są pogrupowane i łatwo przeoczyć pomyłkę.</p>

<p>Jeśli masz zamiar oczekiwać od użytkownika wprowadzenia jakichś danych, to zrób co w twojej mocy, żeby przyjąć możliwie dużo popularnych formatów. Powyższy przykład jest o tyle idiotyczny, że na samej karcie numer zawiera spacje, a system wymaga wpisania go w zupełnie nietypowym formacie.</p>

Technorati Tags: <a href="http://technorati.com/tag/application" rel="tag">application</a>, <a href="http://technorati.com/tag/interface" rel="tag">interface</a>, <a href="http://technorati.com/tag/design" rel="tag">design</a>, <a href="http://technorati.com/tag/input" rel="tag">input</a>, <a href="http://technorati.com/tag/validation" rel="tag">validation</a>, <a href="http://technorati.com/tag/usability" rel="tag">usability</a>
