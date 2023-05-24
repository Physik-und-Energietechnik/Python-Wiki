# Python - Einführung in Matplotlib

## 1. Titel
Willkommen zur Einführung in Matplotlib! Erlerne die Grundlagen dieser leistungsstarken Python-Bibliothek zur Visualisierung von Daten.

## 2. Einführung
Matplotlib ist ein mächtiges Werkzeug, um deine Daten zum Leben zu erwecken. In diesem Tutorial werden wir lernen, wie wir mit Matplotlib Diagramme und Plots erstellen können. Egal, ob du Daten analysieren möchtest, um beeindruckende Visualisierungen zu erstellen oder einfach nur neugierig bist, wie du deine wissenschaftlichen Ergebnisse ansprechend darstellen kannst, Matplotlib ist dein treuer Begleiter.

Nach Abschluss dieses Tutorials wirst du in der Lage sein:
- Diagramme wie Linien-, Balken- und Tortendiagramme zu erstellen.
- Achsenbeschriftungen, Titel und Legenden hinzuzufügen.
- Farben, Stile und Größen anzupassen, um deine Diagramme individuell zu gestalten.
- Matplotlib-Code zu lesen und anzupassen, um deine eigenen Visualisierungen zu erstellen.

Lass uns nun in die wundervolle Welt der Visualisierung mit Matplotlib eintauchen!

## 3. Theorie
### Grundlagen von Matplotlib
Matplotlib ist eine Python-Bibliothek, die auf einer einfachen Idee beruht: Daten sollten einfach dargestellt werden können, ohne dass du ein Genie sein musst. Matplotlib bietet eine Vielzahl von Funktionen zum Erstellen von Diagrammen, die du mithilfe von Code anpassen und personalisieren kannst.

Bevor wir loslegen, lass uns zunächst einen Blick auf ein allgemeines Code-Beispiel werfen, um ein Gefühl für Matplotlib zu bekommen:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

plt.plot(x, y)
plt.show()
```

Das obige Beispiel zeigt, wie einfach es ist, eine einfache Linie zu zeichnen. Die `plot`-Funktion nimmt zwei Listen `x` und `y` als Eingabe und erzeugt eine Linie, die durch die gegebenen Punkte verläuft. Mit `plt.show()` wird das Diagramm angezeigt.

Jetzt schauen wir uns das gleiche Beispiel als explizites Code-Beispiel an:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

plt.plot(x, y)
plt.xlabel('X-Achse')
plt.ylabel('Y-Achse')
plt.title('Mein erstes Diagramm')
plt.grid(True)
plt.show()
```

Hier haben wir die Funktionen `xlabel`, `ylabel`, `title` und `grid` verwendet, um Achsenbeschriftungen, einen Diagrammtitel und ein Raster hinzuzufügen.

### Arbeiten mit verschiedenen Diagrammtypen
Matplotlib bietet viele verschiedene Diagrammtypen, die wir verwenden können, um Daten darzustellen. Hier sind einige Beispiele:

#### Balkendiagramm

```python
import matplotlib.pyplot as plt

x = ['A', 'B', 'C', 'D']
y = [3, 7, 2, 5]

plt.bar(x, y

#### Tortendiagramm

```python
import matplotlib.pyplot as plt

labels = ['Äpfel', 'Bananen', 'Orangen', 'Erdbeeren']
sizes = [30, 25, 20, 15]

plt.pie(sizes, labels=labels, autopct='%1.1f%%')
plt.axis('equal')
plt.show()
```

### 4. Praxis
Jetzt ist es an der Zeit, dein Wissen in die Praxis umzusetzen! Hier sind zwei Aufgaben für dich:

#### Aufgabe 1: Erstelle ein Linien-Diagramm
Gegeben sind die folgenden Daten:
```python
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]
```
Erstelle ein Linien-Diagramm, das diese Daten darstellt. Füge eine Achsenbeschriftung, einen Diagrammtitel und ein Raster hinzu.

Musterlösung:
```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

plt.plot(x, y)
plt.xlabel('X-Achse')
plt.ylabel('Y-Achse')
plt.title('Mein Linien-Diagramm')
plt.grid(True)
plt.show()
```

#### Aufgabe 2: Erstelle ein Balkendiagramm
Gegeben sind die folgenden Daten:
```python
x = ['A', 'B', 'C', 'D']
y = [3, 7, 2, 5]
```
Erstelle ein Balkendiagramm, das diese Daten darstellt. Füge eine Achsenbeschriftung, einen Diagrammtitel und ein Raster hinzu.

Musterlösung:
```python
import matplotlib.pyplot as plt

x = ['A', 'B', 'C', 'D']
y = [3, 7, 2, 5]

plt.bar(x, y)
plt.xlabel('X-Achse')
plt.ylabel('Y-Achse')
plt.title('Mein Balkendiagramm')
plt.grid(True)
plt.show()
```

Viel Spaß beim Erkunden von Matplotlib und dem Erstellen beeindruckender Visualisierungen!