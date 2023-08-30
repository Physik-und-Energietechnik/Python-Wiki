## Einführung

In diesem Abschnitt wirst du lernen, wie du Zeitreihen und Trends mithilfe von Matplotlib visualisieren kannst. Das ist besonders nützlich, wenn du Daten hast, die sich über die Zeit erstrecken, wie zum Beispiel Aktienkurse, Wetterdaten oder Social-Media-Trends. Mit Matplotlib kannst du diese Daten in anschauliche Grafiken verwandeln und Muster und Trends leichter erkennen.

## Theorie

### Visualisierung von Zeitreihen

Jetzt wollen wir uns auf Zeitreihen konzentrieren. Stell dir vor, du hast Daten, die sich über die Zeit erstrecken, wie zum Beispiel monatliche Verkaufszahlen. Matplotlib kann dir helfen, diese Daten in eine hübsche Linienvisualisierung zu verwandeln:

```python
import matplotlib.pyplot as plt

months = ['Jan', 'Feb', 'Mar', 'Apr', 'May']
sales = [100, 150, 120, 200, 180]

plt.plot(months, sales)
plt.xlabel('Monate')
plt.ylabel('Verkaufszahlen')
plt.title('Monatliche Verkaufstrends')
plt.show()
```

## Praxis

### Aufgabe 1

Zeit für eine kleine Übung! Du hast monatliche Besucherzahlen deiner Website gesammelt. Erstelle eine Linienvisualisierung, um diese Daten darzustellen. Vergiss nicht, Achsenbeschriftungen und einen Titel hinzuzufügen!

```python
import matplotlib.pyplot as plt

months = ['Jan', 'Feb', 'Mar', 'Apr', 'May']
visitors = [1200, 1300, 1450, 1100, 1600]

plt.plot(months, visitors)
plt.xlabel('Monate')
plt.ylabel('Besucherzahlen')
plt.title('Monatliche Website-Besucher')
plt.show()
```

### Aufgabe 2

Jetzt der ultimative Test! Du hast Daten über den Verlauf von Social-Media-Followern gesammelt. Erstelle eine Linienvisualisierung, um den Trend über die Zeit zu zeigen. Verleihe deiner Grafik mit verschiedenen Farben und Linienstilen den letzten Schliff!

```python
import matplotlib.pyplot as plt

months = ['Jan', 'Feb', 'Mar', 'Apr', 'May']
followers = [500, 520, 550, 600, 620]

plt.plot(months, followers, marker='o', color='b', linestyle='--', label='Follower-Trend')
plt.xlabel('Monate')
plt.ylabel('Follower-Anzahl')
plt.title('Social-Media-Follower-Trends')
plt.legend()
plt.show()
```

## Fazit
Herzlichen Glückwunsch, du hast erfolgreich Zeitreihen und Trends mit Matplotlib visualisiert! Du bist nun bereit, Daten zum Leben zu erwecken und beeindruckende Visualisierungen zu erstellen.

Viel Spaß beim Experimentieren und Erkunden der fabelhaften Welt der Datenvisualisierung!

## Links / Weiteres Material
### Dokumentation
### W3Schools
### YouTube