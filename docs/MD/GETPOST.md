# Get und Post in PHP

[Themen](MD/THEMEN.md)

[Quelle](https://www.php-einfach.de/php-tutorial/_get-und-_post/)

## Datenübergabe mittels $_GET

Bei der GET-Methode spricht man von Variablenwerten, die mittels der URL übergeben werden. Vielleicht ist euch im Browser bereits aufgefallen, dass viele URLs ein ? hinter dem Dateinamen haben gefolgt von entsprechenden Werten. Dies sind die GET-Variablen der Website. Im PHP-Script könnt ihr auf diese wie folgt zugreifen.

```php
<?php
$vorname = $_GET['vorname'];
$nachname = $_GET['nachname'];
echo "Hallo $vorname $nachname";
?>
```

Wenn ihr diese Seite auf eurem Webspace mittels *get.php?vorname=Max&nachname=Meier* aufruft, so übergebt ihr dem Script zwei $_GET-Variablen.

## Datenübergabe mittels $_POST

Im Gegensatz zu $_GET werden $_POST-Variablen nicht per URL, sondern per Formular übertragen.

Formular Beispiel:

```php
<form action="seite2.php?wochentag=Sonntag" method="post">
Vorname: <input type="text" name="vorname" /><br />
Namename: <input type="text" name="nachname" /><br />
<input type="Submit" value="Absenden" />
</form>
```

Es ist auch wichtig, dass wir allen Eingabefeldern einen einzigartigen Namen zuweisen, damit sie nach dem Absenden auf der zweiten Seite auch korrekt abgefragt werden können.

Im obigen Formular hat manr bei action die Zielseite definiert und bei method die POST-Methode ausgewählt.
Nun kann man auf *seite2.php* folgender eingabe die POST-Variablen abrufen.

```php
<?php
$vorname = $_POST["vorname"];
$nachname = $_POST["nachname"];
echo "Hallo $vorname $nachname";
?>
```

## POST oder GET?

Möchte man eine Eingaben aus einem Formular übergeben, so sollte man immer POST benutzen weil bei GET die Eingaben der URL angehängt werden, wodurch die Textlänge eingeschränkt ist, außerdem kann jeder im Browser-Verlauf an der URL erkennen, was als Daten übermittelt wurde, und bei einer Passworteingabe ist das nicht so schön.

**Vorteil von GET:**
GET wird benutzt, wenn man einfache Informationen übergeben möchte. Soll zum Beispiel mit dem Klick auf einen Link eine Auswahl übergeben werden, so benutzt man die Methode GET.