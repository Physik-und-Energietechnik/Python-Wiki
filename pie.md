## Einführung
In diesem Abschnitt werden wir uns mit dem "pie Plot" in Matplotlib beschäftigen. Keine Sorge, es geht hier nicht um köstliche Obstkuchen, sondern um die Visualisierung von Daten in einem Kreisdiagramm. Mit dem pie Plot kannst du Datenprozentsätze auf unterhaltsame und ansprechende Weise präsentieren. Du wirst lernen, wie man das pie Plot-Diagramm erstellt und es für verschiedene Anwendungsfälle nutzt.

## Theorie

Bevor wir in die Praxis einsteigen, wollen wir uns ein wenig mit der Theorie hinter dem pie Plot befassen. Ein Kreisdiagramm, auch bekannt als "Pie Chart" (ja, wie ein Stück Kuchen), ist eine Möglichkeit, Datenprozentsätze darzustellen. Es besteht aus einem Kreis, der in Sektoren unterteilt ist. Jeder Sektor repräsentiert einen Datenpunkt, und die Größe des Sektors entspricht dem Prozentsatz, den dieser Datenpunkt in Bezug auf das Gesamte ausmacht.

Hier ist ein allgemeines Beispiel, um das Konzept zu verdeutlichen:

```python
import matplotlib.pyplot as plt

labels = ['Äpfel', 'Bananen', 'Kirschen']
sizes = [35, 45, 20]

plt.pie(sizes, labels=labels)
plt.show()
```

In diesem Beispiel haben wir drei Datenpunkte: Äpfel, Bananen und Kirschen. Die Größen der Sektoren im Kreisdiagramm entsprechen den Prozentsätzen 35%, 45% und 20%. Durch die Verwendung der Funktion `plt.pie()` und die Angabe von `labels` und `sizes` erstellen wir das Kreisdiagramm. Schließlich verwenden wir `plt.show()`, um das Diagramm anzuzeigen.

Jetzt wollen wir das gleiche Beispiel mit spezifischem Code in Python sehen:

```python
import matplotlib.pyplot as plt

labels = ['Äpfel', 'Bananen', 'Kirschen']
sizes = [35, 45, 20]

plt.pie(sizes, labels=labels, autopct='%1.1f%%', startangle=90)
plt.axis('equal')  # Stellt sicher, dass das Diagramm kreisförmig bleibt
plt.title('Früchteverteilung')
plt.show()
```

Hier haben wir das gleiche Kreisdiagramm, aber mit einigen zusätzlichen Optionen. Die `autopct`-Option fügt Prozentsätze zu den Sektoren hinzu, die den genauen Anteil anzeigen. Die `startangle`-Option dreht das Diagramm um einen bestimmten Winkel. `plt.axis('equal')` stellt sicher, dass das Diagramm kreisförmig bleibt. Schließlich haben wir mit `plt.title()` einen Titel für das Diagramm hinzugefügt.

## Praxis

Jetzt ist es Zeit, dein Wissen in die Praxis umzusetzen! Wir haben zwei Aufgaben für dich vorbereitet: eine leichte und eine schwerere. Du kannst dir sicher sein, dass wir dir bei beiden helfen werden.

### Aufgabe 1
Erstelle ein Kreisdiagramm, das die Verteilung von Internetbrowsern darstellt. Verwende die folgenden Daten:

- Chrome

: 65%
- Firefox: 20%
- Safari: 10%
- Andere: 5%

Hier ist ein Musterlösungscode, den du als Referenz verwenden kannst:

```python
import matplotlib.pyplot as plt

labels = ['Chrome', 'Firefox', 'Safari', 'Andere']
sizes = [65, 20, 10, 5]

plt.pie(sizes, labels=labels, autopct='%1.1f%%')
plt.axis('equal')
plt.title('Internetbrowserverteilung')
plt.show()
```

### Aufgabe 2
Erstelle ein Kreisdiagramm, das die Verteilung der Tierarten in einem Zoo darstellt. Verwende die folgenden Daten:

- Löwen: 40%
- Affen: 25%
- Elefanten: 20%
- Giraffen: 10%
- Pinguine: 5%

Viel Erfolg! Hier ist ein Musterlösungscode, um dich zu unterstützen:

```python
import matplotlib.pyplot as plt

labels = ['Löwen', 'Affen', 'Elefanten', 'Giraffen', 'Pinguine']
sizes = [40, 25, 20, 10, 5]

plt.pie(sizes, labels=labels, autopct='%1.1f%%', startangle=90)
plt.axis('equal')
plt.title('Tierverteilung im Zoo')
plt.show()
```
## Fazit
Das war's! Du hast erfolgreich den pie Plot in Matplotlib gemeistert. Ob du nun Fruchtverteilungen oder Zoo-Tierverteilungen darstellen möchtest, du kannst das pie Plot-Diagramm nutzen, um deine Daten auf unterhaltsame Weise zu präsentieren. Viel Spaß beim Experimentieren und Erkunden weiterer Funktionen von Matplotlib!

## Links / Weiteres Material
### W3Schools
### YouTube