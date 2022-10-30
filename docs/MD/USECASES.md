# Use-Cases und Anforderungen


## Alle Use-Cases

| Use-Case | Beschreibung |
|----------|--------------|
| Gasttabelle anzeigen | Die Tabelle mit allen aktive  Gäste wird angezigt |
| Archivtabelle anzeigen | Die Tabelle im Archiv wird angezeigt |
| Navbar funktionier | Navigieren über die Navbar möglich |
| Detaillierte Informationen ansehen | Die Detaillierten Informationen von einem Gast sind über einen Knopf einsehbar |
| Gast löschen | Ein Gast kann über einen Knopf gelöscht werden |
| Gast editieren | Gastinformationen können über einen Knopf editiert werden |
| Gast hinzufügen | Gast kann über einen Knopf hinzugefügt werden |
| Feedback bei signifikanten Änderungen | Feedback an User wenn etwas geändert / erstelltg wurde |
| Gast wieder aktivieren | Gelöschter Gast von Archiv wieder aktiv setzen |
| Korrekte Validierung der Eingabefelder | Alle angabedaten werden Korrekt validiert |
| Abbruch von Erstellung eines Gast | Erstellen eines Gastes kann abgebrochen werden |

## Anforderungen der Use-Cases

**Gasttabelle anzeigen**
- Aktiver Testgast wird in der Tabelle angezeigt
- Deaktivierter Testgast wird nicht in der Tabelle angezeigt
- Tabelleninformationen von Testgast werden korrekt angezeigt
- Button: Editieren und Details Anzeigen werden in Tabelle angezeigt

**Archivtabelle anzeigen**
- Aktiver Testgast wird in der Tabelle angezeigt
- Deaktivierter Testgast wird in der Tabelle angezeigt
- Tabelleninformationen von Testgast werden korrekt angezeigt
- Button: Editieren und Details Anzeigen werden in Tabelle angezeigt

**Navbar funktioniert**
- Beim Betätigen von Personen kommt die Seite mit aktiven Gästen
- Beim Betätigen von Archiv kommt die Seite mit aktiven und inaktiven Gästen
- Hintergrund des Button in der Navbar wird bei Nutzung geändert

**Detaillierte Informationen ansehen**
- Beim Knopf "detaillierte Informationen" öffnet sich Fenster "detaillierte Informationen"
- Beim Knopf "detaillierte Informationen" öffnet sich Fenster mit allen Informationen des Benutzers
- Fenster kann wieder geschlossen werden
- Informationen sind vollständig
- Nur Informationen anzeigen, die der Gast-Typ aktiv hat

**Gast löschen**
- Aktiver Testgast kann in Gast-Tabelle gelöscht werden
- Aktiver Testgast wird bei löschung aus Gast-Tabelle entfernt, bleibt aber im Archiv
- Testgast kann im Archiv gelöscht werden
- Deaktivierter Testgast welcher im Archiv gelöscht wird, wird komplett gelöscht

**Gast editieren**
- Bei betätigen des Knopfes "Editieren" bei Testgast öffnet sich ein neues Fenster
- Bei betätigen des Knopfes "Editieren" bei Testgast öffnet sich ein neues Fenster mit Eingabe Felder
- Beim wählen des Eingabefeld "Gasttyp" ändern sich die Eingabefelder je nach geforderten Informationen
- Pflichtfelder werden rot und zeigen einen Fehler, wenn sie einen ungültigen Datensatz beinhalten
- Fenster kann geschlossen werden, was gleichzeitig zum Abbruch führt
- Editieren kann abbgebrochen werden, was gleichzeitig zum schliessen des Fenster führt
- Editieren kann abgeschlossen werden -> Änderungen werden beim Testgast übernommen

**Gast hinzufügen**
- Bei betätigen des Knopfes "hinzufügen" öffnet sich ein Fenster
- Bei betätigen des Knopfes "hinzufügen" öffnet sich ein Fenster mit Eingabefelder
- Beim wählen des Eingabefeld "Gasttyp" ändern sich die Eingabefelder je nach geforderten Informationen
- Pflichtfelder werden rot und zeigen einen Fehler, wenn sie einen ungültigen Datensatz beinhalten
- Fenster kann geschlossen werden, was gleichzeitig zum Abbruch führt
- Editieren kann abbgebrochen werden, was gleichzeitig zum schliessen des Fenster führt
- Neue Testgast wird anschliessend in Tabelle Gast-Tabelle und Archiv-Tabelle angezeigt
- Informationen stimmen mit den eigebenen Informationen überein

