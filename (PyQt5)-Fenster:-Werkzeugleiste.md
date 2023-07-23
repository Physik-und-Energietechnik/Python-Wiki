## Einführung
Herzlich willkommen zum Python-GUI-Tutorial mit PyQt5! In diesem Tutorial werden wir uns mit dem Erstellen von Fenstern und Werkzeugleisten beschäftigen. Aber hey, bevor du vor Angst in die Tastatur beißt, lass mich dir versichern, dass es einfacher ist, als es klingt!

Hier lernst du, wie du mithilfe von PyQt5 beeindruckende grafische Benutzeroberflächen erstellst, die es dir ermöglichen, interaktive und benutzerfreundliche Anwendungen zu entwickeln. Mit GUIs kannst du coole Fenster, Schaltflächen, Eingabefelder und vieles mehr erstellen, um deine Python-Programme aufzupeppen.

## Theorie
### Was ist eine Werkzeugleiste?
Eine Werkzeugleiste ist wie ein gut sortierter Werkzeugkasten für deine GUI. Stell dir vor, du bist ein Handwerker, der ein fantastisches Möbelstück bauen möchte. Du hast all deine Werkzeuge ordentlich in einer Werkzeugkiste organisiert. Wenn du ein Werkzeug benötigst, greifst du einfach zur Kiste und holst es dir - easy peasy!

In der Welt der GUIs sind Werkzeugleisten nichts anderes als Sammlungen von Schaltflächen, Symbolen und Funktionen, die dem Benutzer bestimmte Aktionen ermöglichen. Denke an Schaltflächen zum Öffnen und Speichern von Dateien, zum Drucken oder zum Ausführen einer speziellen Funktion in deinem Programm.

**Code-Beispiel: Grundgerüst einer Werkzeugleiste:**

```python
import sys
from PyQt5.QtWidgets import QMainWindow, QApplication, QAction, QToolBar

class MyWindow(QMainWindow):
    def __init__(self):
        super().__init__()

        toolbar = QToolBar("Meine Werkzeugleiste")
        self.addToolBar(toolbar)

        action = QAction("Klick mich!", self)
        toolbar.addAction(action)

app = QApplication(sys.argv)
window = MyWindow()
window.show()
sys.exit(app.exec_())
```
**Explizites Code-Beispiel: Werkzeugleiste mit Icons:**

```python
import sys
from PyQt5.QtWidgets import QMainWindow, QApplication, QAction, QToolBar
from PyQt5.QtGui import QIcon

class MyWindow(QMainWindow):
    def __init__(self):
        super().__init__()

        toolbar = QToolBar("Meine Werkzeugleiste")
        self.addToolBar(toolbar)

        action = QAction(QIcon("icon.png"), "Klick mich!", self)
        toolbar.addAction(action)

app = QApplication(sys.argv)
window = MyWindow()
window.show()
sys.exit(app.exec_())
```
## Praxis
### Leichte Aufgabe
Erstellt eine kleine Anwendung mit einer Werkzeugleiste, die einen Button enthält. Der Button soll eine einfache Meldung ausgeben, wenn er geklickt wird. Verwendet das erste Code-Beispiel als Ausgangspunkt.

### Musterlösung:

´´´python
import sys
from PyQt5.QtWidgets import QMainWindow, QApplication, QAction, QToolBar, QMessageBox

class MyWindow(QMainWindow):
    def __init__(self):
        super().__init__()

        toolbar = QToolBar("Meine Werkzeugleiste")
        self.addToolBar(toolbar)

        action = QAction("Klick mich!", self)
        action.triggered.connect(self.show_message)
        toolbar.addAction(action)

    def show_message(self):
        QMessageBox.information(self, "Hallo!", "Ihr habt mich geklickt!")

app = QApplication(sys.argv)
window = MyWindow()
window.show()
sys.exit(app.exec_())
´´´

### Schwere Aufgabe
Erweitert eure Anwendung, indem ihr der Werkzeugleiste einen weiteren Button hinzufügt. Dieser Button soll ein Icon haben und eine neue Funktion auslösen, die euch eine Glückwunschmeldung anzeigt, wenn ihr den Button anklickt. Verwendet das zweite Code-Beispiel als Ausgangspunkt.

### Musterlösung:
```python
import sys
from PyQt5.QtWidgets import QMainWindow, QApplication, QAction, QToolBar, QMessageBox
from PyQt5.QtGui import QIcon

class MyWindow(QMainWindow):
    def __init__(self):
        super().__init__()

        toolbar = QToolBar("Meine Werkzeugleiste")
        self.addToolBar(toolbar)

        action = QAction(QIcon("icon.png"), "Klick mich!", self)
        action.triggered.connect(self.show_message)
        toolbar.addAction(action)

    def show_message(self):
        QMessageBox.information(self, "Glückwunsch!", "Ihr habt den Icon-Button geklickt!")

app = QApplication(sys.argv)
window = MyWindow()
window.show()
sys.exit(app.exec_())
```
## Fazit
Herzlichen Glückwunsch! Ihr habt erfolgreich gelernt, wie man mit PyQt5 eine schicke Werkzeugleiste erstellt. Ihr könnt nun eure eigenen kreativen GUI-Anwendungen mit interaktiven Werkzeugen ausstatten. Die Möglichkeiten sind endlos! Also, auf geht's und lasst eurer Fantasie freien Lauf! Happy Coding! 🚀😄
