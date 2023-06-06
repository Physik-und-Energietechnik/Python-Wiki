## Einführung
Willkommen zu unserem Python-Tutorial für unerfahrene Nutzer! In diesem Tutorial werden wir uns mit der GUI-Darstellung von Graphen beschäftigen. Aber was genau bedeutet das? Nun, GUI steht für Graphical User Interface, also eine grafische Benutzeroberfläche. Ein Graph ist hierbei eine Darstellung von Datenpunkten, die durch Knoten und Kanten verbunden sind. In diesem Tutorial lernst du, wie du mithilfe der Tkinter-Bibliothek in Python Graphen erstellen und anzeigen kannst. Das erlangte Wissen ermöglicht es dir, ansprechende und interaktive grafische Darstellungen in deinen Python-Programmen zu erstellen. Das ist nicht nur praktisch, sondern auch ziemlich cool!

## Theorie
### Grundlagen von Tkinter
Tkinter ist eine Python-Bibliothek, die es uns ermöglicht, GUI-Anwendungen zu erstellen. Es bietet eine Vielzahl von Widgets (grafische Elemente) wie Buttons, Textfelder, Labels und mehr. Um Tkinter zu verwenden, müssen wir es zuerst importieren:

´´´python

import tkinter as tk

´´´
## Erstellen eines Fensters
Um ein Fenster zu erstellen, benötigen wir ein sogenanntes root-Widget. Das ist das Hauptfenster unserer Anwendung. Hier ist ein Beispielcode, der ein einfaches Fenster erstellt:

´´´python
import tkinter as tk

root = tk.Tk()  # Das Hauptfenster erstellen
root.mainloop()  # Das Fenster anzeigen
´´´

## Erstellen eines Graphen
Nun, da wir ein Fenster haben, möchten wir einen Graphen darin anzeigen. Glücklicherweise bietet Tkinter das Canvas-Widget, das uns dabei hilft. Hier ist ein Beispielcode, der einen einfachen Graphen erstellt:

´´´python

import tkinter as tk

root = tk.Tk()  # Das Hauptfenster erstellen

canvas = tk.Canvas(root, width=400, height=300)  # Ein Canvas-Widget erstellen
canvas.pack()

# Einen roten Kreis als Knoten zeichnen
canvas.create_oval(100, 100, 200, 200, fill="red")

# Eine Linie als Kante zeichnen
canvas.create_line(100, 100, 200, 200)

root.mainloop()  # Das Fenster anzeigen

´´´

## Praxis
### Leichte Aufgabe: Erstelle einen einfachen Graphen
Deine Aufgabe besteht darin, einen einfachen Graphen mit zwei Knoten und einer Kante zu erstellen. Verwende verschiedene Farben für die Knoten und die Kante, um es interessanter zu gestalten.

Hier ist eine Musterlösung:

´´´python
import tkinter as tk

root = tk.Tk()  # Das Hauptfenster erstellen

canvas = tk.Canvas(root, width=400, height=300)  # Ein Canvas-Widget erstellen
canvas.pack()

# Ersten Knoten zeichnen
canvas.create_oval(100, 100, 150, 150, fill="blue")

# Zweiten Knoten zeichnen
canvas.create_oval(250, 100, 300, 150, fill="green")

# Kante zeichnen
canvas.create_line(125, 125, 275, 125, fill="red", width=2)

root.mainloop()  # Das Fenster anzeigen

´´´
## Schwierigere Aufgabe: Erstelle einen interaktiven Graphen

Jetzt wird es etwas anspruchsvoller! Deine Aufgabe besteht darin, einen interaktiven Graphen zu erstellen, der es dem Benutzer ermöglicht, Knoten hinzuzufügen, zu verschieben und zu löschen. Du kannst dabei die Mausereignisse verwenden, um die Interaktion umzusetzen.

Hier ist eine Musterlösung, um dich zu inspirieren:

´´´python
import tkinter as tk

# Funktion zum Hinzufügen eines neuen Knotens
def add_node(event):
    x = event.x
    y = event.y
    canvas.create_oval(x-25, y-25, x+25, y+25, fill="purple")

root = tk.Tk()  # Das Hauptfenster erstellen

canvas = tk.Canvas(root, width=400, height=300)  # Ein Canvas-Widget erstellen
canvas.pack()

# Mausereignis zum Hinzufügen eines neuen Knotens binden
canvas.bind("<Button-1>", add_node)

root.mainloop()  # Das Fenster anzeigen
´´´
## Fazit
Herzlichen Glückwunsch! Du hast erfolgreich gelernt, wie du mit Python und Tkinter Graphen in einer grafischen Benutzeroberfläche darstellen kannst. Wir haben die Grundlagen von Tkinter kennengelernt und sowohl einfache als auch interaktive Graphen erstellt. Du kannst dieses Wissen nutzen, um beeindruckende Datenvisualisierungen, Spiele oder andere spannende Anwendungen zu entwickeln. Lass deiner Kreativität freien Lauf und hab Spaß beim Programmieren!