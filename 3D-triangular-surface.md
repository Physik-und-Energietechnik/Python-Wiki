## Einführung

Willkommen zum aufregenden Abenteuer der dreidimensionalen, dreieckigen Oberflächenvisualisierung mit Matplotlib! In diesem Tutorial werden wir uns anschauen, wie man mit Matplotlib atemberaubende 3D-Diagramme erstellen kann, die aus einer Ansammlung von dreieckigen Flächen bestehen. Keine Sorge, wenn du bisher noch keine Erfahrung mit Python oder Matplotlib hast - wir werden dich behutsam in diese aufregende Welt einführen.

## Theorie

#### Was ist eine 3D dreieckige Oberfläche?

Eine 3D dreieckige Oberfläche ist im Grunde genommen eine Art 3D-Diagramm, bei dem die Oberfläche durch eine Sammlung von Dreiecken dargestellt wird. Jedes Dreieck wird durch drei Punkte im dreidimensionalen Raum definiert. Diese Punkte werden auch als Eckpunkte bezeichnet. Indem wir eine ausreichende Anzahl von Dreiecken erzeugen und sie entsprechend positionieren, können wir eine komplexe dreidimensionale Oberfläche darstellen.

#### Code-Beispiel: Allgemein

```python
# Importiere die benötigten Module
import matplotlib.pyplot as plt
import numpy as np

# Definiere die Eckpunkte der Dreiecke
x = np.array([0, 1, 0.5])
y = np.array([0, 0, np.sqrt(3)/2])

# Definiere die Dreiecke
triangles = np.array([[0, 1, 2]])

# Erzeuge das 3D-Diagramm
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.plot_trisurf(x, y, triangles)

# Zeige das Diagramm an
plt.show()
```

#### Code-Beispiel: Direkt in Python

```python
# Importiere die benötigten Module
import matplotlib.pyplot as plt
import numpy as np

# Erzeuge zufällige Punkte
num_points = 100
x = np.random.rand(num_points)
y = np.random.rand(num_points)
z = np.sin(2 * np.pi * x) * np.cos(2 * np.pi * y)

# Definiere die Dreiecke
triangles = np.random.choice(num_points, (num_points, 3))

# Erzeuge das 3D-Diagramm
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.plot_trisurf(x, y, z, triangles=triangles)

# Zeige das Diagramm an
plt.show()
```

## Praxis

Jetzt wird es Zeit, dein neu erlangtes Wissen auf die Probe zu stellen! Wir haben zwei Aufgaben für dich vorbereitet - eine leichte und eine etwas kniffligere. Aber keine Sorge, wir haben auch Musterlösungen, falls du mal feststeckst.

### Aufgabe 1

Erzeuge eine dreidimensionale, dreieckige Oberfläche, die wie ein schickes Hügelpanorama aussieht. Verwende dafür eine geeignete Funktion, um die Z-Werte der Punkte zu berechnen. Experimentiere mit verschiedenen Funktionen, um das beste Ergebnis zu erzielen.

Musterlösung:

```python
import matplotlib.pyplot as plt
import numpy as np

# Erzeuge eine 3

D-Funktion
def hill(x, y):
    return np.sin(x) * np.sin(y)

# Erzeuge die Datenpunkte
x = np.linspace(-5, 5, 100)
y = np.linspace(-5, 5, 100)
X, Y = np.meshgrid(x, y)
Z = hill(X, Y)

# Definiere die Dreiecke
triangles = plt.tri.Triangulation(X.flatten(), Y.flatten()).triangles

# Erzeuge das 3D-Diagramm
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.plot_trisurf(X.flatten(), Y.flatten(), Z.flatten(), triangles=triangles)

# Zeige das Diagramm an
plt.show()
```

### Aufgabe 2

Erzeuge ein interessantes 3D-Diagramm, das aus einer zufälligen Anordnung von Punkten und Dreiecken besteht. Verwende dazu die NumPy-Funktionen `np.random.rand` und `np.random.choice`.

Musterlösung:

```python
import matplotlib.pyplot as plt
import numpy as np

# Erzeuge zufällige Punkte
num_points = 100
x = np.random.rand(num_points)
y = np.random.rand(num_points)
z = np.sin(2 * np.pi * x) * np.cos(2 * np.pi * y)

# Definiere die Dreiecke
triangles = np.random.choice(num_points, (num_points, 3))

# Erzeuge das 3D-Diagramm
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.plot_trisurf(x, y, z, triangles=triangles)

# Zeige das Diagramm an
plt.show()
```
## Fazit
Super! Du hast es geschafft! Du kannst jetzt beeindruckende dreidimensionale, dreieckige Oberflächen mit Matplotlib erstellen. Spiele weiter mit den verschiedenen Funktionen und experimentiere mit den Möglichkeiten, um noch faszinierendere Visualisierungen zu erschaffen. Viel Spaß beim Erkunden der fantastischen Welt der 3D-Grafiken!

## Links / Weiteres Material
### W3Schools
### YouTube