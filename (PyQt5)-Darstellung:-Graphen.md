## Einführung
Willkommen, wagemutige Python-Entdecker, zu einer neuen Episode des epischen Abenteuers in die wunderbare Welt der GUI-Programmierung mit PyQt5! Heute werden wir nicht nur Knöpfe und Texte bewundern, sondern auch die Mysterien der Graphen-Darstellung enthüllen.

In diesem Tutorial wirst du lernen, wie man mithilfe der Kraft von PyQt5 und Matplotlib atemberaubende Graphen erstellt. Von einfachen Linien bis hin zu farbenfrohen Balkendiagrammen - du wirst die Macht der Visualisierung in deinen Händen halten!

## Theorie

**Matplotlib - Dein Grafik-Zauberstab**

Matplotlib ist wie ein Pinsel in der Hand eines Künstlers - es erlaubt uns, Diagramme, Graphen und Visualisierungen zu erstellen. Es ist so, als ob du Daten in eine magische Leinwand verwandelst!

### Allgemeines Code-Beispiel
Lass uns zuerst einen schnellen Blick auf ein allgemeines Code-Beispiel werfen, um deine Graphenreise zu beginnen:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 15, 7, 12, 9]

plt.plot(x, y)
plt.xlabel('X-Achse')
plt.ylabel('Y-Achse')
plt.title('Mein erster Graph')
plt.show()
```
### Explizites Code-Beispiel - Balkendiagramm
Hier ist ein Beispiel für ein schickes Balkendiagramm, das wir mit Matplotlib und PyQt5 erstellen können:
```python
import sys
from PyQt5.QtWidgets import QApplication, QMainWindow, QVBoxLayout, QWidget
from matplotlib.backends.backend_qt5agg import FigureCanvasQTAgg as FigureCanvas
from matplotlib.figure import Figure

class BalkenDiagrammApp(QMainWindow):
    def __init__(self):
        super().__init__()

        self.setWindowTitle('Balkendiagramm')
        self.setGeometry(100, 100, 600, 400)

        layout = QVBoxLayout()

        canvas = FigureCanvas(Figure(figsize=(5, 3)))
        layout.addWidget(canvas)

        self.setCentralWidget(QWidget(self))
        self.centralWidget().setLayout(layout)

        self.plot_balkendiagramm(canvas.figure)

    def plot_balkendiagramm(self, figure):
        ax = figure.add_subplot(111)
        categories = ['Äpfel', 'Bananen', 'Kirschen', 'Trauben']
        counts = [23, 17, 35, 29]
        ax.bar(categories, counts)

if __name__ == '__main__':
    app = QApplication(sys.argv)
    window = BalkenDiagrammApp()
    window.show()
    sys.exit(app.exec_())
```
## Praxis
### Leichte Aufgabe
Erstelle eine GUI-Anwendung mit PyQt5, die einen einfachen Liniengraphen darstellt. Verwende die Daten [1, 2, 3, 4, 5] für die x-Achse und [10, 15, 7, 12, 9] für die y-Achse.

### Musterlösung - Leichte Aufgabe:

```python
import sys
from PyQt5.QtWidgets import QApplication, QMainWindow, QVBoxLayout, QWidget
from matplotlib.backends.backend_qt5agg import FigureCanvasQTAgg as FigureCanvas
from matplotlib.figure import Figure

class LinienGraphApp(QMainWindow):
    def __init__(self):
        super().__init__()

        self.setWindowTitle('Liniengraph')
        self.setGeometry(100, 100, 600, 400)

        layout = QVBoxLayout()

        canvas = FigureCanvas(Figure(figsize=(5, 3)))
        layout.addWidget(canvas)

        self.setCentralWidget(QWidget(self))
        self.centralWidget().setLayout(layout)

        self.plot_liniengraph(canvas.figure)

    def plot_liniengraph(self, figure):
        ax = figure.add_subplot(111)
        x = [1, 2, 3, 4, 5]
        y = [10, 15, 7, 12, 9]
        ax.plot(x, y)
        ax.set_xlabel('X-Achse')
        ax.set_ylabel('Y-Achse')
        ax.set_title('Mein erster Liniengraph')

if __name__ == '__main__':
    app = QApplication(sys.argv)
    window = LinienGraphApp()
    window.show()
    sys.exit(app.exec_())
