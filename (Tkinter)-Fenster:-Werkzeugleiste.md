## Einführung

Willkommen zu unserem Python-Tutorial für unerfahrene Nutzer! In diesem Tutorial werden wir uns mit der Erstellung und Anpassung von GUI-Fenstern in Python beschäftigen. Genauer gesagt werden wir uns auf die Werkzeugleiste konzentrieren, die es uns ermöglicht, verschiedene Funktionen und Optionen für unsere Benutzeroberfläche hinzuzufügen.

Aber Moment mal, was ist eine GUI überhaupt? GUI steht für *Graphical User Interface* (grafische Benutzeroberfläche) und ist das, was uns erlaubt, mit Programmen auf eine visuelle Weise zu interagieren. Stell dir vor, du möchtest ein Spiel spielen, aber alles, was du siehst, sind Buchstaben und Zahlen auf einem schwarzen Bildschirm - das wäre ziemlich langweilig, oder? Mit einer GUI können wir stattdessen bunte Fenster, Buttons und andere Elemente erstellen, um unsere Programme benutzerfreundlicher und ansprechender zu gestalten.

In diesem Tutorial werden wir die Tkinter-Bibliothek verwenden, die eine der Standardbibliotheken in Python ist und bereits mit Python installiert wird. Tkinter bietet uns alles, was wir brauchen, um GUIs zu erstellen und anzupassen. Klingt spannend, oder? Also lass uns direkt loslegen!

## Theorie

### Werkzeugleiste hinzufügen

Eine Werkzeugleiste ist ein nützliches Element in einer GUI, das verschiedene Optionen und Funktionen bereitstellt. In Tkinter können wir eine Werkzeugleiste mit Hilfe der `Frame`-Klasse erstellen. Hier ist ein Beispiel, wie wir eine Werkzeugleiste zu unserem Fenster hinzufügen können:

```python
import tkinter as tk

fenster = tk.Tk()

werkzeugleiste = tk.Frame(fenster)
werkzeugleiste.pack(side=tk.TOP, fill=tk.X)

fenster.mainloop()
```

In diesem Beispiel haben wir zuerst eine Instanz der `Frame`-Klasse erstellt und sie der Variablen `werkzeugleiste` zugewiesen. Dann haben wir die `pack()`-Methode verwendet, um die Werkzeugleiste oben im Fenster zu positionieren und es horizontal (in X-Richtung) auszufüllen.

### Beispiel: Fenster mit Werkzeugleiste

Hier ist ein vollständiges Beispiel, das sowohl die Erstellung eines Fensters als auch das Hinzufügen einer Werkzeugleiste demonstriert:

```python
import tkinter as tk

def beenden():
    fenster.quit()

fenster = tk.Tk()

werkzeugleiste = tk

.Frame(fenster)
werkzeugleiste.pack(side=tk.TOP, fill=tk.X)

beenden_button = tk.Button(werkzeugleiste, text="Beenden", command=beenden)
beenden_button.pack(side=tk.LEFT)

fenster.mainloop()
```

In diesem Beispiel haben wir eine Funktion `beenden()` definiert, die aufgerufen wird, wenn der "Beenden"-Button in der Werkzeugleiste gedrückt wird. Der Button selbst wird mit der `Button`-Klasse erstellt und der Funktion `beenden()` als Befehl zugewiesen. Der Button wird dann in der Werkzeugleiste platziert.

## Praxis

### Aufgabe 1

Deine Aufgabe besteht darin, ein Fenster zu erstellen und diesem eine Werkzeugleiste hinzuzufügen

**Musterlösung:**
```python
import tkinter as tk

def button_click():
    print("Button wurde geklickt!")

# Fenster erstellen
fenster = tk.Tk()
fenster.title("Werkzeugleiste Beispiel")

# Werkzeugleiste erstellen
werkzeugleiste = tk.Frame(fenster)
werkzeugleiste.pack(side=tk.TOP, fill=tk.X)

# Schaltflächen (Buttons) zur Werkzeugleiste hinzufügen
button1 = tk.Button(werkzeugleiste, text="Button 1", command=button_click)
button1.pack(side=tk.LEFT)

button2 = tk.Button(werkzeugleiste, text="Button 2", command=button_click)
button2.pack(side=tk.LEFT)

# Fenster ausführen
fenster.mainloop()
```

**Erklärung:**
In dieser Aufgabe haben wir eine Werkzeugleiste erstellt und zwei Schaltflächen (Buttons) "Button 1" und "Button 2" hinzugefügt. Die Schaltflächen sind so konfiguriert, dass die Funktion **'button_click'** aufgerufen wird, wenn sie geklickt werden. Hier wurde eine einfache Ausgabe "Button wurde geklickt!" implementiert, aber du kannst diese Funktion nach Belieben anpassen.

### Aufgabe 2

Deine Aufgabe besteht darin, zwei Schaltflächen zur Werkzeugleiste hinzuzufügen: eine zum Drucken und eine zum Speichern. Verwende die vorhandenen Code-Beispiele als Ausgangspunkt und experimentiere ein wenig:

**Müsterlösung:**

```python
import tkinter as tk

def beenden():
    fenster.quit()

fenster = tk.Tk()

werkzeugleiste = tk.Frame(fenster)
werkzeugleiste.pack(side=tk.TOP, fill=tk.X)

beenden_button = tk.Button(werkzeugleiste, text="Beenden", command=beenden)
beenden_button.pack(side=tk.LEFT)

drucken_button = tk.Button(werkzeugleiste, text="Drucken")
drucken_button.pack(side=tk.LEFT)

speichern_button = tk.Button(werkzeugleiste, text="Speichern")
speichern_button.pack(side=tk.LEFT)

fenster.mainloop()
```

**Erklärung:**
In diesem aktualisierten Code wurde für die Schaltflächen "Drucken" und "Speichern" die entsprechenden Funktionen drucken und speichern als command angegeben. Diese Funktionen werden aufgerufen, wenn die Schaltflächen geklickt werden. Hier habe ich sie einfach implementiert, um eine Nachricht in der Konsole auszugeben, aber du kannst sie nach Bedarf anpassen, um die gewünschte Funktionalität zu erreichen.

## Fazit

Herzlichen Glückwunsch! Du hast gelernt, wie man mit Tkinter Fenster erstellt und eine Werkzeugleiste hinzufügt. Du kannst nun Schaltflächen hinzufügen, Funktionen definieren und sogar Farben auswählen. Mit diesen Grundlagen kannst du deine eigenen benutzerfreundlichen GUIs in Python erstellen und sie nach Belieben anpassen.

Wir hoffen, dass dir dieses Tutorial geholfen hat und dass du Spaß dabei hattest, Python zu entdecken. Denk daran, dass dies nur ein kleiner Einblick in die Welt der GUI-Programmierung ist, und es gibt noch so viel mehr zu lernen und zu entdecken. Also mach weiter und werde ein echter GUI-Meister!