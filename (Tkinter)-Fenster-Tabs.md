## Einführung
Willkommen zu unserem Python-Tutorial über die Erstellung von GUI-Fenstern mit Tabs! In diesem Tutorial werden wir lernen, wie man mit der Tkinter-Bibliothek in Python mehrere Registerkarten in einem Fenster erstellt.

Hast du dich jemals gefragt, wie Programme wie Webbrowser oder Texteditoren es schaffen, mehrere offene Dateien oder Webseiten in einem einzigen Fenster zu organisieren? Die Antwort lautet: Tabs! Tabs ermöglichen es uns, den verfügbaren Platz effizient zu nutzen und zwischen verschiedenen Inhalten einfach zu navigieren.

In diesem Tutorial wirst du lernen, wie du Tabs in Python-GUI-Anwendungen erstellst und sie mit Inhalten füllst. Du wirst in der Lage sein, Benutzeroberflächen zu entwerfen, die verschiedene Funktionen oder Informationen in übersichtlichen Tabs organisieren. Dieses Wissen ist besonders nützlich, wenn du eigene Anwendungen entwickeln möchtest, bei denen es wichtig ist, den Benutzern eine klare und intuitive Benutzeroberfläche anzubieten.

## Theorie
### Tkinter - Die Python GUI-Bibliothek
In diesem Tutorial werden wir die Tkinter-Bibliothek verwenden, um GUI-Fenster mit Tabs zu erstellen. Tkinter ist in Python standardmäßig verfügbar, so dass du keine zusätzlichen Installationen vornehmen musst.

Tkinter bietet eine Vielzahl von Funktionen und Widgets (Elemente der Benutzeroberfläche), mit denen wir interaktive Anwendungen erstellen können. Eines dieser Widgets ist das Notebook-Widget, das uns ermöglicht, Tabs in unserem Fenster zu erstellen.

### Allgemeines Code-Beispiel
Hier ist ein allgemeines Beispiel, um das Konzept der Tabs zu verdeutlichen:

```python
import tkinter as tk
from tkinter import ttk

# Erstelle ein neues Fenster
fenster = tk.Tk()

# Erstelle ein Notebook-Widget, das die Tabs enthält
notebook = ttk.Notebook(fenster)

# Erstelle die Tabs
tab1 = ttk.Frame(notebook)
tab2 = ttk.Frame(notebook)

# Füge die Tabs zum Notebook hinzu
notebook.add(tab1, text="Tab 1")
notebook.add(tab2, text="Tab 2")

# Packe das Notebook in das Fenster
notebook.pack()

# Starte die Hauptereignisschleife
fenster.mainloop()
```
### Explizites Code-Beispiel
Hier ist ein spezifisches Beispiel, das dir zeigt, wie man einem Tab Inhalt hinzufügt:

```python
import tkinter as tk
from tkinter import ttk

def btn_click():
    label.configure(text="Hallo von Tab 2!")

fenster = tk.Tk()

notebook = ttk.Notebook(fenster)

tab1 = ttk.Frame(notebook)
tab2 = ttk.Frame(notebook)

# Erstelle ein Label für Tab 1
label = ttk.Label(tab1, text="Willkommen zu Tab 1")
label.pack()

# Erstelle einen Button für Tab 2
button = ttk.Button(tab2, text="Klick mich!", command=btn_click)
button.pack()

notebook.add(tab1, text="Tab 1")
notebook.add(tab2, text="Tab 2")

notebook.pack()

fenster.mainloop()
```
## Praxis
### Aufgabe 1
Erstelle ein GUI-Fenster mit zwei Tabs. Füge jedem Tab einen Button hinzu und lasse ihn eine Funktion aufrufen, die eine Nachricht auf der Konsole ausgibt.

### Musterlösung für Aufgabe 1
Hier ist eine mögliche Lösung für Aufgabe 1:

```python
import tkinter as tk
from tkinter import ttk

def btn_click():
    print("Button wurde geklickt!")

fenster = tk.Tk()

notebook = ttk.Notebook(fenster)

tab1 = ttk.Frame(notebook)
tab2 = ttk.Frame(notebook)

button1 = ttk.Button(tab1, text="Klick mich!", command=btn_click)
button1.pack()

button2 = ttk.Button(tab2, text="Klick mich auch!", command=btn_click)
button2.pack()

notebook.add(tab1, text="Tab 1")
notebook.add(tab2, text="Tab 2")

notebook.pack()

fenster.mainloop()
```
### Aufgabe 2
Erweitere das GUI-Fenster, indem du jedem Tab zusätzlichen Inhalt hinzufügst, wie z.B. Labels oder Eingabefelder.

### Musterlösung für Aufgabe 2
Hier ist eine mögliche Lösung für Aufgabe 2:

```python
import tkinter as tk
from tkinter import ttk

fenster = tk.Tk()

notebook = ttk.Notebook(fenster)

tab1 = ttk.Frame(notebook)
tab2 = ttk.Frame(notebook)

label1 = ttk.Label(tab1, text="Willkommen zu Tab 1")
label1.pack()

label2 = ttk.Label(tab2, text="Hallo von Tab 2!")
label2.pack()

notebook.add(tab1, text="Tab 1")
notebook.add(tab2, text="Tab 2")

notebook.pack()

fenster.mainloop()
```

## Fazit
In diesem Tutorial haben wir gelernt, wie man mit der Tkinter-Bibliothek in Python GUI-Fenster mit Tabs erstellt. Tabs ermöglichen es uns, verschiedene Inhalte übersichtlich in einem einzigen Fenster zu organisieren. Durch die Verwendung von Tkinter können wir mit wenig Code leistungsstarke GUI-Anwendungen erstellen.

Du bist jetzt in der Lage, eigene Python-Anwendungen zu entwickeln, bei denen die Informationen oder Funktionen in Tabs organisiert werden. Du hast gelernt, wie man Tabs erstellt, ihnen Inhalt hinzufügt und auf Benutzerinteraktionen reagiert. Viel Spaß beim Erstellen toller Benutzeroberflächen für deine Python-Anwendungen!