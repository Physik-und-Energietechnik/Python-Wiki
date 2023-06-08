## Einführung

In diesem Abschnitt werden wir uns mit einem spannenden Teil von Matplotlib befassen - dem `stackplot` Plot. Aber bevor wir in die Tiefen dieses Plots eintauchen, lassen Sie uns zunächst darüber sprechen, was Sie durch dieses Tutorial erreichen können und wie Sie dieses neu erworbene Wissen einsetzen können.

Hier werden Sie lernen, wie Sie mit Matplotlib beeindruckende Diagramme erstellen können, die verschiedene Datensätze stapeln und Ihnen dabei helfen, komplexe Muster zu erkennen. Das Wissen über den `stackplot` Plot wird Ihnen ermöglichen, Daten visuell ansprechend darzustellen und gleichzeitig Einblicke in die Verteilung der Daten zu gewinnen. Ganz gleich, ob Sie Daten analysieren, Finanzdiagramme erstellen oder einfach nur Ihren Freunden zeigen möchten, wie cool Python ist, dieser Plot wird Ihnen helfen, Ihre Ziele zu erreichen!

## Theorie

Bevor wir uns in den Code stürzen, lassen Sie uns kurz die Theorie hinter dem `stackplot` Plot verstehen. Der `stackplot` Plot ist ein Diagramm, das uns ermöglicht, verschiedene Datenreihen aufeinander zu stapeln und ihre Verteilung zu visualisieren. Es eignet sich hervorragend, um Veränderungen im Laufe der Zeit darzustellen oder um die Beiträge verschiedener Kategorien zu einem Gesamtwert zu zeigen.

Schauen wir uns zunächst ein allgemeines Beispiel an:

```python
import matplotlib.pyplot as plt

# Daten für die Kategorien
kategorie1 = [1, 3, 2, 4, 3]
kategorie2 = [2, 2, 3, 2, 1]
kategorie3 = [5, 1, 2, 6, 4]

# Stapelung der Daten
plt.stackplot(range(5), kategorie1, kategorie2, kategorie3, labels=['Kategorie 1', 'Kategorie 2', 'Kategorie 3'])

# Legende anzeigen
plt.legend()

# Diagramm anzeigen
plt.show()
```

Hier haben wir drei Kategorien: Kategorie 1, Kategorie 2 und Kategorie 3. Die Daten für jede Kategorie sind in separaten Listen gespeichert. Durch die Verwendung von `plt.stackplot` können wir diese Datenreihen stapeln und die Verteilung der Beiträge jeder Kategorie visualisieren. Die `labels`-Parameter ermöglichen es uns, die Kategorien in der Legende zu beschriften.

Nun wollen wir ein spezifischeres Beispiel betrachten und uns den Code direkt in Python anschauen:

```python
import matplotlib.pyplot as plt

# Jahre
jahre = [2016, 2017, 2018, 2019, 2020]

# Umsätze der Kategorien
kategorie1 = [100, 150, 200, 180, 220]
kategorie2 = [80, 130, 160, 170, 190]
kategorie3 = [120, 170, 140, 150, 160]

# Stapelung der Daten
plt.stackplot(jahre, kategorie1, kategorie2, kategorie3, labels=['Kategorie 1', 'Kategorie 2', 'Kategorie 3'])

# Legende anzeigen
plt.legend()

# Achsentitel
plt.xlabel('Jahre')
plt.ylabel('Umsatz in Millionen')

# Diagramm anzeigen
plt.show()
```

In diesem Beispiel haben wir die Umsätze für drei verschiedene Kategorien über einen Zeitraum von fünf Jahren. Die Jahre sind in der Liste `jahre` gespeichert, während die Umsätze für jede Kategorie in separaten Listen (`kategorie1`, `kategorie2`, `kategorie3`) enthalten sind. Durch die Verwendung von `plt.stackplot` stapeln wir die Datenreihen und erhalten ein Diagramm, das uns zeigt, wie sich die Umsätze jeder Kategorie im Laufe der Zeit entwickelt haben.

## Praxis

Nun, da Sie die Theorie hinter dem `stackplot` Plot kennen, ist es Zeit, Ihr neu erworbenes Wissen in die Praxis umzusetzen. Machen Sie sich bereit für ein paar Übungen!

**Aufgabe 1:** Stellen Sie sich vor, Sie haben Daten über die Verkaufszahlen von drei verschiedenen Produkten in den Monaten Januar bis Mai. Erstellen Sie ein `stackplot` Diagramm, das die Verkaufszahlen für jedes Produkt darstellt. Vergessen Sie nicht, eine geeignete Legende und Achsentitel hinzuzufügen.

```python
import matplotlib.pyplot as plt

# Monate
monate = ['Jan', 'Feb', 'Mar', 'Apr', 'Mai']

# Verkaufszahlen der Produkte
produkt1 = [50, 70, 90, 80, 100]
produkt2 = [40, 60, 70, 90, 80]
produkt3 = [70, 80, 60, 50, 40]

# Stapelung der Daten
plt.stackplot(monate, produkt1, produkt2, produkt3, labels=['Produkt 1', 'Produkt 2', 'Produkt 3'])

# Legende anzeigen
plt.legend()

# Achsentitel
plt.xlabel('Monate')
plt.ylabel('Verkaufszahlen')

# Diagramm anzeigen
plt.show()
```

**Aufgabe 2:** Stellen Sie sich vor, Sie haben Daten über die Verteilung der Niederschläge in drei verschiedenen Regionen (A, B, C) über die vier Jahreszeiten (Frühling, Sommer, Herbst, Winter). Erstellen Sie ein `stackplot` Diagramm, das die Verteilung der Niederschläge in jeder Region zeigt. Fügen Sie eine geeignete Legende und Achsentitel hinzu.

```python
import matplotlib.pyplot as plt

# Jahreszeiten
jahreszeiten = ['Frühling', 'Sommer', 'Herbst', 'Winter']

# Niederschlagsverteilung der Regionen
region_a = [30, 60, 40, 20]
region_b = [50, 40, 30, 50]
region_c = [20, 30, 50, 30]

# Stapelung der Daten
plt.stackplot(jahreszeiten, region_a, region_b, region_c, labels=['Region A', 'Region B', 'Region C'])

# Legende anzeigen
plt.legend()

# Achsentitel
plt.xlabel('Jahreszeiten')
plt.ylabel('Niederschlagsverteilung in mm')

# Diagramm anzeigen
plt.show()
```

## Fazit
Herzlichen Glückwunsch! Sie haben gerade den `stackplot` Plot gemeistert. Mit diesem Wissen können Sie nun beeindruckende stapelbasierte Diagramme erstellen und Ihre Daten zum Leben erwecken. Gehen Sie raus und setzen Sie Ihre Python-Künste ein, um die Welt der Datenvisualisierung zu erobern!

Happy Coding!

## Links / Weiteres Material
### W3Schools
### YouTube