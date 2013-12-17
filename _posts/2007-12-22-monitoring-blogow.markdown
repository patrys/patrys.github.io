---
layout: post
status: publish
published: true
title: Monitoring blogów
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 421
wordpress_url: http://room-303.com/blog/2007/12/22/monitoring-blogow/
date: 2007-12-22 16:47:08.000000000 +01:00
categories:
- web
tags: []
comments:
- id: 12282
  author: opi
  author_url: http://bronikowski.com
  date: '2007-12-22 16:52:01 +0100'
  date_gmt: '2007-12-22 15:52:01 +0100'
  content: Ciekawe, możesz podać jakieś zakresy IP, z których pingają?
- id: 12283
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-12-22 16:56:18 +0100'
  date_gmt: '2007-12-22 15:56:18 +0100'
  content: "A pewnie, że mogę:\r\n\r\n<code>213.17.224.130</code> - <code>213.17.224.159</code>"
- id: 12284
  author: chlitto
  author_url: http://www.chlitto.pl
  date: '2007-12-22 17:05:37 +0100'
  date_gmt: '2007-12-22 16:05:37 +0100'
  content: '"Od dłuższego czasu"?'
- id: 12285
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-12-22 17:19:00 +0100'
  date_gmt: '2007-12-22 16:19:00 +0100'
  content: "chlitto:\r\n\r\nDotąd denerwowało mnie tylko to, że automat zamiast korzystać
    z RSS zaciągał całe strony. Tyle, że w zeszłym miesiącu nie zjadali mi tyle pasma,
    ile 10przykazan potrzebuje na monitorowanie 100 blogów."
- id: 12287
  author: Zamber
  author_url: http://zamber.jogger.pl/
  date: '2007-12-22 17:52:01 +0100'
  date_gmt: '2007-12-22 16:52:01 +0100'
  content: "\"PRESS-SERVICE wykorzystuje najnowsze rozwiązania informatyczne oraz
    wieloletnie doświadczenie wysokiej klasy profesjonalistów. Oferuje swoim Klientom
    najwyższą jakość usług i gwarantuje produkty o europejskim standardzie. Doświadczenie
    i umiejętności monitoringu PRESS-SERVICE doceniają zarówno duże korporacje, jak
    i małe czy średnie firmy z różnych branż, a także ministerstwa, instytucje rządowe
    np. Senat RP, NIK, PARP.\"\r\n\r\nUwielbiam te reklamowe papki :D."
- id: 12288
  author: Piotr Konieczny
  author_url: http://blog.konieczny.be
  date: '2007-12-22 19:02:09 +0100'
  date_gmt: '2007-12-22 18:02:09 +0100'
  content: "U mnie to samo, ledwie połowa miesiąca mija, a inforia już ma 1GB pożartego
    transferu na liczniku...\r\n\r\nMoże zaczniemy ich wpólnie redirectować na jakieś
    XXX?"
- id: 12289
  author: Robert Drózd
  author_url: http://www.webaudit.pl/blog/
  date: '2007-12-22 19:10:38 +0100'
  date_gmt: '2007-12-22 18:10:38 +0100'
  content: "Pisałem o tym parę tygodni temu:\r\nhttp://www.webaudit.pl/blog/2007/monitoring-mediow-press-service-amatorka-na-granicy-ataku-dos/\r\n\r\ndeny
    from inforia.net pomogło."
- id: 12290
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-12-22 19:21:32 +0100'
  date_gmt: '2007-12-22 18:21:32 +0100'
  content: Tak się zastanawiam, jak ma się przetwarzanie blogów przez zamknięte serwisy
    do warunków licencji? Ja udostępniam treść jako BY-NC-SA, więc tworzenie utworów
    zależnych w celach komercyjnych (rozumiem, że inforia - w przeciwieństwie do Google
    - sprzedaje wyniki swojego wyszukiwania) można chyba traktować jako złamanie prawa
    autorskiego?
- id: 12291
  author: Pooh
  author_url: ''
  date: '2007-12-22 19:32:36 +0100'
  date_gmt: '2007-12-22 18:32:36 +0100'
  content: "...i jeszcze dziury XSS u siebie mają:\r\nhttp://press-service.com.pl/new.php?id=1.3&amp;l=%22%3E%3Cbody%20onload=alert(document.cookie)%3E\r\n:-)"
