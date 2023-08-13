
## Einführung
Herzlich willkommen zu unserem Tutorial über die Darstellung von Graphen mit Kivy und Matplotlib in Python! In diesem Tutorial wirst du lernen, wie du mit Hilfe der Kivy-Bibliothek interaktive grafische Benutzeroberflächen (GUIs) erstellen kannst, um beeindruckende und aussagekräftige Graphen darzustellen. Graphen sind nicht nur nützlich, um Daten visuell ansprechend zu präsentieren, sondern sie können auch dabei helfen, komplexe Informationen leicht verständlich zu machen.

## Theorie
### Kivy - Eine kurze Einführung
Kivy ist eine Python-Bibliothek, die es dir ermöglicht, plattformübergreifende GUI-Anwendungen zu erstellen. Mit Kivy kannst du ansprechende Benutzeroberflächen erstellen, die sowohl auf Desktop-Computern als auch auf mobilen Geräten funktionieren.

### Matplotlib - Dein Werkzeug für Graphen
Matplotlib ist eine beliebte Python-Bibliothek zur Erstellung von Grafiken und Diagrammen. Du kannst damit verschiedenste Arten von Graphen erstellen, angefangen bei einfachen Linien- und Balkendiagrammen bis hin zu komplexen 3D-Plots.

### Allgemeines Code-Beispiel
```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 15, 7, 12, 9]

plt.plot(x, y)
plt.xlabel('X-Achse')
plt.ylabel('Y-Achse')
plt.title('Einfacher Graph')
plt.show()
```
### Explizites Code-Beispiel mit Kivy und Matplotlib:

```python
from kivy.app import App
from kivy.uix.boxlayout import BoxLayout
from kivy.garden.matplotlib.backend_kivyagg import FigureCanvasKivyAgg

import matplotlib.pyplot as plt

class GraphApp(App):
    def build(self):
        layout = BoxLayout(orientation='vertical')
        
        x = [1, 2, 3, 4, 5]
        y = [10, 15, 7, 12, 9]

        plt.plot(x, y)
        plt.xlabel('X-Achse')
        plt.ylabel('Y-Achse')
        plt.title('Kivy und Matplotlib')
        
        graph = FigureCanvasKivyAgg(plt.gcf())
        layout.add_widget(graph)
        
        return layout

if __name__ == '__main__':
    GraphApp().run()
```
## Praxis
### Aufgabe 1: Einfacher Graph
Erstelle einen einfachen Graphen mit den x-Werten von 1 bis 10 und den y-Werten als Quadratzahlen der x-Werte.

### Musterlösung:

```python
import matplotlib.pyplot as plt

x = list(range(1, 11))
y = [val**2 for val in x]

plt.plot(x, y)
plt.xlabel('X-Achse')
plt.ylabel('Y-Achse')
plt.title('Quadratischer Graph')
plt.show()
```
## Aufgabe 2: Interaktiver Kivy-Graph
Erstelle eine Kivy-Anwendung, die einen Button enthält. Beim Drücken des Buttons wird ein Graph angezeigt, der die Sinus-Funktion darstellt.

### Musterlösung:

```python
from kivy.app import App
from kivy.uix.boxlayout import BoxLayout
from kivy.uix.button import Button
from kivy.garden.matplotlib.backend_kivyagg import FigureCanvasKivyAgg

import matplotlib.pyplot as plt
import numpy as np

class InteractiveGraphApp(App):
    def build(self):
        layout = BoxLayout(orientation='vertical')
        
        button = Button(text='Zeige Sinus-Graph')
        button.bind(on_press=self.show_graph)
        layout.add_widget(button)
        
        self.graph_layout = BoxLayout()
        layout.add_widget(self.graph_layout)
        
        return layout
    
    def show_graph(self, instance):
        self.graph_layout.clear_widgets()
        
        x = np.linspace(0, 2 * np.pi, 100)
        y = np.sin(x)

        plt.plot(x, y)
        plt.xlabel('X-Achse')
        plt.ylabel('Y-Achse')
        plt.title('Sinus-Graph')
        
        graph = FigureCanvasKivyAgg(plt.gcf())
        self.graph_layout.add_widget(graph)

if __name__ == '__main__':
    InteractiveGraphApp().run()
```
## Fazit
Herzlichen Glückwunsch! Du hast gelernt, wie du mit Kivy und Matplotlib beeindruckende Graphen in Python erstellen kannst. Mit Kivy kannst du interaktive Benutzeroberflächen gestalten, während Matplotlib dir die Möglichkeit gibt, vielfältige Grafiken zu erstellen. Jetzt kannst du deine Daten anschaulich visualisieren und deine eigenen GUI-Anwendungen entwickeln!

Gib nicht auf und experimentiere weiter mit verschiedenen Graphentypen und Interaktionsmöglichkeiten. Die Welt der Datenvisualisierung und GUI-Entwicklung steht dir offen!

Viel Spaß beim Coden!





