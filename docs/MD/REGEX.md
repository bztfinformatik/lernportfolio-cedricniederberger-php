# Regex

[Themen](MD/THEMEN.md)

[Quelle](https://en.wikipedia.org/wiki/Regular_expression)
[Quelle](https://www.massiveart.com/blog/regex-zeichenfolgen-die-das-entwickler-leben-erleichtern)

## Was ist Regex?

Regex oder [Regular Expression](https://en.wikipedia.org/wiki/Regular_expression) ist ein **string-search algorithmus**. Mithilfe von diversen ausdrücken die in verschiedenen Formen geschrieben werden können, kann man diverse Zeichenketten, Zahlenfolgen und weiters in langen Texts, Code usw... finden.

## Warum nutzt man Regex?

Regex ist ein sehr effiziente funktion Zahlenfolgen, oder Zeichenketten mit nur wenig Schreiben zu finden. Man kann damit sehr detailliert Zeichenketten finden z.B in einer Datenbank, einem Artikel, in Codes oder Datensammlungen. Regex ist aber nicht ganz einfach zu verwenden.

## Beispiele von Regex

**Folgende Zeichen finden**

´´´regex
[abc]
´´´

**Zeichen in einem bestimmten Alphabet bereich finden**

´´´regex
[a-e]
´´´

**Komplexere Sachen wie E-Mail validiereung**
´´´regex
[A-Za-z0-9\-\_\.\+]{1,64}@[A-Za-z0-9\-\_\.]+\.[a-zA-Z]+
´´´

**Weitere Beispiele**
´´´regex
Unix Pfad: (/([\w_%!$@:.,~-]+|\\.)*)+

Windows Pfad: (?>[A-Za-z]+:|\\)(?:\\[^\\?*]*)+

Hexadezimal: (?<![0-9A-Fa-f])(?:[+-]?(?:0x)?(?:[0-9A-Fa-f]+))

Quoted String: (?>(?<!\\)(?>"(?>\\.|[^\\"]+)+"|""|(?>'(?>\\.|[^\\']+)+')|''|(?>`(?>\\.|[^\\`]+)+`)|``))
´´´

