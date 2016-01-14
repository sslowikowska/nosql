<B>Komputer</b>, na którym byly wykonywane obliczenia: <br>
    Procesor: Intel(R) Core(TM) i5-4460 CPU @ 3.20GHz 3.20 GHz<br>
    RAM: 4GB<br>
    System operacyjny: Windows 7 professional N (64-bitowy)<br>
    Dysk: HDD WD 500GB 7200 16MB<br><br>
    Wersja <b>MongoDB</b>: Windows 64-bit 2008plus 3.0.7<br>
    Wersja <b>PostgreSQL</b>: Windows 64-bit 9.4.5-1<br><br>
    
♥ EDA<br><br>

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

♥ Aggregation Pipeline<br><br>
