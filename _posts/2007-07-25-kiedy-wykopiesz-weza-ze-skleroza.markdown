---
layout: post
status: publish
published: true
title: Kiedy wykopiesz węża ze sklerozą...
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 392
wordpress_url: http://room-303.com/blog/2007/07/25/kiedy-wykopiesz-weza-ze-skleroza/
date: 2007-07-25 02:43:28.000000000 +02:00
categories:
- code
tags: []
comments:
- id: 8268
  author: Nivertius
  author_url: http://nivertius.uaznia.net/
  date: '2007-07-25 07:31:36 +0200'
  date_gmt: '2007-07-25 06:31:36 +0200'
  content: "Trzeci akapit, drugie zdanie - nie chodziło czasem o 'stertę' [heap]?
    Bo wydaje mi się, że 'automatyczne' usuwanie obiektów ze stosu to ma 'nawet' C.\r\nPrzykład
    z przejrzystością kodu jest średni, powiem szczerze, że nie wiem co on robi, domyślam
    się, że łączy elementy podanej tablicy znakiem spacji w jeden string. I naprawdę,
    żeby to zrobić wykonuje się metode znaku [ew. stringu]? Cóż, jak dla mnie to powinna
    być metoda tablicy stringów, ze znakiem jako parametrem...\r\nGC - fajna zabawka,
    ale myślę, że dobre programy z niej w ogóle nie korzystają. To nie jest wielki
    wysiłek stworzyć aplikacje tak, żeby wiedzieć gdzie tworzone dynamicznie obiekty
    kończą swoją przydatność i mogą być usunięte..."
- id: 8270
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-07-25 07:52:07 +0200'
  date_gmt: '2007-07-25 06:52:07 +0200'
  content: "Nivertius:\r\n\r\nTam wcale nie powinno być stosu, tylko pamięć, ale pisałem
    to w środku nocy.\r\n\r\nPrzykład z przejrzystością - ten kawałek kodu jest bzdurny,
    ale spróbuj napisać to samo w C (z dynamicznym złączeniem wektora asciiz).\r\n\r\nCo
    to znaczy, że dobre programy nie korzystają z cechy języka?\r\n\r\nPS: Jakbyś
    nie zauważył, to powyższy tekst jest narzekaniem na inny tekst."
- id: 8272
  author: Cause
  author_url: ''
  date: '2007-07-25 09:26:45 +0200'
  date_gmt: '2007-07-25 08:26:45 +0200'
  content: Dlaczego trafił na Wykop? Idiotyczne pytanie. Bo mógł :)
- id: 8273
  author: Nivertius
  author_url: http://nivertius.uaznia.net/
  date: '2007-07-25 09:50:28 +0200'
  date_gmt: '2007-07-25 08:50:28 +0200'
  content: "Patrys:\r\n\r\nNapisać to samo w C - zawsze możesz sobie to opakować w
    funkcje ładną, albo ściągnąć pakiet odpowiedni, albo nie być masochistą i nie
    korzystać z C ;-&gt;\r\nTak czy owak join(char**, int, char) do mnie bardziej
    przemawia niż ta metoda.\r\n\r\nPoprawka do 'dobrych programów': Mój błąd, myślałem,
    że w Javie/Pythonie GC nie zajmuje się usuwaniem obiektów explicite, ani po wyjściu
    ze scope, wydawało mi się, że działa w trybie 'search &amp; destroy' na obiektach
    bez referencji. Tak więc korekta: Dobre programy nie posiadają deallokacji implicite
    nigdzie poza wyjściami ze scope [i chyba powiedziałem gdzieś jeszcze, ale już
    nie pamiętam].\r\n\r\nPS. Spoko, widzę. Ja tak dla poprawności ;-)"
- id: 8279
  author: qx
  author_url: http://pieknedni.blogspot.com/
  date: '2007-07-25 21:02:44 +0200'
  date_gmt: '2007-07-25 20:02:44 +0200'
  content: Wykop ostatnimi czasy jest coraz bardziej podobny do pudelka.
