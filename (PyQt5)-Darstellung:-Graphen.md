## Einführung
Willkommen zum aufregenden Abenteuer der GUI-Programmierung in Python mit PyQt5! Dieses Tutorial wird dich in die zauberhafte Welt der Graphen entführen, nicht die Art von Graphen, die in Mathebüchern auftauchen, sondern hübsche visuelle Darstellungen von Daten.

In diesem Tutorial wirst du lernen, wie du mit der PyQt5-Bibliothek beeindruckende Graphen und Diagramme erstellen kannst. Du wirst in der Lage sein, Daten auf eine Art und Weise zu visualisieren, die nicht nur informativ, sondern auch ansprechend ist. Also schnall dich an, denn wir werden bunte Linien und Balken zum Tanzen bringen!

## Theorie
### Einführung in die Graphen-Darstellung:
Graphen sind großartig. Sie nehmen Daten und machen sie visuell, damit du auf den ersten Blick verstehen kannst, was los ist. Hier sind zwei Haupttypen von Graphen, die wir erforschen werden:

1. Linien-Diagramme: Diese zeigen Datenpunkte auf einer Linie, die sich über den Bildschirm erstreckt. Perfekt, um Trends und Veränderungen im Laufe der Zeit zu erkennen.

2. Balken-Diagramme: Diese verwenden Balken unterschiedlicher Längen, um Werte zu vergleichen. Sie sind wie Schokoriegel der Information – je größer der Balken, desto wichtiger ist der Wert!

### Allgemeines Code-Beispiel
Bevor wir in die spezifischen Beispiele eintauchen, lass uns kurz einen allgemeinen Code anschauen, der das Skelett für unsere graphischen Meisterwerke bereitstellt:
```python
# Zuerst importieren wir die magische PyQt5-Bibliothek
from PyQt5.QtWidgets import QApplication, QMainWindow

# Dann erstellen wir eine Anwendung
app = QApplication([])

# Und ein Hauptfenster für unsere Kunstwerke
window = QMainWindow()
window.setWindowTitle('Meine fantastische Graphen-Anwendung')
window.setGeometry(100, 100, 800, 600)  # x, y, Breite, Höhe

# Jetzt zeigen wir alles an
window.show()

# Und starten die Anwendungsschleife
app.exec()
```
### Explizites Code-Beispiel - Linien-Diagramm
Hier ist ein Beispiel für ein einfaches Linien-Diagramm:
```python
from PyQt5.QtWidgets import QApplication, QMainWindow
import pyqtgraph as pg  # Spezialzauber für Graphen

app = QApplication([])

window = QMainWindow()
window.setWindowTitle('Linien-Diagramm')
window.setGeometry(100, 100, 800, 600)

# Erstelle ein PlotWidget für unser Diagramm
plot_widget = pg.PlotWidget(window)
plot_widget.setGeometry(50, 50, 700, 500)

# Fügen wir ein bisschen Magie hinzu - einige Testdaten
x = [1, 2, 3, 4, 5]
y = [10, 6, 8, 4, 7]

# Fügen wir die Daten zum Diagramm hinzu
plot_widget.plot(x, y, pen='r')  # 'r' für rot, wir sind kreativ!

window.show()

app.exec()
```
## Praxis
### Leichte Aufgabe
Erstelle eine GUI-Anwendung mit PyQt5, die ein Balken-Diagramm mit den Umsatzzahlen verschiedener Monate für dein imaginäres Eiscreme-Geschäft zeigt.

### Musterlösung - Leichte Aufgabe:

