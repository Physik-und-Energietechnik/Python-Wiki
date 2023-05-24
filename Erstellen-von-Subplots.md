## Matplotlib - Erstellen von Subplots

### Einführung

Willkommen zu unserem Python Tutorial! In diesem Abschnitt werden wir uns mit dem Erstellen von Subplots in Matplotlib beschäftigen. Aber was sind Subplots überhaupt? Stell dir vor, du möchtest mehrere Diagramme oder Grafiken nebeneinander darstellen, um sie leichter vergleichen zu können. Genau das ermöglichen uns Subplots!

In diesem Tutorial lernst du, wie du mit Matplotlib Subplots erstellen kannst. Du wirst verstehen, wie sie aufgebaut sind und wie du sie an deine Bedürfnisse anpassen kannst. Das Wissen, das du hier erlangst, wird dir dabei helfen, professionell aussehende Visualisierungen zu erstellen und deine Daten auf eine anschauliche Art und Weise darzustellen.

### Theorie

Bevor wir mit dem Spaß beginnen, lass uns einen kurzen Blick auf die Theorie werfen. Ein Subplot besteht aus einer Rasteranordnung von Achsen, auf denen wir unsere Diagramme platzieren können. Die Achsen bilden das Grundgerüst für unsere Grafiken und wir können sie individuell gestalten, um unsere Daten optimal darzustellen.

Um Subplots in Matplotlib zu erstellen, verwenden wir die `subplots()`-Funktion. Diese Funktion gibt uns ein Figure-Objekt und ein Array von Axes-Objekten zurück. Das Figure-Objekt repräsentiert das gesamte Bild, während jedes Axes-Objekt einen einzelnen Subplot darstellt.

Lass uns das Ganze anhand eines Beispiels veranschaulichen:

```python
import matplotlib.pyplot as plt

# Subplots erstellen
fig, axes = plt.subplots(nrows=2, ncols=2)

# Daten plotten
axes[0, 0].plot([1, 2, 3, 4], [1, 4, 2, 3])
axes[0, 1].scatter([1, 2, 3, 4], [1, 4, 2, 3])
axes[1, 0].bar([1, 2, 3, 4], [1, 4, 2, 3])
axes[1, 1].pie([1, 2, 3, 4])

# Diagramme beschriften
axes[0, 0].set_title('Linienplot')
axes[0, 1].set_title('Punktwolke')
axes[1, 0].set_title('Balkendiagramm')
axes[1, 1].set_title('Kreisdiagramm')

# Subplot-Layout optimieren
plt.tight_layout()

# Grafik anzeigen
plt.show()
```

In diesem Beispiel erstellen wir ein 2x2-Subplot-Raster mit insgesamt 4 Subplots. Wir plotten verschiedene Arten von Diagrammen in jedem Subplot und beschriften sie entsprechend. Durch die Verwendung von `tight_layout()` stellen wir sicher, dass die Diagramme ordentlich angeordnet werden.

### Praxis

Jetzt wird es Zeit, das erlangte Wissen in die Praxis umzusetzen! Lass uns eine leichte und eine schwerere Aufgabe lösen, um sicherzustellen, dass du alles verstanden hast.

**Leichte Aufgabe:**

Erstelle ein 2x1-Subplot-Raster und plotte in jedem Subplot eine einfache Linienkurve. Bes

chrifte die Subplots mit den Titeln "Kurve 1" und "Kurve 2".

**Musterlösung:**

```python
import matplotlib.pyplot as plt

# Subplots erstellen
fig, axes = plt.subplots(nrows=2, ncols=1)

# Daten plotten
axes[0].plot([1, 2, 3, 4], [1, 4, 2, 3])
axes[1].plot([1, 2, 3, 4], [4, 2, 3, 1])

# Subplot-Titel setzen
axes[0].set_title('Kurve 1')
axes[1].set_title('Kurve 2')

# Subplot-Layout optimieren
plt.tight_layout()

# Grafik anzeigen
plt.show()
```

**Schwere Aufgabe:**

Erstelle ein 2x2-Subplot-Raster und plotte in jedem Subplot ein Streudiagramm. Beschrifte die Subplots mit den Titeln "Daten 1", "Daten 2", "Daten 3" und "Daten 4".

**Musterlösung:**

```python
import matplotlib.pyplot as plt
import numpy as np

# Subplots erstellen
fig, axes = plt.subplots(nrows=2, ncols=2)

# Zufällige Daten generieren
np.random.seed(42)
x = np.random.rand(100)
y = np.random.rand(100)

# Daten plotten
axes[0, 0].scatter(x, y)
axes[0, 1].scatter(x, -y)
axes[1, 0].scatter(-x, y)
axes[1, 1].scatter(-x, -y)

# Subplot-Titel setzen
axes[0, 0].set_title('Daten 1')
axes[0, 1].set_title('Daten 2')
axes[1, 0].set_title('Daten 3')
axes[1, 1].set_title('Daten 4')

# Subplot-Layout optimieren
plt.tight_layout()

# Grafik anzeigen
plt.show()
```

Herzlichen Glückwunsch! Du hast erfolgreich Subplots in Matplotlib erstellt. Mit diesem Wissen kannst du nun auf kreative Weise deine Daten visualisieren und beeindruckende Grafiken erstellen.

Viel Spaß beim Experimentieren und Erkunden der wunderbaren Welt der Subplots!