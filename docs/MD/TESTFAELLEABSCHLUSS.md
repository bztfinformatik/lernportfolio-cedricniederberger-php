# Testfälle Abschluss

[Themen](MD/THEMEN.md)

## User-Cases Abschluss

| **Use-Case**                           | **Ist**                                         | **Erfolg**    |
|----------------------------------------|-------------------------------------------------|---------------|
| Gasttabelle anzeigen                   | Gasttabelle wird angezeigt                      | Erfüllt       |
| Archivtabelle anzeigen                 | Archivtabelle wird angezeigt                    | Erfüllt       |
| Navbar funktionier                     | Navbar funktioniert                             | Erfüllt       |
| Detaillierte Informationen ansehen     | Detailansicht eines Gastes kann geöffnet werden | Erfüllt       |
| Gast löschen                           | Gast kann gelöscht werden                       | Erfüllt       |
| Gast editieren                         | Gast kann editiert werden                       | Erfüllt       |
| Gast hinzufügen                        | Gast kan erstellt werden                        | Erfüllt       |
| Feedback bei signifikanten Änderungen  | Nur Warnungen kein Feedback                     | Nicht erfüllt |
| Gast wieder aktivieren                 | Gast kann wieder aktiviert werden               | Erfüllt       |
| Korrekte Validierung der Eingabefelder | Kaum Validierung                                | Nicht erfüllt |
| Abbruch von Erstellung eines Gast      | Erstellen kann abgebrochen werden               | Erfüllt       |


## Testszenarios Abschluss

**Gast hinzufügen**

| **Name**                  | **Soll**                                                     | **Ist**               | **Erfolg**  |
|---------------------------|--------------------------------------------------------------|-----------------------|-------------|
| Ein Gast wird hinzugefügt | Gast wird hinzugefügt nachdem alle angaben eingegeben wurden | Gast wird hinzugefügt | Erfolgreich |


**Gast löschen**

| **Name**               | **Soll**                                                                       | **Ist**                                                       | **Erfolg**  |
|------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------|-------------|
| Ein Gast wird gelöscht | Ein bestimmter Gast sollte durch einen Knopfdruck vom Benutzer gelöscht werden | Gast kann durch Aktionsspalte gelöscht oder archiviert werden | Erfolgreich |


**Gast editieren**

| **Name**               | **Soll**                                                                                                     | **Ist**                          | **Erfolg**  |
|------------------------|--------------------------------------------------------------------------------------------------------------|----------------------------------|-------------|
| Ein Gast wird editiert | Benutzer drückt auf editieren. Die gewüschten Felder können dann editiert und anschliessend bestätigt werden | Benutzer kann den Gast editieren | Erfolgreich |


**Gast Informationen ansehen**

| **Name**                                                        | **Soll**                                                                                    | **Ist**                                                                         | **Erfolg**  |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|-------------|
| Detaillierte Informationen eines Gastes können eingesehen werde | Mehr Informationen eines Gastes können über einen Knopfdruck vom Benutzer eingesehen werden | Benutzer kann über die Aktionsspalte detaillierte Informationen anzeigen lassen | Erfolgreich |


**Gast vom Archiv wiederherstellen**

| **Name**                                                                       | **Soll**                                                                                   | **Ist**                                                                                | **Erfolg**  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|-------------|
| Ein Gast kann vom Archiv zurück zu den aktiven Gästen wiederhergestellt werden | Ein Gast kann vom Benutzer im Archiv zurück zu den aktiven Gästen wiederhergestellt werden | Der Benutzer kann über die Aktionsspalte im Archiv ein inaktiven Gast wiederherstellen | Erfolgreich |