- id: 12292
  author: Tomasz Topa
  author_url: http://tomasz.topa.pl
  date: '2007-12-22 19:52:04 +0100'
  date_gmt: '2007-12-22 18:52:04 +0100'
  content: U mnie też prawie 10% wyciągają. Chyba zrobię jakiegoś redirecta na ich
    własne serwery...
- id: 12293
  author: RAFi
  author_url: http://ja.rafi.pl
  date: '2007-12-22 19:55:44 +0100'
  date_gmt: '2007-12-22 18:55:44 +0100'
  content: A ja ich wyciąłem bez płaczów w mejlach.
- id: 12294
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-12-22 20:06:49 +0100'
  date_gmt: '2007-12-22 19:06:49 +0100'
  content: "RAFi:\r\n\r\nPewnie, w mordę też można dać - prościej niż napisać.\r\n\r\nPiko,
    Tomasz Topa:\r\n\r\nPóki co, u mnie działa:\r\n\r\n<blockquote><pre><code>RewriteCond
    %{REMOTE_ADDR} ^213\\.17\\.224\\.140^\r\nRewriteRule .* http://press-service.com.pl/monitoring_blogow
    [R=301,L]</code></pre></blockquote>"
- id: 12295
  author: Altair
  author_url: ''
  date: '2007-12-22 20:22:07 +0100'
  date_gmt: '2007-12-22 19:22:07 +0100'
  content: Wiesz, ja rozumiem że oni mają ten system skopany, rozumiem także Twoją
    irytację, ale czy nie mogłeś najpierw napisać do nich maila bez straszenia ich
    sądem i obrażania w pierwszych zdaniach?
- id: 12296
  author: rzepak
  author_url: ''
  date: '2007-12-22 21:50:11 +0100'
  date_gmt: '2007-12-22 20:50:11 +0100'
  content: rozumiem złość ale z tym zakładem pracy chronionej trochę "niefajnie" użyte
- id: 12297
  author: Marcin Badurowicz
  author_url: http://www.ktos.info/notatki/
  date: '2007-12-22 22:38:46 +0100'
  date_gmt: '2007-12-22 21:38:46 +0100'
  content: "Ja patrzę u siebie - no i fakt, 38.52% kilobajtów w tym miesiącu to na
    213.17.224.140 idzie. Prawie 0,5 GB znaczy. A się zastanawiałem czy taki popularny
    ten blog mam, że tyle transferu żre...\r\n\r\nChyba i ja nad deny from się zastanowię..."
- id: 12298
  author: yZZuF
  author_url: ''
  date: '2007-12-22 22:52:19 +0100'
  date_gmt: '2007-12-22 21:52:19 +0100'
  content: Ja rozumiem, że można się wkurwić itp. ale wycieczki w stylu przyrównywania
    innych do osób specjalnej troski jest trochę niesmaczne, żeby nie napisać inaczej
    i bardziej dosadnie.
- id: 12299
  author: Patrys
  author_url: http://room-303.com/
  date: '2007-12-22 23:08:38 +0100'
  date_gmt: '2007-12-22 22:08:38 +0100'
  content: "rzepak, yZZuF:\r\n\r\nZgadzam się, że mnie poniosło, ale nie mam już siły
    do tych ludzi. Oczywiście rozumiem, że ludzie upośledzeni są tu niewinni i porównanie
    ich do pracowników Inforii jest obraźliwe. Mea culpa."
- id: 12300
  author: Fuzzy
  author_url: ''
  date: '2007-12-22 23:19:57 +0100'
  date_gmt: '2007-12-22 22:19:57 +0100'
  content: "Napisali na http://press-service.com.pl/monitoring_blogow że monitorują
    także komentarze. Pewnie też dlatego chodzą po stronach zamiast korzystać tylko
    z rss'ów. A komentarze pojawiają się zwykle często i w niokreślonych ilościach
    stąd masa odwiedzin. Mogliby się wprawdzie ograniczyć np. do 1 dziennie, ale nie
    widzę lepszego sposobu żeby realizować to co twierdzą, że robią. (Zmiany user-agent
    są rzeczywiście nieuzasadnione.)\r\nCo do problemów licencyjnych, to nie wiem,
    czy opublikowanie streszczenia czy recenzji książki w jakiejś gazecie wymaga specjalnego
    opłacania autora/wydawcy/kogokolwiek? Chyba nie, a to co robią to chyba dokładnie
    to samo."
