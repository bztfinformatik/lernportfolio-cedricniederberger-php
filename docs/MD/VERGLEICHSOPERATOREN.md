# Vergleichsoperatoren

[Themen](MD/THEMEN.md)

[Quelle](https://www.php-einfach.de/php-tutorial/php-vergleichsoperatoren/)

## Tabelle Vergleichsoperatoren

In folgender Tabelle kann man die Vergleichsoperatoren sehen:

![Vergleichsoperatoren](img/tabelle_vergleichsoperatoren.png)

## Unterschied **==** und **=**

In PHP existieren die Vergleichsoperatoren == und === um auf Gleichheit zu überprüfen bzw. != und !== um auf Ungleichheit zu überprüfen.

Der Unterschied zwischen == und ===, dass bei == nur der Wert überprüft wird, bei === wird zusätzlich der Typ der Variable überprüft. Habt ihr in der einen Variable beispielsweise den Integer 1 hinterlegt, in der anderen Variable den String "1", so würde == ein true zurückgeben, der Operator === aber false, da die Typen der Variablen verschieden war.

Beispiel:

```php
<?php
$integer = 1;
$string = "1";

echo "Ergebnis von ==: ";
var_dump($integer == $string);

echo "<br /> Ergebnis von ===: ";
var_dump($integer === $string);
?>
```

In den meisten Fällen wird ==  bzw. !=  verwendet, allerdings ist es notwendig in manchen Situationen auf ===  bzw. !==  umzusteigen. Die Funktion strpos($text, $suchwort)  gibt die Position des $suchwort im $text zurück. Sollte es nicht gefunden werden, so wird false zurückgegeben. Nun kann strpos() aber auch Position 0 zurückgeben, sollte das Suchwort zu Beginn des Textes stehen. Allerdings, wie das folgende Beispiel zeigt, würde hier ein Vergleich mit != nicht mehr funktionieren:

```php
<?php
$text = "Dies ist ein Text";
$suchwort = "Dies";

$position = strpos($text, $suchwort);

if($position == false) {
   echo "Dein Suchwort wurde im Text nicht gefunden";
} else {
   echo "Dein Suchwort wurde an Position $position gefunden";
}
?>
```