```
**Erklärung:**

   * Du importierst die benötigten Module, einschließlich PyQt5 und Matplotlib.
  
   * Du erstellst eine Klasse LinienGraphApp, die von QMainWindow erbt und die GUI-Anwendung repräsentiert.

   * Im Konstruktor der Klasse stellst du das Fensterlayout ein und legst den Fenstertitel und die Größe fest.

   * Du erstellst ein FigureCanvas, das das Matplotlib-Figure-Objekt verwendet. Dieses Canvas wird dem Layout hinzugefügt.

   * Das Hauptlayout (VBoxLayout) des Fensters wird erstellt, und das FigureCanvas wird diesem Layout hinzugefügt.

   * Du erstellst die Methode plot_liniengraph, die den eigentlichen Liniengraphen mit Matplotlib erstellt. Du verwendest die gegebenen Daten für die x- 
     und y-Achsenwerte und stellst das Achsenbeschriftungen und Titel ein.

   * Schließlich erstellst du die QApplication, die LinienGraphApp-Instanz und zeigst das Fenster an, um die GUI-Anwendung auszuführen.

 Mit diesem Code hast du erfolgreich einen Liniengraphen erstellt und in einer PyQt5-basierten GUI-Anwendung dargestellt. Das ist ein großer Schritt, um Daten visuell ansprechend darzustellen!

### Schwere Aufgabe
Erstelle eine GUI-Anwendung mit PyQt5, die ein gestapeltes Balkendiagramm darstellt. Verwende die Daten [23, 17, 35, 29] für die verschiedenen Kategorien "Äpfel", "Bananen", "Kirschen" und "Trauben".

### Musterlösung - Schwere Aufgabe:
```python
import sys
from PyQt5.QtWidgets import QApplication, QMainWindow, QVBoxLayout, QWidget
from matplotlib.backends.backend_qt5agg import FigureCanvasQTAgg as FigureCanvas
from matplotlib.figure import Figure

class GestapeltesBalkendiagrammApp(QMainWindow):
    def __init__(self):
        super().__init__()

        self.setWindowTitle('Gestapeltes Balkendiagramm')
        self.setGeometry(100, 100, 600, 400)

        layout = QVBoxLayout()

        canvas = FigureCanvas(Figure(figsize=(5, 3)))
        layout.addWidget(canvas)

        self.setCentralWidget(QWidget(self))
        self.centralWidget().setLayout(layout)

        self.plot_gestapeltes_balkendiagramm(canvas.figure)

    def plot_gestapeltes_balkendiagramm(self, figure):
        ax = figure.add_subplot(111)
        categories = ['Äpfel', 'Bananen', 'Kirschen', 'Trauben']
        data = [[23, 17, 35, 29]]
        ax.bar(categories, data[0])
        ax.set_xlabel('Kategorien')
        ax.set_ylabel('Anzahl')
        ax.set_title('Gestapeltes Balkendiagramm')

if __name__ == '__main__':
    app = QApplication(sys.argv)
    window = GestapeltesBalkendiagrammApp()
    window.show()
    sys.exit(app.exec_())
```

**Erklärung:**
   * Du importierst die notwendigen Module, darunter PyQt5 und Matplotlib.

   * Du erstellst die Klasse GestapeltesBalkendiagrammApp, die von QMainWindow erbt und die GUI-Anwendung repräsentiert.

   * Im Konstruktor der Klasse stellst du das Fensterlayout ein und legst den Fenstertitel und die Größe fest.

   * Du erstellst ein FigureCanvas, das das Matplotlib-Figure-Objekt verwendet. Dieses Canvas wird dem Layout hinzugefügt.

   * Das Hauptlayout (VBoxLayout) des Fensters wird erstellt, und das FigureCanvas wird diesem Layout hinzugefügt.

   * Du erstellst die Methode plot_gestapeltes_balkendiagramm, die das gestapelte Balkendiagramm mit Matplotlib erstellt. Du verwendest die gegebenen 
     Daten für die Kategorien und die Datenwerte, um gestapelte Balken zu erzeugen.

   * Schließlich erstellst du die QApplication, die GestapeltesBalkendiagrammApp-Instanz und zeigst das Fenster an, um die GUI-Anwendung auszuführen.

   Du hast erfolgreich ein gestapeltes Balkendiagramm mit PyQt5 und Matplotlib erstellt. Du kannst jetzt Daten auf anschauliche Weise visualisieren und darstellen. Großartige Arbeit!

## Fazit
Du hast es geschafft, oh furchtloser Python-Pionier! Du hast gelernt, wie man Graphen mit PyQt5 und Matplotlib erstellt. Jetzt kannst du Daten in lebendige Diagramme und Graphen verwandeln. Ganz gleich, ob du einen einfachen Liniengraph oder ein komplexes Balkendiagramm erstellen möchtest, du besitzt die Fähigkeiten, um deine Daten auf kreative Weise darzustellen. Also zeig der Welt, wie cool du als Grafik-Künstler bist!