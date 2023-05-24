# Matplotlib - Kombinieren verschiedener Plot-Typen in einem Subplot

## Einführung

Willkommen zum Python-Tutorial über die Kombination verschiedener Plot-Typen in einem Subplot mit Matplotlib! In diesem Tutorial werden wir lernen, wie wir unsere Daten auf kreative und informative Weise visualisieren können.

Hast du jemals versucht, verschiedene Arten von Diagrammen nebeneinander darzustellen? Zum Beispiel einen Balken- und einen Liniendiagramm? Mit Matplotlib ist das ganz einfach! Wir werden lernen, wie man Subplots erstellt, um mehrere Plot-Typen auf einer einzigen Figure anzuzeigen. 

Nach Abschluss dieses Tutorials wirst du in der Lage sein, verschiedene Plot-Typen wie Balkendiagramme, Liniendiagramme und Scatterplots zu kombinieren und deine Daten auf eine ansprechende und informative Weise zu visualisieren.

## Theorie

Bevor wir uns in die Praxis stürzen, lassen Sie uns etwas über die Theorie hinter der Kombination verschiedener Plot-Typen in einem Subplot erfahren.

Ein Subplot ist im Grunde genommen ein Raster von Plot-Bereichen, in denen wir verschiedene Diagramme erstellen können. Jeder Bereich kann ein anderes Plot-Element enthalten, wie zum Beispiel ein Balkendiagramm, ein Liniendiagramm oder einen Scatterplot. Durch die Kombination dieser Elemente können wir unsere Daten umfassender analysieren und visualisieren.

Schauen wir uns ein allgemeines Beispiel an, um das Konzept besser zu verstehen:

```python
import matplotlib.pyplot as plt

# Erstelle den Subplot und die Axes-Objekte
fig, axes = plt.subplots(nrows=2, ncols=2)

# Erstes Plot-Element: Balkendiagramm
axes[0, 0].bar([1, 2, 3], [4, 5, 6])

# Zweites Plot-Element: Liniendiagramm
axes[0, 1].plot([1, 2, 3], [4, 5, 6])

# Drittes Plot-Element: Scatterplot
axes[1, 0].scatter([1, 2, 3], [4, 5, 6])

# Viertes Plot-Element: Balkendiagramm
axes[1, 1].barh([1, 2, 3], [4, 5, 6])

# Zeige den Subplot an
plt.show()
```

In diesem Beispiel haben wir einen 2x2-Subplot erstellt und verschiedene Plot-Typen hinzugefügt. Jedes Plot-Element wird mit Hilfe des entsprechenden Axes-Objekts hinzugefügt. Durch die Angabe der Position des Axes-Objekts im Subplot können wir die Diagramme anordnen.

Lass uns nun ein spezifisches Beispiel betrachten, in dem wir Daten zu den Verkaufszahlen von verschiedenen Produkten visualisieren möchten:

```python
import matplotlib.pyplot as plt

# Erstelle den Subplot und die Axes-Objekte
fig, axes = plt.subplots(nrows=1, ncols=2)

# Erstes Plot-Element: Balkendiagramm der Verkaufszahlen
products = ['Produkt A', 'Produkt B', 'Produkt C']
sales = [50, 80, 

120]
axes[0].bar(products, sales)

# Zweites Plot-Element: Liniendiagramm der Umsätze
months = ['Jan', 'Feb', 'März', 'Apr', 'Mai']
revenue = [1000, 1200, 800, 1500, 2000]
axes[1].plot(months, revenue)

# Titel und Beschriftungen hinzufügen
axes[0].set_title('Verkaufszahlen nach Produkt')
axes[0].set_xlabel('Produkte')
axes[0].set_ylabel('Verkaufszahlen')

axes[1].set_title('Umsätze pro Monat')
axes[1].set_xlabel('Monate')
axes[1].set_ylabel('Umsätze in Euro')

# Zeige den Subplot an
plt.tight_layout()
plt.show()
```

In diesem Beispiel haben wir zwei Plot-Elemente hinzugefügt: ein Balkendiagramm der Verkaufszahlen nach Produkt und ein Liniendiagramm der Umsätze pro Monat. Durch die Verwendung von `set_title`, `set_xlabel` und `set_ylabel` können wir den Plots Titel und Beschriftungen hinzufügen, um sie besser zu verstehen.