- id: 12301
  author: Piotr Konieczny
  author_url: http://blog.konieczny.be
  date: '2007-12-23 01:21:53 +0100'
  date_gmt: '2007-12-23 00:21:53 +0100'
  content: Dowiedzmy sie po prostuy kto to od nich kupuje, i zacznijmy bojkotowac/flame'owac/BlackPR-owac/palic
    na stosie ;-)
- id: 12304
  author: opi
  author_url: http://bronikowski.com
  date: '2007-12-23 08:24:21 +0100'
  date_gmt: '2007-12-23 07:24:21 +0100'
  content: No, miałeś racje -- po mnie też jadą. I nie po RSS, a po prostu ssanie
    całych stron. Dzięki za hint. Idę ich wykopać.
- id: 12305
  author: opi
  author_url: http://bronikowski.com
  date: '2007-12-23 08:25:37 +0100'
  date_gmt: '2007-12-23 07:25:37 +0100'
  content: '@Fuzzy: u mnie można się zapisać na wątek via RSS, to nie jest usprawiedliwienie
    takiego nadużywania moich łączy.'
- id: 12306
  author: Marcin
  author_url: http://www.pilsniak.pl
  date: '2007-12-23 09:51:31 +0100'
  date_gmt: '2007-12-23 08:51:31 +0100'
  content: "&gt; Cieszcie się, że 10przykazan nie pisali ludzie z Press Service:\r\nDlaczego,
    10p może by się wtedy rozwijało."
- id: 12573
  author: Adam Ścibior PRESS-SERVICE Monitoring Mediów
  author_url: http://www.press-service.com.pl
  date: '2007-12-27 13:16:54 +0100'
  date_gmt: '2007-12-27 12:16:54 +0100'
  content: "Witam,\r\n\r\nw imieniu firmy PRESS-SERVICE chciałbym się ustosunkować
    do powyższej dyskusji. Na wstępie należą się słowa przeprosin wszystkim (właścicielowi
    tego bloga jak i komentującym), którzy odczuli niewłaściwe działanie naszego sytemu
    monitorującego internet. Był on projektowany z myślą o dużych portalach i faktycznie
    w przypadku blogów czy niewielkich serwisów może być dokuczliwy dla ich właścicieli.
    \r\n\r\nWczytujemy się we wszystkie opinie, komentarze, a także sugestie (monitoring
    RSS) i zapewniam, że podejmujemy takie działania, aby zniwelować do minimum uciążliwe
    skutki prowadzonego monitoringu. Tymczasowe zmiany powinny być dla Państwa zauważalne
    już w tej chwili, a wkrótce problem będzie całkowicie rozwiązany.\r\n\r\nObecnie
    w Polsce rola blogów jest jeszcze bagatelizowana. Jako firma robimy bardzo dużo,
    aby popularyzować te źródła informacji. Już udało nam się przekonać kilku naszych
    klientów do konieczności śledzenia blogosfery i poważnego traktowania tego medium.
    Uważamy, że dla tych klientów informacje zamieszczane na blogach są istotne. Nie
    ukrywamy, że mamy satysfakcję z tego, że informując ich o treściach zawartych
    na najbardziej opiniotwórczych blogach w polskiej sieci, m.in. takich jak ten,
    możemy nie tylko przekazywać im cenne biznesowo informacje, ale także promować
    blogi jako wiarygodne i cenne medium. Oczywiście dołożymy wszelkich starań, żeby
    odbywało się to bez szkody dla twórców blogosfery.\r\n\r\nOdnosząc się do losowego
    wyświetlania przeglądarki to nie jest to działanie celowe, a raczej kwestia przeoczenia.
    Możliwie najszybciej \"podpiszemy\" odpowiednio aktywność robota - nie mamy na
    celu ukrywania się z monitoringiem, bo jest to działalność tak naprawdę korzystna
    dla wszystkich stron.\r\n\r\nPrzepraszając raz jeszcze za niedogodności, proszę
    o przychylniejsze spojrzenie na naszą działalność promującą internet, blogi i
    treści tworzone przez użytkowników wśród PR-owców i marketingowców.\r\n\r\n\r\n\r\nZ
    poważaniem\r\n\r\n\r\nAdam Ścibior\r\n\r\nPRESS-SERVICE Monitoring Mediów"
