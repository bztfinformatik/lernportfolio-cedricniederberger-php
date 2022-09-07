# For-Schleifen

[Themen](MD/THEMEN.md)

[Quelle](https://www.php-einfach.de/php-tutorial/php-schleifen/)

## For-Schleifen in PHP

Ähnlich wie bei der while-Schleife, lässt sich die for-Schleife nutzen um Anweisungen solange auszuführen, wie eine bestimmte Bedingung erfüllt ist. Die Syntax der for-Schleife ist dabei wie folgt:

```php
<?php
for(Startwert; Bedingung; Schleifenschritt) {
   Anweisungen
}
?>
```

Ein Anwendungsbeispiel wäre

```php
<?php
for($i=0; $i < 10; $i++) {
   echo "$i, ";
}
?>
```

## Unterschied zur while-Schleife

Der Unterschied zur zuvor vorgestellten while-Schleife liegt nur in der Schreibweise. Mittels beiden Schleifentypen lässt sich die gleiche Funktionalität implementieren.

Aufgrund der einfacheren Syntax wird die for-Schleife aber zumeist verwendet bei dem hochzählen von Werten. Bei einer while-Schleife sind der Startwert, die Bedingung und der abschließende Schleifenschritt zum Erhöhen der Zählvariable auf drei Zeilen verteilt, bei einer for-Schleife finden sich alle Informationen in ein und der selben Zeile.