## Praxis

Jetzt ist es Zeit, das erlernte Wissen in die Praxis umzusetzen! Wir werden zwei Aufgaben haben: eine leichte und eine schwerere. Du kannst deine Lösungen mit den Musterlösungen vergleichen, die am Ende angegeben sind.

### Leichte Aufgabe

Erstelle einen Subplot mit einem Balkendiagramm und einem Liniendiagramm. Das Balkendiagramm soll die Anzahl der verkauften Einheiten pro Tag zeigen, und das Liniendiagramm soll den Umsatz pro Tag anzeigen. Verwende die folgenden Daten:

```python
days = ['Montag', 'Dienstag', 'Mittwoch', 'Donnerstag', 'Freitag']
units_sold = [30, 40, 25, 55, 35]
revenue = [500, 700, 400, 900, 600]
```

### Schwere Aufgabe

Erweitere den Subplot aus der leichten Aufgabe, indem du einen Scatterplot hinzufügst. Der Scatterplot soll das Verhältnis zwischen den verkauften Einheiten und dem Umsatz pro Tag zeigen. Verwende weiterhin die oben genannten Daten.

Viel Spaß beim Codieren!

### Musterlösungen

Hier sind die Musterlösungen für die leichte und die schwere Aufgabe:

**Leichte Aufgabe:**

```python
import matplotlib.pyplot as plt

# Erstelle den Subplot und die Axes-Objekte
fig, axes = plt.subplots(nrows=1, ncols=2)

# Erstes Plot-Element: Balkendiagramm der verkauften Einheiten pro Tag
days = ['Montag', 'Dienstag', 'Mittwoch', 'Donnerstag', 'Freitag']
units_sold = [30, 40, 25, 55, 35]
axes[0].bar(days, units_sold)

# Zweites Plot-Element: Liniendiagramm des Umsatzes pro Tag
revenue = [500, 700, 400, 900, 600]
axes[1].plot(days, revenue)

# Titel und Beschriftungen hinzufügen
axes[0].set_title('Verkaufte Einheiten pro Tag')
axes[0

].set_xlabel('Tage')
axes[0].set_ylabel('Anzahl der verkauften Einheiten')

axes[1].set_title('Umsatz pro Tag')
axes[1].set_xlabel('Tage')
axes[1].set_ylabel('Umsatz in Euro')

# Zeige den Subplot an
plt.tight_layout()
plt.show()
```

**Schwere Aufgabe:**

```python
import matplotlib.pyplot as plt

# Erstelle den Subplot und die Axes-Objekte
fig, axes = plt.subplots(nrows=1, ncols=3)

# Erstes Plot-Element: Balkendiagramm der verkauften Einheiten pro Tag
days = ['Montag', 'Dienstag', 'Mittwoch', 'Donnerstag', 'Freitag']
units_sold = [30, 40, 25, 55, 35]
axes[0].bar(days, units_sold)

# Zweites Plot-Element: Liniendiagramm des Umsatzes pro Tag
revenue = [500, 700, 400, 900, 600]
axes[1].plot(days, revenue)

# Drittes Plot-Element: Scatterplot des Verhältnisses von verkauften Einheiten und Umsatz pro Tag
axes[2].scatter(units_sold, revenue)

# Titel und Beschriftungen hinzufügen
axes[0].set_title('Verkaufte Einheiten pro Tag')
axes[0].set_xlabel('Tage')
axes[0].set_ylabel('Anzahl der verkauften Einheiten')

axes[1].set_title('Umsatz pro Tag')
axes[1].set_xlabel('Tage')
axes[1].set_ylabel('Umsatz in Euro')

axes[2].set_title('Verhältnis von verkauften Einheiten und Umsatz')
axes[2].set_xlabel('Verkaufte Einheiten')
axes[2].set_ylabel('Umsatz in Euro')

# Zeige den Subplot an
plt.tight_layout()
plt.show()
```

Vergleiche deine Lösungen mit den Musterlösungen, um zu überprüfen, ob sie korrekt sind.

Viel Erfolg!