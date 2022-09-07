# While-Schleifen

[Themen](MD/THEMEN.md)

[Quelle](https://www.php-einfach.de/php-tutorial/php-schleifen/)

## While-Schleifen in PHP

Der Syntax einer while-Schleife ist wie folgt aufgebaut:

```php
<?php
while(Bedingung) {
   Anweisungen
}
?>
```

Eine while-Schleife führt einen Befehl aus solange eine bestimmte Bedingung erfüllt wird.

Beispiel:

```php
<?php
$i = 0;
while($i < 10) {
   echo "$i, ";
   $i++;
}
?>
```

## break und continue

In PHP gibt es zwei nützliche Befehele **break** und **continue**

Mittels **break** können wir den Schleifenablauf in der Schleife beenden.

Beispiel für **break**:

```php
<?php
$max = 30;
$zaehler = 0;
$increment = 2;

while($zaehler < $max) {
   if($zaehler == 10) {
      echo "Bei der Zahl 10 hören wir auf";
      break;
   }
   echo "$zaehler , ";
   $zaehler += $increment; //Erhöht den $zaehler um den Wert $increment
}
?>
```

Bei **continue** wird die restliche Schleife einfach übersprungen.

Beispiel für **continue**:

```php
<?php
$max = 30;
$zaehler = 0;
$increment = 2;

while($zaehler < $max) {
   $zaehler += $increment; //Erhöht den $zahler um den Wert $increment
   if($zaehler >= 10 AND $zaehler <= 15) {
      echo "Eine Zahl zwischen 10 und 15 <br>";
      continue;
   }

   echo "$zaehler <br>"; 
}
?>
```

## do-While-Schleife

Eine kleine Modifikation der while-Schleife ist die **do-while-Schleife**. Bei dieser wird die Bedingung der Schleife erst nach dem Schleifenkörper überprüft. Das bedeutet, dass der Schleifenkörper auf alle Fälle mindestens einmal durchläuft.

Der Syntax sieht folgendermassen aus:

```php
<?php
do {
   Anweisungen
} while(Bedingung);
?>
```

Ein Praxisbeispiel könnte so aussehen:

```php
<?php
$zufall = rand(0, 30);
while($zufall > 10 AND $zufall < 20) {
   $zufall = rand(0, 30);
}

echo "Unsere Zufallszahl: $zufall";
?>
```

