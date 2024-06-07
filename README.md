https://predavacialgebra-my.sharepoint.com/personal/algebra_nastava_predavaci_algebra_hr/_layouts/15/stream.aspx?id=%2Fpersonal%2Falgebra%5Fnastava%5Fpredavaci%5Falgebra%5Fhr%2FDocuments%2FRecordings%2FPripreme%20za%20zavr%C5%A1ni%20ispit%20BEDEV%2026%2E03%2E2024%2E%2D20240326%5F173510%2DSnimka%20sastanka%2Emp4&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&ga=1&referrer=StreamWebApp%2EWeb&referrerScenario=AddressBarCopied%2Eview%2Eb4f6ea55%2D0f24%2D40f8%2Db614%2D237a1d331270

__Linux komande:__
- pwd -> ispisi trenutni direktorij (Current Working Directory)
- mkdir -> kreiraj direktorij
- cat -> pokazi sadrzaj datoteke
- ls ->	listaj sve (fileovi i foldere) u trenutnom  direktoriju
- cd ->	change directory
- cp ->	copy
- mv ->	move ili rename (ako navedemo isti direktorij i durgi naziv datoteke)
- hostname -I -> za prikaz ip adrese _

__Editori__: Vi/Vim, Nano, Emacs
- Vi:
	- ima 3 mode-a: command, insert, replace mode
	- :wq! za izaci i spremiti promjene :w(write)q(quit)!(execute)

___
__Sto je Apache?__ 

Apache HTTP poslužitelj (Apache HTTP server) je besplatni web poslužitelj otvorenog koda.
___
__Kako se konfigurira Apache?__

Apache se konfigurira postavljanjem direktiv u obicnu tekstualnu datoteku. Glavna konfiguracijska datoteka obično se naziva httpd.conf
___
__Sto je httpd.conf?__

Glavna konfiguracijska datoteka za konfiguriranje Apache-a
___
__Koja je osnovna svrha Apache2 na Ubuntu 22 serveru?__

Web poslužitelj - web server
___
__Koja naredba se koristi za instalaciju Apache2 na Ubuntu 22?__

`sudo apt install apache2`
___
__Koji je zadani korijenski direktorij za web Apache2 na Ubuntu 22?__ 

/var/www/html
___
__Koja se konfiguracijska datoteka obično koristi za mijenjanje postavki Apachea na Ubuntu 22?__

/etc/apache2/httpd.conf
___
__Kako možete ponovno pokrenuti uslugu Apache2 nakon što napravite promjene u konfiguraciji?__ 

`sudo systemctl restart apache2`
___
__Koja naredba se koristi za omogućavanje stranice u Apache2?__ 

`sudo a2ensite`
___
__Koja je svrha naredbe `a2enmod` u Apache2?__ 

Omogućavanje Apache modula
___
__Na kojem portu Apache2 obično sluša dolazne HTTP zahtjeve?__ 

Port 80
___
__Koja naredba se koristi za provjeru sintakse Apache konfiguracijskih datoteka bez ponovnog pokretanja usluge?__ 

`sudo apachectl configtest`
___
__Kako možete onemogućiti zadani Apache2 site na Ubuntu 22?__ 

`sudo a2dissite default`

*****

# HTML 

__Sto je HTML?__ 

HTML je kratica za HyperText Markup Language, što znači prezentacijski jezik za izradu web stranica.
___
__<!DOCTYPE html>__ 

Svi HTML dokumenti __moraju poceti__ s <!DOCTYPE> deklaracijom. U HTML5 deklaracija je <!DOCTYPE html>
___
__Par HTML tagova:__ 

| Tag           	| Primjer       |
| ------------- 	| ------------- |
| Hiperveza (Hiperlink)	| `<a href="/link-do-sljedece-stranice"> Tekst hiperveze </a>` |
| Tablica		| `<table> </table>` |
| Slike			| `<img alt="opis slike" src="izvor slike">` |
| Odlomak		| `<p> Tekst odlomka </p>` |		
___
__`<meta charset="UTF-8">`__ 

za koristenje specijalnih karaktera čćšđž...


*******************************************************
# PHP

__COMPOSER__

Upravitelj paketa za PHP
___
__var_dump($var)__ 

Funckija koja ispise strukturirane informacije jednje ili vise varija, ukljucujuci tip varijable i vrijednost
___
__switch bez break u case-u:__

ako nema break onda se pokrene sljedeci block od case npr:
```
switch($broj){
	case 0:
	case 1:
	case 2: echo "<=2" break;
}
```
ispisat ce se "<=2" ako je $broj jednak 0, 1 ili 2
___
__Što je PHP?___

PHP (rekurzivni akronim i backronim za „PHP: Hypertext Preprocessor“, prije „Personal Home Page Tools“) je jedan programski jezik koji se orijentira po C i Perl sintaksi, namijenjen prvenstveno programiranju dinamičnih web stranica. PHP je kao slobodni softver distribuiran pod PHP licencnim uvjetima. PHP se ističe širokom podrškom raznih baza podataka i internet protokola kao i raspoloživosti brojnih programerskih knjižnica.
___
__Kako se označava početak PHP skripte?__

`<?php` označava početak PHP skripte
___
__Kako ispisujemo tekst?__

