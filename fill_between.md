## Einführung

Willkommen zurück zu unserem Python-Tutorial für Anfänger! Heute werden wir uns mit einem spannenden Thema beschäftigen: dem `fill_between` Plot in Matplotlib. Wenn du bereits die Grundlagen von Matplotlib kennst und dich fragst, wie du bestimmte Bereiche zwischen Linien oder Kurven einfärben kannst, dann bist du hier genau richtig!

In diesem Tutorial lernst du, wie du den `fill_between` Plot in Matplotlib verwenden kannst, um visuell ansprechende Flächen zwischen zwei Linien oder Kurven zu erzeugen. Mit diesem Wissen kannst du deine Daten auf eine kreative und informative Weise visualisieren. Ob du nun Diagramme für deine Präsentationen erstellen oder Datenmuster besser verstehen möchtest, der `fill_between` Plot ist ein mächtiges Werkzeug, das dir dabei hilft!

## Theorie

Bevor wir uns in die Praxis stürzen, lass uns kurz die Theorie hinter dem `fill_between` Plot verstehen. Der `fill_between` Plot ermöglicht es uns, den Bereich zwischen zwei Linien oder Kurven mit Farbe zu füllen. Das kann besonders nützlich sein, um Unterschiede oder Beziehungen zwischen Daten darzustellen.

Schauen wir uns dazu ein allgemeines Beispiel an:

```python
# Allgemeines Code-Beispiel
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y1 = [1, 2, 3, 2, 1]
y2 = [0, 1, 2, 1, 0]

plt.fill_between(x, y1, y2, color='skyblue')
plt.plot(x, y1, color='blue', label='Line 1')
plt.plot(x, y2, color='red', label='Line 2')
plt.legend()
plt.show()
```

In diesem Beispiel haben wir zwei Linien, `Line 1` und `Line 2`, die von den Punkten `(1, 1)`, `(2, 2)`, `(3, 3)`, `(2, 2)` und `(1, 1)` bzw. `(1, 0)`, `(2, 1)`, `(3, 2)`, `(2, 1)` und `(1, 0)` dargestellt werden. Der `fill_between` Plot färbt den Bereich zwischen diesen beiden Linien mit der Farbe 'skyblue' ein.

Jetzt schauen wir uns ein explizites Code-Beispiel direkt in Python an:

```python
# Explizites Code-Beispiel
import numpy as np
import matplotlib.pyplot as plt

x = np.linspace(0, 10, 100)
y1 = np.sin(x)
y2 = np.cos(x)

plt.fill_between(x, y1, y2, color='lightgreen')
plt.plot(x, y1, label='sin(x)')
plt.plot(x, y2, label='cos(x)')
plt.legend()
plt.show()
```

Hier haben wir zwei Kurven, `sin(x)` und `cos(x)`, die den Sinus bzw. Kosinus von Werten zwischen 0 und 10 darstellen. Der `fill_between` Plot färbt den Bereich zwischen den beiden Kurven mit der Farbe 'lightgreen' ein.

## Praxis

Jetzt bist du an der Reihe! Lass uns das erlangte Wissen in die Praxis umsetzen.



### Aufgabe 1

Deine Aufgabe besteht darin, eine Fläche zwischen zwei Linien zu füllen. Erstelle einen `fill_between` Plot mit den folgenden Daten:

```python
x = [1, 2, 3, 4, 5]
y1 = [1, 2, 3, 2, 1]
y2 = [0, 1, 2, 1, 0]
```

### Musterlösung für die leichte Aufgabe

Hier ist eine mögliche Lösung:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y1 = [1, 2, 3, 2, 1]
y2 = [0, 1, 2, 1, 0]

plt.fill_between(x, y1, y2, color='skyblue')
plt.plot(x, y1, color='blue', label='Line 1')
plt.plot(x, y2, color='red', label='Line 2')
plt.legend()
plt.show()
```
![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Plottypen/Basic/fill_between/ms_aufgabe1.png)

### Aufgabe 2

Für diejenigen, die eine größere Herausforderung suchen, hier ist eine schwierigere Aufgabe:

Deine Aufgabe besteht darin, den Bereich zwischen zwei Kurven einzufärben. Erstelle einen `fill_between` Plot mit den folgenden Daten:

```python
import numpy as np

x = np.linspace(0, 10, 100)
y1 = np.sin(x)
y2 = np.cos(x)
```

### Musterlösung für die schwere Aufgabe

Hier ist eine mögliche Lösung:

```python
import numpy as np
import matplotlib.pyplot as plt

x = np.linspace(0, 10, 100)
y1 = np.sin(x)
y2 = np.cos(x)

plt.fill_between(x, y1, y2, color='lightgreen')
plt.plot(x, y1, label='sin(x)')
plt.plot(x, y2, label='cos(x)')
plt.legend()
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Plottypen/Basic/fill_between/ms_aufgabe2.png)

## Fazit

Das war's schon für den `fill_between` Plot in Matplotlib. Du hast jetzt gelernt, wie du Bereiche zwischen Linien oder Kurven einfärben kannst, um deine Visualisierungen aufzupeppen. Experimentiere mit verschiedenen Farben und Daten, um einzigartige und aussagekräftige Plots zu erstellen. Viel Spaß beim Programmieren und bis zum nächsten Tutorial!

## Links / Weiteres Material
### Dokumentation
https://matplotlib.org/stable/plot_types/basic/fill_between.html
### W3Schools
### YouTube

