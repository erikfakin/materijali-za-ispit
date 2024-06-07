# Sadržaj
* [Linux](#linux)
* [HTML](#html)
* [PHP](#php)



Stream "Pripreme za završni ispit":

https://predavacialgebra-my.sharepoint.com/personal/algebra_nastava_predavaci_algebra_hr/_layouts/15/stream.aspx?id=%2Fpersonal%2Falgebra%5Fnastava%5Fpredavaci%5Falgebra%5Fhr%2FDocuments%2FRecordings%2FPripreme%20za%20zavr%C5%A1ni%20ispit%20BEDEV%2026%2E03%2E2024%2E%2D20240326%5F173510%2DSnimka%20sastanka%2Emp4&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&ga=1&referrer=StreamWebApp%2EWeb&referrerScenario=AddressBarCopied%2Eview%2Eb4f6ea55%2D0f24%2D40f8%2Db614%2D237a1d331270


****************
# Linux

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

Svi HTML dokumenti __moraju poceti__ s <!DOCTYPE> deklaracijom. U HTML5 deklaracija je `<!DOCTYPE html>`
___
__Par HTML tagova:__ 

| Tag           		| Primjer       |
| ------------- 		| ------------- |
| Hiperveza (Hiperlink)	| `<a href="/link-do-sljedece-stranice"> Tekst hiperveze </a>` |
| Tablica				| `<table> </table>` |
| Slike					| `<img alt="opis slike" src="izvor slike">` |
| Odlomak				| `<p> Tekst odlomka </p>` |		
___
__`<meta charset="UTF-8">`__ 

za koristenje specijalnih karaktera čćšđž...


*******************************************************
# PHP

__COMPOSER__

Composer je alat za upravljanje ovisnim paketima u aplikacijama napisanim u PHP programskom jeziku. Pomoću alata Composer moguće je instalirati i ažurirati sve pakete koji su navedeni kao potrebni u aplikaciji koju programer razvija.
___
__var_dump($var)__ 

Funckija koja ispise strukturirane informacije jednje ili vise varijabla, ukljucujuci tip i vrijednost.
```
$a = array(1, 2, array("a", "b", "c"));
var_dump($a);

// Ispisati će:

array(3) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  array(3) {
    [0]=>
    string(1) "a"
    [1]=>
    string(1) "b"
    [2]=>
    string(1) "c"
  }
}

```

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

spl_autoload_register() omogućuje nam da registriramo jednu uli više funkcija (ili statičke metode iz naše Autoload klase) koje će PHP staviti u stack/queue i pozvati ih sekvencijalno kada deklariramo "new Class".

Primjer:
- mozemo "strpat" sve potrebne klase u jedanom folderu i includat sve odjednom:
  ```
  function my_autoloader($class) {
  	include 'classes/' . $class . '.class.php';
  }
  
  spl_autoload_register('my_autoloader');
  ```
Ili koristeći anonimnu funkciju (closure):
```
spl_autoload_register(function ($class) {
	include 'classes/' . $class . '.class.php';
});
```
___
__Što je GET metoda?__

GET metoda se koristi za dobivanje (get) podataka iz jednog resursa.

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

POST metoda se koristi za slanje (post) podataka poslužitelju radi stvaranja/ažuriranja resursa.

Podaci poslani poslužitelju s POST-om pohranjuju se u `request body`-u POST requesta.

Napomene:
- POST zahtjevi se nikada ne spremaju u cache
- POST zahtjevi ne ostaju u povijesti preglednika
- POST zahtjeve nije moguće označiti knjižnom oznakom
- POST zahtjevi nemaju ograničenja u duljini podataka
___
__Koja je razlika između `"` i `'`?__

Stringovi definirani pomoću dvostrukih navodnika " omogućuju interpretaciju posebnih znakova i varijabli unutar stringa. 
Ovo znači da će PHP parsirati string i zamijeniti varijable njihovim vrijednostima, kao i obraditi escape sekvence posebnih znakova.+

Npr:
```
$name = "Marko";
$greeting = "Pozdrav, $name!"; // Rezultat: Pozdrav, Marko!
$escape = "Ovo je nova linija.\nOvo je nova rečenica."; // \n se interpretira kao nova linija
```

Stringovi definirani pomoću jednostrukih navodnika ne omogućuju interpretaciju varijabli ili posebnih znakova (osim escape sekvenci za jednostruki navodnik i backslash). 
Ovo znači da će se string prikazati točno onako kako je napisan.

Npr:
```
$name = 'Marko';
$greeting = 'Pozdrav, $name!'; // Rezultat: Pozdrav, $name!
$escape = 'Ovo je nova linija.\nOvo je nova rečenica.'; // \n se interpretira doslovno
```
___
__Koja je razlika između string koji je null ili prazan?__

Null znači da string nema vrijednosti, dok prazan string je string koji kao vrijednost nema nista, tj ima "".
___
__Što su `&&` i `||`?__ 

`&&` AND i `||` OR su logičke operacije koje u PHP-u uvijek vračaju boolean true ili false.

Npr:

| Primjer           	| Rezultat       |
| ------------- 		| ------------- |
| `$a and $b`			| `true` ako i $a i $b su `true`. |
| `$a && $b`			| `true` ako i $a i $b su `true`. |
| `$a or $b`			| `true` ako bilo koja $a ili $b je `true`. |
| `$a \|\| $b`			| `true` ako bilo koja $a ili $b je `true`. |
___	
__Kako se deklarira funkcija?__
```
function naziv_funkcije(parametri) { 
	// tijelo funkcije 
}
```
___
__Kako vraćamo vrijednost u funkciji?__

Za vracanje vrijednosti iz funkcije koristimo `return`.
___
__Kako u funkiciji definiramo da prima varijabilni broj argumentata? Što to znači?__
PHP ima podršku za argumenata varijabilne duljine u korisnički definiranim funkcijama korištenjem `...` tokena.
​`...`  označava da funkcija prihvaća promjenjivi broj argumenata koji će biti proslijeđeni u zadanu varijablu kao niz.
Npr:
```
function sum(...$numbers) {
    $acc = 0;
    foreach ($numbers as $n) {
        $acc += $n;
    }
    return $acc;
}
echo sum(1, 2, 3, 4); // vratit će 10
```
___
__Što su globalne varijable i kako ih definiramo i koristimo?__

Globalne varijable su varijable koje su dostupne u svim dijelovima skripte, uključujući funkcije, metode i objekte. 
Globalne varijable su definirane izvan funkcija i klasa, u globalnom opsegu.
Za koristiti globalne varijable koristimo keyword `global` ili ih pristupamo koristeći superglobalnu varijablu `$GLOBALS`.
Npr:
```
$globalVar = "Ovo je globalna varijabla";

function myFunction() {
    global $globalVar;
    echo $globalVar; // Ispisuje: Ovo je globalna varijabla
	// ili  echo $GLOBALS['globalVar]
}
```
PHP također ima niz predefiniranih superglobalnih varijabli koje su uvijek dostupne, bez potrebe za korištenjem ključne riječi global. Neke od najčešće korištenih superglobalnih varijabli su:

- $_GET: podaci poslani putem URL parametara
- $_POST: podaci poslani putem HTTP POST metode
- $_REQUEST: podaci poslani putem GET, POST ili COOKIE
- $_SESSION: podaci sesije
- $_COOKIE: podaci kolačića
- $_SERVER: informacije o serveru i izvršenju skripte
- $_FILES: podaci o uploadanim datotekama
- $_ENV: informacije o varijablama okoline
___
__Kako brišemo cookies u PHP-u?__

Cookie brišemo postavljanjem cookie-a koji želimo brisati s istim imenom , ali s isteklim vremenom trajanja. To se radi pomoću funkcije setcookie() s vremenom trajanja u prošlosti.
Npr:
```
// Brisanje kolačića s imenom "user"
setcookie("user", "", time() - 3600, "/"); // Postavite vrijeme isteka na prošlost
```
___
__Što je pointer ili referenca na varijablu?__

Referenca ili pointer na varijablu stvara se pomoću operatora &. 
Kada se referenca stvori, obje varijable koje dijele referencu ukazuju na istu memorijsku lokaciju.
Možete proslijediti varijablu funkciji po referenci tako da funkcija može izravno mijenjati varijablu.
___
__Koja je razlika između indeksirane nizove i asocijativne nizove?__

Indeksirani nizovi koriste numeričke indekse, koji počinju od nule.
Asocijativni nizovi koriste ključeve koji mogu biti stringovi ili cijeli brojevi.
```
// Indeksirani niz
$indeksiraniNiz = ["Jabuka", "Banana", "Trešnja"];
ili
$indeksiraniNiz = array("Jabuka", "Banana", "Trešnja");

// Asocijativni niz
$asocijativniNiz = ["ime" => "Marko", "godine" => 25, "grad" => "Zagreb"];
ili
$asocijativniNiz = array("ime" => "Marko", "godine" => 25, "grad" => "Zagreb");

```
___
__Kako čitamo cijli sadržaj datoteke kao string?__

```
$filename = "example.txt";

// Čitanje cijelog sadržaja datoteke
$content = file_get_contents($filename);
```
___
__Kako premiještamo učitanu datoteku?__

```
move_uploaded_file(string $from, string $to);
```
Ova funkcija provjerava je li datoteka koju označava `$from` valjana datoteka za učitavanje (što znači da je učitana putem PHP-ovog HTTP POST mehanizma učitavanja). Ako je datoteka važeća, bit će premještena u naziv datoteke iz varijable `$to`.
___
__Što su sesije i kako ih koristimo?__
Sesije u PHP-u omogućuju pohranu podataka na serveru za korištenje tijekom više stranica. One se često koriste za pohranu informacija o korisnicima, poput podataka za prijavu ili podataka o košarici za kupnju, dok korisnik pregledava web mjesto. Sesije su korisne jer omogućuju zadržavanje stanja između HTTP zahtjeva, što je korisno za funkcionalnosti koje zahtijevaju praćenje korisničkog stanja.

Sesiju inicijaliziramo pozivanjem:
`session_start();`
Svaki put kada želimo dohvatiti ili spremiti podatke u sesiju MORAMO prije pozivati `session_start()`

Podatke iz sesije spremamo:
`$_SESSION['username'] = 'Marko';`

Podatke iz sesije čitamo:
`echo $_SESSION['username'];`

Podatke is sesije brišemo:
`unset($_SESSION['username']);`



*****************
# MySQL


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
