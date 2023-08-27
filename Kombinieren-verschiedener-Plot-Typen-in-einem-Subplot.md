## Einführung

In diesem Tutorial werden wir lernen, wie wir unsere Daten auf kreative und informative Weise visualisieren können.

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
sales = [50, 80, 120]
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

### Aufgabe 1

Erstelle einen Subplot mit einem Balkendiagramm und einem Liniendiagramm. Das Balkendiagramm soll die Anzahl der verkauften Einheiten pro Tag zeigen, und das Liniendiagramm soll den Umsatz pro Tag anzeigen. Verwende die folgenden Daten:

```python
days = ['Montag', 'Dienstag', 'Mittwoch', 'Donnerstag', 'Freitag']
units_sold = [30, 40, 25, 55, 35]
revenue = [500, 700, 400, 900, 600]
```

Musterlösung:

```python
import matplotlib.pyplot as plt

# Daten
days = ['Montag', 'Dienstag', 'Mittwoch', 'Donnerstag', 'Freitag']
units_sold = [30, 40, 25, 55, 35]
revenue = [500, 700, 400, 900, 600]

# Erstelle den Subplot
fig, (ax1, ax2) = plt.subplots(2, 1, figsize=(10, 8))

# Balkendiagramm (Anzahl der verkauften Einheiten)
ax1.bar(days, units_sold, color='blue')
ax1.set_ylabel('Verkaufte Einheiten')
ax1.set_title('Verkaufte Einheiten und Umsatz pro Tag')

# Liniendiagramm (Umsatz)
ax2.plot(days, revenue, marker='o', color='green', linestyle='-', linewidth=2)
ax2.set_ylabel('Umsatz')
ax2.set_xlabel('Tage')

# Zeige den Plot
plt.tight_layout()
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Subplots_und_mehrere_Achsen/Kombinieren_verschiedener_Plot-Typen_in_einem_Subplot/ms_aufgabe1.png)

### Aufgabe 2

Erweitere den Subplot aus der leichten Aufgabe, indem du einen Scatterplot hinzufügst. Der Scatterplot soll das Verhältnis zwischen den verkauften Einheiten und dem Umsatz pro Tag zeigen. Verwende weiterhin die oben genannten Daten.

Musterlösung:

```python
import matplotlib.pyplot as plt

# Daten
days = ['Montag', 'Dienstag', 'Mittwoch', 'Donnerstag', 'Freitag']
units_sold = [30, 40, 25, 55, 35]
revenue = [500, 700, 400, 900, 600]

# Erstelle den Subplot
fig, (ax1, ax2, ax3) = plt.subplots(3, 1, figsize=(10, 12))

# Balkendiagramm (Anzahl der verkauften Einheiten)
ax1.bar(days, units_sold, color='blue')
ax1.set_ylabel('Verkaufte Einheiten')
ax1.set_title('Verkaufte Einheiten, Umsatz und Verhältnis pro Tag')

# Liniendiagramm (Umsatz)
ax2.plot(days, revenue, marker='o', color='green', linestyle='-', linewidth=2)
ax2.set_ylabel('Umsatz')

# Scatterplot (Verhältnis)
ratio = [rev / units for rev, units in zip(revenue, units_sold)]
ax3.scatter(days, ratio, color='red', marker='x')
ax3.set_ylabel('Verhältnis (Umsatz/Verkaufte Einheiten)')
ax3.set_xlabel('Tage')

# Zeige den Plot
plt.tight_layout()
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Subplots_und_mehrere_Achsen/Kombinieren_verschiedener_Plot-Typen_in_einem_Subplot/ms_aufgabe2.png)


## Fazit
Viel Spaß beim Codieren!

Viel Erfolg!