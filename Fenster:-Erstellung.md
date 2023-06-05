## Einführung

Willkommen zu diesem Abschnitt, in dem wir lernen, wie man in Python ein GUI-Fenster erstellt! In diesem Tutorial werden wir die Grundlagen der Fenstererstellung mit Python kennenlernen. 

Bevor wir beginnen, lass uns kurz erklären, was ein GUI-Fenster ist. GUI steht für "Graphical User Interface" und bezieht sich auf die visuelle Darstellung von Programmen mit Fenstern, Schaltflächen, Textfeldern und anderen grafischen Elementen. Python bietet verschiedene Bibliotheken zur Erstellung von GUIs, und in diesem Abschnitt werden wir uns auf Tkinter konzentrieren.

In diesem Abschnitt lernst du:

- Wie man ein einfaches GUI-Fenster in Python erstellt
- Wie man die Größe des Fensters anpasst

Mit diesem Wissen kannst du deine eigenen benutzerfreundlichen Anwendungen erstellen und beeindruckende GUIs entwickeln!

## Theorie

In Python verwenden wir die Tkinter-Bibliothek, um ein GUI-Fenster zu erstellen. Hier ist ein allgemeines Code-Beispiel, das den grundlegenden Aufbau zeigt:

```python
import tkinter as tk

fenster = tk.Tk()
fenster.mainloop()
```

Lass uns den Code im Detail erklären:

- Zuerst importieren wir die Tkinter-Bibliothek mit dem Kürzel `tk`.
- Dann erstellen wir eine Instanz des Tkinter-Fensters mit `tk.Tk()`.
- Schließlich rufen wir die `mainloop()`-Methode auf, die das Fenster anzeigt und auf Benutzereingaben wartet.

Jetzt schauen wir uns ein explizites Code-Beispiel an:

```python
import tkinter as tk

fenster = tk.Tk()
fenster.geometry("400x300")
fenster.mainloop()
```

In diesem Beispiel haben wir unserem Fenster einen Titel mit `fenster.title()` gegeben und die Größe des Fensters mit `fenster.geometry()` auf 400 Pixel Breite und 300 Pixel Höhe festgelegt.

## Praxis

Jetzt ist es Zeit, dein Wissen in die Praxis umzusetzen!

### Aufgabe 1

Erstelle ein einfaches GUI-Fenster mit Tkinter. Das Fenster soll 600 Pixel breit und 400 Pixel hoch sein.

Musterlösung:

  ```python
  import tkinter as tk

  fenster = tk.Tk()
  fenster.geometry("600x400")
  fenster.mainloop()
  ```

Gut gemacht! Du hast erfolgreich gelernt, wie man ein GUI-Fenster in Python erstellt und die Größe anpasst.

## Fazit

In diesem Abschnitt haben wir gelernt, wie man mit Python und der Tkinter-Bibliothek ein GUI-Fenster erstellt. Wir haben die theoretischen Grundlagen erklärt und praktische Übungen durchgeführt, um das Gelernte anzuwenden.

Jetzt bist du bereit, mit GUI-Programmierung in Python zu experimentieren und eigene Fenster zu erstellen. Denke daran, dass dies nur der Anfang ist, und es gibt noch viele weitere Möglichkeiten, um dein GUI zu verbessern und interaktive Anwendungen zu entwickeln. Viel Spaß beim Coden und Erstellen deiner eigenen benutzerfreundlichen Programme!