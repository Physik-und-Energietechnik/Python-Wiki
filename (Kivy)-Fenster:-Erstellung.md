## Einführung
Willkommen zu unserem Python Tutorial über die Erstellung von Fenstern mit der Kivy-Bibliothek! Hast du dich jemals gefragt, wie du deine eigenen Benutzeroberflächen in Python erstellen kannst, die nicht nur funktional, sondern auch ansprechend sind? Nun, mit Kivy kannst du genau das tun!

In diesem Tutorial wirst du lernen, wie du mit Kivy Fenster erstellst, die es dir ermöglichen, interaktive Anwendungen zu entwickeln. Du musst kein Design-Experte sein, um coole und benutzerfreundliche Oberflächen zu gestalten. Lass uns gemeinsam erkunden, wie du mit Kivy die Fenster deiner Träume erstellen kannst!

## Theorie
Einführung in Kivy
Kivy ist eine Python-Bibliothek, die sich auf die Entwicklung von Multi-Touch-Anwendungen und Benutzeroberflächen spezialisiert hat. Es ist ideal für Anfänger, da es einfach zu erlernen ist und die Erstellung interaktiver Oberflächen erleichtert.

### Allgemeines Code-Beispiel
Hier ist ein einfaches Code-Beispiel, das das Grundgerüst eines Kivy-Fensters zeigt:

```python
from kivy.app import App
from kivy.uix.label import Label

class MeinApp(App):
    def build(self):
        return Label(text="Hallo, Kivy!")

if __name__ == "__main__":
    MeinApp().run()
```
### Explizites Code-Beispiel - Ein Fenster erstellen
Schauen wir uns ein Beispiel an, wie wir ein einfaches Fenster mit Kivy erstellen können:

```python
from kivy.app import App
from kivy.uix.button import Button

class MeinApp(App):
    def build(self):
        return Button(text="Klick mich!")

if __name__ == "__main__":
    MeinApp().run()
```
## Praxis
### Leichte Aufgabe
Erstelle eine Kivy-Anwendung, die ein Fenster mit einem Label enthält. Das Label soll den Text "Willkommen zu meiner Kivy-App!" anzeigen.

### Musterlösung - Leichte Aufgabe:
```python
from kivy.app import App
from kivy.uix.label import Label

class MeinApp(App):
    def build(self):
        return Label(text="Willkommen zu meiner Kivy-App!")

if __name__ == "__main__":
    MeinApp().run()
```
### Schwere Aufgabe
Erstelle eine Kivy-Anwendung, die zwei Buttons enthält. Ein Button soll den Text "Hallo" anzeigen, und der andere Button soll den Text "Tschüss" anzeigen. Beim Klicken auf einen Button soll eine Nachricht mit dem entsprechenden Text angezeigt werden.

### Musterlösung - Schwere Aufgabe:

```python
from kivy.app import App
from kivy.uix.button import Button
from kivy.uix.label import Label
from kivy.uix.boxlayout import BoxLayout

class MeinApp(App):
    def build(self):
        layout = BoxLayout(orientation='vertical')
        hello_button = Button(text="Hallo")
        goodbye_button = Button(text="Tschüss")
        message_label = Label(text="")

        hello_button.bind(on_press=lambda instance: self.show_message(message_label, "Hallo geklickt!"))
        goodbye_button.bind(on_press=lambda instance: self.show_message(message_label, "Tschüss geklickt!"))

        layout.add_widget(hello_button)
        layout.add_widget(goodbye_button)
        layout.add_widget(message_label)

        return layout

    def show_message(self, label, text):
        label.text = text

if __name__ == "__main__":
    MeinApp().run()
```
**Erklärung:**
   * Es wird eine Kivy-Anwendung (App) erstellt, indem eine Klasse namens MeinApp erstellt wird, die von App erbt.
   * Die build-Methode der MeinApp-Klasse wird überschrieben, um das Layout der Anwendung zu erstellen. Hier wird ein vertikaler BoxLayout erstellt, der 
     alle GUI-Elemente enthält.
   * Zwei Button-Widgets (Button) namens hello_button und goodbye_button werden erstellt und mit den Texten "Hallo" und "Tschüss" beschriftet.
   * Ein Label-Widget (Label) namens message_label wird erstellt, das standardmäßig keinen Text anzeigt.
   * Die bind-Methode wird verwendet, um Funktionen an die Klick-Events der Buttons zu binden. Beim Klicken eines Buttons wird die Methode show_message 
     aufgerufen, um den entsprechenden Text im message_label anzuzeigen.
   * Die Buttons und das Label werden dem BoxLayout hinzugefügt.
   * Die build-Methode gibt das Layout zurück, das dann als Hauptlayout der Anwendung dient.
   * Die Methode show_message aktualisiert den Text des Labels mit dem übergebenen Text.
   * Die Anwendung wird gestartet, indem eine Instanz von MeinApp erstellt und die run-Methode aufgerufen wird.
   * Die GUI-Anwendung enthält zwei Buttons ("Hallo" und "Tschüss"), und wenn einer der Buttons geklickt wird, wird der entsprechende Text im Label 
     angezeigt, um anzuzeigen, welcher Button geklickt wurde.

## Fazit
Du hast es geschafft! Du hast gelernt, wie man mit Kivy Fenster in Python erstellt und interaktive Benutzeroberflächen gestaltet. Egal, ob du einfache Labels oder komplexe Buttons erstellen möchtest, du hast jetzt das Werkzeug, um deine eigenen GUI-Anwendungen zu entwerfen. Viel Spaß beim Experimentieren und Erstellen mit Kivy!