`echo "nesto";`
___
__PHP tipovi podataka?__

- cijeli brojevi (engl. integer)
- realni brojevi (engl. floating point numbers)
- tekstni podatci (engl. string)
- logičke varijable, nizovi i objekti
___
__Kako označavamo komentare?__

- `//`
- `/*`
- `#`
___
__Što je closure?__

Closure je anonimna funckija. Koriste se uglavnom kao callable parametar u drugim funkcijama (callback). 
Closure funkciju možemo također spremiti u varijablu i pozvati ih tako u programu.
Primjer:
```
function(){
	echo "moja funkcija";
}
```
___
__Što je spl_autoload_register?__

spl_autoload_register() omogućuje nam da registriramo mnogobrojne funkcije (ili statičke metode iz naše Autoload klase) koje će PHP staviti u stack/queue i pozvati ih sekvencijalno kada deklariramo "new Class".

Primjer:
- mozemo "strpat" sve potrebne klase u jedanom folderu i require sve odjednom
  ```
  function my_autoloader($class) {
  	include 'classes/' . $class . '.class.php';
  }
  
  spl_autoload_register('my_autoloader');
  ```
Ili koristeći anonimnu funkciju:
```
spl_autoload_register(function ($class) {
	include 'classes/' . $class . '.class.php';
});
```
___
__Što je GET metoda?__

GET metoda se koristi za dobivanje podataka iz jednog resursa.

Niz upita (parovi names/values) šalju se u URL-u zahtjeva GET:

`/test/demo_form.php?name1=value1&name2=value2`

Napomene:
- GET zahtjevi mogu se spremiti u cache
- GET zahtjevi ostaju u povijesti preglednika
- GET zahtjevi mogu biti označeni knjižnom oznakom
- GET zahtjevi nikada se ne smiju koristiti kada se radi o osjetljivim podacima
- GET zahtjevi imaju ograničenja duljine
- GET zahtjevi koriste se samo za traženje podataka (ne i za izmjenu)
___
__Što je POST metoda?__

POST metoda se koristi za slanje podataka poslužitelju radi stvaranja/ažuriranja resursa.

Podaci poslani poslužitelju s POST-om pohranjuju se u `request body` POST zahtjeva.

Napomene:
- POST zahtjevi se nikada ne spremaju u cache
- POST zahtjevi ne ostaju u povijesti preglednika
- POST zahtjeve nije moguće označiti knjižnom oznakom
- POST zahtjevi nemaju ograničenja u duljini podataka
___
__Koja je razlika između `"` i `'`?__

__
- " i ' - u " idu special char \n, i varijable
- null i prazan string - null nema vrijednosti, "" je prazan string https://www.google.com/url?sa=i&url=https%3A%2F%2Fcseducators.stackexchange.com%2Fquestions%2F6977%2Freal-world-examples-for-the-difference-between-null-and-zero&psig=AOvVaw2yprP-J8KJIXJEw_C5HOFk&ust=1706124191494000&source=images&cd=vfe&opi=89978449&ved=0CBMQjRxqFwoTCOCXsIae9IMDFQAAAAAdAAAAABAH
- & i | - and i or
- deklaracija funckije . function naziv_funkcije(parametri) { // tijelo funkcije }
- sza vracanje funcjike - return
- promjenjiv broju argumeata - function imeFunckije(...$vars){}
- globalna varijabla - global $varijabla; ili $GLOBALS['variable_name'];
- kako brisemo cookie - stavimo expiration u proslost
- pointer/referenca &varijabla
- niz indexirani, asocijativni - indexirani koriste brojeve kao kljuc, asocijativni stringove
- kako se ucitana datoteka premjesta - move_uploaded_file
- stvaranje sessiona - session_start() 



*******************************************************
			MySQL
*******************************************************

Baza podataka je organizirani skup podataka pohranjenih u računalu na sustavan način

Relacijski model baze podataka - svaka relacija mora da ima definiran primarni ključ, opcionalno može da posjeduje i strani ključ 

Osnovi element naziva se entitet. 

relacija - e jedan prema jedan, jedan prema više odnosno više prema jedan te više prema više.

SQL   - structured query language - strukturni upitni jezik
      - Jezik visoke razine

mysql -u root -p   - za otboriti mysql klijent u cmd/shell kao user root

 SQL jezik sastoji se od ključnih riječi na engleskom koje se mogu podijeliti u nekoliko
grupa:
– DCL (engl. Data Control Language) – jezika za kontrolu podataka
– DML (engl. Data Manipulation Language) – jezik za manipulaciju podacima
– DDL (engl. Data Definition Language) – jezik za definiranje podataka
– DQL (engl. Data Query Language) – jezik za izvršavanje upita nad podacima

Sto je normalizacija, reference, kljucevi, relacije, primarni i unique kljuc
razlika izmedu unique i primarni: unique moze biti null i ako je null ne treba biti unique, moze viswe redaka biti null

kompozitni kljuc za pivot table ili intermidiate table

kardinalnost- vrsta relacije 1 ->N, 1->1, N->M
normalizacija smanjuje redundanciju



*******************************************************
			Napredni PHP
*******************************************************

spl_autoload_register
PSR-4
