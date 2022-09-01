# Arrays in PHP

[Themen](MD/THEMEN.md)

[Quelle](https://www.php-einfach.de/php-tutorial/php-array/)

## Arrays definieren

Beispiel Array definieren:

```php
<?php
$wochentage = array("Sonntag","Montag","Dienstag",
"Mittwoch","Donnerstag","Freitag","Samstag");
echo $wochentage[1];
?>
```

Um nun auf ein Array Feld zuzugreifen, kann man folgendes verwenden:

```php
<?php
echo $wochentage[1];
?>
```

Ausgabe: *Montag*

## Assoziative Arrays definieren

Bei grossen Arrays kann es umständlich sein zu wissen, in welchem Array Feld sich welcher Wert befindet. Deshalb kann man Assoziative Arrays definieren. Man gibt dem Arrays Feld eigentlich wie einen Alias.

Beispiel:

```php
<?php
$wochentage = array(
"so" => "Sonntag",
"mo" => "Montag",
"di" => "Dienstag",
"mi" => "Mittwoch",
"do" => "Donnerstag",
"fr" => "Freitag",
"sa" => "Samstag");

echo $wochentage["mo"];
?>
```

Nun kann man einfacher auf den Arrays zugreifen:

```php
echo $wochentage["mo"];
```