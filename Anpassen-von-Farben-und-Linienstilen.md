# Matplotlib - Anpassen von Farben und Linienstilen

## Einführung

Willkommen zu unserem Python-Tutorial über das Anpassen von Farben und Linienstilen in Matplotlib! In diesem Abschnitt werden wir lernen, wie wir unsere Diagramme in Matplotlib mit verschiedenen Farben und Linienstilen personalisieren können. 

Durch das Erlernen der Anpassung von Farben und Linienstilen können wir unsere Diagramme noch ansprechender gestalten und unseren eigenen Stil verleihen.

In diesem Tutorial werden wir lernen, wie wir die Farben von Diagrammelementen wie Linien, Balken und Text anpassen können. Außerdem werden wir verschiedene Linienstile kennenlernen, um unseren Diagrammen zusätzliche visuelle Attraktivität zu verleihen. 

## Theorie

### Farbanpassung

Bei der Farbanpassung haben wir verschiedene Optionen. Wir können vordefinierte Farben verwenden, indem wir Namen wie "rot", "blau" oder "grün" angeben. Außerdem können wir Farben mithilfe des RGB-Farbmodells spezifizieren, indem wir den Rot-, Grün- und Blauanteil angeben. Ein Beispielcode für die Verwendung von Farben sieht wie folgt aus:

```python
import matplotlib.pyplot as plt

# Vordefinierte Farben
plt.plot([1, 2, 3, 4], [1, 4, 9, 16], color='red')

# RGB-Farbmodell
plt.plot([1, 2, 3, 4], [1, 4, 9, 16], color=(0.2, 0.8, 0.3))
```

### Linienstilanpassung

Wir können auch den Stil der Linien in unseren Diagrammen anpassen. Matplotlib bietet verschiedene vordefinierte Linienstile wie "solid" (durchgezogen), "dashed" (gestrichelt), "dotted" (gepunktet) und "dashdot" (Strich-Punkt). Ein Beispielcode für die Verwendung von Linienstilen sieht wie folgt aus:

```python
import matplotlib.pyplot as plt

# Durchgezogene Linie
plt.plot([1, 2, 3, 4], [1, 4, 9, 16], linestyle='solid')

# Gestrichelte Linie
plt.plot([1, 2, 3, 4], [1, 4, 9, 16], linestyle='dashed')

# Gepunktete Linie
plt.plot([1, 2, 3, 4], [1, 4, 9, 16], linestyle='dotted')

# Strich-Punkt-Linie
plt.plot([1, 2, 3, 4], [1, 4, 9, 16], linestyle='dashdot')
```

## Praxis

Lassen Sie uns das Gelernte in die Praxis umsetzen! Hier sind zwei Aufgaben für Sie:

### Aufgabe 1

Erstellen Sie ein Liniendiagramm, das die folgenden Daten darstellt:

```
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]
```

Passen Sie die Linienfarbe auf "blau" und den Linienstil auf "gestrichelt" an.

#### Musterlösung 1

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

plt.plot(x, y, color='blue', linestyle='dashed')
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Anpassen_und_Stilisierung/Anpassen_von_Farben_und_Linienstilen/ms_aufgabe1.png)

### Aufgabe 2

Erstellen Sie ein Balkendiagramm, das die folgenden Daten darstellt:

```
labels = ['A', 'B', 'C', 'D']
values = [3, 7, 2, 5]
```

Passen Sie die Farben der Balken auf "rot", "grün", "blau" und "gelb" an und verwenden Sie den Linienstil "durchgezogen".

#### Musterlösung 2

```python
import matplotlib.pyplot as plt

labels = ['A', 'B', 'C', 'D']
values = [3, 7, 2, 5]

colors = ['red', 'green', 'blue', 'yellow']

plt.bar(labels, values, color=colors, linestyle='solid')
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Anpassen_und_Stilisierung/Anpassen_von_Farben_und_Linienstilen/ms_aufgabe2.png)

Viel Spaß beim Experimentieren mit Farben und Linienstilen in Matplotlib! Nutzen Sie Ihr neues Wissen, um beeindruckende und einzigartige Diagramme zu erstellen.