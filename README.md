<B>Komputer</b>, na którym byly wykonywane obliczenia: <br>
    Procesor: Intel(R) Core(TM) i5-4460 CPU @ 3.20GHz 3.20 GHz<br>
    RAM: 4GB<br>
    System operacyjny: Windows 7 professional N (64-bitowy)<br>
    Dysk: HDD WD 500GB 7200 16MB<br><br>
    Wersja <b>MongoDB</b>: Windows 64-bit 2008plus 3.0.7<br>
    Wersja <b>PostgreSQL</b>: Windows 64-bit 9.4.5-1<br><br>

♥ Aggregation Pipeline<br><br>

Dane, ktore wybralam do zaimportowania do bazy to komentarze z Reddita.

<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/1_zpsncnnem9s.png">
<br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/2_zpsknzhi2y2.png"><br>

<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/3_zpshproszov.png"><br><br>

Jak widać zuzycie pamieci z czasem pracy roslo:
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/4_zps0iihg54r.png"><br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/5_zpsqqscpcte.png"><br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/6_zpslbbhdebp.png"><br><br>

Import dzialal bezproblemowo do momentu az nie zabraklo pamieci na dysku:
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/7_zps4yy5f5qb.png"><br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/8_zpsfukfi8cj.png"><br>
By umozliwic wykonanie zadania, usunelam lub przenioslam czesc plikow na drugi dysk.
Niestety nie udalo sie zaimportowac przez to wszystkich rekordow, jednak okazalo sie, ze jest ich wystarczajaco duzo, by moc efektywnie na nich pracowac:<br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/9_zpsnozgm1b0.png">
<br><br>
Zaimportowano 31 750 000 rekordow. <br>
Import wykonywal sie nieco ponad 3 godziny. <br><br>
Tak wyglada przykladowy rekord z bazy: 
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/10_zpss5yxxs8p.png"><br><br>

<b>Wykonane agregacje:</b>
<br><br>
- Ilosc najgorszych wpisow u trzech najgorszych autorow:<br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/12_zpsz1xg8thr.png"><br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/11_zpsogtxhywn.png"><br>
Wynik:<br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/13_zpstaetzalg.png"><br><br>

- Ilosc nieedytowanych wpisow:<br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/18_zps2kw9dypv.png"><br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/21_zpsjc5w9gx6.png"><br>
Wynik:<br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/22_zpsyj5ugbwf.png">
<br><br>

- Ilosc najmniej kontrowersyjnych komentarzy:<br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/27_zpsa9wiem8e.png"><br>
Wynik:<br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/28_zpsxwbcqeyo.png"><br><br>

- Ilosc postow, ktorych autor jest plci zenskiej:<br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/30_zpsx3vx30re.png"><br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/31_zps14fzle0s.png"><br>
Wynik:<br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/32_zps0ly2nvql.png"><br><br>

- Ilosc postow autora "dwimback":<br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/34_zpspvwlad3q.png"><br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/35_zpsa31m5j7z.png"><br>
Wynik:<br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql2/36_zpsw7fv7niu.png">

<br>
Wykonano 5 agregacji.<br>
Kazda z nich wykonywala sie ok. 20-30 minut. <br><br>
    
♥ EDA + GeoJSON<br><br>

<b>2a</b>.<br><br>

Do zaimportowania wybralam plik .json z ksiazkami i ich ocenami. 
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql/24_zpsgerafsck.png"><br>
...

Import do bazy MongoDB wygladal nastepujaco:

<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql/7_zpsedq3zwvy.png">

Zajelo to 0,631s
<br><br>
Zuzycie procesora i pamieci nie zmienilo sie znacznie. <br>

<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql/8_zpssgtrp1mt.png"><br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql/9_zpsvm9niw1n.png"><br>

Import do bazy PostgreSQL wygladal nastepujaco:<br>

<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql/21_zpsyzczlkaa.png"><br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql/22_zpsg8nhyvql.png"><br>

Rowniez w przypadku tej bazy zajelo to mniej niz 1 sekunde. Do zaimportowania pliku json do tejze bazy uzylam narzedzia <b>pgfutter</b> w wersji 0.3.2<br><br>


<b>2b</b>.<br><br>

Wprawdzie obie bazy podaly ilosc zaimportowanych rekordow juz przy importowaniu, ale zliczenie ich dla bazy MongoDB wygladalo tak:<br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql/10_zpsf6n1qel9.png"><br><br>

A dla PostgreSQL tak: <br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql/23_zps4jwqnqk9.png"> <br><br>

<b>2c</b>.<br><br>
Skrypt dla MongoDB:<br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql/25_zpsch34kol7.png"><br><br>

<b>2d</b>.<br><br>

Za pomoca geojson.io zaznaczylam obszar wojewodztwa pomorskiego i znajdujace sie w nim parki. Parki krajobrazowe oznaczone sa markerem czerwonym, a narodowe niebieskim.<br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql/26_zpscreugqjw.png"><br>
Przykladowy rekord:<br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql/27_zpsixyqdxkn.png"><br><br>
Import pliku geojson do bazy danych:<br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql/17_zpszstlid0n.png"><br><br>
Dodajemy geo-indeks do kolekcji <i>parki</i>:<br>
<img src="http://i1315.photobucket.com/albums/t589/incube91/nosql/18_zpsy9t6ng70.png"><br><br>


