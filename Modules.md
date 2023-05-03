# Python - Modules

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
import numpy as np

print(np.array([1, 2, 3]))   # Ausgabe: [1 2 3]
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
import os

print(os.getcwd())   # Ausgabe: /home/user
```

## Praxis

### Leichte Aufgabe
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

### Schwerere Aufgabe
Schreibe eine Funktion `zufallsliste(n)`, die eine Liste mit `n` Zufallszahlen zwischen 0 und 100 zurückgibt. Verwende das `random`-Modul.

Musterlösung:

```python
import random

import random

def zufallsliste(n):
    return [random.randint(0, 100) for _ in range(n)]

print(zufallsliste(10))