---
<p>Zupełnie nie rozumiem, czemu <a href="http://www.wykop.pl/link/22481/odsmiecanie-pamieci-w-pythonie">na Wykop</a> trafił <a href="http://www.pydev.pl/?p=29">artykuł o odśmiecaniu pamięci w Pythonie</a>, wiem za to, że jest to świetna okazja, żeby się nad nim nieco popastwić. Zacznijmy od tego, że Python nie kończy się niemą samogłoską i nie odmieniamy go z apostrofem.</p>

<p>W przydługim wstępie do jeszcze dłuższego tekstu czytamy, że Python jest językiem. Świetnie. Zastanawiam się w tym momencie, jaki jest <q>target audience</q> owego dzieła, zanosi się bowiem na wykład dla początkujących. Po przecinku atakuje nas jednak automatyczna alokacja pamięci (i co to właściwie znaczy <q>automatyczna</q> — alokacja następuje wtedy, kiedy programista tworzy nowy obiekt).</p>

<p>Atakuje bez uprzedzenia, wypadałoby chociaż wspomnieć, że w językach niższego poziomu istnieją specjalne operatory i wymagane jest jawne zarządzanie zasobami. W Pythonie (w Javie, PHP…) nie jest wymagane jawne usuwanie obiektów, to prawda. Nie zgodzę się jednak z podsumowaniem, że główną zaletą tego rozwiązania jest fakt, że programiści <q>nie muszą się martwić o zabezpieczenie pamięci.</q></p>

<p>Główną zaletą posiadania dużego trawnika nie jest możliwość rzadszego sprzątania po swoim psie, tak zbieranie psich bobków, jak pilnowanie zakresów buforów jest świętym obowiązkiem programisty i żaden język go w tym nie wyręczy. Autor tego akapitu chyba nigdy nie próbował napisać w C odpowiednika <code>alaMaKota = ' '.join(('Ala', 'ma', 'kota'))</code>, gdyby spróbował, to wiedziałby, co jest główną zaletą. <em>Przejrzystość kodu</em>.</p>

<p>Podsumowując wstęp, Python nie jest <q>wymarzonym narzędziem dla programisty.</q> Python jest jednym z języków i — jak każdy z języków (nie zaczynających się słowem <q>visual</q>) — nadaje się do jednych rzeczy, a nie nadaje do innych. Nie wiem też, jakie powinienem mieć oczekiwania względem procesu śmieciarza, ale praktyka każe mi usuwać duże zbędne obiekty niezależnie od używanego języka.</p>

<p>Dalej mamy całą masę oderwanej od przykładów teorii. Wystarczyłoby powiedzieć, że z odśmiecaniem pamięci wiążą się trzy potencjalne problemy:</p>

<ul>
<li>fragmentacja pamięci, która powoduje, że tworzenie dużych ciągłych struktur staje się bardzo kosztowne,</li>
<li>wykrywanie wysp, czyli obiektów odwołujących się do siebie nawzajem, ale oderwanych od aktualnego stanu programu,</li>
<li>przechowywanie obiektów, które często zmieniają swój rozmiar, na przykład typów numerycznych o nieskończonej precyzji.</li>
</ul>

<p>Resztę można sprowadzić do stwierdzenia (którego w artykule brak, co oznacza, że ze swoim tytułem nie ma nic wspólnego), że CPython radzi sobie z wszystkimi trzema wymienionymi powyżej. Ni więcej, ni mniej. Żadnej alokacji, dzielenia stosu ani tablic uchwytów przywoływać tu nie trzeba, bo — za przeproszeniem — robi się burdel, a nic z tego nie wynika.</p>

<p>Podsumowując, możesz w Pythonie programować tak samo jak w Javie albo Rubym i wcale nie musisz z głowy recytować algorytmu śmieciarza. Genialne, tylko o czym był ten artykuł i po co trafił na Wykop?</p>
