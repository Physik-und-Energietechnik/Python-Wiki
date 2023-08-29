## Einführung

Herzlich willkommen zum aufregenden Abenteuer in der wundervollen Welt von Matplotlib! In diesem Tutorial werden wir uns mit einem faszinierenden Plot-Typ namens `pcolormesh` beschäftigen. Du fragst dich vielleicht, was das überhaupt ist und wozu man es verwenden kann. Nun, stell dir vor, du könntest Daten auf einer Karte visualisieren oder eine Wärmekarte erstellen, um Muster und Trends zu erkennen. Genau das ermöglicht uns der `pcolormesh` Plot!

## Theorie

Aber bevor wir uns in das bunte Treiben stürzen, lass uns etwas Theorie durchgehen. Der `pcolormesh` Plot ist eine großartige Möglichkeit, zweidimensionale Daten zu visualisieren. Er erstellt eine Gitterdarstellung, bei der jeder Punkt in diesem Gitter eine Farbe basierend auf dem Wert des entsprechenden Datenpunkts hat. Das klingt ein bisschen wie Malen nach Zahlen, oder?

Um dir eine Vorstellung davon zu geben, wie das aussieht, werfen wir einen Blick auf ein allgemeines Beispiel. Angenommen, wir haben eine 3x3-Matrix mit einigen Werten:

```python
import matplotlib.pyplot as plt
import numpy as np

data = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

plt.pcolormesh(data)
plt.colorbar()
plt.show()
```

Das Ergebnis wird dich umhauen! Du wirst eine schöne Rasterdarstellung mit verschiedenen Farben sehen, die jedem Wert in der Matrix entsprechen.

Jetzt, da wir das allgemeine Konzept verstanden haben, lassen uns ein spezifisches Beispiel betrachten. Angenommen, du hast die Temperaturdaten von verschiedenen Standorten gesammelt und möchtest diese Daten auf einer Karte anzeigen. Hier ist ein Beispiel, das dir zeigt, wie es gemacht wird:

```python
import matplotlib.pyplot as plt
import numpy as np

# Koordinaten der Standorte
lats = np.array([51.5074, 40.7128, 34.0522])
lons = np.array([-0.1278, -74.0060, -118.2437])

# Temperaturdaten an den Standorten
temps = np.array([22.5, 18.9, 26.1])

# Kartenplot mit `pcolormesh`
plt.figure(figsize=(8, 6))
plt.scatter(lons, lats, c=temps, cmap='coolwarm')
plt.colorbar(label='Temperatur (°C)')
plt.xlabel('Längengrad')
plt.ylabel('Breitengrad')
plt.title('Temperaturverteilung')
plt.grid(True)
plt.show()
```

Schau dir das an! Du hast gerade deine Temperaturdaten auf einer Karte visualisiert. Das ist doch ziemlich cool, oder?

## Praxis

Jetzt ist es an der Zeit, dein erlangtes Wissen in die Praxis umzusetzen. Mach dir keine Sorgen, wir haben zwei Aufgaben für dich vorbereitet, eine leichte und eine schwerere. Du kannst gerne herumexperimentieren und deine Kreativität einfließen lassen!

### Aufgabe 1

Erstelle eine 5x5-Matrix mit Zufallswerten zwischen 0 und 1 und visualisiere sie mit einem `pcolormesh` Plot.

**Musterlösung:**

```python
import matplotlib.pyplot as plt
import numpy as np

data = np.random.rand(5, 5)

plt.pcolormesh(data)
plt.colorbar()
plt.show()
```
![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Plottypen/Array_Fields/pcolormesh/ms_aufgabe1.png)

### Aufgabe 2

Angenommen, du bist ein Biologe, der die Verteilung von verschiedenen Pflanzenarten in einem bestimmten Ökosystem untersucht. Du hast Daten über die relative Häufigkeit dieser Pflanzenarten in verschiedenen Regionen des Ökosystems gesammelt. Deine Aufgabe ist es nun, diese Daten mithilfe von pcolormesh in Form einer Farbdarstellung zu visualisieren. Dabei soll jede Pflanzenart durch eine bestimmte Farbe repräsentiert werden, und die X- und Y-Koordinaten auf der Karte sollen die verschiedenen Regionen des Ökosystems darstellen.

Hier ist eine beispielhafte Musterlösung, die du als Ausgangspunkt verwenden kannst:

**Musterlösung:**

```python
import matplotlib.pyplot as plt
import numpy as np

# Simulierte Pflanzenartendaten (Beispielwerte)
# Zeilen repräsentieren Regionen, Spalten repräsentieren Pflanzenarten
plant_data = np.array([
    [0.1, 0.3, 0.5, 0.1],
    [0.4, 0.2, 0.2, 0.2],
    [0.2, 0.1, 0.6, 0.1],
    [0.3, 0.4, 0.1, 0.2]
])

# Farbcodes für Pflanzenarten
cmap = plt.get_cmap('tab20')  # Verwende eine vordefinierte Farbpalette
colors = cmap(np.linspace(0, 1, plant_data.shape[1]))

# Erstelle X- und Y-Koordinaten für die Regionen
x_coords = np.arange(plant_data.shape[0])
y_coords = np.arange(plant_data.shape[1])
X, Y = np.meshgrid(x_coords, y_coords)

# Verwende pcolormesh, um die Pflanzenartendaten darzustellen
plt.pcolormesh(X, Y, plant_data, cmap=cmap)
plt.colorbar(label='Relative Häufigkeit')
plt.title('Verteilung von Pflanzenarten im Ökosystem')
plt.xlabel('Region')
plt.ylabel('Pflanzenart')
plt.xticks(x_coords, ['Region 1', 'Region 2', 'Region 3', 'Region 4'])
plt.yticks(y_coords, ['Art A', 'Art B', 'Art C', 'Art D'])
plt.show()
```
![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Plottypen/Array_Fields/pcolormesh/ms_aufgabe2.png)

## Fazit
Wir hoffen, du hattest Spaß beim Erkunden des `pcolormesh` Plots! Diese einfache, aber mächtige Visualisierungstechnik wird dir sicherlich dabei helfen, Daten auf eine völlig neue Art und Weise zu betrachten. Viel Erfolg beim Experimentieren und Erkunden weiterer Matplotlib-Plots!

## Links / Weiteres Material
### Dokumentation
https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.pcolormesh.html