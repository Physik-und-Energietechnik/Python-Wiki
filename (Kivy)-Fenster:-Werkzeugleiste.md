## Einführung
Willkommen zum aufregenden Abenteuer der GUI-Programmierung in Python mit Kivy! In diesem Tutorial wirst du die faszinierende Welt der Werkzeugleisten in GUI-Anwendungen kennenlernen. Aber Moment mal, was zur Hölle ist eine Werkzeugleiste? Keine Sorge, wir werden das gemeinsam erkunden!

Stell dir vor, du hättest einen magischen Werkzeugkasten, der dir erlaubt, Schaltflächen, Schieber und andere coole Dinge zu deiner Benutzeroberfläche hinzuzufügen. Werkzeugleisten sind wie deine persönlichen Superkräfte, um deine GUI interaktiv und ansprechend zu gestalten.

In diesem Tutorial wirst du lernen, wie du Kivy verwendest, um Fenster mit Werkzeugleisten zu erstellen. Wir werden gemeinsam durch die Theorie und Praxis gehen, und am Ende wirst du in der Lage sein, erstaunliche GUI-Anwendungen zu bauen, die sogar deinen Kaffeekocher vor Neid erblassen lassen!

## Theorie
**Grundlagen der Werkzeugleiste**
Eine Werkzeugleiste ist im Grunde genommen eine Sammlung von Schaltflächen, Symbolen und anderen Interaktionselementen, die es dem Benutzer ermöglichen, verschiedene Aktionen auszuführen. Denke an sie wie an ein Menü von Zaubertränken, die deine Anwendung zum Leben erwecken!

Wir werden uns auf einige wichtige Elemente konzentrieren:

**ToolButtons:** Das sind die Helden deiner Werkzeugleiste. Jeder ToolButton hat ein Symbol und kann angeklickt werden, um eine bestimmte Aktion auszuführen.

**Action:** Aktionen sind die Befehle, die von den ToolButtons ausgeführt werden. Sie sagen deiner Anwendung, was passieren soll, wenn der Benutzer auf einen Button klickt.

### Allgemeines Code-Beispiel
Bevor wir in die spezifischen Python-Beispiele eintauchen, schauen wir uns ein allgemeines Code-Beispiel an, das dir den Grundgedanken einer Werkzeugleiste vermittelt:

```python
from kivy.app import App
from kivy.uix.boxlayout import BoxLayout
from kivy.uix.button import Button

class MyToolbarApp(App):
    def build(self):
        layout = BoxLayout(orientation='horizontal')

        button1 = Button(text='Aktion 1')
        button2 = Button(text='Aktion 2')

        layout.add_widget(button1)
        layout.add_widget(button2)

        return layout

if __name__ == '__main__':
    MyToolbarApp().run()
```
### Explizites Code-Beispiel - Werkzeugleiste erstellen
Hier ist ein Beispiel, wie du mit Kivy eine einfache Werkzeugleiste erstellst:

```python
from kivy.app import App
from kivy.uix.boxlayout import BoxLayout
from kivy.uix.button import Button

class MyToolbarApp(App):
    def build(self):
        layout = BoxLayout(orientation='horizontal')

        action1 = Button(text='Aktion 1')
        action2 = Button(text='Aktion 2')

        layout.add_widget(action1)
        layout.add_widget(action2)

        return layout

if __name__ == '__main__':
    MyToolbarApp().run()
```
## Praxis
### Leichte Aufgabe
Erstelle eine GUI-Anwendung mit Kivy, die eine Werkzeugleiste mit zwei ToolButtons enthält. Jeder Button soll eine Aktion auslösen, die eine Nachricht in der Konsole ausgibt.

### Musterlösung - Leichte Aufgabe:

```python
from kivy.app import App
from kivy.uix.boxlayout import BoxLayout
from kivy.uix.button import Button

class MyToolbarApp(App):
    def action1(self):
        print("Aktion 1 wurde ausgeführt!")

    def action2(self):
        print("Aktion 2 wurde ausgeführt!")

    def build(self):
        layout = BoxLayout(orientation='horizontal')

        action1_button = Button(text='Aktion 1')
        action1_button.bind(on_press=self.action1)

        action2_button = Button(text='Aktion 2')
        action2_button.bind(on_press=self.action2)

        layout.add_widget(action1_button)
        layout.add_widget(action2_button)

        return layout

if __name__ == '__main__':
    MyToolbarApp().run()
```
**Erklärung:**
 
   * Die Zeile from kivy.app import App importiert die 'App-Klasse' aus der Kivy-Bibliothek, die als Basis für unsere GUI-Anwendung dient.

   * from 'kivy.uix.boxlayout' import 'BoxLayout' importiert die 'BoxLayout-Klasse', die es ermöglicht, Widgets horizontal oder vertikal anzuordnen.

     from 'kivy.uix.button' import 'Button' importiert die 'Button-Klasse', mit der wir Schaltflächen erstellen können.

   * class 'MyToolbarApp' (App): definiert eine eigene Klasse 'MyToolbarApp', die von der App-Klasse von Kivy erbt. Diese Klasse repräsentiert unsere 
     GUI-Anwendung.

   * **def action1(self)**: definiert eine Methode namens action1, die ausgeführt wird, wenn der erste Button geklickt wird. In diesem Fall wird einfach 
      "Aktion 1 wurde ausgeführt!" in der Konsole ausgegeben.

   * **def action2(self)**: definiert eine Methode namens action2, die ausgeführt wird, wenn der zweite Button geklickt wird. Auch hier wird "Aktion 2 
       wurde ausgeführt!" in der Konsole ausgegeben.

   * **def build(self)**: ist eine Methode, die von der App-Klasse erwartet wird. Hier definieren wir das Layout unserer Anwendung.

   * layout = BoxLayout(orientation='horizontal') erstellt ein horizontales BoxLayout, das die beiden Buttons nebeneinander anordnet.

   * action1_button = Button(text='Aktion 1') erstellt einen Button mit dem Text "Aktion 1".

   * action1_button.bind(on_press=self.action1) verknüpft den ersten Button mit der Methode action1, sodass diese Methode aufgerufen wird, wenn der 
     Button geklickt wird.

   * Ähnlich wird action2_button erstellt und mit der Methode action2 verknüpft.

   * layout.add_widget(action1_button) fügt den ersten Button zum Layout hinzu.

   * layout.add_widget(action2_button) fügt den zweiten Button zum Layout hinzu.

   * return layout gibt das Layout als Hauptelement der GUI-Anwendung zurück.

   * if __name__ == '__main__': überprüft, ob der Code direkt ausgeführt wird (statt importiert zu werden).

   * MyToolbarApp().run() erstellt eine Instanz der MyToolbarApp-Klasse und startet die GUI-Anwendung.

   Dieser Code erstellt eine GUI-Anwendung mit zwei Buttons in einer horizontalen Werkzeugleiste. Wenn einer der Buttons geklickt wird, wird die 
   zugehörige Methode ausgeführt und eine Nachricht wird in der Konsole angezeigt. Du kannst diesen Code ausführen, um die Funktionsweise einer einfachen 
   Werkzeugleiste in Kivy zu sehen.


