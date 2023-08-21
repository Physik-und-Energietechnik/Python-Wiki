## Einführung

In diesem Abschnitt werden wir uns mit dem Bar Plot beschäftigen.

Ein Bar Plot ist eine Art von Diagramm, das uns dabei hilft, Daten in einer visuell ansprechenden Weise darzustellen. Du kannst dir das Ganze wie eine Bar an der Bartheke vorstellen. Wenn du in einer Bar stehst, möchtest du natürlich wissen, wie viele Getränke du bereits konsumiert hast, um sicherzustellen, dass du nicht plötzlich auf dem Boden landest, oder? Genau das ermöglicht uns ein Bar Plot, aber statt alkoholischer Getränke zählen wir Datenwerte!

In diesem Tutorial wirst du lernen, wie du Bar Plots mit Matplotlib erstellen kannst. Du wirst sehen, wie du deine Daten in Balken verwandelst und ihnen Farben gibst, um sie angenehm für die Augen zu machen. Das ist nicht nur nützlich, um deine Daten zu analysieren, sondern auch, um deine Freunde auf Partys mit deinen erstaunlichen Diagrammfähigkeiten zu beeindrucken!

## Theorie

Bevor wir richtig loslegen, lass uns ein bisschen Theorie durchgehen. In einem Bar Plot haben wir eine x-Achse und eine y-Achse. Die x-Achse repräsentiert die Kategorien oder Labels, während die y-Achse die Werte darstellt. Jeder Balken repräsentiert eine Kategorie und seine Höhe gibt den Wert für diese Kategorie an.

Um das Ganze besser zu verstehen, schauen wir uns ein einfaches Beispiel an:

```python
import matplotlib.pyplot as plt

# Kategorien
kategorien = ['Apfel', 'Banane', 'Orange', 'Erdbeere']

# Werte für jede Kategorie
werte = [25, 32, 12, 19]

# Erstelle den Bar Plot
plt.bar(kategorien, werte)

# Zeige das Diagramm an
plt.show()
```

In diesem Beispiel haben wir vier Kategorien (Apfel, Banane, Orange und Erdbeere) und für jede Kategorie haben wir einen Wert angegeben. Der Code `plt.bar(kategorien, werte)` erstellt den Bar Plot und `plt.show()` zeigt das Diagramm an.

Jetzt hast du bereits ein grundlegendes Verständnis davon, wie ein Bar Plot erstellt wird. Aber wir können noch mehr tun! Du kannst beispielsweise die Farben der Balken ändern, um das Ganze interessanter zu gestalten. Schau dir dieses Beispiel an:

```python
import matplotlib.pyplot as plt

kategorien = ['Apfel', 'Banane', 'Orange', 'Erdbeere']
werte = [25, 32, 12, 19]

# Erstelle den Bar Plot und ändere die Farbe der Balken
plt.bar(kategorien, werte, color=['red', 'blue', 'orange', 'green'])

plt.show()
```

In diesem Beispiel haben wir die Farben der Balken geändert. Der Code `color=['red', 'blue', 'orange', 'green']` weist den Balk

en jeweils eine Farbe zu.

Das war die kurze Theorie hinter dem Bar Plot. Nun lass uns etwas Praxis machen, um das Gelernte anzuwenden!

## Praxis

### Aufgabe 1

Deine leichte Aufgabe besteht darin, einen Bar Plot für die Anzahl der verkauften Eistüten pro Monat zu erstellen. Hier sind die Daten:

- Januar: 100
- Februar: 85
- März: 120
- April: 105

Viel Erfolg! 
Hier ist ein Beispiel, wie der Code aussehen könnte:

```python
import matplotlib.pyplot as plt

monate = ['Januar', 'Februar', 'März', 'April']
verkäufe = [100, 85, 120, 105]

# Erstelle den Bar Plot
plt.bar(monate, verkäufe)

plt.show()
```

Hier ist eine mögliche Musterlösung für die leichte Aufgabe 1:

