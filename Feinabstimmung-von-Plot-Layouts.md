# Matplotlib - Feinabstimmung von Plot Layouts

## Einführung

Willkommen zu unserem Python-Tutorial über die Feinabstimmung von Plot Layouts mit Matplotlib! In diesem Tutorial werden wir uns damit beschäftigen, wie wir unsere Diagramme und Plots in Python so gestalten können, dass sie nicht nur informativ, sondern auch ästhetisch ansprechend sind. Wir werden lernen, wie wir die Größe, den Abstand und die Positionierung von Diagrammelementen anpassen können, um professionell aussehende Grafiken zu erstellen.

Nachdem du dieses Tutorial durchgearbeitet hast, wirst du in der Lage sein, deine eigenen maßgeschneiderten Diagramme zu erstellen und diese in deinen Projekten einzusetzen. Egal, ob du Daten visualisieren möchtest, um Erkenntnisse zu gewinnen oder einfach nur beeindruckende Grafiken erstellen möchtest, dieses Tutorial wird dir helfen, die Grundlagen zu verstehen und deine Python-Fähigkeiten zu erweitern.

## Theorie

### Layout-Anpassungen

Die Feinabstimmung des Layouts umfasst verschiedene Aspekte, wie die Größe des Diagramms, den Abstand zwischen den Achsen und die Positionierung von Achsentiteln und Legenden. Matplotlib bietet eine Reihe von Funktionen und Eigenschaften, mit denen wir diese Anpassungen vornehmen können.

#### Größe des Diagramms

Die Größe des Diagramms ist wichtig, um sicherzustellen, dass unsere Grafiken auf dem Bildschirm oder in gedruckter Form gut lesbar sind. Wir können die Größe des Diagramms mithilfe der `figure`-Funktion von Matplotlib festlegen. Hier ist ein allgemeines Beispiel, das dir zeigt, wie du die Größe eines Diagramms festlegen kannst:

```python
import matplotlib.pyplot as plt

# Diagrammgröße festlegen
plt.figure(figsize=(8, 6))

# Diagramm erstellen
# ...
```

Und hier ist ein spezifisches Beispiel, um die Größe eines Diagramms auf 8 Zoll Breite und 6 Zoll Höhe festzulegen:

```python
import matplotlib.pyplot as plt

# Diagrammgröße festlegen
plt.figure(figsize=(8, 6))

# Diagramm erstellen
# ...
```

#### Abstandsanpassungen

Der Abstand zwischen den Achsen und den Rändern des Diagramms kann die Lesbarkeit und das Erscheinungsbild unserer Grafiken verbessern. Matplotlib ermöglicht es uns, den Abstand mit der `subplots_adjust`-Funktion anzupassen. Hier ist ein allgemeines Beispiel für die Anpassung des Abstands:

```python
import matplotlib.pyplot as plt

# Diagramm erstellen
fig, ax = plt.subplots()

# Abstand anpassen
plt.subplots_adjust(left=0.1, right=0.9, top=0.9, bottom=0.1)

# Daten plotten
# ...
```

#### Positionierung von Achsentiteln und Legenden

Die Positionierung von Achsentiteln und Legenden kann dazu beitragen, dass unsere Grafiken besser lesbar sind und die Informationen klarer vermitteln. Mit Matplotlib können wir die Position von Achsentiteln und Legenden mithilfe der entsprechenden Funktionen anpassen. Hier ist ein allgemeines Beispiel für die Positionierung von Achsentiteln und Legenden:

```python
import matplotlib.pyplot as plt

# Diagramm erstellen


fig, ax = plt.subplots()

# Achsentitel hinzufügen
ax.set_xlabel('X-Achse')
ax.set_ylabel('Y-Achse')

# Legende hinzufügen
ax.legend()

# Daten plotten
# ...
```

## Praxis

### Aufgabe 1

Deine erste Aufgabe besteht darin, ein einfaches Liniendiagramm zu erstellen, das die Funktion y = x^2 darstellt. Verwende die Informationen aus dem Theorieabschnitt, um das Layout des Diagramms anzupassen und sicherzustellen, dass die Achsentitel gut lesbar sind.

Hier ist ein Musterlösungscode, den du verwenden kannst:

```python
import matplotlib.pyplot as plt
import numpy as np

# Daten generieren
x = np.linspace(0, 10, 100)
y = x ** 2

# Diagrammgröße festlegen
plt.figure(figsize=(8, 6))

# Diagramm erstellen
plt.plot(x, y)

# Achsentitel hinzufügen
plt.xlabel('X-Achse')
plt.ylabel('Y-Achse')

# Daten plotten
plt.show()
```

### Aufgabe 2

Deine zweite Aufgabe besteht darin, ein gestapeltes Balkendiagramm zu erstellen, das die Umsatzverteilung verschiedener Produkte zeigt. Passe das Layout des Diagramms an, indem du den Abstand zwischen den Balken und den Rand des Diagramms anpasst.

Hier ist ein Musterlösungscode, den du verwenden kannst:

```python
import matplotlib.pyplot as plt

# Daten für das Diagramm
produkte = ['Produkt A', 'Produkt B', 'Produkt C']
umsatz = [500, 800, 300]

# Diagrammgröße festlegen
plt.figure(figsize=(8, 6))

# Diagramm erstellen
plt.bar(produkte, umsatz)

# Abstand anpassen
plt.subplots_adjust(left=0.1, right=0.9, top=0.9, bottom=0.2)

# Achsentitel hinzufügen
plt.xlabel('Produkte')
plt.ylabel('Umsatz')

# Daten plotten
plt.show()
```

Viel Spaß beim Experimentieren mit der Feinabstimmung von Plot Layouts in Matplotlib!