**Feedback bei signifikanten Änderungen**
- Alert bei Testgast hinzufügen
- Alert bei Aktion abbrechen
- Alert bei Testgast löschen
- Alert bei Testgast editierung
- Alert bei Testgast reaktivierung 

**Gast wieder aktivieren**
- Inaktiver Testgast in Archiv kann mit Knopf reaktiviert werden
- Reaktivierter Testgast wird in Gast-Tabelle angezeigt
- Reaktivierter Testgast informationen stimmen mit den alten Informationen vor der reaktivierung überein

**Korrekte Validierung der Eingabefelder**
- Alle Eingabefelder werden validiert
- Eingabefelder mit ungültiger Eingabe werden einen Fehler angezeigt bekommen
- Eingabefelder mit ungültiger Eingabe werden rot
- Testgast kann erst mit gültiger Validierung hinzugefügt werden

**Abbruch von Erstellung eines Gast**
- Bei Erstellung des Testgast kann man mit einem Knopf den Vorgang abbrechen
- Bei Abbruch schliesst sich das Fenster
- Fenster kann auch geschlossen werden um den Vorgang abbzubrechen
- Der Benutzer wird bei abbruch nicht erstellt

## Testszenarios

**Gast hinzufügen**


| Name | Gast hinzufügen |
|----------------------|-----------------|
| Ziel im Kontext      | Ein Gast wird hinzugefügt |
| Akteure              | Benutzer, Gast |
| Trigger              | Benutzer drückt den Hinzufügen Knopf |
| Essenzielle Schritte | 1. Benutzer drückt den Hinzufügen Knopf 2. Benutzerwählt den Gasttyp aus 3. Benutzer füllt die Felder mit korrekten angaben 4. Benutzer drückt den Bestätigungsknopf |

**Gast löschen**
| Name                 | Gast löschen |
|----------------------|--------------|
| Ziel im Kontext      | Ein Gast wird gelöscht |
| Akteure              | Benutzer, Gast |
| Trigger              | Benutzer drückt den löschen Knopf |
| Essenzielle Schritte | 1. Benutzer drückt den löschen Knopf 2. Benutzerwählt den Gast aus 4. Benutzer bestätigt die Aktion |

**Gast editieren**
| Name                 | Gast editieren |
|----------------------|----------------|
| Ziel im Kontext      | Ein Gast wird editiert |
| Akteure              | Benutzer, Gast |
| Trigger              | Benutzer drückt den editieren Knopf |
| Essenzielle Schritte | 1. Benutzer drückt den editieren Knopf 2. Benutzer ändert die gewünschten Felder 4. Benutzer drückt den bestätigen Knopf |

**Gast Informationen ansehen**
| Name                 | Gastinformationen ansehen |
|----------------------|------------------------|
| Ziel im Kontext | Detaillierte Informationen eines Gastes können eingesehen werde |
| Akteure              | Benutzer, Gast |
| Trigger              | Benutzer drückt den detaillierte Informationen Knopf |
| Essenzielle Schritte | 1. Benutzer drückt auf den detaillierte Informationen Knopf 2. Benutzer schaut sich die gewünschten Informationen an 3. Benutzer schliesst das Fenster |

**Gast vom Archiv wiederherstellen**
| Name  | Archiv Gast wiederherstellen |
|-------|---------------|
| Ziel im Kontext      | Ein Gast kann vom Archiv zurück zu den aktiven Gästen wiederhergestellt werden |
| Akteure | Benutzer, Gast |
| Trigger | Benutzer drückt im Archiv auf den wiederherstellen Knopf |
| Essenzielle Schritte | 1. Benutzer drückt auf den Gast wiederherstellen Knopf im Archiv 2. Benutzer bestätigt die Aktion 3. Benutzer Überprüft, ob Gast wiederhergestellt wurde |