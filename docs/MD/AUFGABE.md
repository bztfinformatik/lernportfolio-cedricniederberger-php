# Aufgaben

## Array in Tabelle wiedergeben

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

```html
<form method="post">
    Text: <input type="text" name="text" /><br />
    <input type="Submit" value="Absenden" />
</form>

<?php

echo $_POST["text"];

?>
```