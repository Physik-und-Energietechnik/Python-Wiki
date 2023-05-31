# Matplotlib - Arbeiten mit verschiedenen Schriftarten und -größen

## Einführung

Willkommen zu unserem Python Tutorial! In diesem Abschnitt werden wir lernen, wie wir verschiedene Schriftarten und -größen in unseren Grafiken verwenden können.

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

Hier ist ein Beispielcode, um dich zu inspirieren:

```python
import matplotlib.pyplot as plt

years = [2017, 2018, 2019, 2020, 2021]
revenue = [50000, 60000, 55000, 70000, 80000]

plt.plot(years, revenue)
plt.xlabel('Jahr')
plt.ylabel('Umsatz')
plt.title('Umsatzentwicklung')

# Schriftart und

 -größe festlegen
plt.rcParams['font.family'] = 'Roboto'
plt.rcParams['font.size'] = 10
plt.rcParams['axes.labelsize'] = 12

plt.show()
```

### Aufgabe 2

Erstelle ein gestapeltes Säulendiagramm mit Matplotlib, das den Anteil der verschiedenen Früchte in einem Obstkorb darstellt. Verwende die Schriftart "Comic Sans MS" und eine Schriftgröße von 14 für den Text im Diagramm und eine Schriftgröße von 16 für die Achsenbeschriftungen.

Hier ist ein Beispielcode, um dich zu inspirieren:

```python
import matplotlib.pyplot as plt

fruits = ['Apfel', 'Banane', 'Orange']
percentages = [60, 30, 10]

plt.bar(fruits, percentages)
plt.xlabel('Früchte')
plt.ylabel('Prozentsatz')
plt.title('Anteil der Früchte im Obstkorb')

# Schriftart und -größe festlegen
plt.rcParams['font.family'] = 'Comic Sans MS'
plt.rcParams['font.size'] = 14
plt.rcParams['axes.labelsize'] = 16

plt.show()
```

Vergiss nicht, deine eigenen Daten einzufügen, um die Grafiken anzupassen! Viel Spaß beim Experimentieren!

## Musterlösungen

Hier sind die Musterlösungen für die beiden Aufgaben:

### Aufgabe 1 - Musterlösung

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

### Aufgabe 2 - Musterlösung

```python
import matplotlib.pyplot as plt

fruits = ['Apfel', 'Banane', 'Orange']
percentages = [60, 30, 10]

plt.bar(fruits, percentages)
plt.xlabel('Früchte')
plt.ylabel('Prozentsatz')
plt.title('Anteil der Früchte im Obstkorb')

# Schriftart und -größe festlegen
plt.rcParams['font.family'] = 'Comic Sans MS'
plt.rcParams['font.size'] = 14
plt.rcParams['axes.labelsize'] = 16

plt.show()
```

Probier sie aus und schau dir an, wie die Grafiken mit verschiedenen Schriftarten und -größen aussehen!