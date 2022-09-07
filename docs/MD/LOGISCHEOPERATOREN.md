# Logische Operatoren

[Themen](MD/THEMEN.md)

[Quelle](https://www.php-einfach.de/php-tutorial/logische-operatoren/)

## Was sind logische Operatoren

Oft reicht es nicht aus in einer if-Anweisungen nur eine Bedingung zu überprüfen. Wenn man z.B. eine Passwortabfrage macht, möchte man wissen ob der Benutzername und das Passwort korrekt sind.

Für diesen Zweck gibt es die **logischen Operatoren**. Mittels lassen sich beliebig viele Bedingungen überprüfen. Um mehrere Bedingungen zu überprüfen existieren die folgenden Schlüsselwörter:

* Mittels **AND** oder der alternativen Schreibweise &&  müssen beide Bedingungen erfüllt sein.
* Mittels **OR**  oder der alternativen Schreibweise ||  muss nur eine Bedingung erfüllt sein.
* Mittels dem Ausrufezeichen !  lassen sich Bedingungen negieren, d.h. damit diese erfüllt ist, darf die Bedingung nicht zutreffen.
* Mittels Klammern (  und )  lassen sich Bedingungen noch gruppieren.

## AND und OR

Mit **AND** kann man zwei oder mehrere Bedingungen verknüpfen. Alternativ kann man **&&** schreiben.

Bei **OR** kann man bestimmen, dass eine erfüllte Bedingung ausreichend ist. Alternativ kann man **||** schreiben.

Beispiel:
```php
<?php 
$username = "Nils"; 
$passwort = "php-einfach"; 
if($username == "Nils" AND $passwort == "php-einfach") { 
   echo "Beide Bedingungen waren erfüllt - Zugriff erlaubt. <br />"; 
} 

if($username == "Nils" OR $passwort == "php-einfach") {
  echo "Eine oder beide Bedingungen waren erfüllt.";
}
?>
```

## Gruppieren mittels Klammern

Man kann AND und OR kombinieren. Damit dies muss man Klammer verwenden um die Bedingungen zu gruppieren.

Beispiel:

```php
<?php
$username = "Nils";
$passwort = "php-einfach";

if( ($username == "Nils" AND $passwort == "php-einfach") OR ($username == "Paul" AND $passwort == "geheim") ) {
  echo "Benutzername und Passwort passten zusammen. <br />";
}

if( $username == "Nils" AND ($passwort == "php-einfach" OR $passwort == "geheim") ) {
  echo "Der Benutzername war Nils, und das Passwort entweder php-einfach oder geheim.";
}
```

## Negation von Bedingungen

Mittel **!** lassen sich Bedingungen verneinen. Man kann Bedingungen bzw. auch mehrere Bedingungen verneinen.

Beispiel:

```php
<?php
$zahl = 25;

if($zahl >= 10 AND $zahl <= 20) {
   echo "Die Zahl ist zwischen 10 und 20. <br />";
}

if( !($zahl >= 10 AND $zahl <= 20) ) {
   echo "Die Zahl war NICHT zwischen 10 und 20 <br />";
}
?>
```