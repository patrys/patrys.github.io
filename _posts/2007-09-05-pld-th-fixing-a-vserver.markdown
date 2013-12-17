---
layout: post
status: publish
published: true
title: 'PLD Th: fixing a vserver'
author: Patrys
author_login: admin
author_email: patrys@pld-linux.org
author_url: http://room-303.com/blog/
wordpress_id: 405
wordpress_url: http://room-303.com/blog/2007/09/05/pld-th-fixing-a-vserver/
date: 2007-09-05 15:34:39.000000000 +02:00
categories:
- linux
- software
tags: []
comments:
- id: 8451
  author: mklimek
  author_url: http://mklimek.org
  date: '2007-09-05 18:59:01 +0200'
  date_gmt: '2007-09-05 17:59:01 +0200'
  content: "Eh.. PLD, takie rzeczy na produkcji..\r\n\r\n;-)"
- id: 8452
  author: Andrzej Dopierała
  author_url: http://andrzej.dopierala.name/
  date: '2007-09-05 20:24:30 +0200'
  date_gmt: '2007-09-05 19:24:30 +0200'
  content: "ech, th, takie rzeczy na produkcji.. ;)\r\nto tak jak debian unstable...
    a potem się dziwić że ludzie mają pld za niestabilne ;p"
- id: 8453
  author: Wojtosz
  author_url: http://www.blaszkowski.com
  date: '2007-09-05 23:10:59 +0200'
  date_gmt: '2007-09-05 22:10:59 +0200'
  content: "Nie miałem czasu by przetestować Twój pomysł, ale rozwiązanie wygląda
    na poprawne :)\r\nSwego czasu konsultowałem ten problem z RM Th, na forum PLD
    próbował pomagać Light-I. \r\nDotychczas jednym z rozwiązań jakim się ratowałem
    było postawienie vservera PLD-Ac na Ac i zmigrowanie go na Th - niefajne, ale
    działało."
---
<p>Niniejszy post jest oparty o historię z pola bitwy. Bardzo techniczny i nieszczególnie ciekawy, jeśli ktoś nie używa wymienionych technologii. Być może komuś się przyda.</p>

<h4>Awaria</h4>

<p>Poszukiwanie przyczyn pozwoliło nam ustalić następujące fakty:</p>

<ul>
<li>W jednej z maszyn wirtualnych ktoś zainstalował pakiety <code>rpm</code> i <code>poldek</code>, a następnie użył ich do instalacji oprogramowania;</li>
<li>Maszyna miała cały czas zamontowaną zewnętrzną bazę <code>rpm</code> (prawdopodobnie <code>utils-vserver</code> zdechło i pozostawiło po sobie bałagan, ale o tym później);</li>
<li>Wewnętrzny <code>rpm</code> miał inną wersję i w jakiś sposób uszkodził bazę zainstalowanych pakietów;</li>
<li>Następujący po nim <code>rpm --rebuilddb</code> bezpowrotnie wyczyścił bazę pakietów maszyny;</li>
<li>W międzyczasie miał miejsce upgrade pakietów <code>rpm</code> i <code>poldek</code> w zewnętrznym systemie;</li>
</ul>

<p>Postanowiliśmy zatem przeinstalować maszynę od nowa, rekonstruując na podstawie działających usług listę niezbędnych pakietów.</p>

<h4>Nosem w dół</h4>

<p>Dość szybko okazało się, że nie będzie tak łatwo:</p>

<blockquote><pre><code>ncontext: vc_net_create(): Invalid argument</code></pre></blockquote>

<p>Tak właśnie kończyło się każde wywołanie narzędzi <code>vrpm</code> i <code>vpoldek</code>. Winnym okazało się wywołanie <code>chbind</code>, a poprawka wygląda tak:</p>

<blockquote><pre><code>--- /usr/lib/util-vserver/functions~    2007-09-05 16:09:16.967334575 +0200
+++ /usr/lib/util-vserver/functions     2007-09-05 16:10:29.456275993 +0200
@@ -1171,5 +1171,5 @@
     export RPM_FAKE_CHROOT RPM_FAKE_CTX RPM_FAKE_CAP RPM_FAKE_FLAGS
     
     LD_PRELOAD=$_RPM_FAKE_SO${LD_PRELOAD:+:$LD_PRELOAD} \
-       exec $_CHBIND "${CHBIND_OPTS[@]}" "$@"
+       exec $_CHBIND --nid $RPM_FAKE_CTX "${CHBIND_OPTS[@]}" "$@"
 }</code></pre></blockquote>

<p>Dość szybko okazało się, że radość jest przedwczesna. O ile <code>vrpm</code> i <code>vpoldek</code> zaczęły działać, to żadne z nich nie potrafiło nic zmienić. Odpytywanie bazy nie przysparzało żadnych trudności, próba instalacji lub usunięcia pakietu kończyły się kolejnym radosnym komunikatem:</p>

<blockquote><pre><code>error: cannot open Basenames index using db3 - No such file or directory (2)</code></pre></blockquote>

<h4>Winny</h4>

<p>Okazało się, że winny jest <code>rpm-4.4.9</code> w połączeniu z <code>db4.6</code>. Nie miałem okazji sprawdzić, co dokładnie powoduje nieprawidłowe działanie, dość było upewnić się, że działa wersja <code>rpm-4.4.9-1</code>, zbudowana z pakietem <code>db4.5-devel</code>.</p>

<p>Problemem jest fakt, że <code>db4.6</code> automatycznie konwertuje każdą otwartą bazę do swojego formatu, co oznacza, że po wykonaniu downgrade pakietu <code>rpm</code> zostaniemy z bezużytecznym narzędziem.</p>

<h4>Rozwiązanie</h4>

<p>Jeff, autor <code>rpm</code> pomógł mi cofnąć upgrade:</p>

<ol>
<li>Instalujemy pakiet <code>db4.6-utils</code>, kopiujemy z niego program <code>db_dump</code>;</li>
<li>Odinstalowujemy <code>db4.6-utils</code>, zachowując sam <code>db4.6</code>;</li>
<li>Instalujemy pakiet <code>db4.5-utils</code>;</li>
<li>Cofamy wersję <code>rpm</code> i instalujemy pakiet <code>poldek</code> zbudowany dla tej wersji <code>rpm</code>;</li>
<li>Wykonujemy:
<blockquote><pre><code>cd /var/lib/rpm
rm __db*
mv Packages{,.old}
db_dump_4.6 Packages.old &gt; Packages.dump
db_load Packages &lt; Packages.dump
rpm --rebuilddb</code></pre></blockquote></li>
<li>Powyższą czynność powtarzamy dla wszystkich katalogów <code>/vservers/.pkg/*/rpm/state</code>, które zdążyły się zaktualizować do nowej wersji, odpowiednio modyfikując pierwszą linię i do ostatniej dopisując <code>--dbpath &lt;sciezka_do_katalogu_state&gt;</code></li>
</ol>

<h4>Kolejny problem</h4>

<p>Ostatnim krokiem było przekonanie narzędzia <code>vpoldek</code>, że instalowane pakiety są dla właściwej architektury. Tutaj rozwiązaniem było dopisanie do każdego pliku <code>/vservers/.pkg/*/rpm/etc/macros</code> linijki:</p>

<blockquote><pre><code>%_host_os %_os</code></pre></blockquote>

<p>Voila, wszystko działa, maszyna została przebudowana. Następnym razem postaram się pozbyć irytujących komunikatów <code>LD_PRELOAD</code>.</p>
