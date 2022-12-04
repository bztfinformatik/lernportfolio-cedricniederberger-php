# Prepared Statements

[Themen](MD/THEMEN.md)

[Quelle](https://www.w3schools.com/php/php_mysql_prepared_statements.asp)

## Was sind Prepared statement

Ein prepared Statement ist grundsätzlich ein feature in form einer Funktion die es ermöglicht gleiche oder ähnliche [SQL Statement](https://www.dataquest.io/blog/sql-commands/) auszuführen. Dies ermöglicht hohe effizienz und weniger Fehlermöglichkeiten.

## Beispiele für Prepared Statements in PDO

**Ein SQL Statement ausführen**

```php
$this->db->query("INSERT INTO `GaesteTabelle` 
        (`vorname`, `nachname`, `mail`, `gastart`, `kartenart`, `eintritt`, `austritt`)
        VALUES (:vorname, :nachname, :mail, :gastart, :kartenart, :eintritt, :austritt)");
```

In diesem Prepared Statement namens **query()** was auch als **prepare()** bekannst ist, wird ein neues Item in den Tabelle *GaesteTabelle* erstellt.

Für die Values also die Daten welcher der neu erstellte Gast erhalten sollte werden Variablen verwendet. Doch wie werden diese Variablen mit Daten verbunden?

**Bind()**

```php
$this->db->bind(':vorname',$data['inputVorname']);
        $this->db->bind(':nachname',$data['inputNachname']);
        $this->db->bind(':mail',$data['inputMail']);
        $this->db->bind(':gastart',$data['inputGastart']);
        $this->db->bind(':kartenart',$data['inputKartenart']);
        $this->db->bind(':eintritt',$data['inputEintritt']);
        $this->db->bind(':austritt',$data['inputAustritt']);
```

Hier werden die oben genannten Variablen mit den Daten gefüllt, welche uns ein Controller zur Verfügung stellt.
Dies tut man vor allem um sogenannte [SQL Injections](https://www.w3schools.com/sql/sql_injection.asp) unmöglich zu machen, denn die funktion **bind()** überprüft die gegebenen Daten.

So sieht **bind()** im Hintergrund aus:

```php
public function bind($param, $value, $type = null)
{
    // Falls der Type nicht mitgegeben wird - überprüfen
    if (is_null($type)) {
        switch (true) {
            case is_int($value):
                $type = PDO::PARAM_INT;
                break;
            case is_bool($value):
                $type = PDO::PARAM_BOOL;
                break;
            case is_null($value):
                $type = PDO::PARAM_NULL;
                break;
            default:
                $type = PDO::PARAM_STR;
        }
    }

    $this->stmt->bindValue($param, $value, $type);
}
```

## Vergleich Prepared Statements und Traditionelle Statements

Wenn Traditionelle Statements verwendet werden, dann wird das Statement nicht validiert. Man schreibt Variablen z.B direkt in das Statement.

**Unterschied**

```php
<?php
// Prepared-Statement

$stmt = $db->prepare("SELECT * FROM GaesteTabelle WHERE id = :id");
$stmt->bindParam(':id', $id);
$stmt->execute();

// Traditionelles Statement

$stmt = $db->query("SELECT * FROM GaesteTabelle WHERE id = $id");

```
