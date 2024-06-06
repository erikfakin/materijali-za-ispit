https://predavacialgebra-my.sharepoint.com/personal/algebra_nastava_predavaci_algebra_hr/_layouts/15/stream.aspx?id=%2Fpersonal%2Falgebra%5Fnastava%5Fpredavaci%5Falgebra%5Fhr%2FDocuments%2FRecordings%2FPripreme%20za%20zavr%C5%A1ni%20ispit%20BEDEV%2026%2E03%2E2024%2E%2D20240326%5F173510%2DSnimka%20sastanka%2Emp4&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&ga=1&referrer=StreamWebApp%2EWeb&referrerScenario=AddressBarCopied%2Eview%2Eb4f6ea55%2D0f24%2D40f8%2Db614%2D237a1d331270

__Linux komande:__
	- pwd - 	ispisi trenutni direktorij (Current Working Directory)
	- mkdir - kreiraj direktorij
	- cat - 	pokazi sadrzaj datoteke
	- ls - 	listaj sve (fileovi i foldere) u trenutnom  direktoriju
	- cd - 	change directory
	- cp - 	copy
	- mv - 	move ili rename (ako navedemo isti direktorij i durgi naziv datoteke)
	- hostname -I - za prikaz ip adrese 
__Editori__ - Vi/Vim, Nano, Emacs
	- Vi 	- ima 3 mode-a: command, insert, replace mode
		- :wq! za izaci i spremiti promjene :w(write)q(quit)!(execute)


__Sto je Apache?__ Apache HTTP poslužitelj (Apache HTTP server) je besplatni web poslužitelj otvorenog koda.

__Kako se konfigurira Apache?__ Apache se konfigurira postavljanjem direktiv u obicnu tekstualnu datoteku. Glavna konfiguracijska datoteka obično se naziva httpd.conf

__Sto je httpd.conf?__ Glavna konfiguracijska datoteka za konfiguriranje Apache-a

__Koja je osnovna svrha Apache2 na Ubuntu 22 serveru?__ Web poslužitelj - web server

__Koja naredba se koristi za instalaciju Apache2 na Ubuntu 22?__ `sudo apt install apache2`

__Koji je zadani korijenski direktorij za web Apache2 na Ubuntu 22?__ /var/www/html

__Koja se konfiguracijska datoteka obično koristi za mijenjanje postavki Apachea na Ubuntu 22?__ /etc/apache2/httpd.conf

__Kako možete ponovno pokrenuti uslugu Apache2 nakon što napravite promjene u konfiguraciji?__ `sudo systemctl restart apache2`

__Koja naredba se koristi za omogućavanje stranice u Apache2?__ `sudo a2ensite`

__Koja je svrha naredbe `a2enmod` u Apache2?__ Omogućavanje Apache modula

__Na kojem portu Apache2 obično sluša dolazne HTTP zahtjeve?__ 80

__Koja naredba se koristi za provjeru sintakse Apache konfiguracijskih datoteka bez ponovnog pokretanja usluge?__ `sudo apachectl configtest`

__Kako možete onemogućiti zadani Apache2 site na Ubuntu 22?__ `sudo a2dissite default`

*****

# HTML 

__Sto je HTML?__ HTML je kratica za HyperText Markup Language, što znači prezentacijski jezik za izradu web stranica.
__<!DOCTYPE html>__ - Svi HTML dokumenti __moraju poceti__ s <!DOCTYPE> deklaracijom. U HTML5 deklaracija je <!DOCTYPE html>
__Par HTML tagova:__ 
	- hiperveza (hiperlink): 	`<a href="/link-do-sljedece-stranice"> Tekst hiperveze </a>`
	- tablica: 			`<table> </table>`
        - slike: 			`<img alt="opis slike" src="izvor slike">`
	- odlomak: 			`<p> Tekst odlomka </p>`

__<meta charset="UTF-8">__ za koristenje specijalnih karaktera čćšđž...


*******************************************************
# PHP

COMPOSER - upravitelj paketa za php
var_dump($var) ispisuje tip varijable i vrijesnost


switch: ako nema break onda se pokrene sljedeci block od case npr:
switch($nesto){
case 0:
case 1:
case 2: echo "<=2" break;}


PHP
- sto je PHP - 
- sintaksa za pokretanje php-a? <?php
. echo "nesto"; - za ispis teksta
- sto nije vrsta podataka - decimal
- nacini komentiranja //, /*, #
- closure - anonimna funckija function () {}
- spl_autoload_register - Register given function as __autoload() implementation | ucita sve fileove preko neke funkcije npr. 
   - mozemo strpat sve u jedan foldser i require sve odjednom
   function my_autoloader($class) {
      include 'classes/' . $class . '.class.php';
   }

   spl_autoload_register('my_autoloader');

   // Or, using an anonymous function
   spl_autoload_register(function ($class) {
      include 'classes/' . $class . '.class.php';
   });

- post - get razlike
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
