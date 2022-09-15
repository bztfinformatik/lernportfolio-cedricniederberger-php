# Objektorientierung in PHP

[Themen](MD/THEMEN.md)

[Quelle](https://www.php-einfach.de/experte/objektorientierte-programmierung-oop/)

## Einstieg

Objektorientierte Programmierung (OOP) ist ein Modell der Computerprogrammierung, bei dem das Softwaredesign auf Daten oder Objekten basiert und nicht auf Funktionen und Logik. Ein Objekt kann als ein Datenfeld definiert werden, das eindeutige Attribute und Verhaltensweisen aufweist.

OOP konzentriert sich auf die Objekte, die Entwickler bearbeiten wollen, und nicht auf die Logik, die zu ihrer Bearbeitung erforderlich ist. Dieser Programmieransatz eignet sich gut für Programme, die umfangreich und komplex sind und aktiv aktualisiert oder gepflegt werden. Dazu gehören Programme für die Fertigung und Konstruktion sowie mobile Anwendungen. Objektorientierte Programmierung kann beispielsweise für Simulationssoftware für Fertigungssysteme verwendet werden.

## Wie wird in PHP instanziert?

Wenn eine einfach Klasse erstellt wird kann man diese folgendermassen instanziieren:

```php
$meinObjekt = new MeineKlasse();
```

Man definiert ein neues Objekt, in unserem Fall **$meinObjek** und instanziieren dieses Objekt von einer Klasse z.B **MeineKlasse()**

In einem erweiterten Beispiel kann man nun noch Methoden in der Klasse **MeineKlasse()** definieren und diese anschliessend mit dem Objekt **$meinObjekt** ausgeben:

```php
<?php
 
class MeineKlasse
{
    public $gib_laut = 'Hallo Welt';
}
 
$meinObjekt = new MeineKlasse();
 
echo $meinObjekt->gib_laut;
 
?>
```

**Augabe:** Hallo Welt

## Was bedeutet der Pfeil?

Wenn man eine Methode ausgibt dann verwendet man folgenden Pfeil:

```php
echo $meinObjekt->gib_laut;
```

Der Pfeil zeigt auf eine Funktion oder Methode.
Der Pfeil kann auch in verwendung mit **$this** verwendet werden.

```php
<?php
//Definition der Klasse User
class User {
    public $email;
    $this->email = $newEmail;
}
?>
```

Grundsätzlich kann man sich den Pfeil **->** wie der **.** in Java vorstellen:

* Statt **this.name** ist **$this->name**
* Statt **meinObjekt.methode** ist **$meinObjekt->methode**

## Was bedeutet $this?

**$this** hat die gleiche funktionalität wie **this** in java. Das bedeutet, wenn auf eine Variabel ausserhalb einer Funktion zugreifen möchte,  dann wird mit **\$this** vor der Variabel den zugriff auf die äussere Variabel durchgeführt.

Dies könnte so aussehen:

```php
<?php
//Definition der Klasse User
class User {
    //Definition der Eigenschaften name, email und password
    public $name;
    public $email;
    public $password;

    //Definition der Methode setEmail
    function setEmail($newEmail) {
        if(filter_var($newEmail, FILTER_VALIDATE_EMAIL) !== false) {
            $this->email = $newEmail;
            return true;
        }
        return false; //Neue E-Mail-Adresse konnte nicht gespeichert werden, da diese ungültig war
    }
    }
?>
```

## Syntax Methoden, Konstruktoren

### Methoden

Der Syntax einer Methode sieht so aus:

```php
<?php
class User {
 function methode1() { //Public Methode ohne Parameter 
 }
 
 public function methode2($parmater) { //Public Methode mit Paramter
 }
 
 protected function methode2($parmater1, $parameter2) { //Protected Methode mit zwei Paramtern
 }
 
 private function methode3() { //Private Methode ohne Paramter
 }
}
?>
```

Möchte man andere Klassenmethoden innerhalb der Klasse aufrufen, so muss man entsprechend **$this->nameDerMethode()** schreiben. Bei Objekten, d.h. bei konkreten Instanzen einer Klasse, muss man entsprechend **\$nameDesObjects->nameDerMethode()** schreiben.

### Konstruktoren

Der Syntax eines Konstruktors sieht so aus:

```php
<?php
class User {
    public $erstellungsdatum;
    public $name;
    public $email;

    public function __construct() {
        $this->erstellungsdatum = date("d.m.Y H:i:s");
    }
}

$max = new User();
$max->name = "Max Mustermann";
echo "Das Objekt von $max->name wurde erstellt am $max->erstellungsdatum";
?>
```

Methode **__construct()**  wird aufgerufen, sobald ein Objekt der Klasse erzeugt wird.

Sobald man hier **new User();** ausführt, wird die Methode **__construct()**  ausgeführt, welche in diesem Fall das Erstellungsdatum in der Klasseneigenschaft **$erstellungsdatum** hinterlegt.

Man kann auch Parameter spezifizieren:

```php
<?php
class User {
    public $erstellungsdatum;
    public $name;
    public $email;

    public function __construct($name, $email = "") {
        $this->name = $name;
        $this->email = $email;
        $this->erstellungsdatum = date("d.m.Y H:i:s");
    }
}

$max = new User("Max Mustermann", "max@muster.de");
echo "Das Objekt von $max->name wurde erstellt am $max->erstellungsdatum";
?>
```

Hier haben wir zwei Parameter für den Konstruktor spezifiziert. Den verpflichtenden Parameter $name und den optionalen Parameter **$email**.

Möchte man nun neue **User-Objekte** erstellen, so muss man entweder **new User("Name");**  oder **new User("Name", "Email");** ausführen.
