# Python - Syntax, Comments

## Titel
In diesem Abschnitt geht es um die Syntax von Python und um die Verwendung von Kommentaren.

## Einführung
Python ist eine Programmiersprache, die sehr lesbar und intuitiv ist. Die Syntax von Python ist vergleichsweise einfach zu lernen und zu verstehen. In diesem Abschnitt lernst du die Grundlagen der Python-Syntax und wie du Kommentare in deinem Code verwenden kannst.

## Theorie
### Python-Syntax
Die Syntax von Python definiert die Regeln und Strukturen, die in Python-Code verwendet werden. Ein Beispiel für Python-Syntax ist das Einrücken von Codeblöcken. In Python wird Einrückung verwendet, um Codeblöcke zu definieren. Ein Codeblock wird durch das Einrücken von Code innerhalb von Schleifen, Bedingungen oder Funktionen gebildet. 

#### Allgemeines Code-Beispiel:
```
if x > 0:
    print("x ist größer als 0")
else:
    print("x ist kleiner als oder gleich 0")
```

#### Explizites Code-Beispiel direkt in Python:
```python
if x > 0:
    print("x ist größer als 0")
else:
    print("x ist kleiner als oder gleich 0")
```

### Kommentare
Kommentare sind Texte, die im Code stehen, um den Zweck und die Funktionsweise des Codes zu beschreiben. In Python werden Kommentare mit dem Symbol `#` am Anfang der Zeile eingeführt. Python ignoriert alles nach dem `#`-Symbol. Kommentare sind nützlich, um deinen Code zu dokumentieren und anderen zu helfen, ihn zu verstehen.

#### Allgemeines Code-Beispiel:
```
# Dies ist ein Kommentar
print("Hallo Welt") # Dies ist auch ein Kommentar
```

#### Explizites Code-Beispiel direkt in Python:
```python
# Dies ist ein Kommentar
print("Hallo Welt") # Dies ist auch ein Kommentar
```

## Praxis
### Aufgabe 1
Schreibe ein Programm, das die Summe der Zahlen von 1 bis 10 berechnet und das Ergebnis ausgibt. Verwende Kommentare, um deinen Code zu dokumentieren.

#### Musterlösung
```python
# Berechne die Summe der Zahlen von 1 bis 10
summe = 0
for zahl in range(1, 11):
    summe += zahl
# Gib das Ergebnis aus
print("Die Summe der Zahlen von 1 bis 10 ist:", summe)
```

### Aufgabe 2
Schreibe ein Programm, das eine Liste von Zahlen sortiert. Verwende Kommentare, um deinen Code zu dokumentieren.

#### Musterlösung
```python
# Definiere eine Liste von Zahlen
zahlen = [3, 6, 1, 8, 2, 10, 5]
# Sortiere die Liste
zahlen.sort()
# Gib die sortierte Liste aus
print("Die sortierte Liste lautet:", zahlen)
```