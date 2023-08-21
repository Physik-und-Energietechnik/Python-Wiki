## Einführung
In diesem Tutorial dreht sich alles um den 3D Scatterplot mit Matplotlib. Aber Moment, was ist ein Scatterplot überhaupt? Nun, es ist im Grunde genommen ein Diagramm, das Punkte in einem Koordinatensystem darstellt. Stell dir vor, du hast Daten über die Größe von Dinosauriern und deren Gehgeschwindigkeit. Mit einem 2D Scatterplot kannst du sie auf eine Fläche projizieren und schauen, ob es da draußen einen schnellen und riesigen T-Rex gab. Doch was ist, wenn du eine zusätzliche Dimension hast, wie zum Beispiel das Gewicht? Hier kommt der 3D Scatterplot ins Spiel!

In diesem Tutorial werden wir lernen, wie wir mit Matplotlib beeindruckende 3D Scatterplots erstellen können. Du wirst lernen, wie du Datenpunkte in einem dreidimensionalen Raum visualisierst, um komplexe Zusammenhänge zu entdecken. Außerdem wirst du sehen, wie vielseitig diese Art der Darstellung ist, sei es für wissenschaftliche Visualisierungen, Datenanalyse oder einfach nur zum Spaß!

## Theorie

### Grundlagen des 3D Scatterplots
Um einen 3D Scatterplot zu erstellen, benötigen wir drei Dimensionen: x, y und z. Stell dir diese Dimensionen als die Achsen eines Würfels vor. Die x- und y-Achsen repräsentieren die horizontale und vertikale Position eines Punktes, während die z-Achse die Höhe darstellt. Jeder Punkt im Scatterplot hat also eine eindeutige x-, y- und z-Koordinate.

Hier ist ein einfaches Code-Beispiel, um dir die Grundlagen zu verdeutlichen:

```python
import matplotlib.pyplot as plt
import numpy as np

# Daten generieren
x = np.random.rand(100)  # x-Koordinaten
y = np.random.rand(100)  # y-Koordinaten
z = np.random.rand(100)  # z-Koordinaten

# Scatterplot erstellen
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.scatter(x, y, z)

# Achsen beschriften
ax.set_xlabel('X-Achse')
ax.set_ylabel('Y-Achse')
ax.set_zlabel('Z-Achse')

# Plot anzeigen
plt.show()
```

Mit diesem Code kannst du 100 zufällige Punkte im dreidimensionalen Raum darstellen. Wenn du den Plot ausführst, kannst du ihn mit der Maus drehen und von verschiedenen Blickwinkeln betrachten. Spannend, oder?

### Fortgeschrittene Anpassungen
Der 3D Scatterplot bietet viele Möglichkeiten zur Anpassung, um deine Visualisierung beeindruckender zu gestalten. Du kannst die Größe und Farbe der Punkte ändern, Achsenbeschriftungen hinzufügen, den Hintergrund anpassen und vieles mehr! Lass uns einen Blick auf ein spezifisches Beispiel werfen:

```python
import matplotlib.pyplot as plt
import numpy as np

# Daten generieren
x = np.random.rand(100)
y = np.random.rand(100)
z = np.random.rand(100)
colors = np.random.rand(100) 

 # Farben der Punkte (zufällig generiert)

# Scatterplot erstellen und anpassen
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.scatter(x, y, z, c=colors, s=50, alpha=0.6)  # Anpassung der Punktgröße, Farbe und Transparenz

# Achsenbeschriftungen
ax.set_xlabel('X-Achse')
ax.set_ylabel('Y-Achse')
ax.set_zlabel('Z-Achse')

# Hintergrund anpassen
ax.set_facecolor('black')

# Plot anzeigen
plt.show()
```

In diesem Beispiel haben wir den 3D Scatterplot mit individuellen Punktgrößen, zufälligen Farben und einem dunklen Hintergrund angepasst. Du kannst diese Anpassungen nach Belieben ändern, um deinen eigenen einzigartigen Plot zu erstellen!

## Praxis
### Aufgabe 1
Okay, genug Theorie! Lass uns dein Wissen in die Tat umsetzen. Deine Aufgabe besteht darin, einen 3D Scatterplot zu erstellen, der die Temperatur, den Luftdruck und die Windgeschwindigkeit an verschiedenen Orten darstellt. Hier sind die Daten für dich:

```python
import matplotlib.pyplot as plt
import numpy as np

# Daten
temperature = np.random.uniform(15, 35, 100)  # Temperatur in Celsius
pressure = np.random.uniform(900, 1100, 100)  # Luftdruck in hPa
wind_speed = np.random.uniform(0, 20, 100)  # Windgeschwindigkeit in km/h

# Scatterplot erstellen
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.scatter(temperature, pressure, wind_speed)

# Achsenbeschriftungen
ax.set_xlabel('Temperatur (°C)')
ax.set_ylabel('Luftdruck (hPa)')
ax.set_zlabel('Windgeschwindigkeit (km/h)')

# Plot anzeigen
plt.show()
```

Führe den Code aus und bewundere deinen eigenen 3D Scatterplot mit Wetterdaten! Verändere die Blickwinkel und erkunde, ob du irgendwelche Zusammenhänge entdecken kannst.

### Aufgabe 2
Du hast die leichte Aufgabe gemeistert? Bravo! Jetzt wird es etwas schwieriger. Deine nächste Herausforderung besteht darin, einen 3D Scatterplot zu erstellen, der die Beziehung zwischen Alter, Einkommen und Ausgaben darstellt. Hier sind die Daten:

```python
import matplotlib.pyplot as plt
import numpy as np

# Daten
age = np.random.randint(18, 65, 200)  # Alter in Jahren
income = np.random.normal(40000, 15000, 200)  # Einkommen in USD
expenses = np.random.normal(25000, 10000, 200)  # Ausgaben in USD

# Scatterplot erstellen
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.scatter(age, income, expenses)

# Achsenbeschriftungen
ax.set_xlabel('Alter')
ax.set_ylabel('Einkommen (USD)')
ax.set_zlabel('Ausgaben (USD)')

# Plot anzeigen
plt.show()
```
Versuche, die Beziehung zwischen Alter, Einkommen und Ausgaben zu erkennen. Gibt es vielleicht einen bestimmten Lebensabschnitt, in dem die Ausgaben höher sind als das Einkommen? Experimentiere mit verschiedenen Blickwinkeln und finde es heraus!

## Fazit
Herzlichen Glückwunsch, du hast gerade die magische Welt der 3D Scatterplots mit Matplotlib betreten! Mit diesem mächtigen Werkzeug kannst du Daten auf eine ganz neue Art und Weise visualisieren und versteckte Muster enthüllen. Es gibt noch viel mehr zu entdecken, also erkunde weiter und habe Spaß beim Programmieren!

## Links / Weiteres Material
### W3Schools
### YouTube