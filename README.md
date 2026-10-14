# JetaKryeziu-SistemiMenaxhiminAutoshkollave
Tema: Sistemi per Menaxhimin e Autoshkollave

## Raporti 1

Ideja eshte te behet nje sistem per menaxhimin e autoshkollave, ne menyre qe te kene me te leht instruktorat dhe studentet navigimin dhe kompletimin e detyrave qe te marrin patent shoferin ne menyre me efikase dhe te sigurt.


### Kerkesat

kerkesat per kete sistem jane;
- sistemi duhet te lejoj qasjen instruktorave dhe studenteve
- instruktoret mund ti shokojne oraret me studentat dhe llojin e kategoris, llojin e shpejtesis(manual apo automatik) dhe nivelin
- instruktoret me ane te sistemit mund te lajmerojn studentet ne ndryshim te orarit
- mund te rezervojne llojin e automjetit per orare te ndryshme dhe shikimin e makinave qe jane ne dispozicion per ate orar
- studentet mund te vijojne testet te ndryshme, shpjegimet dhe rregullat e trafiku 
- mund e vijojne orarn e tyre per kohen se kur e kan tesin teorik dh eate te vozitjes
- kan teste te gatshme per ushtrime ku mund te shikojne se sa jane te gatshem per shvillimin dhe kompletimin e testit
- secili instruktor mun te shoh te dhenate e studentit te tij dhe ndihmoj ku ka ngecje
- website mund te ken nje pershkrim te thjesht per autoshkollen ku studentet mund te kontaktojn autoshkollen per regjistrim, apo online mund te behet regjistrimi
- adminet, apo personat e veqant mund te shohin regjistrimet dhe mund te pranojn apo anulojn ate regjistrim, dhe ne baz te informatave mund te dergoj nje email me kontarten dhe informatat shtes qe duhet te permbush studenti per te pasur regjistrim te plot dhe kompletues
- instruktoret mund ti shohin studentet e ri dhe nese ju pershtatet informatat qe i ka dorezuar ai student mund ti dergojn ftes
- nes eme shume nje instruktor ka zgjedhur studentitn e njete, studenti  mund te shoh infrmatat e aitj instruktori dhe mund te zgjehd ate qe ai preferon
- ...


- ne website duhet te konfirmohet regjisrimi, pra autentifikim
- siguria e passwordid duhet te behet me hash
- qdo person duhet te ket id e veqant
- website duhet te jete responsiv per qdo lloj ekrani
- duhet te jet leht i kuptueshem dhe navigueshem
- darja e profile duhet te jete ku secili rol dueht te kry funksionet e veta
- pas qdo kerkese se pari admini duhet te verifikoj dhe konfirmoj pasi te behen ndryshime


### Teknikat/arkitektura

#### frontend
HTML, CSS, JavaScript, Boostrap
- faqet e studenteve, instruktoreve, admineve
- dizajni responsiv dhe teste

#### backend 
PHP: autentifikim, role, orare, reservime, aprovime, teste dhe njoftime

#### database
mySQL/MaraDB: perdoruesi, instruktoret, studentet, autormjetet,oraret, regjistrimet, rezultatet e testeve

Modeli filestar i databazes i sugjeruar, ku do kete rekomandime sipas nevojes:

|Tabela	|Për çfarë shërben|
|:---|:---|
|users	|Llogaritë, email-i, password hash dhe roli, hierraki me students, insturctors|
|students	|Të dhënat shtesë të studentëve|
|instructors	|Të dhënat e instruktorëve|
|categories	|Kategoritë e patentë-shoferit|
|vehicles	|Automjetet, kategoria dhe manual/automatik|
|registrations	|Kërkesat e reja për regjistrim dhe statusi i tyre|
|instructor_requests	|Ftesat dhe preferencat për instruktor|
|lessons	|Orari i mësimeve dhe rezervimet|
|exams	|Testet teorike dhe praktike, datat dhe statuset|
|questions	|Pyetjet për testet teorike|
|answers	|Përgjigjet e mundshme për pyetjet|
|test_attempts	|Tentimet dhe rezultatet e studentëve|
|notifications	|Njoftimet për studentët dhe instruktorët|
|approvals	|Kërkesat që presin shqyrtim nga administratori|



#### arkitektura
rekomandohet te jete monolitike, ku modulet ndahet sipas funksionalitetit

Modulet:
Perdoruesi, orari, regjistrimet, mesimi/ligjerata dhe teste, njoftime, administrimi


### Plan pune

sugjerimi: kerkesat -> dizajnimi -> implementimi -> verifikimi -> testimi

