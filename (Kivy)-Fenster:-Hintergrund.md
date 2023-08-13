## Einführung
Willkommen zum aufregenden Python Tutorial über GUI-Programmierung mit Kivy! Hier dreht sich alles um die Gestaltung von Fenstern und die Farben, die das Herz deiner Anwendung ausmachen werden. Keine Sorge, wenn du denkst, dass Hintergründe nur für Maler und Tapetenfans sind – nach diesem Tutorial wirst du sehen, wie sie deine Benutzeroberfläche wirklich zum Leuchten bringen!

In diesem Tutorial wirst du lernen, wie man nicht nur Fenster erstellt, sondern auch wie man ihnen einen individuellen Anstrich verleiht. Wir werden uns mit Hintergrundfarben beschäftigen und du wirst in der Lage sein, deine Anwendung mit einem wunderbaren visuellen Ambiente auszustatten.

## Theorie
**Grundlagen von Kivy-Fenstern**
In der Welt von Kivy sind Fenster deine Leinwand, auf der du deine kreativen Ideen zaubern kannst. Hier sind einige Grundlagen:
1. **Fenster erstellen:** Du kannst ein Fenster mit Kivy ganz einfach erstellen, indem du die App- und BoxLayout-Klassen verwendest.

2. **Hintergrundfarben:** Du kannst die Hintergrundfarbe eines Fensters leicht ändern, um deiner Anwendung eine persönliche Note zu verleihen.

### Code-Beispiel - Hintergrundfarbe ändern
Schauen wir uns an, wie man die Hintergrundfarbe eines Kivy-Fensters ändert:

```python
from kivy.app import App
from kivy.uix.boxlayout import BoxLayout
from kivy.uix.label import Label

class FarbigeApp(App):
    def build(self):
        layout = BoxLayout(orientation='vertical', padding=10)
        
        # Ändere die Hintergrundfarbe auf Hellblau (0.6, 0.8, 1, 1)
        layout.background_color = (0.6, 0.8, 1, 1)
        
        label = Label(text="Ich habe einen coolen Hintergrund!", font_size=20)
        layout.add_widget(label)
        
        return layout

if __name__ == '__main__':
    FarbigeApp().run()
```
## Praxis
### Leichte Aufgabe
Erstelle eine Kivy-Anwendung, die ein Fenster mit einem grünen Hintergrund enthält.

### Musterlösung - Leichte Aufgabe:

```python
from kivy.app import App
from kivy.uix.boxlayout import BoxLayout
from kivy.core.window import Window

class GrueneApp(App):
    def build(self):
        
        layout = BoxLayout(orientation='vertical', padding=10)
        
        # Ändere die Hintergrundfarbe auf Grün (0, 1, 0, 1)
        Window.clearcolor = (0, 1, 0, 1)
        
        return layout

if __name__ == '__main__':
    GrueneApp().run()
```

### Schwere Aufgabe
Erstelle eine Kivy-Anwendung mit einem Fenster, das einen Farbverlauf als Hintergrund hat. Zum Beispiel von Schwarz (links) nach Blau (rechts).

### Musterlösung - Schwere Aufgabe:
```python
from kivy.app import App
from kivy.uix.boxlayout import BoxLayout
from kivy.graphics import Line, Color
from kivy.core.window import Window

class Background(BoxLayout):
    def __init__(self):
        super(Background, self).__init__()
        self.width = Window.size[0]
        self.height = Window.size[1]
        self.add_gradient()

    def add_gradient(self):
        alpha_channel_rate = 0
        increase_rate = 1 / self.width

        for sep in range(self.width):
            self.canvas.add(Color(rgba=(0, 0, 1, alpha_channel_rate)))
            self.canvas.add(Line(points=[sep, 0, sep, self.height], width=1))
            alpha_channel_rate += increase_rate

class FarbverlaufApp(App):
    def build(self):
        background = Background()
        return background

if __name__ == '__main__':
    FarbverlaufApp().run()

# Quelle: https://stackoverflow.com/a/65401770
```

## Fazit
Das war's! Du hast nun gelernt, wie du in Kivy Fenster erstellst und sie mit Hintergrundfarben gestaltest. Von nun an kannst du deine Anwendungen nicht nur funktional, sondern auch optisch ansprechend gestalten. Spiele mit Farben herum und lass deiner Kreativität freien Lauf! Deine Anwendungen werden garantiert so strahlen wie ein Regenbogen.