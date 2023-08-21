# Matplotlib - Arbeiten mit mehreren Achsen

## Einführung

Herzlich willkommen zum Tutorial über das Arbeiten mit mehreren Achsen in Matplotlib! In diesem Abschnitt werden wir uns mit einer wichtigen Funktion von Matplotlib beschäftigen, die es uns ermöglicht, mehrere Achsen in einem Diagramm zu verwenden. Dieses Wissen ist besonders nützlich, um komplexe Visualisierungen zu erstellen und unterschiedliche Datensätze miteinander zu vergleichen.

Nachdem du dieses Tutorial abgeschlossen hast, wirst du in der Lage sein, mehrere Achsen in Matplotlib-Diagrammen zu erstellen und diese für verschiedene Zwecke einzusetzen. Du wirst lernen, wie du Diagramme mit verschiedenen Skalen, Einheiten und Ausrichtungen erstellen kannst, um deine Daten bestmöglich darzustellen.

## Theorie

Bevor wir in die Praxis einsteigen, werfen wir einen Blick auf die theoretischen Grundlagen des Arbeitens mit mehreren Achsen in Matplotlib. Zunächst einmal: Was ist eine Achse? In einem Diagramm repräsentiert eine Achse die x- oder y-Dimension und wird verwendet, um die Daten darzustellen.

### Subplots erstellen

In Matplotlib können wir Subplots erstellen, die aus mehreren Achsen bestehen. Ein Subplot ist ein Raster aus Achsen, das es uns ermöglicht, mehrere Diagramme innerhalb eines einzigen Figure-Objekts darzustellen. Um einen Subplot zu erstellen, verwenden wir die Funktion `plt.subplots()`. Hier ist ein allgemeines Beispiel:

```python
import matplotlib.pyplot as plt

# Subplot mit 2 Zeilen und 2 Spalten erstellen
fig, axes = plt.subplots(nrows=2, ncols=2)

# Die erstellten Achsen verwenden
ax1 = axes[0, 0]
ax2 = axes[0, 1]
ax3 = axes[1, 0]
ax4 = axes[1, 1]

# Weitere Anpassungen und Plots durchführen
# ...

# Diagramme anzeigen
plt.show()
```

### Achsen anpassen

Sobald wir unsere Achsen erstellt haben, können wir sie individuell anpassen. Wir können die Skala und Einheiten der Achsen ändern, Beschriftungen hinzufügen und vieles mehr. Hier ist ein Beispiel, wie du die Achsen deines Diagramms anpassen kannst:

```python
import matplotlib.pyplot as plt

fig, ax = plt.subplots()

# Achsenbeschriftungen hinzufügen
ax.set_xlabel('X-Achse')
ax.set_ylabel('Y-Achse')

# Achsenskala ändern
ax.set_xscale('log')
ax.set_yscale('log')

# Achsenticks anpassen
ax.set_xticks([1, 10, 100])
ax.set_yticks([0.1, 1, 10])

# Achsentick-Labels anpassen
ax.set_xticklabels(['Eins', 'Zehn', 'Hundert'])
ax.set_yticklabels(['0.1', '1', '10'])

# Weitere Anpassungen und Plots durchführen
# ...

# Diagramm anzeigen
plt.show()
```

## Praxis

Jetzt ist es an der Zeit, das erlernte Wissen in die Praxis umzusetzen. Wir werden eine leichte und eine schwerere Aufgabe haben, um deine Fähigkeiten zu testen.

### Aufgabe 1: Temperaturvergleich

Erstelle ein Diagramm, das die Temperaturverläufe von zwei Städten vergleicht. Verwende dafür zwei Achsen, um die Temperaturen über die Zeit darzustellen. Hier ist ein Beispiel, wie du das machen könntest:

```python
import matplotlib.pyplot as plt

# Daten für die Temperaturen
tage = [1, 2, 3, 4, 5]
stadt1_temps = [25, 26, 28, 30, 27]
stadt2_temps = [22, 24, 26, 28, 25]

# Subplot mit zwei Achsen erstellen
fig, ax1 = plt.subplots()
ax2 = ax1.twinx()

# Linienplots erstellen
ax1.plot(tage, stadt1_temps, 'r-', label='Stadt 1')
ax2.plot(tage, stadt2_temps, 'b-', label='Stadt 2')

# Achsenbeschriftungen hinzufügen
ax1.set_xlabel('Tage')
ax1.set_ylabel('Temperatur (Stadt 1)')
ax2.set_ylabel('Temperatur (Stadt 2)')

# Legende hinzufügen
ax1.legend(loc='upper left')
ax2.legend(loc='upper right')

# Diagramm anzeigen
plt.show()
```

### Aufgabe 2: Umsatzanalyse

Erstelle ein Balkendiagramm, das den Umsatz von drei Produkten für verschiedene Monate darstellt. Verwende dafür drei Achsen, um die Umsätze getrennt darzustellen. Hier ist ein Beispiel, wie du das machen könntest:

```python
import matplotlib.pyplot as plt
import numpy as np

# Daten für den Umsatz
monate = ['Jan', 'Feb', 'März', 'April', 'Mai']
produkt1_umsatz = [10000, 12000, 8000, 15000, 9000]
produkt2_umsatz = [8000, 11000, 9000, 12000, 10000]
produkt3_umsatz = [12000, 9000, 10000, 11000, 8000]

# Subplot mit drei Achsen erstellen
fig, (ax1, ax2, ax3) = plt.subplots(nrows=3, sharex=True)

# Balkendiagramme erstellen
ax1.bar(monate, produkt1_umsatz, label='Produkt 1')
ax2.bar(monate, produkt2_umsatz, label='Produkt 2')
ax3.bar(monate, produkt3_umsatz, label='Produkt 3')

# Achsenbeschriftungen hinzufügen
ax3.set_xlabel('Monate')
ax1.set_ylabel('Umsatz (Produkt 1)')
ax2.set_ylabel('Umsatz (Produkt 2)')
ax3.set_ylabel('Umsatz (Produkt 3)')

# Legende hinzufügen
ax1.legend()
ax2.legend()
ax3.legend()

# Diagramm anzeigen
plt.show()
```

Gut gemacht! Du hast nun gelernt, wie du mit Matplotlib mehrere Achsen verwenden kannst. Du bist bereit, beeindruckende Diagramme zu erstellen und deine Daten noch besser zu visualisieren. Experimentiere weiter, probiere neue Ideen aus und habe Spaß beim Erkunden der Möglichkeiten, die Matplotlib bietet!