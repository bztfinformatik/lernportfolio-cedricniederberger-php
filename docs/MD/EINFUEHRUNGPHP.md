# Einführung PHP

## Erste Schritte

### Prüfen ob PHP läuft

Um zu Überprüfen ob PHP installiert ist, kann man in einer PHP Datei (z.B phpinfo.php) folgendes ausführen:

```php
<?php
phpinfo();
?>
```

Ruft man nun die Seite *phpinfo.php* auf, so sollte falls der Server installiert ist, Informationen über PHP erscheinen.

### PHP Code einbinden

Damit PHP im code eingebunden werden kann so muss zuerst eine Script-umgebung gestartet werden. Dies kann man mit *<?php* machen. Geschlossen wird die umgebung mit *?>*.

So könnte das im Code aussehen:

```html
<!DOCTYPE html>
<html> 
<head>
	<meta charset="UTF-8" />
	<title>Eure erster PHP-Script</title> 
</head>
 
<body>
<h1>Herzlich Willkommen</h1>

<p>Dies ist eure erste PHP-Datei. Eine Scriptumgebung könnt ihr wie folgt starten: 
<?php
echo "Mittels echo können Daten ausgegeben werden";
?></p>

<p>Später könnt ihr in PHP dynamische Inhalte erzeugen. Ein einfaches Beispiel ist das aktuelle Datum auszugeben: 
<?php
echo date("d.m.Y H:i:s");
?></p>
 
</body>
</html>
```


## Text ausgeben per echo

#### Standart Text ausgeben

In PHP kann man per echo text ausgeben lassen.
Hierfür ein Beispiel:

```php
<?php
echo "Hello World";
?>
```

Wird die Datei mit diesem Inhalt nun im Browser geöffnet so wird das *Hello World* oben links angezeigt.

#### Text mit HTML Sonderzeichen ausgeben

Möchte man etwas ausgeben was bestimmte sondezeichen beinhaltet so wird man eine Fehlermeldung erhalten.

Beispiel für möglicher Stolperstein:

```php
<?php
echo "Hello "World"";
?>
```

Damit die **""** nicht als Code verstanden werden so kann man vor den **""** \ verwenden.

Beispiel:

```php
<?php
echo "Hello \"World\"";
?>
```


## Kommentare

#### Einzeilige Kommentare

Um Kommentare zu schreiben kann man entweder mit **//** oder **#** nutzen.

Beispiel:

```php
<?php
echo "Hallo Welt! <br>";
//Dies ist ein Kommentar

#Ein weiterer Kommentar - Ausgabe des Text
echo "Wie ihr feststellt, sind die Kommentare bei der Ausgabe nicht sichtbar.";
?>
```

#### Mehrzeilige Kommentare

Mehrzeilige Kommentare können mit **/\*** geöffnet und mit **\*/** geschlossen werden.

Beispiel:

```php
<?php
/* Die erste Zeile des Kommentars
Zweite Zeile des Kommentars
Die letzte Zeile des Kommentars */
echo "Hallo Welt. Wie ihr feststellt, wird nur dieser Text angezeigt. Die Kommentare vor sind nicht sichtbar.";
?>
```

## Variabeln

Variablen in PHP beginnen immer mit einem Dollarzeichen **$**, direkt gefolgt vom Variablen-Namen.

Beispiel:

```php
2
3
	
<?php
$name = "Cedric Niederberger";
?>
```

Damit man die Variabel abrufen kann, muss man die Variabel am benötigten Ort im Code schreiben.

Beispiel:

```php
<?php
$name = "Cedric Niederberger";
echo "Mein Name ist $name";
?>
```

Ausgabe: *Mein Name ist Cedric Niederberger*


Wenn man einen Text an eine Variabel anhängen will, dann kann man dies mit einem **.** machen.

Beispiel:

```php
<?php
$name = "Cedric ";
$name .= "Niederberger";
echo $name;
?>
```

Ausgabe: *Cedric Niederberger*