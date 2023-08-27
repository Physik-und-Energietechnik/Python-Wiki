## Einführung
Willkommen zu unserem Python-Tutorial über die Verwendung verschiedener Marker und Linienstile in Matplotlib! In diesem Tutorial werden wir lernen, wie wir unsere Diagramme mit verschiedenen Markern und Linienstilen aufpeppen können. Dieses Wissen wird dir helfen, beeindruckende und aussagekräftige Grafiken zu erstellen, sei es für Präsentationen, Berichte oder einfach nur zum Spaß!

## Theorie
Bevor wir in die Praxis eintauchen, werfen wir einen Blick auf die Theorie hinter den Markern und Linienstilen in Matplotlib. Markers repräsentieren einzelne Datenpunkte in einem Diagramm, während Linienstile das Erscheinungsbild der Linien zwischen den Datenpunkten beeinflussen.

### Marker
Ein Marker kann zum Beispiel ein Punkt, ein Kreis, ein Quadrat oder ein Dreieck sein. Er ermöglicht es uns, Datenpunkte auf unserer Grafik zu kennzeichnen und so visuell hervorzuheben. Hier ist ein allgemeines Beispiel, wie Marker in Matplotlib verwendet werden:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 5, 8, 3, 6]

plt.plot(x, y, marker='o')
plt.show()
```

Und hier ist ein spezifisches Beispiel, das dir zeigt, wie du einen grünen Kreuzmarker verwenden kannst:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 5, 8, 3, 6]

plt.plot(x, y, marker='x', color='green')
plt.show()
```

Hier ist eine Liste mit einigen der gängigsten Arten von Markern in Matplotlib:

- Punkt ('.')
- Kreis ('o')
- Quadrat ('s')
- Dreieck ('^')
- X ('x')
- Diamant ('D')
- Pentagramm ('p')
- Kreuz ('+')

### Linienstile
Linienstile beeinflussen das Aussehen der Linien zwischen den Datenpunkten. Du kannst verschiedene Linienstile verwenden, wie zum Beispiel eine durchgezogene Linie, eine gestrichelte Linie oder eine gepunktete Linie. Hier ist ein allgemeines Beispiel, wie Linienstile in Matplotlib verwendet werden:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 5, 8, 3, 6]

plt.plot(x, y, linestyle='--')
plt.show()
```

Und hier ist ein spezifisches Beispiel, das dir zeigt, wie du eine gestrichelte rote Linie verwenden kannst:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 5, 8, 3, 6]

plt.plot(x, y, linestyle='--', color='red')
plt.show()
```

Hier ist eine Liste mit einigen der gängigsten Arten von Linienstilen in Matplotlib:

- Durchgezogen ('-')
- Gestrichelt ('--')
- Gepunktet (':')
- Strichpunkt ('-.')

Diese Liste ist nicht abschließend, sondern gibt dir eine gute Ausgangsbasis, um verschiedene Marker und Linienstile auszuprobieren. Du kannst auch weitere Arten von Markern und Linienstilen in der Matplotlib-Dokumentation finden, um deine Grafiken weiter anzupassen und zu individualisieren. Viel Spaß beim Entdecken!

## Praxis
Jetzt, da wir die Theorie hinter uns haben, lass uns das erlangte Wissen in die Praxis umsetzen! Wir werden zwei Aufgaben durchführen - eine leichte und eine schwerere.

### Aufgabe 1
Zeichne ein einfaches Liniendiagramm mit roten Kreuzmarkern und einer gestrichelten blauen Linie. Verwende die folgenden Datenpunkte:
```python
x = [1, 2, 3, 4, 5]
y = [10, 5, 8, 3, 6]
```

Musterlösung:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 5, 8, 3, 6]

plt.plot(x, y, marker='x', color='red', linestyle='--', color='blue')
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Grundlagen_des_Plottings/Verwendung_verschiedener_Marker_und_Linienstile/ms_aufgabe1.png)

### Aufgabe 2
Zeichne ein gestapeltes Säulendiagramm mit grünen Quadratmarkern und einer durchgezogenen schwarzen Linie. Verwende die folgenden Datenpunkte:

```python
x = [1, 2, 3, 4, 5]
y1 = [10, 5, 8, 3, 6]
y2 = [5, 7, 4, 2, 9]
```

Musterlösung:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y1 = [10, 5, 8, 3, 6]
y2 = [5, 7, 4, 2, 9]

plt.plot(x, y1, marker='s', color='green', linestyle='-', label='Serie 1')
plt.plot(x, y2, marker='s', color='green', linestyle='-', label='Serie 2')
plt.legend()
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Grundlagen_des_Plottings/Verwendung_verschiedener_Marker_und_Linienstile/ms_aufgabe2.png)

## Fazit
Super, du hast es geschafft! Du kannst nun verschiedene Marker und Linienstile in Matplotlib verwenden, um deine Diagramme zu verbessern und deine Daten ansprechend darzustellen. Viel Spaß beim Experimentieren und Erstellen beeindruckender Visualisierungen!

## Links / Weiteres Material
### Dokumentation
### W3Schools
### YouTube