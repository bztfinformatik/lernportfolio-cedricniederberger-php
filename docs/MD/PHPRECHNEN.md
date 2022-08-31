# PHP Rechnen mit Variablen

[Themen](MD/THEMEN.md)

[Quelle](https://www.php-einfach.de/php-tutorial/rechnen-mit-variablen/)

## Grundlagen Rechnen

**Zwei Variablen zusammenrechnen:**

```php
<?php
$zahl1 = 10;
$zahl2 = 5;
$ergebnis = $zahl1 + $zahl2;
echo "Ergebnis: $ergebnis";
?>
```

Ausgabe: *Ergebnis: 15*

**Zahl zu einer Variabel dazurechnen:**

```php
<?php
$zahl = 1;
$ergebnis = $zahl + 5;
echo $ergebnis;
?>
```

Ausgabe: *6*

**Beispiele für alle einfachen Berechnungen:**

```php
<?php
$zahl1 = 10;
$zahl2 = 5;
echo $zahl1 + $zahl2; //addieren

echo $zahl1 - $zahl2; //subtrahieren

echo $zahl1 * $zahl2; //multiplizieren

echo $zahl1 / $zahl2; //dividieren

echo pow($zahl1,$zahl2); //Zahl1 hoch Zahl2 (10^5)

echo sqrt(64); // Wurzel von 64

echo 2*$zahl1 + 5*$zahl2 - 3; //Berechnet 2*10 + 5*5 - 3
?>
```

## Dekrementieren und Inkrementieren

Wenn man eine Variabel um 1 erhöhen oder um 1 verkleinern, gibt es einen einfachen Trick:

**Erhöhen:**

```php
<?php
$erhoehen = 1;
$erhoehen++;
echo $erhoehen;
?>
```

Ausgabe: *2*

**Verkleinern**

```php
<?php
$senken = 2;
$senken--;
echo $senken;
?>
```

Ausgabe: *1*

## Kurzschreibweise

Weil **$zahl = $zahl + 10;** viel zu lange ist kann man **$zahl += 10;** stattdessen verwenden um ganze 0.5 sekunden seiner Lebenszeit zu sparen. Bei Grossen Programmen können das zusammen locker 1.5 Minuten betragen.