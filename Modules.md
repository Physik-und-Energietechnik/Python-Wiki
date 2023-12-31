
## Einführung

In Python gibt es eine Vielzahl von Funktionen und Methoden, die uns das Leben als Entwickler erleichtern. Aber was, wenn es eine bestimmte Funktion gibt, die Python nicht standardmäßig zur Verfügung stellt? Hier kommen sogenannte "Modules" ins Spiel.

Modules sind praktisch kleine Helferlein, die zusätzliche Funktionalitäten zur Verfügung stellen und uns Entwicklern helfen, unsere Arbeit effektiver zu gestalten. Ein weiterer Vorteil von Modules ist, dass sie uns die Möglichkeit geben, den Code modular aufzubauen und somit strukturiert zu gestalten. 

## Theorie

### Einbinden von Modulen
In Python können wir ein Modul in unserem Code einbinden, indem wir das `import`-Statement verwenden. Wenn wir eine Funktion oder ein Objekt aus einem Modul importieren möchten, können wir auch den Namen der Funktion oder des Objekts angeben.

```python
import math

print(math.sqrt(16))   # Ausgabe: 4.0
```

Alternativ können wir auch ein Modul mit einem Alias importieren, indem wir dem Modulnamen ein Alias mit dem `as`-Keyword zuweisen. Dies kann hilfreich sein, wenn wir ein langes Modul mit einem kurzen Alias verwenden möchten.

```python
import math as m

print(m.pi)  # 3.141592653589793
print(m.sqrt(4))  # 2.0
```

### Eigene Module erstellen
Wir haben auch die Möglichkeit, unsere eigenen Module zu erstellen. Hierfür können wir einfach eine neue Datei mit dem gewünschten Modulnamen erstellen und unsere Funktionen oder Klassen definieren. Um das Modul in unserem Code zu verwenden, müssen wir es einfach nur importieren.

```python
# Beispielmodul: hallo.py

def sag_hallo(name):
    print("Hallo, " + name + "!")

# main.py

import hallo

hallo.sag_hallo("Max")   # Ausgabe: Hallo, Max!
```

### Standardmodule
Python verfügt über viele Standardmodule, die häufig verwendete Funktionalitäten enthalten. Hier sind einige Beispiele:

- `os`: Funktionen zum Arbeiten mit dem Betriebssystem
- `datetime`: Funktionen zum Arbeiten mit Datum und Uhrzeit
- `random`: Funktionen zur Erzeugung von Zufallszahlen
- `re`: Funktionen zum Arbeiten mit regulären Ausdrücken

```python
import random

# Generiere eine zufällige Ganzzahl zwischen 1 und 10 (inklusive)
zahl = random.randint(1, 10)

# Gebe die generierte Zahl aus
print("Die zufällige Zahl ist:", zahl)
```

## Praxis

### Aufgabe 1
Schreibe eine Funktion `addiere_zahlen(x, y)`, die zwei Zahlen addiert. Importiere diese Funktion in einem anderen Python-Script und verwende sie.

Musterlösung:

```python
# modul.py

def addiere_zahlen(x, y):
    return x + y

# main.py

from modul import addiere_zahlen

ergebnis = addiere_zahlen(3, 5)
print(ergebnis)   # Ausgabe: 8
```

In der Musterlösung wurde die Funktion `addiere_zahlen(x, y)` in einem Modul `modul.py` definiert. Die Funktion nimmt zwei Parameter x und y und gibt die Summe zurück. 

Dann wird in einem anderen Python-Skript, `main.py`, die Funktion `addiere_zahlen` aus dem Modul `modul.py` importiert. Dies geschieht durch die Zeile `from modul import addiere_zahlen`. Dadurch ist die Funktion `addiere_zahlen` im Skript `main.py` verfügbar.

Anschließend wird die Funktion `addiere_zahlen` mit den Argumenten 3 und 5 aufgerufen und das Ergebnis in der Variablen `ergebnis` gespeichert. Schließlich wird das Ergebnis mit der `print`-Funktion auf der Konsole ausgegeben.

### Aufgabe 2
Schreibe eine Funktion `zufallsliste(n)`, die eine Liste mit `n` Zufallszahlen zwischen 0 und 100 zurückgibt. Verwende das `random`-Modul.

Musterlösung:

```python

import random

def zufallsliste(n):
    return [random.randint(0, 100) for _ in range(n)]

print(zufallsliste(10))
```

Die Musterlösung importiert zunächst das `random`-Modul, um zufällige Zahlen zu generieren.

Dann definiert die Funktion `zufallsliste(n)` mit dem Parameter `n`. Innerhalb der Funktion wird eine List Comprehension verwendet, um eine Liste von n Zufallszahlen zwischen 0 und 100 zu erzeugen. 

`random.randint(0, 100)` gibt eine zufällige Ganzzahl zwischen 0 und 100 zurück, und `range(n)` erzeugt eine Liste von `n` Elementen, wobei jedes Element eine zufällige Zahl zwischen 0 und 100 ist.

Die Funktion gibt diese Liste von Zufallszahlen zurück.

Zuletzt wird die Funktion mit dem Argument 10 aufgerufen und das Ergebnis mit der `print`-Funktion auf der Konsole ausgegeben.

## Fazit

Herzlichen Glückwunsch! Du hast erfolgreich die Grundlagen von Python-Modulen erlernt und gelernt, wie man Standardmodule und eigene Module erstellt. Durch das Importieren von Modulen können wir unseren Code strukturieren und zusätzliche Funktionalitäten nutzen, die Python standardmäßig nicht bietet. 

Denk daran, dass es eine Vielzahl von Standardmodulen in Python gibt, die dir die Arbeit erleichtern können. Es gibt jedoch auch viele Drittmodule, die du installieren und nutzen kannst, um noch komplexere Aufgaben zu lösen.

## Links / Weiteres Material

- [W3Schools Python Module Tutorial](https://www.w3schools.com/python/python_modules.asp)
- [Python Standard Library](https://docs.python.org/3/library/index.html)