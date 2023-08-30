## Einführung

Willkommen zum Python-Tutorial zur Darstellung von Bildern in einer grafischen Benutzeroberfläche (GUI) mit Hilfe von Tkinter und Pillow! In diesem Tutorial werden wir lernen, wie man Bilder in eine Tkinter-Anwendung integriert und sie in der GUI darstellt.

Bilder sind eine großartige Möglichkeit, um Benutzeroberflächen ansprechender und visuell ansprechender zu gestalten. Sie können verwendet werden, um Logos, Hintergrundbilder, Schaltflächenbilder und vieles mehr anzuzeigen.

## Theorie

### Ein Bild anzeigen

Um ein Bild in Tkinter anzuzeigen, müssen wir es zuerst mit Pillow öffnen und dann in ein von Tkinter verständliches Format konvertieren. Dies können wir mit der Funktion `Image.open()` und der Funktion `ImageTk.PhotoImage()` erreichen. Anschließend kann es mithilfe eines Labels im Fenster angezeigt werden.

Hier ist ein allgemeines Code-Beispiel, in welchem das Bild "bild.jpg" angezeigt wird:

```python
import tkinter as tk
from PIL import Image, ImageTk

# Tkinter-Fenster erstellen
window = tk.Tk()

# Bild öffnen
image = Image.open("bild.jpg")

# Bild in Tkinter-Format konvertieren
photo = ImageTk.PhotoImage(image)

# Bild in einem Tkinter-Label anzeigen
label = tk.Label(window, image=photo)
label.pack()

# Tkinter-Schleife starten
window.mainloop()
```

Stelle sicher, dass du den Pfad zur Bilddatei entsprechend anpasst.

## Praxis

### Aufgabe 1

Integriere ein Bild in deine Tkinter-Anwendung und zeige es in einem Label an. Das Bild kann in seiner ursprünglichen Größe angezeigt werden.

**Musterlösung:**

```python
import tkinter as tk
from PIL import Image, ImageTk

# Tkinter-Fenster erstellen
window = tk.Tk()

# Bild öffnen
image = Image.open("bild.jpg")

# Bild in Tkinter-Format konvertieren
photo = ImageTk.PhotoImage(image)

# Bild in einem Tkinter-Label anzeigen
label = tk.Label(window, image=photo)
label.pack()

# Tkinter-Schleife starten
window.mainloop()
```

### Aufgabe 2

Integriere ein Bild in deine Tkinter-Anwendung und zeige es in einem Label an. Passe die Größe des Bildes vorher auf `300x200` an.

**Musterlösung:**

```python
import tkinter as tk
from PIL import Image, ImageTk

# Tkinter-Fenster erstellen
window = tk.Tk()

# Bild importieren und die Größe anpassen
image = Image.open("bild.jpg")
resized_image = image.resize((300, 200))

# Bild integrieren
resized_photo = ImageTk.PhotoImage(resized_image)
resized_label = tk.Label(window, image=resized_photo)
resized_label.pack()

# Tkinter-Schleife starten
window.mainloop()
```

## Fazit

Herzlichen Glückwunsch! Du hast gelernt, wie man Bilder in Tkinter integriert und sie in einer grafischen Benutzeroberfläche darstellt. Bilder sind ein großartiges Werkzeug, um deine Benutzeroberfläche zu verbessern und sie ansprechender zu gestalten. Du kannst nun kreative Anwendungen mit visuellen Elementen erstellen. Viel Spaß beim Programmieren!