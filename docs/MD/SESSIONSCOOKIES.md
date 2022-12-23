# Sessions & Cookies

[Themen](MD/THEMEN.md)

[Quelle](https://www.php-einfach.de/php-tutorial/php-sessions/)
[Quelle](https://www.php-einfach.de/php-tutorial/cookies/)

## Sessions

### Wo benötigt man Sessions?

In HTTP werden Informationen zwischen verschiedenen aufrufen nicht zwischengespeichert. Da man Oft gewisse Informationen speichern muss z.B Benutzername, E-Mail etc. Damit man dieses Problem lösen kann verwendet man Sessions.

### Wie wird eine Session erstellt?

Jedem Benutzer wird eine einzigartife Session-ID zugeordnet. Sobald sich der Benutzer erneut auf die Webseite zugreift, schickt der Browser die Session-ID an den Webserver weiter, damit dieser vorherige Informationen wiedergeben kann.

Doch wie startet man nun eine Session?

```php
<?php
session_start();
?>
```

Mit eben genannter Funktion kann am Anfang einer PHP Seite eine Session-ID generiert werden

Nun kann man selber noch Werte dieser Session zuteilen. Z.B einen Benutzername:

```php
<?php
$_SESSION['benutzername'] = "user";
?>
```

## Cookies

### Wo benötigt man Cookies?

Cookies haben den gleichen Nutzen wie Sessions nämlich Daten während einer Folge von Aufrufen einer webseite festzuhalten.
Der Unterschied ist dabei, dass Cookies lokal auf dem Gerät des Benutzers gespeichert werden. Man Benutzt sie vorallem um Benutzer nach dem ablaufen einer Session zu identifizieren. Der Benutzer kann Cookies jedoch immer ablehnen.

### Wie wird ein Cookie erstellt?

Ganz oben in einem PHP können wir einen Cookie setzen:

```php
<?php
setcookie("benutzername","Hans",0); 
?>
```

**Was bedeuten die einzelnen Angaben?**

* benutzername: Ist den Name des Cookies über dem der Cookie später erreichbar sein wird.
* Hans: Das ist der Wert welcher im Cookie gespeichert wird.
* 0: Eine Zeitangabe, wenn der Cookie abläuft. 0 bedeutet der Cookie hält solange bis der Benutzer den Browser schliesst.

Um einen Cookie später auszulesen kann man folgenden Code verwenden:

```php
<?php 
$benutzername = $_COOKIE["benutzername"]; 
echo "Der Name ist: $benutzername";
?>
```

## Gästezähler

```php
<?php
session_start();

$momentaneSession = session_id()

setcookie("momentaneSession", $momentaneSession, time());

if(isset($_COOKIE["zähler"])) {

    $anzahl = $_COOKIE["zähler"];
    $anzahl++;
    setcookie("zähler", $anzahl, time());

} else {

    setcookie("zähler",0, time());

}

echo "Momentane Sessions: " . $momentaneSessions;
echo "Cookie Sessions: " . $_COOKIE["momentaneSession"]
echo "Zähler: " . $_COOKIE["zähler"];

?>
```