## Einführung
In diesem Tutorial werden wir uns damit beschäftigen, wie man mehrere Diagramme in einem einzigen Fenster erstellt und anordnet. Dieses Wissen ist besonders nützlich, wenn du komplexe Daten visualisieren möchtest oder verschiedene Ansichten deiner Daten vergleichen möchtest.

Nachdem du dieses Tutorial abgeschlossen hast, wirst du in der Lage sein:
- Mehrere Subplots zu erstellen und sie in verschiedenen Anordnungen anzuzeigen.
- Die Größe und den Abstand der Subplots anzupassen, um den Platz optimal zu nutzen.
- Deine Diagramme anzupassen und anzupassen, um sie ansprechend und aussagekräftig zu gestalten.

Lasst uns nun mit der Theorie beginnen!

## Theorie

### Subplots erstellen
In Matplotlib können wir mehrere Subplots erstellen, indem wir die Funktion `subplots()` verwenden. Diese Funktion ermöglicht es uns, ein Raster von Subplots zu erstellen, das aus Zeilen und Spalten besteht. Jeder Subplot wird dann anhand seiner Position im Raster identifiziert.

Hier ist ein allgemeines Code-Beispiel, das dir zeigt, wie man Subplots erstellt:

```python
import matplotlib.pyplot as plt

fig, axes = plt.subplots(nrows=2, ncols=2)
```

Lass uns das anhand eines spezifischen Beispiels in Python betrachten:

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 2*np.pi, 100)
y1 = np.sin(x)
y2 = np.cos(x)
y3 = np.tan(x)
y4 = np.exp(x)

fig, axes = plt.subplots(nrows=2, ncols=2)
axes[0, 0].plot(x, y1)
axes[0, 1].plot(x, y2)
axes[1, 0].plot(x, y3)
axes[1, 1].plot(x, y4)

plt.show()
```

### Anpassen der Subplot-Anordnung und -Größe
Matplotlib bietet verschiedene Methoden, um die Anordnung und Größe der Subplots anzupassen. Einige der nützlichsten Methoden sind `subplots_adjust()`, `tight_layout()` und `gridspec`.

Mit der Funktion `subplots_adjust()` kannst du den Abstand zwischen den Subplots anpassen. Du kannst Parameter wie `left`, `right`, `bottom`, `top` verwenden, um den Abstand zu ändern.

```python
import matplotlib.pyplot as plt

fig, axes = plt.subplots(nrows=2, ncols=2)
plt.subplots_adjust(left=0.1, right=0.9, bottom=0.1, top=0.9)
```

Die Funktion `tight_layout()` passt automatisch den Abstand zwischen den Subplots an, um Platz für die Achsenbeschriftungen, Titel usw. zu schaffen.

```python
import matplotlib.pyplot as plt

fig, axes = plt.subplots(nrows=2, ncols=2)
plt.tight_layout()
```

Das Modul `gridspec` bietet eine flexiblere Möglichkeit, die Größe und Anordnung der Subplots anzupassen. Du kannst benutzerdefinierte Raster und Zellen erstellen, um die Subplots genau zu positionieren.

Hier ist ein Beispiel, das `gridspec` verwendet:

```python
import matplotlib.gridspec as gridspec
import matplotlib.pyplot as plt

fig = plt.figure()
gs = gridspec.GridSpec(2, 2)

ax1 = fig.add_subplot(gs[0, 0])
ax2 = fig.add_subplot(gs[0, 1])
ax3 = fig.add_subplot(gs[1, :])

# Plots hinzufügen...

plt.show()
```

## Praxis
Lass uns das gelernte Wissen in die Praxis umsetzen! Wir werden eine leichte und eine schwerere Aufgabe haben, um dein Verständnis zu überprüfen.

### Aufgabe 1
Erstelle ein Diagramm mit zwei Subplots nebeneinander. Das erste Diagramm soll eine Sinus-Kurve und das zweite Diagramm eine Cosinus-Kurve enthalten.

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 2*np.pi, 100)
y1 = np.sin(x)
y2 = np.cos(x)

fig, axes = plt.subplots(nrows=1, ncols=2)
axes[0].plot(x, y1)
axes[1].plot(x, y2)

plt.show()
```

### Aufgabe 2
Erstelle ein Diagramm mit drei Subplots. Das erste Diagramm soll eine Sinus-Kurve enthalten, das zweite Diagramm eine Cosinus-Kurve und das dritte Diagramm eine Tangens-Kurve.

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 2*np.pi, 100)
y1 = np.sin(x)
y2 = np.cos(x)
y3 = np.tan(x)

fig, axes = plt.subplots(nrows=1, ncols=3)
axes[0].plot(x, y1)
axes[1].plot(x, y2)
axes[2].plot(x, y3)

plt.show()
```

Herzlichen Glückwunsch! Du hast erfolgreich Subplots erstellt und ihre Anordnung und Größe angepasst. Du bist auf dem besten Weg, beeindruckende Datenvisualisierungen mit Matplotlib zu erstellen!

Ich hoffe, du hattest Spaß bei diesem Tutorial. Weiterhin viel Erfolg beim Python-Programmieren!