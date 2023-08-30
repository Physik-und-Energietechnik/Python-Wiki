## Einführung

Hast du dich jemals gefragt, wie du beeindruckende Dreiecksvisualisierungen erstellen kannst? Nun, das ist dein Glückstag! In diesem Tutorial wirst du lernen, wie du mit Matplotlib Dreiecksplots erstellst, um deine Daten auf eine dreieckige Reise zu schicken. Egal, ob du wissenschaftliche Daten visualisierst oder einfach nur coole Muster erstellen möchtest, `triplot` ist dein Begleiter.

## Theorie

### Grundlagen

Bevor wir loslegen, lass uns kurz die Grundlagen durchgehen. Ein Dreiecksplot ist eine Möglichkeit, Daten auf einem dreieckigen Koordinatensystem darzustellen. Dies ist besonders nützlich, wenn deine Daten auf drei Variablen basieren. Stell dir vor, du hast Daten zu den Seitenlängen eines Dreiecks – du könntest diese mit `triplot` auf einen Blick darstellen.

### Code-Beispiel - Grundstruktur

Hier ist eine grundlegende Vorstellung davon, wie der Code aussehen könnte:

```python
import matplotlib.pyplot as plt

# Deine Daten
x = [0.2, 0.5, 0.8]
y = [0.1, 0.9, 0.3]

# Erstelle den Dreiecksplot
plt.triplot(x, y)

# Zeige den Plot an
plt.show()
```

### Fortgeschrittene Anpassungen

Natürlich können wir nicht nur die Ecken eines Dreiecks darstellen. Du kannst Marker und Farben hinzufügen, Achsen beschriften und vieles mehr! Schau dir dieses erweiterte Beispiel an:

```python
import matplotlib.pyplot as plt

# Deine Daten
x = [0.2, 0.5, 0.8]
y = [0.1, 0.9, 0.3]

# Erstelle den Dreiecksplot mit Anpassungen
plt.triplot(x, y, marker='o', color='r')
plt.xlabel('X-Achse')
plt.ylabel('Y-Achse')
plt.title('Mein Dreiecksplot')

# Zeige den Plot an
plt.show()
```

## Praxis

### Aufgabe 1

Erstelle einen einfachen Dreiecksplot mit den Eckpunkten (0, 0), (1, 0) und (0.5, 0.7).

Musterlösung zu Aufgabe 1:
```python
import matplotlib.pyplot as plt

# Deine Daten
x = [0, 1, 0.5]
y = [0, 0, 0.7]

# Erstelle den Dreiecksplot
plt.triplot(x, y)

# Zeige den Plot an
plt.show()
```
![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Plottypen/Unstrukturierte_Koordinaten/triplot/ms_aufgabe1.png)

### Aufgabe 2

Du hast bereits gelernt, wie man statische Dreiecksplots erstellt. Aber wie wäre es mit einem interaktiven Plot, bei dem du die Eckpunkte des Dreiecks per Mausklick verschieben kannst? Verwende die Bibliothek matplotlib.widgets, um diese Interaktivität zu erreichen.

Erstelle einen interaktiven Dreiecksplot, bei dem die Eckpunkte des Dreiecks initial auf den Koordinaten (0, 0), (1, 0) und (0.5, 0.7) platziert werden. Die Benutzer sollten in der Lage sein, die Eckpunkte des Dreiecks durch Klicken und Ziehen mit der Maus zu verschieben. Zeige außerdem die Koordinaten der Eckpunkte in Echtzeit an, während sie verschoben werden.

Hinweis: Du musst die matplotlib.widgets-Bibliothek installieren, falls sie noch nicht installiert ist. Du kannst dies mit dem Befehl pip install matplotlib tun.

Musterlösung zu Aufgabe 2:
```python
import matplotlib.pyplot as plt
from matplotlib.widgets import Slider, Button
import numpy as np

# Initialisierung der Eckpunkte
x = np.array([0, 1, 0.5])
y = np.array([0, 0, 0.7])

fig, ax = plt.subplots()
plt.subplots_adjust(bottom=0.3)

# Plot des initialen Dreiecks
triplot, = plt.plot(x, y, 'ro-')

# Text-Anzeige der Koordinaten
coord_text = ax.text(0.5, -0.1, f'Punkte: ({x[0]:.2f}, {y[0]:.2f}), ({x[1]:.2f}, {y[1]:.2f}), ({x[2]:.2f}, {y[2]:.2f})',
                      transform=ax.transAxes, fontsize=10, ha='center')

# Interaktive Punkte
point_hands = [ax.plot(x[i], y[i], 'go', markersize=10, alpha=0.7)[0] for i in range(3)]

# Slider für Koordinaten
x_slider = Slider(plt.axes([0.2, 0.15, 0.65, 0.03]), 'X-Koordinate', 0, 1)
y_slider = Slider(plt.axes([0.2, 0.1, 0.65, 0.03]), 'Y-Koordinate', 0, 1)

# Funktion zum Aktualisieren der Punkte
def update(val):
    idx = int(val)
    x[idx] = x_slider.val
    y[idx] = y_slider.val
    point_hands[idx].set_data(x[idx], y[idx])
    triplot.set_data(x, y)
    coord_text.set_text(f'Punkte: ({x[0]:.2f}, {y[0]:.2f}), ({x[1]:.2f}, {y[1]:.2f}), ({x[2]:.2f}, {y[2]:.2f})')
    plt.draw()

x_slider.on_changed(update)
y_slider.on_changed(update)

plt.show()
```
![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Plottypen/Unstrukturierte_Koordinaten/triplot/ms_aufgabe2.png)

## Fazit
Und das war's! Du hast jetzt einen Einblick in die wunderbare Welt von `triplot` in Matplotlib erhalten. Experimentiere weiter mit Anpassungen und lass deiner Kreativität freien Lauf!

Keep on triangulating!

## Links / Weiteres Material
### Dokumentation
https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.triplot.html