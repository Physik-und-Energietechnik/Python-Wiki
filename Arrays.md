## Einführung

Hey ihr Python-Neulinge! Heute werfen wir einen Blick auf ein spannendes Thema - Arrays in Python. Aber Moment mal, was ist eigentlich ein Array und warum ist es wichtig, das zu lernen?

Ein Array ist eine Art von Datenstruktur, die es dir ermöglicht, mehrere Werte in einer einzigen Variablen zu speichern. Das macht Arrays besonders nützlich, wenn du mit einer Liste von Werten arbeiten möchtest, wie zum Beispiel einer Liste von Zahlen, Wörtern oder anderen Daten. Mit Arrays kannst du Daten effizient organisieren und auf sie zugreifen, was dir bei vielen Aufgaben in der Programmierung helfen kann.

In diesem Tutorial werden wir uns anschauen, wie man Arrays in Python erstellt, darauf zugreift und sie manipuliert. Du wirst lernen, wie man Arrays deklariert, Werte in Arrays speichert und aus Arrays liest. Aber keine Sorge, wir werden es in einfachen Worten erklären und mit humorvollen Beispielen arbeiten, um sicherzustellen, dass ihr alle Spaß beim Lernen habt!

## Theorie

### Array-Deklaration

Um ein Array in Python zu erstellen, musst du es zuerst deklarieren. Die Syntax dafür ist ziemlich einfach:

```python
mein_array = []
```

Hier haben wir ein leeres Array mit dem Namen `mein_array` erstellt. Du kannst auch ein Array mit vordefinierten Werten erstellen:

```python
mein_array = [1, 2, 3, 4, 5]
```

Du kannst jeden Datentyp in einem Array speichern, sei es Zahlen, Strings oder andere Objekte.

### Array-Zugriff

Sobald du ein Array erstellt hast, kannst du auf die einzelnen Werte zugreifen. Das erfolgt mit Hilfe von Indexen, die die Positionen der Werte im Array angeben. Hier ein Beispiel:

```python
mein_array = [1, 2, 3, 4, 5]
erster_wert = mein_array[0]
print(erster_wert)
```

In diesem Beispiel greifen wir auf den ersten Wert im Array `mein_array` zu, indem wir den Index 0 verwenden. Beachte, dass in Python die Indexierung bei 0 beginnt, also ist der erste Wert an Position 0, der zweite an Position 1 und so weiter.

### Array-Manipulation

Du kannst auch Werte in einem Array ändern, indem du einfach den Wert an einem bestimmten Index zuweist. Hier ein Beispiel:

```python
mein_array = [1, 2, 3, 4, 5]
mein_array[2] = 42
print(mein_array)
```

In diesem Beispiel ändern wir den Wert an Index 2 in `mein_array` von 3 auf 42.

Es gibt auch viele eingebaute Funktionen in Python, die dir helfen, Arrays zu manipulieren, wie zum Beispiel `append()`, `pop()`, `remove()` und viele mehr. Du kannst sie verwenden, um Arrays zu erweitern, Elemente aus Arrays zu entfernen oder nach bestimmten Werten in Arrays zu suchen.
Hier sind einige wichtige Array-Manipulationsfunktionen:

- `append(element)`: Fügt `element` am Ende des Arrays hinzu. Beispiel: `mein_array.append(42)` fügt die Zahl 42 am Ende von `mein_array` an.

- `pop(index)`: Entfernt das Element an Position `index` aus dem Array und gibt es zurück. Beispiel: `letztes_element = mein_array.pop()` entfernt das letzte Element aus `mein_array` und gibt es zurück.

- `remove(element)`: Entfernt das erste Vorkommen von `element` aus dem Array. Beispiel: `mein_array.remove(42)` entfernt die Zahl 42 aus `mein_array`.

- `len()`: Gibt die Anzahl der Elemente im Array zurück. Beispiel: `array_laenge = len(mein_array)` speichert die Länge von `mein_array` in der Variablen `array_laenge`.

Diese Funktionen sind sehr nützlich, wenn es darum geht, Arrays zu manipulieren und auf sie zuzugreifen.

## Aufgabe 1

Okay, jetzt seid ihr dran! Hier ist eine Aufgabe für euch, um euer Wissen über Arrays in Python zu überprüfen:

Gegeben ist ein Array mit den Werten `[10, 20, 30, 40, 50]`. Deine Aufgabe ist es, den Wert an Index 2 im Array zu ändern und anschließend den aktualisierten Array auszugeben.

```python
# Gegebenes Array
mein_array = [10, 20, 30, 40, 50]

# Wert an Index 2 ändern
mein_array[2] = 35

# Aktualisierten Array ausgeben
print(mein_array)
```

Musterlösung:

```python
# Aktualisierter Array
[10, 20, 35, 40, 50]
```

Herzlichen Glückwunsch! Du hast erfolgreich den Wert im Array geändert. Probiere jetzt mit verschiedenen Arrays herum und nutze die verschiedenen Array-Manipulationsfunktionen, um dein Verständnis weiter zu vertiefen.

## Aufgabe 2

Hier ist eine etwas anspruchsvollere Aufgabe:

Gegeben ist ein Array von Zahlen. Schreibe eine Funktion `filtern(arr)`, die das Array als Eingabe erhält und eine neue Liste zurückgibt, die nur die geraden Zahlen aus dem ursprünglichen Array enthält.

Beispiel:

```python
# Gegebenes Array
mein_array = [3, 7, 8, 12, 15, 21, 24, 31, 36]

# Funktion zum Filtern der geraden Zahlen
def filtern(arr):
    # Code hier einfügen
    return ergebnis

# Ergebnis ausgeben
ergebnis = filtern(mein_array)
print(ergebnis)
```

Die Ausgabe sollte sein:

```
[8, 12, 24, 36]
```

Musterlösung:

```python
# Gegebenes Array
mein_array = [3, 7, 8, 12, 15, 21, 24, 31, 36]

# Funktion zum Filtern der geraden Zahlen
def filtern(arr):
    ergebnis = []
    for zahl in arr:
        if zahl % 2 == 0:
            ergebnis.append(zahl)
    return ergebnis

# Ergebnis ausgeben
ergebnis = filtern(mein_array)
print(ergebnis)
```

Die Funktion geht das Array durch und fügt jede gerade Zahl in eine neue Liste `ergebnis` ein. Diese Liste wird schließlich von der Funktion zurückgegeben und gedruckt.

Herzlichen Glückwunsch! Du hast erfolgreich eine Funktion geschrieben, die bestimmte Elemente aus einem Array filtert. Mit dieser Funktion kannst du zukünftige Programmieraufgaben effizienter lösen.

Wir hoffen, dass du Spaß hattest, während du diese Aufgabe durchgegangen bist. Probiere jetzt mit verschiedenen Arrays und Filterbedingungen herum, um dein Verständnis weiter zu vertiefen.

Das war's! Du hast jetzt eine grundlegende Vorstellung von Arrays in Python. Du kennst die Syntax zur Array-Deklaration, den Array-Zugriff und die Array-Manipulation. Jetzt kannst du diese mächtige Datenstruktur nutzen, um deine Python-Programme noch leistungsfähiger zu gestalten.

Wir hoffen, dass du Spaß hattest, während du dieses Tutorial durchgegangen bist. Python kann manchmal wie ein Zoo aussehen, aber keine Sorge, mit etwas Übung wirst du bald zum Python-Profi. Viel Erfolg beim Experimentieren mit Arrays in Python!