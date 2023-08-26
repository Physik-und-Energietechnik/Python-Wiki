## Matplotlib - Der `pcolormesh` Plot

### Einführung

Herzlich willkommen zum aufregenden Abenteuer in der wundervollen Welt von Matplotlib! In diesem Tutorial werden wir uns mit einem faszinierenden Plot-Typ namens `pcolormesh` beschäftigen. Du fragst dich vielleicht, was das überhaupt ist und wozu man es verwenden kann. Nun, stell dir vor, du könntest Daten auf einer Karte visualisieren oder eine Wärmekarte erstellen, um Muster und Trends zu erkennen. Genau das ermöglicht uns der `pcolormesh` Plot!

### Theorie

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

### Praxis

Jetzt ist es an der Zeit, dein erlangtes Wissen in die Praxis umzusetzen. Mach dir keine Sorgen, wir haben zwei Aufgaben für dich vorbereitet, eine leichte und eine schwerere. Du kannst gerne herumexperimentieren und deine Kreativität einfließen lassen!

**Aufgabe 1:**

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

**Aufgabe 2:**

Du hast eine CSV-Datei mit den Ergebnissen eines Spiels. Die CSV-Datei enthält eine 10x10-Matrix, wobei jeder Wert den Spielstand an einer bestimmten Position im Spiel repräsentiert. Lies die Daten aus der CSV-Datei ein und visualisiere sie mit einem `pcolormesh` Plot.

**Musterlösung:**

```python
import matplotlib.pyplot as plt
import numpy as np
import csv

data = []
with open('spielstand.csv', 'r') as csvfile:
    csvreader = csv.reader(csvfile)
    for row in csvreader:
        data.append([float(value) for value in row])

data = np.array(data)

plt.pcolormesh(data)
plt.colorbar()
plt.show()

# Da sich die jeweilige CSV-Datei unterscheiden kann, gibt es natürlich keine konkrete Lösung als Bild.
```

## Fazit
Wir hoffen, du hattest Spaß beim Erkunden des `pcolormesh` Plots! Diese einfache, aber mächtige Visualisierungstechnik wird dir sicherlich dabei helfen, Daten auf eine völlig neue Art und Weise zu betrachten. Viel Erfolg beim Experimentieren und Erkunden weiterer Matplotlib-Plots!

## Links / Weiteres Material
### Dokumentation
https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.pcolormesh.html