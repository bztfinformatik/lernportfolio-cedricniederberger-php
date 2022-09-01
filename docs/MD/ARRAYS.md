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

## Arrays erweitern

Wenn man einen Array mit einem Feld erweitern will so geht das ganz einfach:

```php
<?php
$mitarbeiter = array("Bob","Peter");
$mitarbeiter[] = "Lisa";

echo $mitarbeiter[2];
?>
```

Bei Assoziativen Arrays muss man noch einen Schlüssel angeben:

```php
<?php
$mitarbeiter = array(
   "Bob" => "Bob Meier",
   "Peter" => "Peter Schröder");
$mitarbeiter["Lisa"] = "Lisa Müller";

echo $mitarbeiter["Lisa"];
?>
```

## Konvertieren von Arrays

#### Array zu String

Man kann Arrays in Strings also Zeichenketten konvertieren. Dies funktioniert folgendermassen:

```php
<?php
$namen = array("Paul", "Max", "Hans");

echo "Namen per Komma trennen: <br>";
$namenStr = implode(", ", $namen);
echo $namenStr; 

echo "<br><br>";
echo "Ein Name pro Zeile: <br>";
echo implode("<br>", $namen);
```

Mit *implode($trennzeichen,$array)* kann man ein Arrays mit einem Trennzeichen zwischen den Feldern zusammenfügen.

#### String zu Array

Im Gegensatz zu implode() lässt sich mittels explode($trennzeichen, $text) ein Text (String) in ein Array konvertieren. Hierbei wird der Text an allen Vorkommen von $trennzeichen getrennt.

```php
<?php
$text = "Paul,Max,Hannes";
$namen = explode(",", $text ); //Konvertierung des Strings in ein Array
echo "<pre>"; var_dump($namen); echo "</pre>"; //Formartierte Ausgabe des Arrays


//Ersetze die 1. Person durch neuen Namen
$namen[1] = "Lisa";

//Verwandel das Array zurück in einen String
$text = implode(", ", $namen);
echo $text;
```

## Mehrdemensionale Arrays

In einem Array kann man ein weiteres Array speichern. Und in diesem Array ein weiteres Arrray usw. Solche Arrays nennt man dann mehrdimensionale Arrays.

Beispiel:

```php
<?php
$mitarbeiter = array(
  array("Klaus", "Zabel"),
  array("Arnie", "Meier"),
  array("Willi", "Brand")
);

//Daten ausgeben
echo "Vorname: ".$mitarbeiter[0][0];
echo " Nachname: ".$mitarbeiter[0][1];
?>
```

Ausgabe: *Vorname: Klaus Nachname: Zabel*

Dies geht natürlich auch mit noch mehr Dimensionen, z.B. so:

```php
<?php
$mitarbeiter = array();
$mitarbeiter["Klaus"]["Vorname"] = "Klaus";
$mitarbeiter["Klaus"]["Nachname"] = "Zabel";
$mitarbeiter["Klaus"]["Kinder"][] = "Klaus-Junior";
$mitarbeiter["Klaus"]["Kinder"][] = "Kind2";

//Daten ausgeben
echo "Vorname: ".$mitarbeiter["Klaus"]["Vorname"];
echo " Nachname: ".$mitarbeiter["Klaus"]["Nachname"];
echo "<br> Er hat ";
echo count($mitarbeiter["Klaus"]["Kinder"])." Kinder";

//Ausgabe von Kind1:
//$mitarbeiter["Klaus"]["Kinder"][0];

echo "<br> Kinder: <br>";
foreach($mitarbeiter["Klaus"]["Kinder"] AS $name) {
   echo $name."<br>";
}
?>
```

## Arrays durchsuchen

So kann man Arrays durchsuchen

```php
$mitarbeiter = array("Bob","Peter","Lisa");
$name = "Bob";
if(in_array($name,$mitarbeiter)) {
   echo "Der Name $name ist in dem Array enthalten";
}
?>
```