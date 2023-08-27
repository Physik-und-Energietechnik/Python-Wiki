## Einführung

Willkommen zum Python-Tutorial über das Hinzufügen von Hintergrundbildern und Gatterlinien in Matplotlib! In diesem Abschnitt werden wir lernen, wie wir mit Matplotlib, einer Python-Bibliothek zur Visualisierung von Daten, Hintergrundbilder und Gatterlinien in Diagrammen hinzufügen können.

Durch das Hinzufügen von Hintergrundbildern und Gatterlinien können wir unsere Diagramme noch interessanter gestalten und wichtige Informationen betonen.


## Theorie

### Hintergrundbilder

Ein Hintergrundbild ist ein Bild, das als Hintergrund in einem Diagramm angezeigt wird. Es kann beispielsweise ein Foto, eine Textur oder eine Grafik sein. Mit Matplotlib können wir ein Hintergrundbild hinzufügen, um unseren Diagrammen eine persönliche Note zu verleihen.

Um ein Hintergrundbild hinzuzufügen, müssen wir zuerst das Bild in Matplotlib laden und dann das Bildobjekt als Hintergrund für das Diagramm festlegen. Hier ist ein allgemeines Code-Beispiel, um dir eine Vorstellung davon zu geben:

```python
import matplotlib.pyplot as plt
import matplotlib.image as mpimg

# Bild laden
img = mpimg.imread('hintergrundbild.png')

# Diagramm erstellen
plt.figure(figsize=(10, 6))

# Hintergrundbild festlegen
plt.imshow(img, extent=[0, 10, 0, 6])

# Diagramm anzeigen
plt.show()
```

Hier ist ein explizites Code-Beispiel, um das Hintergrundbild in einem Balkendiagramm anzuzeigen:

```python
import matplotlib.pyplot as plt
import matplotlib.image as mpimg
import numpy as np

# Bild laden
img = mpimg.imread('hintergrundbild.png')

# Daten für das Balkendiagramm
categories = ['A', 'B', 'C', 'D', 'E']
values = [3, 7, 2, 6, 5]

# Diagramm erstellen
plt.figure(figsize=(8, 6))

# Hintergrundbild festlegen
plt.imshow(img, extent=[0, 10, 0, 8], alpha=0.5)

# Balkendiagramm erstellen
plt.bar(categories, values)

# Diagramm anzeigen
plt.show()
```

### Gatterlinien

Gatterlinien sind horizontale und vertikale Linien, die das Diagramm in regelmäßige Gitterzellen unterteilen. Sie helfen uns, die Daten im Diagramm leichter abzulesen und zu interpretieren. Matplotlib ermöglicht es uns, Gatterlinien hinzuzufügen und sie an unsere Bedürfnisse anzupassen.

Um Gatterlinien hinzuzufügen, verwenden wir die `grid()`-Funktion von Matplotlib. Diese Funktion akzeptiert verschiedene Parameter, mit denen wir das Erscheinungsbild der Gatterlinien steuern können. Hier ist ein allgemeines Code-Beispiel:


```python
import matplotlib.pyplot as plt

# Diagramm erstellen
plt.figure(figsize=(8, 6))

# Gatterlinien hinzufügen
plt.grid(True)

# Daten plotten
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]
plt.plot(x, y)

# Diagramm anzeigen
plt.show()
```

Hier ist ein explizites Code-Beispiel, um Gatterlinien in einem Scatterplot hinzuzufügen:

```python
import matplotlib.pyplot as plt
import numpy as np

# Diagramm erstellen
plt.figure(figsize=(8, 6))

# Gatterlinien hinzufügen
plt.grid(True, linestyle='--', linewidth=0.5, alpha=0.7)

# Daten plotten
x = np.random.rand(100)
y = np.random.rand(100)
plt.scatter(x, y)

# Diagramm anzeigen
plt.show()
```

## Praxis

Jetzt ist es Zeit, das erlernte Wissen in die Praxis umzusetzen! Lass uns zwei Aufgaben durchgehen - eine leichte und eine etwas schwierigere. Du kannst die Musterlösungen verwenden, um deine Ergebnisse zu überprüfen.

### Aufgabe 1

Erstelle ein Liniendiagramm, das den Verlauf der Temperatur über eine Woche hinweg darstellt. Füge ein Hintergrundbild hinzu, das eine sonnige Landschaft zeigt.

Musterlösung:

```python
import matplotlib.pyplot as plt
import matplotlib.image as mpimg
import numpy as np

# Hintergrundbild laden
img = mpimg.imread('sonnige_landschaft.png')

# Temperaturdaten
days = np.arange(1, 8)
temperature = np.array([25, 26, 28, 30, 29, 27, 26])

# Diagramm erstellen
plt.figure(figsize=(8, 6))

# Hintergrundbild festlegen
plt.imshow(img, extent=[0, 8, 20, 32], alpha=0.5)

# Liniendiagramm erstellen
plt.plot(days, temperature)

# Achsenbeschriftungen
plt.xlabel('Tage')
plt.ylabel('Temperatur (°C)')

# Diagramm anzeigen
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Anpassungen_und_Stilisierung/Hinzufuegen_von_Hintergrundbildern_und_Gatterlinien/ms_aufgabe1.png)

### Aufgabe 2

Erstelle ein gestapeltes Flächendiagramm, das den Anteil von Äpfeln, Bananen und Orangen am Gesamtobstverbrauch darstellt. Passe die Gatterlinien so an, dass sie gestrichelt und transparent sind.

Musterlösung:

```python
import matplotlib.pyplot as plt

# Daten für das gestapelte Flächendiagramm
fruits = ['Äpfel', 'Bananen', 'Orangen']
consumption = [30, 45, 25]

# Diagramm erstellen
plt.figure(figsize=(8, 6))

# Gatterlinien anpassen
plt.grid(True, linestyle='--', linewidth=0.5, alpha=0.5)

# Gestapeltes Flächendiagramm erstellen
plt.stackplot(fruits, consumption)

# Achsenbeschriftungen
plt.xlabel('Obstsorten')
plt.ylabel('Verbrauch (kg)')

# Diagramm anzeigen
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Anpassungen_und_Stilisierung/Hinzufuegen_von_Hintergrundbildern_und_Gatterlinien/ms_aufgabe2.png)

## Fazit
Herzlichen Glückwunsch! Du hast erfolgreich gelernt, wie man Hintergrundbilder und Gatterlinien in Matplotlib verwendet. Experimentiere weiter und entdecke die vielfältigen Möglichkeiten, die Matplotlib bietet, um deine Diagramme zu verbessern und deine Daten zu visualisieren. Viel Spaß beim Coden!