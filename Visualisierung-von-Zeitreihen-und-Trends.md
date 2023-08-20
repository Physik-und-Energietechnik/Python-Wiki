# Matplotlib - Visualisierung von Zeitreihen und Trends

## Einführung

Willkommen zum Matplotlib-Tutorial! In diesem Tutorial wirst du in die faszinierende Welt der Datenvisualisierung mit Matplotlib eingeführt. Hast du dich jemals gefragt, wie du Daten in anschauliche Diagramme verwandeln kannst? Nun, Matplotlib ist dein Zauberstab für diese Aufgabe!

Du wirst lernen, wie du Zeitreihen und Trends mithilfe von Matplotlib visualisieren kannst. Das ist besonders nützlich, wenn du Daten hast, die sich über die Zeit erstrecken, wie zum Beispiel Aktienkurse, Wetterdaten oder Social-Media-Trends. Mit Matplotlib kannst du diese Daten in anschauliche Grafiken verwandeln und Muster und Trends leichter erkennen.

## Theorie

### Grundlagen der Matplotlib

Matplotlib ist eine Python-Bibliothek, die es dir ermöglicht, beeindruckende Grafiken zu erstellen. Stell dir Matplotlib wie einen Künstler vor, der auf Kommando deine Daten auf Leinwand zaubert. Hier ist eine einfache Vorstellung davon, wie das funktioniert:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 8, 12, 6, 14]

plt.plot(x, y)
plt.xlabel('X-Achse')
plt.ylabel('Y-Achse')
plt.title('Einfache Datenvisualisierung')
plt.show()
```

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

### Leichte Aufgabe

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

### Schwere Aufgabe

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

Herzlichen Glückwunsch, du hast erfolgreich Zeitreihen und Trends mit Matplotlib visualisiert! Du bist nun bereit, Daten zum Leben zu erwecken und beeindruckende Visualisierungen zu erstellen.

Viel Spaß beim Experimentieren und Erkunden der fabelhaften Welt der Datenvisualisierung!