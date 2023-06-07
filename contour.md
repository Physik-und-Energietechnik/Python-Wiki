## Matplotlib - Der contour Plot

### Einführung

Willkommen zurück, ihr Python-Abenteurer! Heute begeben wir uns auf eine Reise in die wunderbare Welt des **contour Plots** mit Matplotlib. Stellt euch vor, ihr habt eine Karte vor euch, auf der die Höhen unterschiedlicher Gebirge mit wunderschönen Linien dargestellt werden. Das ist im Wesentlichen ein contour Plot! Mit diesem nützlichen Werkzeug könnt ihr Daten visualisieren, die als zweidimensionale Felder oder Gitter organisiert sind.

In diesem Tutorial werdet ihr lernen, wie ihr mit Matplotlib konturähnliche Grafiken erstellen könnt, um komplexe Datenmuster zu erkennen und zu präsentieren. Aber haltet euch fest! Bevor wir in die Praxis eintauchen, wollen wir uns ein wenig mit der Theorie beschäftigen.

### Theorie

#### Was ist ein contour Plot?

Ein contour Plot ist eine Art Grafik, die uns dabei hilft, Daten zu analysieren und zu verstehen. Er basiert auf einer kontinuierlichen Farbskala oder Linien, die Höhenlinien auf einer topografischen Karte ähneln. Der Plot zeigt uns, wie Werte in einem zweidimensionalen Feld oder Gitter variieren.

Lasst uns das mit einem Beispiel verdeutlichen:

```python
# Allgemeines Code-Beispiel
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(-5, 5, 100)
y = np.linspace(-5, 5, 100)
X, Y = np.meshgrid(x, y)
Z = np.sin(np.sqrt(X**2 + Y**2))

plt.contour(X, Y, Z)
plt.show()
```

In diesem Beispiel erzeugen wir ein Gitter von x- und y-Werten, berechnen dann die zugehörigen z-Werte mithilfe einer mathematischen Funktion und zeichnen schließlich die Konturlinien mit `plt.contour()`.

Lasst uns das Ganze anhand eines spezifischen Beispiels noch einmal in Python durchgehen:

```python
# Explizites Code-Beispiel
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(-5, 5, 100)
y = np.linspace(-5, 5, 100)
X, Y = np.meshgrid(x, y)
Z = np.sin(np.sqrt(X**2 + Y**2))

plt.figure()
plt.contour(X, Y, Z, colors='black')
plt.contourf(X, Y, Z, cmap='viridis')
plt.colorbar()
plt.title('Ein cooler contour Plot')
plt.xlabel('X-Achse')
plt.ylabel('Y-Achse')
plt.show()
```

Hier erstellen wir einen detaillierteren contour Plot. Mit `plt.contour()` zeichnen wir die Konturlinien als schwarze Linien und mit `plt.contourf()` füllen wir den Bereich zwischen den Linien mit einer Farbskala, die wir mithilfe von `plt.colorbar()` anzeigen lassen können.

### Praxis

Lasst uns das erlernte Wissen auf die Probe stellen! Hier sind zwei Aufgaben für euch:

**Leichte Aufgabe:**

Erstellt einen contour Plot für die Funktion `Z = np.cos(X) + np.sin(Y)` im Bereich von -2π bis 2π für x und y. Verwendet eine geeignete Farbskala und f

ügt Titel, Achsenbeschriftungen hinzu.

```python
# Musterlösung für die leichte Aufgabe
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(-2*np.pi, 2*np.pi, 100)
y = np.linspace(-2*np.pi, 2*np.pi, 100)
X, Y = np.meshgrid(x, y)
Z = np.cos(X) + np.sin(Y)

plt.figure()
plt.contourf(X, Y, Z, cmap='cool')
plt.colorbar()
plt.title('Contour Plot für cos(X) + sin(Y)')
plt.xlabel('X-Achse')
plt.ylabel('Y-Achse')
plt.show()
```

**Schwere Aufgabe:**

Erstellt einen 3D contour Plot für die Funktion `Z = np.cos(X) * np.sin(Y)`. Verwendet unterschiedliche Ebenen für verschiedene Werte von Z und fügt eine geeignete Farbskala hinzu.

```python
# Musterlösung für die schwere Aufgabe
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(-2*np.pi, 2*np.pi, 100)
y = np.linspace(-2*np.pi, 2*np.pi, 100)
X, Y = np.meshgrid(x, y)
Z = np.cos(X) * np.sin(Y)

fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.contour3D(X, Y, Z, 50, cmap='cool')
ax.set_xlabel('X-Achse')
ax.set_ylabel('Y-Achse')
ax.set_zlabel('Z-Achse')
plt.title('3D contour Plot für cos(X) * sin(Y)')
plt.show()
```

Jetzt seid ihr bereit, eure eigenen contour Plots zu erstellen! Macht euch keine Sorgen, wenn es anfangs etwas verwirrend erscheint. Übung macht den Meister, und mit der Zeit werdet ihr zum Meister der Datenvisualisierung!

Vielen Spaß beim Erkunden der wundersamen Welt des contour Plots mit Matplotlib!