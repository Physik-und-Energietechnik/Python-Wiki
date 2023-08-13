
## Einführung
Herzlich willkommen zu unserem Tutorial über die Darstellung von Graphen mit Kivy und Matplotlib in Python! In diesem Tutorial wirst du lernen, wie du mit Hilfe der Kivy-Bibliothek interaktive grafische Benutzeroberflächen (GUIs) erstellen kannst, um beeindruckende und aussagekräftige Graphen darzustellen. Graphen sind nicht nur nützlich, um Daten visuell ansprechend zu präsentieren, sondern sie können auch dabei helfen, komplexe Informationen leicht verständlich zu machen.

## Theorie
### Kivy - Eine kurze Einführung
Kivy ist eine Python-Bibliothek, die es dir ermöglicht, plattformübergreifende GUI-Anwendungen zu erstellen. Mit Kivy kannst du ansprechende Benutzeroberflächen erstellen, die sowohl auf Desktop-Computern als auch auf mobilen Geräten funktionieren.

### Matplotlib - Dein Werkzeug für Graphen
Matplotlib ist eine beliebte Python-Bibliothek zur Erstellung von Grafiken und Diagrammen. Du kannst damit verschiedenste Arten von Graphen erstellen, angefangen bei einfachen Linien- und Balkendiagrammen bis hin zu komplexen 3D-Plots.

### Code-Beispiel mit Kivy und Matplotlib:

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
## Aufgabe 1: Kivy-Graph
Erstelle eine Kivy-Anwendung, welche einen Graph angezeigt, der die Sinus-Funktion darstellt.

### Musterlösung:

```python
from kivy.app import App
from kivy.uix.boxlayout import BoxLayout
from kivy.uix.button import Button
from kivy.garden.matplotlib import FigureCanvasKivyAgg

import matplotlib.pyplot as plt
import numpy as np

class InteractiveGraphApp(App):
    def build(self):
        x = np.linspace(0, 2 * np.pi, 100)
        y = np.sin(x)

        plt.plot(x, y)
        plt.xlabel('X-Achse')
        plt.ylabel('Y-Achse')
        plt.title('Sinus-Graph')
        
        graph = FigureCanvasKivyAgg(plt.gcf())
        return graph
        
if __name__ == '__main__':
    InteractiveGraphApp().run()
```

## Aufgabe 2: Interaktiver Kivy-Graph
Erstelle eine Kivy-Anwendung, die einen Button enthält. Beim Drücken des Buttons wird ein Graph angezeigt, der die Sinus-Funktion darstellt.

### Musterlösung:

```python
from kivy.app import App
from kivy.uix.boxlayout import BoxLayout
from kivy.uix.button import Button
from kivy.garden.matplotlib import FigureCanvasKivyAgg

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

**Erklärung:**

 Du hast eine Kivy-Anwendung namen 'InteractiveGraphApp' erstellt:

   *  'from kivy.app import' App: Du importierst die App-Klasse von Kivy, die als Basis für deine Anwendung dient.

   * 'from kivy.uix.boxlayout' import 'BoxLayout' : Du importierst den 'BoxLayout', der verwendet wird, um Widgets in einer vertikalen oder horizontalen 
      Box anzuordnen.

   * 'from kivy.uix.button' import 'Button' : Du importierst den Button-Widget, den du später verwenden wirst.

   * 'from kivy.garden.matplotlib.backend_kivyagg' import 'FigureCanvasKivyAgg': Du importierst 'FigureCanvasKivyAgg' aus der Kivy Garden-Erweiterung, um 
      Matplotlib-Grafiken in Kivy anzuzeigen.

   *  import 'matplotlib.pyplot' as 'plt' und import 'numpy' as 'np': Du importierst Matplotlib und NumPy für die Erstellung des Sinus-Graphen.

 In der InteractiveGraphApp-Klasse:

   * def 'build(self)' : Hier definierst du die Benutzeroberfläche der App. Du erstellst einen vertikalen BoxLayout, fügst einen Button hinzu und einen 
     leeren BoxLayout, der später für den Graphen genutzt wird.

   * def 'show_graph(self, instance)': Diese Methode wird aufgerufen, wenn der Button gedrückt wird. Sie erstellt den Sinus-Graphen mithilfe von 
     Matplotlib und fügt ihn dann der Benutzeroberfläche hinzu.

   * 'if __name__ == '__main__':' : Diese Zeile überprüft, ob das Skript direkt ausgeführt wird (anstatt importiert zu werden) und startet die Kivy- 
      Anwendung.
 Du hast eine großartige Arbeit geleistet! Deine interaktive Kivy-Anwendung zeigt den Sinus-Graphen an, sobald der Button gedrückt wird. 

## Fazit
Herzlichen Glückwunsch! Du hast gelernt, wie du mit Kivy und Matplotlib beeindruckende Graphen in Python erstellen kannst. Mit Kivy kannst du interaktive Benutzeroberflächen gestalten, während Matplotlib dir die Möglichkeit gibt, vielfältige Grafiken zu erstellen. Jetzt kannst du deine Daten anschaulich visualisieren und deine eigenen GUI-Anwendungen entwickeln!

Gib nicht auf und experimentiere weiter mit verschiedenen Graphentypen und Interaktionsmöglichkeiten. Die Welt der Datenvisualisierung und GUI-Entwicklung steht dir offen!

Viel Spaß beim Coden!

## Links/ weitere Materials

https://www.geeksforgeeks.org/how-to-add-matplotlib-graph-in-kivy/





