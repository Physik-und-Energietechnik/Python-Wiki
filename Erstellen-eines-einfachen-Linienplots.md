## Einführung
In diesem Abschnitt werden wir uns damit beschäftigen, wie wir mithilfe der Matplotlib-Bibliothek einen einfachen Linienplot erstellen können. Aber keine Sorge, wenn du noch nicht viel Erfahrung mit Python hast – wir werden alles Schritt für Schritt erklären!

Nach diesem Abschnitt wirst du Folgendes lernen:
- Wie man Daten für einen Linienplot vorbereitet
- Wie man einen einfachen Linienplot erstellt und anpasst
- Wie man den Plot speichert oder anzeigt

Linienplots sind besonders nützlich, um Daten auf einer x- und y-Achse darzustellen. Du kannst sie zum Beispiel verwenden, um den Verlauf von Aktienkursen, Temperaturänderungen oder sogar deinem täglichen Koffeinkonsum im Laufe der Zeit zu visualisieren!

## Theorie

### Daten für den Linienplot
Bevor wir unseren Linienplot erstellen können, benötigen wir Daten, die wir darstellen möchten. In der Regel bestehen die Daten aus einer Liste von x-Werten und einer entsprechenden Liste von y-Werten. Hier ist ein allgemeines Beispiel:

```python
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]
```

Das bedeutet, dass wir eine Linie haben werden, die die Punkte (1, 2), (2, 4), (3, 6), (4, 8) und (5, 10) verbindet. Du kannst natürlich deine eigenen Daten verwenden!

### Einen einfachen Linienplot erstellen
Nun, da wir unsere Daten vorbereitet haben, können wir endlich unseren Linienplot erstellen! Hier ist der Code, den du verwenden kannst:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

plt.plot(x, y)
plt.xlabel('x-Werte')
plt.ylabel('y-Werte')
plt.title('Mein erster Linienplot')
plt.show()
```

Voilà! Du hast deinen ersten Linienplot erstellt! Das `plot()`-Kommando erzeugt die Linie, `xlabel()` und `ylabel()` legen die Beschriftungen der Achsen fest, und `title()` gibt dem Plot einen Titel. Schließlich zeigt `show()` den Plot an.

### Beispielcode in Aktion
Lass uns das Ganze einmal in Aktion sehen! Hier ist ein Beispiel mit konkreten Daten:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

plt.plot(x, y)
plt.xlabel('Zeit')
plt.ylabel('Koffeinkonsum')
plt.title('Mein täglicher Koffeinkonsum')
plt.show()
```
[[https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Grundlagen des Plottings/beispielcode_1.png|alt=Koffeinkonsum Plot]]

Jetzt kannst du deine eigene Achterbahnfahrt des Koffeinkonsums visualisieren!

## Praxis

### Aufgabe 1
Erstelle einen Linienplot für die folgenden Daten:

```python
x = [0, 1, 2, 3, 4, 5]
y = [0, 1, 4, 9, 16, 25]
```

Verwende passende Achsenbeschriftungen und einen aussagekräftigen Titel für den Plot.
Musterlösung:

```python
import matplotlib.pyplot as plt

x = [0, 1, 2, 3, 4, 5]
y = [0, 1, 4, 9, 16, 25]

plt.plot(x, y)
plt.xlabel('x-Werte')
plt.ylabel('y-Werte')
plt.title('Quadratische Funktion')
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Grundlagen_des_Plottings/Erstellen_eines_einfachen_Linienplots/ms_aufgabe1.png)

### Aufgabe 2
Erstelle einen Linienplot für die Funktion f(x) = sin(x) im Intervall von 0 bis 2π. Hinweis: Du kannst die `numpy`-Bibliothek verwenden, um die Sinusfunktion zu berechnen.

Musterlösung:

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 2*np.pi, 100)
y = np.sin(x)

plt.plot(x, y)
plt.xlabel('x-Werte')
plt.ylabel('y-Werte')
plt.title('Sinusfunktion')
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Grundlagen_des_Plottings/Erstellen_eines_einfachen_Linienplots/ms_aufgabe2.png)

Viel Erfolg bei den Aufgaben!

## Fazit
Herzlichen Glückwunsch! Du hast erfolgreich Linienplots erstellt und bist bereit, deine Daten visuell ansprechend darzustellen.