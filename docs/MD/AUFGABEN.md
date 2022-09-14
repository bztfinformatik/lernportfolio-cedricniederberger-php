# Aufgaben

## Array in Tabelle wiedergeben

## Probleme und gelerntes
Die Aufgabe war relativ einfach und deshalb ware kaum Probleme vorhanden. Ich war mir zuerst unsicher, wie ich die Zahlen in der Tabelle erscheinen lassen möchte da es mehrere möglichkeiten gibt dies zu tun. Ich habe mich mit für die Variante entschieden, einen array als variabel für die einzelnen Zahlen zu verwenden. Der Vorteil davon ist, dass ich die Tabelle ohne probleme ausbauen könnte, sowie Zahlen entfernen und hinzufügen konnte

### Code
```php
<?php

    $zahlen = array(3,7,5,1,8,13,2);

    echo "<table border='1'>";

    echo "<tr><th>Stelle</th><th>Zahl</th></tr>";

    for($a = 0; $a < count($zahlen); $a++){
        echo "<tr><td>$a</td><td>$zahlen[$a]</td></tr>";
    }
    
    echo "</table>"
?>
```

![Tabelle](../img/Screenshot%202022-09-01%20at%2007-50-59%20Screenshot.png)

## Formular eingabe und ausgabe

### Probleme und gelerntes
Die Aufgabe hat mir gezeigt, wie ich eine Formular eingabe ausgeben kann. Die Ausgabe kann man auf einer neuen externen Seite ausgeben oder auf der selben Seite wie das Formular ausgeben. Ich habe mich für die Variante entschieden, dass ich die Ausgabe auf der selben Seite machen lasse. Dies ist etwas einfacher und geht schneller

### Code
```html
<form method="post">
    Text: <input type="text" name="text" /><br />
    <input type="Submit" value="Absenden" />
</form>

<?php

echo $_POST["text"];

?>
```

## Getränke Formular

### Probleme und gelerntes
Durch die Aufgabe konnte ich viel über Formulare in PHP lernen. Auch hier gab es verschiedene Varianten. Ich habe mich entschieden, die Ausgabe auf einer neuen Seite anzeigen zu lassen. Die Eingabe und Ausgabe hat soweit funktioniert.
Probleme hatte ich bei der Ausgabe der gewählten Getränke. Ich wusste nicht wie ich die alles so ausgebe, dass nur angezeigt wird, was auch ausgewählt wurde.

### Code
**Index.html**:
```html
<html>
    <head>
        <title>Getränke Formular</title>
    </head>
    <body>
        <h3>Getraenke</h3>
        <p>Bitte machen Sie folgende Angaben</p>
        <form action="auswertung.php" method="POST">
            <table>
                <tr><td>Anrede:</td><td><label>Herr:</label><input type="radio" name="anrede" value="Herr"><label>Frau:</label><input type="radio" name="anrede" value="Frau"><label>Divers:</label><input type="radio" name="anrede" value=""></td></tr>
                <tr><td>Vorname, Nachname:</td><td><input type="text" name="vorname" placeholder="Vorname"></td><td><input type="text" name="nachname" placeholder="Nachname"></td></tr>
                <tr><td>Adresse:</td><td><input type="text" name="adresse" placeholder="Adresse"></td><td><input type="text" name="plz" placeholder="PLZ"></td></tr>
                <tr><td>E-Mail:</td><td><input type="email" name="email" placeholder="E-Mail"></td></tr>
                
            </table>
            <p>Ihre Getraenkewahl:</p>
            <table>
                <tr><td>Nicht alkoholisch:</td><td><input type="checkbox" name="getraenke" value="nichtalk"></td></tr>
                <tr><td>Schnaps:</td><td><input type="checkbox" name="getraenke" value="schnaps"></td></tr>
                <tr><td>Bier:</td><td><input type="checkbox" name="getraenke" value="bier"></td></tr>
            </table>
            <br>
            <tr><td><input type="submit" name="submit" value="Abschicken"></td>
        </form>
    </body>
</html>
```

**auswertung.php**:
```php
<html>
<head>
<title>Auswertung</title>
</head>
<body style='background-color:pink' >
   <img src="https://c.tenor.com/O_x4UCmt5p0AAAAi/among-us-twerk.gif">
   <img src="https://c.tenor.com/O_x4UCmt5p0AAAAi/among-us-twerk.gif">
   <img src="https://c.tenor.com/O_x4UCmt5p0AAAAi/among-us-twerk.gif">
   <img src="https://c.tenor.com/O_x4UCmt5p0AAAAi/among-us-twerk.gif">
   <br>
	<?php
   $anrede = $_POST["anrede"];
   $vorname = $_POST["vorname"];
   $nachname = $_POST["nachname"];
   $adresse = $_POST["adresse"];
   $plz = $_POST["plz"];
   $email = $_POST["email"];
   
   echo "Sehr geehrte/r $anrede $vorname $nachname";
   echo "<br>";
   echo "<br>";
   echo "Wir haben Ihre Anfrage erhalten. Folgendes haben Sie angegeben:";
   echo "<br>";
   echo "
      <table>
         <tr>
            <td>Name:</td>
            <td>$vorname $nachname</td>
         </tr>
         <tr>
            <td>Adresse:</td>
            <td>$adresse, $plz</td>
         </tr>
         <tr>
            <td>E-Mail:</td>
            <td>$email</td>
         </tr>
         <tr>
            <td>Getraenke:</td>
            <td>Nicht alkoholische<br>Schnaps<br>Bier<br></td>
         </tr>
      </table>
   ";
	?>
   <img src="https://c.tenor.com/O_x4UCmt5p0AAAAi/among-us-twerk.gif">
   <img src="https://c.tenor.com/O_x4UCmt5p0AAAAi/among-us-twerk.gif">
   <img src="https://c.tenor.com/O_x4UCmt5p0AAAAi/among-us-twerk.gif">
   <img src="https://c.tenor.com/O_x4UCmt5p0AAAAi/among-us-twerk.gif">
   <br>
   <img src="https://c.tenor.com/lBoeGrikScQAAAAi/obama-obamium.gif">
   <img src="https://c.tenor.com/lBoeGrikScQAAAAi/obama-obamium.gif">
   <img src="https://c.tenor.com/lBoeGrikScQAAAAi/obama-obamium.gif">
   <img src="https://c.tenor.com/lBoeGrikScQAAAAi/obama-obamium.gif">
</body>
</html>
```