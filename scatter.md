## Einführung
In diesem Abschnitt werden wir uns speziell auf den "Scatter Plot" konzentrieren. Aber was zur Hölle ist ein Scatter Plot? Nun, es ist keine wilde Geschichte über verstreute Flecken oder verängstigte Punkte - keine Sorge! Ein Scatter Plot ist ein Diagramm, das uns hilft, den Zusammenhang zwischen zwei Variablen zu visualisieren. 

In diesem Tutorial werden wir lernen, wie man Scatter Plots erstellt, um Datenpunkte zu analysieren und Muster darin zu entdecken. Mit Matplotlib können wir unsere Ergebnisse in Form von farbenfrohen und anschaulichen Grafiken präsentieren. Es ist wie ein Malbuch für Datenwissenschaftler, nur ohne die Notwendigkeit, zwischen den Linien zu bleiben!

## Theorie

### Grundlagen des Scatter Plots
Bevor wir in den Code eintauchen, lass uns einen kurzen Blick auf die Theorie hinter dem Scatter Plot werfen. Ein Scatter Plot verwendet zwei Achsen, um Datenpunkte in einem Koordinatensystem darzustellen. Eine Achse repräsentiert eine Variable, während die andere Achse die andere Variable darstellt. Jeder Datenpunkt wird dann durch seine Position auf dem Diagramm repräsentiert.

Ein generelles Code-Beispiel sieht folgendermaßen aus:
```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 5, 8, 2, 7]

plt.scatter(x, y)
plt.show()
```

Schauen wir uns ein konkretes Beispiel an, um das Ganze besser zu verstehen. Angenommen, wir möchten den Zusammenhang zwischen der Anzahl der Stunden, die Studierende für das Lernen aufwenden, und ihren Noten untersuchen. Hier ist der Python-Code für unseren Scatter Plot:

```python
import matplotlib.pyplot as plt

study_hours = [2, 4, 6, 8, 10]
grades = [65, 70, 75, 80, 85]

plt.scatter(study_hours, grades)
plt.xlabel("Stunden zum Lernen")
plt.ylabel("Noten")
plt.title("Beziehung zwischen Lernstunden und Noten")
plt.show()
```

In diesem Beispiel haben wir die Stunden, die für das Lernen aufgewendet wurden, auf der x-Achse und die Noten auf der y-Achse. Die Punkte auf dem Scatter Plot zeigen uns nun, wie sich die Noten in Abhängigkeit von den Lernstunden verändern.

### Explizites Code-Beispiel für Scatter Plot mit Anpassungen
Aber warten wir, wir können noch mehr Spaß haben! Wir können unseren Scatter Plot anpassen und ihm einen persönlichen Touch verleihen. Hier ist ein weiteres Beispiel, in dem wir Farben, Markergrößen und Legenden hinzufügen:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 5, 8, 2, 7]
colors = ["r", "g", "b", "c", "m"]
sizes = [30, 80, 120, 200, 300]
labels = ["A", "B", "C", "D", "E"]

plt.scatter(x, y, c=colors, s=sizes, label=labels)
plt.xlabel("X-Achse")
plt.ylabel("Y-Achse")
plt.title("Ein fantastischer Scatter Plot")
plt.legend()
plt.show()
```

In diesem Beispiel haben wir jedem Punkt eine eigene Farbe (rot, grün, blau, cyan, magenta) und Größe zugewiesen. Außerdem haben wir eine Legende hinzugefügt, um zu zeigen, welche Punkte zu welchen Labels gehören. Das ist doch wirklich schick, oder?

## Praxis
Genug Theorie, lass uns jetzt in die Praxis übergehen! Wir haben zwei Aufgaben für dich vorbereitet, um dein frisch erlerntes Wissen zu testen.

### Aufgabe 1
Erstelle einen Scatter Plot, der die Beziehung zwischen der Anzahl der Stunden, die du Videospiele spielst, und der Anzahl der Pizzen, die du isst, zeigt. Verwende die folgenden Daten:

```python
import matplotlib.pyplot as plt

game_hours = [1, 2, 3, 4, 5]
pizzas = [2, 4, 6, 8, 10]

# Dein Code hier

plt.xlabel("Stunden Videospiele")
plt.ylabel("Anzahl der Pizzen")
plt.title("Beziehung zwischen Videospielzeit und Pizzaverzehr")
plt.show()
```

Keine Sorge, wir haben auch die Musterlösungen für dich vorbereitet. Aber versuche erst, die Aufgaben selbst zu lösen, bevor du dir die Lösungen anschaust!

```python
import matplotlib.pyplot as plt

game_hours = [1, 2, 3, 4, 5]
pizzas = [2, 4, 6, 8, 10]

plt.scatter(game_hours, pizzas)
plt.xlabel("Stunden Videospiele")
plt.ylabel("Anzahl der Pizzen")
plt.title("Beziehung zwischen Videospielzeit und Pizzaverzehr")
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Plottypen/Basic/scatter/ms_aufgabe1.png)

### Aufgabe 2
Du bist ein echter Datenanalyse-Ninja! Erstelle einen Scatter Plot, der die Beziehung zwischen der Anzahl der Stunden, die du für die Vorbereitung auf deine Prüfungen aufwendest, und deinen Noten zeigt. Verwende die folgenden Daten:

```python
import matplotlib.pyplot as plt

study_hours = [10, 15, 20, 25, 30]
grades = [70, 80, 85, 90, 95]

# Dein Code hier

plt.xlabel("Stunden für Prüfungsvorbereitung")
plt.ylabel("Noten")
plt.title("Beziehung zwischen Lernstunden und Noten")
plt.show()
```

Hier sind die Musterlösungen zu der Aufgabe 2:

```python
import matplotlib.pyplot as plt

study_hours = [10, 15, 20, 25, 30]
grades = [70, 80, 85, 90, 95]

plt.scatter(study_hours, grades)
plt.xlabel("Stunden für Prüfungsvorbereitung")
plt.ylabel("Noten")
plt.title("Beziehung zwischen Lernstunden und Noten")
plt.show()
```

Probier sie aus und schau dir die beeindruckenden Scatter Plots an, die du erstellt hast! Wenn du Fragen hast oder etwas nicht verstehst, stehe ich dir gerne zur Verfügung.

## Fazit
Viel Spaß beim Erkunden der faszinierenden Welt der Scatter Plots mit Matplotlib!

## Links / Weiteres Material
### Dokumentation
https://matplotlib.org/stable/plot_types/basic/scatter_plot.html#sphx-glr-plot-types-basic-scatter-plot-py
### W3Schools
https://www.w3schools.com/python/matplotlib_scatter.asp
### YouTube