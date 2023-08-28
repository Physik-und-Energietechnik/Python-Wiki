## Einführung

In diesem Tutorial wirst du lernen, wie du schöne und informative Konturplots erstellst, die deine Daten zum Leben erwecken. Matplotlib ist eine mächtige Python-Bibliothek zur Visualisierung von Daten und mit dem contourf Plot kannst du komplexe Muster und Zusammenhänge in deinen Daten entdecken.

Nach Abschluss dieses Tutorials wirst du in der Lage sein, atemberaubende Konturplots zu erstellen und verstehen, wie du sie zur Darstellung verschiedener Arten von Daten verwenden kannst. Du wirst lernen, wie du Farbverläufe nutzt, um die Intensität von Werten darzustellen, und wie du das Erscheinungsbild deiner Plots an deine Bedürfnisse anpasst.

Bist du bereit, die Welt der Konturplots zu erkunden? Lass uns loslegen!

## Theorie

### Was ist ein Konturplot?

Ein Konturplot ist eine Art von 2D-Darstellung, die die Verteilung oder die Veränderung eines Wertes über eine Fläche visualisiert. Der plot besteht aus Linien oder Flächen, die sogenannte Konturlinien oder Konturflächen bilden. Diese Linien oder Flächen haben unterschiedliche Farben oder Intensitäten, um den Wert zu repräsentieren, den sie darstellen.

### Code-Beispiel: Konturplot mit allgemeinen Daten

Um dir eine Vorstellung davon zu geben, wie ein Konturplot aussehen kann, schauen wir uns ein einfaches Beispiel an. Angenommen, wir haben folgende Daten:

```
X = [1, 2, 3, 4]
Y = [1, 2, 3, 4]
Z = [[0, 0, 0, 0],
     [0, 1, 1, 0],
     [0, 1, 1, 0],
     [0, 0, 0, 0]]
```

Hier ist ein Code-Beispiel, wie du einen Konturplot mit diesen Daten erstellen kannst:

```python
import matplotlib.pyplot as plt

X = [1, 2, 3, 4]
Y = [1, 2, 3, 4]
Z = [[0, 0, 0, 0],
     [0, 1, 1, 0],
     [0, 1, 1, 0],
     [0, 0, 0, 0]]

plt.contourf(X, Y, Z)
plt.colorbar()
plt.show()
```

Wenn du diesen Code ausführst, solltest du einen Konturplot mit einem Quadrat sehen, das von einer Kontur umgeben ist. Die Farbe des Quadrats zeigt an, dass der Wert in diesem Bereich 1 ist, während die Kontur die Grenze darstellt.

### Code-Beispiel: Konturplot mit echten Daten

Natürlich werden wir normalerweise mit komplexeren Daten arbeiten. Hier ist ein Beispiel, wie du einen Konturplot mit echten Daten erstellen kannst. Angenommen, du hast zwei NumPy-Arrays `X` und `Y`, die die Koordinaten der Punkte auf der X- und Y-Achse repräsentieren, sowie ein 2D-Array `Z`, das die zugehörigen Werte enthält:

```python
import numpy as np
import matplotlib.pyplot as plt

# Erstelle Beispieldaten
x = np.linspace(-5, 5, 100)
y = np.linspace(-5, 5, 100)
X, Y = np.meshgrid(x, y)
Z = np.sin(np.sqrt(X**2 + Y**2))

# Erstelle Konturplot
plt.contourf(X, Y, Z, cmap='viridis')
plt.colorbar()
plt.xlabel('X')
plt.ylabel('Y')
plt.title('Konturplot von sin(sqrt(X^2 + Y^2))')
plt.show()
```

In diesem Beispiel verwenden wir die NumPy-Funktionen `linspace` und `meshgrid`, um ein Gitter von Koordinaten zu erstellen, und die mathematische Funktion `sin`, um die Werte für den Konturplot zu berechnen. Der Konturplot wird dann mit `contourf` erstellt und mit `cmap='viridis'` wählen wir den Farbverlauf für die Darstellung aus.

## Praxis

### Aufgabe 1

Deine erste Aufgabe besteht darin, einen Konturplot für die Funktion `f(x, y) = x^2 + y^2` zu erstellen. Verwende dazu die `linspace`-Funktion von NumPy, um Werte für `x` und `y` zu generieren, und berechne dann die Werte für `Z`. Erstelle den Konturplot mit einem geeigneten Farbverlauf und beschrifte die Achsen. Viel Erfolg!

#### Musterlösung

Hier ist eine mögliche Lösung für die Aufgabe:

```python
import numpy as np
import matplotlib.pyplot as plt

# Erstelle Beispieldaten
x = np.linspace(-5, 5, 100)
y = np.linspace(-5, 5, 100)
X, Y = np.meshgrid(x, y)
Z = X**2 + Y**2

# Erstelle Konturplot
plt.contourf(X, Y, Z, cmap='cool')
plt.colorbar()
plt.xlabel('X')
plt.ylabel('Y')
plt.title('Konturplot von x^2 + y^2')
plt.show()
```
![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Plottypen/Array_Fields/contourf/ms_aufgabe1.png)

Wenn du den Code ausführst, solltest du einen Konturplot sehen, der eine konzentrische Kreisstruktur zeigt.

### Aufgabe 2

Jetzt wird es etwas herausfordernder! Deine Aufgabe besteht darin, einen Konturplot für die Funktion `f(x, y) = sin(x) * cos(y)` zu erstellen. Verwende NumPy, um Werte für `x` und `y` zu generieren, und berechne die entsprechenden `Z`-Werte. Stelle den Konturplot mit einem Farbverlauf deiner Wahl dar und gib ihm eine aussagekräftige Beschriftung.

#### Musterlösung

Hier ist eine mögliche Lösung für die schwierigere Aufgabe:

```python
import numpy as np
import matplotlib.pyplot as plt

# Erstelle Beispieldaten
x = np.linspace(-np.pi, np.pi, 100)
y = np.linspace(-np.pi, np.pi, 100)
X, Y = np.meshgrid(x, y)
Z = np.sin(X) * np.cos(Y)

# Erstelle Konturplot
plt.contourf(X, Y, Z, cmap='seismic')
plt.colorbar()
plt.xlabel('X')
plt.ylabel('Y')
plt.title('Konturplot von sin(x) * cos(y)')
plt.show()
```
![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Plottypen/Array_Fields/contourf/ms_aufgabe2.png)

Wenn du den Code ausführst, solltest du einen Konturplot sehen, der die Oszillationen der Funktion `sin(x) * cos(y)` in verschiedenen Farben darstellt.

## Fazit
Herzlichen Glückwunsch zu deinen Fortschritten bei der Erstellung von Konturplots in Matplotlib! Du bist nun in der Lage, Daten auf neue und spannende Weise zu visualisieren. Keep up the good work!

## Links / Weiteres Material
### Dokumentation
https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.contourf.html