1. Fazat e zhvillimit të projektit
Faza	Aktivitetet kryesore	Rezultati i pritshëm
1. Analiza e kërkesave	Përcaktimi i funksioneve, roleve, kufizimeve dhe rregullave të sistemit.	Lista përfundimtare e kërkesave funksionale dhe jofunksionale.
2. Dizajnimi i sistemit	Diagrami i arkitekturës, diagrami ER, marrëdhëniet mes tabelave dhe rrjedha e proceseve.	Dizajni teknik dhe modeli i databazës.
3. Krijimi i databazës	Krijimi i tabelave, çelësave primarë dhe të huaj, kufizimeve dhe të dhënave fillestare.	Databaza MySQL/MariaDB e gatshme.
4. Ndërtimi i ndërfaqes	Faqja kryesore, formularët, navigimi, faqet e studentëve, instruktorëve dhe administratorit.	Ndërfaqe responsiv me HTML, CSS, JavaScript dhe Bootstrap.
5. Autentifikimi dhe rolet	Regjistrimi, hyrja, dalja, hashimi i fjalëkalimeve dhe kontrolli i qasjes sipas rolit.	Sistem i sigurt i autentifikimit dhe autorizimit.
6. Menaxhimi i regjistrimeve	Formularët e aplikimit, shqyrtimi i kërkesave, aprovimi/refuzimi dhe caktimi i instruktorit.	Proces funksional i regjistrimit të studentëve.
7. Menaxhimi i orareve	Krijimi i termineve, caktimi i instruktorëve, rezervimi i automjeteve dhe kontrolli i konflikteve.	Sistem funksional i orareve dhe rezervimeve.
8. Moduli mësimor dhe testet	Materialet teorike, pyetjet, përgjigjet, testet praktike dhe rezultatet.	Studentët mund të ushtrohen dhe instruktorët mund t'i përcjellin rezultatet.
9. Njoftimet dhe administrimi	Njoftimet për ndryshime të orarit, email-et, menaxhimi i përdoruesve dhe kërkesave.	Sistem i integruar i njoftimeve dhe administrimit.
10. Testimi dhe dokumentimi	Testet funksionale, siguria, responsiviteti, korrigjimi i gabimeve dhe përgatitja e dokumentacionit.	Versioni përfundimtar i testuar dhe i dokumentuar.
#### Fazat e zhvillimit të projektit

| Faza | Aktivitetet kryesore | Rezultati i pritshëm |
|---|---|---|
| 1. Analiza e kërkesave | Përcaktimi i funksioneve, roleve, kufizimeve dhe rregullave të sistemit. | Lista përfundimtare e kërkesave funksionale dhe jofunksionale. |
| 2. Dizajnimi i sistemit | Diagrami i arkitekturës, diagrami ER, marrëdhëniet mes tabelave dhe rrjedha e proceseve. | Dizajni teknik dhe modeli i databazës. |
| 3. Krijimi i databazës | Krijimi i tabelave, çelësave primarë dhe të huaj, kufizimeve dhe të dhënave fillestare. | Databaza MySQL/MariaDB e gatshme. |
| 4. Ndërtimi i ndërfaqes | Faqja kryesore, formularët, navigimi dhe faqet e studentëve, instruktorëve dhe administratorit. | Ndërfaqe responsive me HTML, CSS, JavaScript dhe Bootstrap. |
| 5. Autentifikimi dhe rolet | Regjistrimi, hyrja, dalja, hashimi i fjalëkalimeve dhe kontrolli i qasjes sipas rolit. | Sistem i sigurt i autentifikimit dhe autorizimit. |
| 6. Menaxhimi i regjistrimeve | Formularët e aplikimit, shqyrtimi i kërkesave, aprovimi/refuzimi dhe caktimi i instruktorit. | Proces funksional i regjistrimit të studentëve. |
| 7. Menaxhimi i orareve | Krijimi i termineve, caktimi i instruktorëve, rezervimi i automjeteve dhe kontrolli i konflikteve. | Sistem funksional i orareve dhe rezervimeve. |
| 8. Moduli mësimor dhe testet | Materialet teorike, pyetjet, përgjigjet, testet praktike dhe rezultatet. | Studentët mund të ushtrohen dhe instruktorët mund t'i përcjellin rezultatet. |
| 9. Njoftimet dhe administrimi | Njoftimet për ndryshime të orarit, email-et, menaxhimi i përdoruesve dhe kërkesave. | Sistem i integruar i njoftimeve dhe administrimit. |
| 10. Testimi dhe dokumentimi | Testet funksionale, siguria, responsiviteti, korrigjimi i gabimeve dhe përgatitja e dokumentacionit. | Versioni përfundimtar i testuar dhe i dokumentuar. |

#### Orai i propozuar 

Java 1: analiza kerkesave, dizajni teknik dhe databaza
Java 2: frontend dhe navigim
Java 3: autentifikim dhe auterizim (login, sesion, role)
Java 4: regjistrim dhe aprovime, orari dhe automjetet
Java 5: Materale dhe teste
java 6-7: njoftime dhe raporte
java 8<: integrim, testim, finalizim