### Schwere Aufgabe
Erstelle eine GUI-Anwendung mit einer Werkzeugleiste, die eine Textbox und einen Button enthält. Wenn der Button geklickt wird, soll der Text aus der Textbox in der Konsole angezeigt werden.

### Musterlösung - Schwere Aufgabe:

```python
from kivy.app import App
from kivy.uix.boxlayout import BoxLayout
from kivy.uix.textinput import TextInput
from kivy.uix.button import Button

class MyToolbarApp(App):
    def display_text(self, instance):
        entered_text = self.text_input.text
        print(f"Eingegebener Text: {entered_text}")

    def build(self):
        layout = BoxLayout(orientation='vertical')

        self.text_input = TextInput(hint_text='Text eingeben...')
        submit_button = Button(text='Anzeigen')
        submit_button.bind(on_press=self.display_text)

        layout.add_widget(self.text_input)
        layout.add_widget(submit_button)

        return layout

if __name__ == '__main__':
    MyToolbarApp().run()
```
**Erklärung:**

  Dieser Python-Code nutzt die Kivy-Bibliothek, um eine GUI-Anwendung zu erstellen, die eine einfache Eingabeaufforderung und einen Button enthält. Wenn 
  der Button geklickt wird, wird der eingegebene Text in der Konsole angezeigt:

  * from kivy.app import App importiert die App-Klasse aus Kivy, die als Grundlage für unsere GUI-Anwendung dient.

  * from kivy.uix.boxlayout import BoxLayout importiert die BoxLayout-Klasse, die es ermöglicht, Widgets vertikal oder horizontal anzuordnen.

  * from kivy.uix.textinput import TextInput importiert die TextInput-Klasse, mit der wir Texteingabefelder erstellen können.

  * from kivy.uix.button import Button importiert die Button-Klasse, um Schaltflächen zu erstellen.

  * class MyToolbarApp(App): definiert eine eigene Klasse namens MyToolbarApp, die von der App-Klasse von Kivy erbt. Diese Klasse repräsentiert unsere 
    GUI-Anwendung.

  * def display_text(self, instance): definiert eine Methode namens display_text, die ausgeführt wird, wenn der Button geklickt wird. Diese Methode liest 
    den eingegebenen Text aus dem Texteingabefeld und gibt ihn in der Konsole aus.

  * def build(self): ist eine Methode, die von der App-Klasse erwartet wird. Hier definieren wir das Layout unserer Anwendung.

  * layout = BoxLayout(orientation='vertical') erstellt ein vertikales BoxLayout, das die Widgets untereinander anordnet.

  * self.text_input = TextInput(hint_text='Text eingeben...') erstellt ein Texteingabefeld mit einem Platzhaltertext.

  * submit_button = Button(text='Anzeigen') erstellt einen Button mit dem Text "Anzeigen".

  * submit_button.bind(on_press=self.display_text) verknüpft den Button mit der Methode display_text, sodass diese Methode aufgerufen wird, wenn der 
    Button geklickt wird.

  * layout.add_widget(self.text_input) fügt das Texteingabefeld zum Layout hinzu.

  * layout.add_widget(submit_button) fügt den Button zum Layout hinzu.

  * return layout gibt das Layout als Hauptelement der GUI-Anwendung zurück.

  * if __name__ == '__main__': überprüft, ob der Code direkt ausgeführt wird (statt importiert zu werden).

  * MyToolbarApp().run() erstellt eine Instanz der MyToolbarApp-Klasse und startet die GUI-Anwendung.

## Fazit
Und da hast du es, den magischen Werkzeugkasten der Kivy GUI-Programmierung! Du hast gelernt, wie du Werkzeugleisten erstellst, mit ToolButtons jonglierst und Aktionen zum Leben erweckst. Mit diesen Fähigkeiten bist du bereit, interaktive und spannende Benutzeroberflächen zu erstellen, die sogar dein Haustier beeindrucken werden. Also ran an den Code und lass die GUI-Zauberei beginnen!