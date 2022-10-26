# Twig Engine

[Themen](MD/THEMEN.md)

[Quelle 1](https://www.youtube.com/watch?v=6VVN-2SCx7Q)
[Quelle 2](https://github.com/ggelashvili/learnphptherightway-project/blob/3.25/views/invoices/index.twig)
[Quelle 3](https://twig.symfony.com/doc/2.x/intro.html)

## Allgemein

Twig ist eine sogenannte [Template-Engine](https://de.wikipedia.org/wiki/Template-Engine) für PHP.

Grundsätzlich kann man sagen, dass PHP bzw. das [View](MD/MVC.md) bereits ein Template ist und man es als solches Verwenden könnte. Dies bringt aber viele Nachteile mit sich, z.B ist das Programmier des Front-End dadurch schwerer, die Wartung der Applikation komplizierter und in der Regel geht alles einfach etwas länger.

Die Vorteile angegeben von den Twig entwicklern:

- **Schnell**: Twig kompiliert templates und optimiert PHP code. PHP Code wurde zu einem minimum reguliert.

- **Sicher**: Twigs, sandbox mode evaluiert unsicherer template code.

- **Flexibel**: Twig funktioniert mit lexer und parser. Entwickler können dadurch selber tags und filter definieren und eigene DSL kreieren.

Über letzteres habe ich kein Wort verstanden aber gut hört es sich an.

## Warum nutz man Twig

Twig benutzt man um sich die Arbeit etwas zu erleichtern. Man kann damit einfacher Views erstellen und das ohne oder kaum PHP zu programmieren.
Um das darzustellen hier ein Beispiel für ein View mit Twig:

```php
<style>
    table {
        width: 100%;
        border-collapse: collapse;
        text-align: center;
    }
    table tr th, table tr td {
        border: 1px #eee solid;
        padding: 5px;
    }
</style>
<table>
    <thead>
        <tr>
            <th>Invoice Number</th>
            <th>Amount</th>
            <th>Status</th>
            <th>Due Date</th>
        </tr>
    </thead>
    <tbody>
        {% for invoice in invoices %}
            <tr>
                <td>{{ invoice.invoiceNumber }}</td>
                <td>{{ invoice.amount|format_currency('USD') }}</td>
                <td>{{ invoice.status }}</td>
                <td>
                    {{ invoice.dueDate is empty ? 'N/A' : invoice.dueDate|date('m/d/Y') }}
                </td>
            </tr>
        {% else %}
            <tr><td colspan="4">No Invoices Found</td></tr>
        {% endfor %}
    </tbody>
</table>
```

Was man hier sieht, ist ein View geschrieben mit Twig. Es erfüllt grundsätzlich die gleichen Funktionen wie eine PHP / HTML View ist aber um einiges einfacher zu programmieren.

## Twig installieren

Twig wird mit dem PHP composer installiert. Dafür einfach folgenden Command eingeben:

```bash
composer require "twig/twig:^2.0"
```