- id: 12726
  author: Wajrus
  author_url: http://cze
  date: '2007-12-29 03:20:20 +0100'
  date_gmt: '2007-12-29 02:20:20 +0100'
  content: lol kofrzysta z google i narzeka ze zle dziala , to napisz nowsze madralo
    :P
- id: 14365
  author: Paweł Tkaczyk
  author_url: http://paweltkaczyk.midea.pl
  date: '2008-01-29 13:36:52 +0100'
  date_gmt: '2008-01-29 12:36:52 +0100'
  content: A właśnie się zastanawiałem, dlaczego nagle dostaję komunikaty o przekroczeniu
    transferu...
- id: 16902
  author: WebAudit Blog &raquo; Monitoring Press Service już nie &#8220;atakuje&#8221;
  author_url: http://www.webaudit.pl/blog/2008/monitoring-press-service-juz-nie-atakuje/
  date: '2008-02-05 16:17:36 +0100'
  date_gmt: '2008-02-05 15:17:36 +0100'
  content: '[...] tygodni po artykule moim oraz Patrysa (który wkurzył się na tyle,
    że wystosował do firmy dosyć ostrego maila) napisał do mnie [...]'
---
<p>Cieszcie się, że <a href="http://10przykazan.com/">10przykazan</a> nie pisali ludzie z <a rel="nofollow" href="http://press-service.com.pl/">Press Service</a>:</p>

<blockquote><p>Witam,</p>

<p>Jestem administratorem i autorem serwisu room-303.com.</p>

<p>Od dłuższego czasu toleruję niekompetencję Państwa pracowników, ale w tym tygodniu przekroczyła ona wszelkie dopuszczalne granice. Nie interesuje mnie, czy jesteście Państwo zakładem pracy chronionej i zatrudniacie ludzi specjalnej troski, ale nie pozwolę, żeby ich nieznajomość technologii narażała mnie na koszty.</p>

<p>W skrócie, Państwa monitoring blogów (inforia.net) sprowadza się do ataków na monitorowane serwisy. Inaczej nie umiem wyjaśnić, dlaczego usługi Google są w stanie śledzić treść mojego bloga pozostawiając swój udział w odwiedzinach na granicy błędu statystycznego, natomiast Państwa nieudolny serwis nie dość, że generuje 5% odwiedzin, to jeszcze plasuje się na pierwszym miejscu pod względem pochłanianego transferu. Na pierwsze miejsce z pewnością zasługuje, gdyż 10% całego wychodzącego ruchu to część niemała. Dla porównania dodam, że drugie miejsce nie zbliżyło się jeszcze do 2%. Do tego - za każdym razem - Państwa roboty przedstawiają się jako losowa wersja przeglądarki, co traktuję jako celowe zacieranie statystyk.</p>

<p>Niniejszym domagam się naprawienia Państwa serwisu, w przeciwnym wypadku będę musiał potraktować Państwa usługi jak próbę ataku na infrastrukturę teleinformatyczną, która posiada znamiona przestępstwa (zakłócanie pracy systemów teleinformatycznych w celu uzyskania korzyści majątkowych). Dodatkowo narażacie mnie Państwo na koszty, gdyż serwis mój znajduje się na komercyjnym hostingu i tak przestrzeń dyskowa, w znakomitej większości zajmowana przez logi generowane przez Państwa, jak i pochłaniany przez Wasze roboty transfer finansowane są z mojej prywatnej kieszeni. Uprzedzam jednocześnie, że jeśli Państwa roboty nie przestaną przedstawiać się jako internauci, cała Państwa klasa adresowa zostanie zablokowana.</p>

<p>Bez poważania,</p>

<p>-- <br />Patryk Zawadzki<br />PLD Linux Distribution</p></blockquote>
