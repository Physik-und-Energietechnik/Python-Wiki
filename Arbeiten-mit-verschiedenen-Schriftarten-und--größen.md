## Einführung

In diesem Abschnitt werden wir lernen, wie wir verschiedene Schriftarten und -größen in unseren Grafiken verwenden können.

Das Verständnis dieser Funktionen ist besonders nützlich, um ansprechende und gut lesbare Diagramme zu erstellen. Egal, ob du Daten präsentieren möchtest oder einfach nur deine Kreativität ausdrücken willst, mit Matplotlib und den verschiedenen Schriftarten und -größen wirst du in der Lage sein, deine Grafiken auf das nächste Level zu bringen.

## Theorie

### Schriftarten

Schriftarten spielen eine wichtige Rolle in der visuellen Kommunikation. Sie können die Stimmung, den Stil und die Lesbarkeit deiner Grafiken beeinflussen. Matplotlib bietet eine breite Auswahl an vordefinierten Schriftarten, die du verwenden kannst.

Hier ist ein allgemeines Beispiel, wie du die Schriftart in Matplotlib ändern kannst:

```python
import matplotlib.pyplot as plt

# Vordefinierte Schriftarten anzeigen
print(plt.rcParams['font.family'])

# Schriftart festlegen
plt.rcParams['font.family'] = 'serif'
```

In diesem Beispiel verwenden wir die Schriftart "serif". Du kannst auch andere vordefinierte Schriftarten wie "sans-serif" oder "monospace" ausprobieren.

### Schriftgrößen

Die Schriftgröße ist ein weiterer wichtiger Aspekt bei der Gestaltung von Grafiken. Mit Matplotlib kannst du die Schriftgröße sowohl für den Text im Diagramm als auch für die Achsenbeschriftungen anpassen.

Hier ist ein Beispiel, wie du die Schriftgröße in Matplotlib ändern kannst:

```python
import matplotlib.pyplot as plt

# Schriftgröße für den Text im Diagramm ändern
plt.rcParams['font.size'] = 12

# Schriftgröße für die Achsenbeschriftungen ändern
plt.rcParams['axes.labelsize'] = 14
```

In diesem Beispiel haben wir die Schriftgröße des Texts im Diagramm auf 12 und die Schriftgröße der Achsenbeschriftungen auf 14 gesetzt. Du kannst die Werte anpassen, um den gewünschten Effekt zu erzielen.

## Praxis

Jetzt wollen wir das Gelernte in die Praxis umsetzen! Hier sind zwei Aufgaben für dich:

### Aufgabe 1

Erstelle ein einfaches Linien-Diagramm mit Matplotlib, das die Umsatzentwicklung eines fiktiven Unternehmens über die letzten fünf Jahre darstellt. Verwende die Schriftart "Roboto" und eine Schriftgröße von 10 für den Text im Diagramm und eine Schriftgröße von 12 für die Achsenbeschriftungen.

Musterlösung:

```python
import matplotlib.pyplot as plt

years = [2017, 2018, 2019, 2020, 2021]
revenue = [50000, 60000, 55000, 70000, 80000]

plt.plot(years, revenue)
plt.xlabel('Jahr')
plt.ylabel('Umsatz')
plt.title('Umsatzentwicklung')

# Schriftart und -größe festlegen
plt.rcParams['font.family'] = 'Roboto'
plt.rcParams['font.size'] = 10
plt.rcParams['axes.labelsize'] = 12

plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Anpassungen_und_Stilisierung/Arbeiten_mit verschiedenen_Schriftarten/ms_aufgabe1.png)

## Fazit
Probier sie aus und schau dir an, wie die Grafiken mit verschiedenen Schriftarten und -größen aussehen!

## Links / Weiteres Material
### Dokumentation
### W3Schools
### YouTube