```python
from PyQt5.QtWidgets import QApplication, QMainWindow
import pyqtgraph as pg

app = QApplication([])

window = QMainWindow()
window.setWindowTitle('Eiscreme-Umsatz')
window.setGeometry(100, 100, 800, 600)

plot_widget = pg.PlotWidget(window)
plot_widget.setGeometry(50, 50, 700, 500)

# Unsere fantasievollen Eiscreme-Umsatzzahlen
monate = ['Jan', 'Feb', 'Mär', 'Apr', 'Mai', 'Jun']
umsatz = [1500, 1800, 2200, 1900, 2400, 2100]

# Zeigen wir sie im Balken-Diagramm
plot_widget.plot(monate, umsatz, pen='b', symbol='o')

window.show()

app.exec()
```
### Erklärung:
    **Import von Bibliotheken:** Du hast die benötigten Bibliotheken importiert, nämlich **'QApplication', 'QMainWindow'** aus PyQt5 und **'pg'** (die 
    **'pyqtgraph**'-Bibliothek für die Diagrammerstellung).

    **Erstellen der Anwendung:** Du hast eine Anwendung mit **'QApplication([])'** erstellt.

    **Erstellen des Hauptfensters:** Du hast ein Hauptfenster (**'QMainWindow**') erstellt und ihm einen Titel "Eiscreme-Umsatz" gegeben. Die Abmessungen 
    wurden mit **'setGeometry'** festgelegt.

    Erstellen des Plot-Widgets: Ein Plot-Widget (**'pg.PlotWidget'**) wurde erstellt, das später das Balken-Diagramm anzeigen wird. Seine Abmessungen 
    wurden ebenfalls festgelegt.

    **Daten vorbereiten:** Du hast zwei Listen erstellt: **'monate'** enthält die Monate und **'umsatz'** enthält die zugehörigen Umsatzzahlen.

    **Balken-Diagramm erstellen:** Das Balken-Diagramm wurde mit **'plot_widget.plot'**('monate', 'umsatz', pen='b', symbol='o') erstellt. Dabei wurde 
    monate auf der x-Achse und umsatz auf der y-Achse platziert. Die Balken werden in Blau (blue) gezeichnet und als Kreise (circles) dargestellt.

    **Anzeigen des Fensters:** Das Hauptfenster und das Balken-Diagramm wurden mit **'window.show()**' angezeigt.

    **Starten der Anwendungsschleife:** Schließlich wurde die Anwendungsschleife mit app.exec() gestartet, um die Benutzerinteraktion zu ermöglichen.

    Der Code erstellt ein schickes Balken-Diagramm, das die Umsatzzahlen für verschiedene Monate anschaulich darstellt. Die zukünftigen Kunden werden 
    begeistert sein, wenn sie sehen, wie gut man Eiscreme verkauft!

### Schwere Aufgabe
Erstelle eine GUI-Anwendung, die zwei Linien-Diagramme zeigt: eines für die Verkaufszahlen von Autos und eines für die Verkaufszahlen von Fahrrädern im Verlauf von fünf Jahren.

### Musterlösung - Schwere Aufgabe:
```python
from PyQt5.QtWidgets import QApplication, QMainWindow
import pyqtgraph as pg

app = QApplication([])

window = QMainWindow()
window.setWindowTitle('Auto vs. Fahrrad Verkäufe')
window.setGeometry(100, 100, 800, 600)

plot_widget = pg.PlotWidget(window)
plot_widget.setGeometry(50, 50, 700, 500)

jahre = ['2018', '2019', '2020', '2021', '2022']
auto_verkauf = [1200, 1300, 1100, 1350, 1250]
fahrrad_verkauf = [800, 950, 900, 1000, 1100]

# Zeigen wir sie im Linien-Diagramm
plot_widget.plot(jahre, auto_verkauf, pen='r', symbol='s', name='Auto Verkäufe')
plot_widget.plot(jahre, fahrrad_verkauf, pen='b', symbol='o', name='Fahrrad Verkäufe')

# Zeigen wir eine Legende für das extra Flair
plot_widget.addLegend()

window.show()

app.exec()
```
## Fazit
Herzlichen Glückwunsch! Du hast gerade die bunte Welt der Graphen-Darstellung mit PyQt5 erkundet. Von Linien-Diagrammen bis hin zu lebendigen Balken-Diagrammen – du kannst jetzt Daten auf eine visuell ansprechende Weise präsentieren. Bringe deine Informationen zum Strahlen und vergiss nicht, dass Graphen nicht nur Mathe-Kram sind, sondern auch große Geschichten erzählen können!
