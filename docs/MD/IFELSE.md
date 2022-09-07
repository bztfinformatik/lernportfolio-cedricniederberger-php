# If-Anweisungen

[Themen](MD/THEMEN.md)

[Quelle](https://www.php-einfach.de/php-tutorial/if-anweisungen/)

## If-else in PHP

Das gerüst für eine simple If-Anweisung sieht so aus:

```php
<?php
if(Bedingung)
   {
   Anweisung
   }
?>
```

Wenn man eine If-else-Anweisung machen möchte, dann sieht das folgendermassen aus:

```php
<?php
if(Bedingung) 
   {
   Anweisung
   } 
else 
   {
   Anweisung
   }
?>
```

## Anwendung in Formular

Zuerst brauchen wir ein Formular:
```php
<form action="seite2.php" method="post">
<input type="Password" name="passwort" />
<input type="Submit" value="Absenden" />
</form>
```

In diesem Formular geben wir dann das Passwort ein. Beim Klick auf "Absenden", wird die Seite seite2.php aufgerufen und gleichzeitig an diese das Passwort übergeben.

seite2.php sieht so aus:
```php
<?php
$passwort = $_POST["passwort"];
 
if($passwort=="geheim")
   {
   echo "Herzlich Willkommen im internen Bereich";
   }
else
   {
   echo "Das Passwort ist leider falsch";
   }
?>
```