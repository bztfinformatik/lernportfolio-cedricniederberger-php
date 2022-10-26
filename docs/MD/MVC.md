# MVC

[Themen](MD/THEMEN.md)

[Quelle](https://developer.mozilla.org/en-US/docs/Glossary/MVC#:~:text=MVC%20(Model%2DView%2DController,of%20labor%20and%20improved%20maintenance.)

## Allgemein

MVC oder auch *Model-View-Controller* ist ein pattern welches oft im Software design bereich verwendet wird. Mit MVC werden Benutzerinterfaces, daten und die logik in den Code inplementiert. Grundsätzlich versucht man die drei Elemente Model, View und Controller zu seperieren damit im nachhinein einfach gearbeitet werden kann sowie der Code später einfach modifiziert und gewartet werden kann. Wie eben genannt besteht das design pattern aus 3 Elementen:

1. Model
2. View
3. Controller

## Beispiel eines MVC

![](../img/mvc.png)

Im obigen Diagramm sieht man den Logischen aufbau eines MVC pattern. Die Pfeile beschreiben wie die MVC Elemente zusammen interagieren und wie der Ablauf einer einfachen Anfrage innerhalb des MVCs funktioniert.

### View

Die View beschreibt welche Daten angezeigt werden sollten.
Es wird definiert wie z.B Listen beim User angezeigt werden sollten.

Der View ist grundsätzlich immer der Anfang oder das Ende einer MVC Anfrage.

### Controller

Der Controller enthält die Logik welches das Model oder View auf anfrage des Benutzers hin updated.

Wenn man z.B einen Button hat welcher Elemente auf der Webseite hinzufügen und entfernen kann,dann manipuliert dies Aktion das Model.Damit das manipulieren des Models aber möglich ist brauch wir einen controller welcher die inputs des Benutzers entgegenimmt, das Model manipuliert und anschliessend auch das View überarbeitet.

Man kann sich den Controller wie als Mittelmann zwischen Model und View vorstellen.

### Model

Das Model definiert welche daten die Applikation enthalten sollte. Das Model kann eine Datenbank sein. Wenn die Datenbank ein Element erhählt oder verliert, dann wird diese Information an das View weitergeleitet welches dass das Element entfernt oder hinzufügt.