```python
import matplotlib.pyplot as plt

monate = ['Januar', 'Februar', 'März', 'April']
verkäufe = [100, 85, 120, 105]

# Erstelle den Bar Plot
plt.bar(monate, verkäufe)

# Achsentitel hinzufügen
plt.xlabel('Monat')
plt.ylabel('Anzahl der verkauften Eistüten')

# Diagrammtitel hinzufügen
plt.title('Verkauf von Eistüten pro Monat')

# Zeige das Diagramm an
plt.show()
```

Dieser Code fügt Achsentitel (`plt.xlabel('Monat')`, `plt.ylabel('Anzahl der verkauften Eistüten')`) und einen Diagrammtitel (`plt.title('Verkauf von Eistüten pro Monat')`) hinzu, um das Diagramm aussagekräftiger zu machen.

### Aufgabe 2

Für die schwierigere Aufgabe erstelle einen Bar Plot, der die Anzahl der verkauften Eistüten in zwei verschiedenen Jahren vergleicht: 2022 und 2023. Hier sind die Daten:

- Jahr 2022: [120, 150, 100, 135]
- Jahr 2023: [140, 160, 110, 145]

Viel Erfolg! Hier ist ein Beispiel, wie der Code aussehen könnte:

```python
import matplotlib.pyplot as plt
import numpy as np

monate = ['Januar', 'Februar', 'März', 'April']
verkäufe_2022 = [120, 150, 100, 135]
verkäufe_2023 = [140, 160, 110, 145]

# Die Breite der Balken
breite = 0.35

# Position der Monate auf der x-Achse
positionen = np.arange(len(monate))

# Erstelle den Bar Plot für 2022
plt.bar(positionen - breite/2, verkäufe_2022, breite, label='2022')

# Erstelle den Bar Plot für 2023
plt.bar(positionen + breite/2, verkäufe_2023, breite, label='2023')

# Füge die Legende hinzu
plt.legend()

plt.show()
```

Aufgabe 2 Musterlösung:

```python
import matplotlib.pyplot as plt
import numpy as np

monate = ['Januar', 'Februar', 'März', 'April']
verkäufe_2022 = [120, 150, 100, 135]
verkäufe_2023 = [140, 160, 110, 145]

# Die Breite der Balken
breite = 0.35

# Position der Monate auf der x-Achse
positionen = np.arange(len(monate))

# Erstelle den Bar Plot für 2022
plt.bar(positionen - breite/2, verkäufe_2022, breite, label='2022')

# Erstelle den Bar Plot für 2023
plt.bar(positionen + breite/2, verkäufe_2023, breite, label='2023')

# Achsentitel hinzufügen
plt.xlabel('Monat')
plt.ylabel('Anzahl der verkauften Eistüten')

# Diagrammtitel hinzufügen
plt.title('Verkauf von Eistüten im Vergleich: 2022 vs. 2023')

# Füge die Legende hinzu
plt.legend()

# Zeige das Diagramm an
plt.show()
```

In dieser Musterlösung verwenden wir die `numpy`-Bibliothek, um die Positionen der Monate auf der x-Achse zu berechnen (`positionen = np.arange(len(monate))`). Dadurch können wir die Balken nebeneinander platzieren. Wir fügen auch Achsentitel und einen Diagrammtitel hinzu, um das Diagramm klarer zu gestalten.

## Fazit
Das war's für den Bar Plot mit Matplotlib! Du hast jetzt die Grundlagen, um Daten in Balkenform darzustellen und sie farbenfroh zu gestalten. Viel Spaß beim Erkunden weiterer Möglichkeiten und beeindrucke deine Freunde mit deinen fantastischen Datenvisualisierungskünsten!

## Links / Weiteres Material
### Dokumentation
https://matplotlib.org/stable/plot_types/basic/bar.html
### W3Schools
https://www.w3schools.com/python/matplotlib_bars.asp
### YouTube