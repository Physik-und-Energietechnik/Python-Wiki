## Einführung
Willkommen zu unserem Python-Tutorial über die Anpassung der Titelleiste von GUI-Fenstern mit Hilfe von PyQt5! In diesem Tutorial werden wir lernen, wie wir die Titelleiste eines Fensters personalisieren können, um unseren eigenen Stil und Charakter einzubringen.

Die Titelleiste ist der oberste Bereich eines Fensters, der den Fenstertitel und verschiedene Steuerelemente wie Minimieren, Maximieren und Schließen enthält. Durch die Anpassung der Titelleiste können wir die Benutzererfahrung verbessern und unser Programm individuell gestalten.

In diesem Tutorial werden wir die grundlegenden Konzepte der PyQt5-Bibliothek einführen und zeigen, wie wir die Titelleiste anpassen können, indem wir den Fenstertitel ändern, benutzerdefinierte Symbole hinzufügen und sogar eigene Steuerelemente erstellen.

Theorie
Fenstertitel ändern
Das Ändern des Fenstertitels ist eine einfache Möglichkeit, um unserem Programm eine persönliche Note zu verleihen. Mit PyQt5 können wir dies mithilfe der 'setWindowTitle()'-Methode erreichen. Hier ist ein allgemeines Beispiel:

```python
import sys
from PyQt5.QtWidgets import QApplication, QMainWindow

app = QApplication(sys.argv)
window = QMainWindow()
window.setWindowTitle("Mein tolles Fenster")
window.show()

sys.exit(app.exec_())
````
In diesem Beispiel verwenden wir die setWindowTitle()-Methode, um den Fenstertitel auf "Mein tolles Fenster" zu ändern. Führe den Code aus und schau dir das Ergebnis an!

### Benutzerdefinierte Symbole hinzufügen
Wir können auch benutzerdefinierte Symbole zur Titelleiste hinzufügen, um unsere Anwendung zu personalisieren. Mit PyQt5 können wir dies tun, indem wir das QIcon-Objekt verwenden. Hier ist ein Beispiel:

```python
import sys
from PyQt5.QtGui import QIcon
from PyQt5.QtWidgets import QApplication, QMainWindow

app = QApplication(sys.argv)
window = QMainWindow()
window.setWindowTitle("Fenster mit Symbol")
window.setWindowIcon(QIcon("icon.png"))
window.show()

sys.exit(app.exec_())
```
In diesem Beispiel verwenden wir das 'QIcon'-Objekt, um ein benutzerdefiniertes Symbol aus einer Bilddatei namens "icon.png" zu laden und der Titelleiste hinzuzufügen. Vergiss nicht, die Bilddatei in das gleiche Verzeichnis wie dein Python-Skript zu legen!

## Eigene Steuerelemente erstellen
Mit PyQt5 haben wir die Freiheit, eigene Steuerelemente für die Titelleiste zu erstellen. Dies ermöglicht uns, unsere Anwendung noch weiter anzupassen. Hier ist ein Beispiel für die Erstellung eines benutzerdefinierten Schalters:

```python
import sys
from PyQt5.QtCore import Qt
from PyQt5.QtGui import QIcon
from PyQt5.QtWidgets import QApplication, QMainWindow, QToolButton

app = QApplication(sys.argv)
window = QMainWindow()
window.setWindowTitle("Fenster mit benutzerdefiniertem Schalter")

button = QToolButton(window)
button.setIcon(QIcon("button_icon.png"))
button.setCheckable(True)
button.setChecked(True)
button.setAutoRaise(True)
button.clicked.connect(lambda: print("Schalter wurde geklickt!"))

window.setWindowFlags(Qt.Window | Qt.WindowTitleHint | Qt.CustomizeWindowHint)
window.setCorner(Qt.TopRightCorner, Qt.RightDockWidgetArea)
window.setCorner(Qt.TopLeftCorner, Qt.LeftDockWidgetArea)
window.setCentralWidget(button)
window.show()

sys.exit(app.exec_())
```
In diesem Beispiel erstellen wir einen benutzerdefinierten Schalter mit dem QToolButton-Widget. Wir setzen ein Symbol für den Schalter, machen ihn an- und abwählbar und fügen eine Reaktion auf den Klick hinzu. Führe den Code aus und entdecke deinen neuen benutzerdefinierten Schalter in der Titelleiste!

## Praxis
Lass uns nun unser erlangtes Wissen anwenden! Hier sind zwei Aufgaben für dich:

### Leichte Aufgabe
Ändere den Titel des Fensters in "Hallo Welt" und füge ein eigenes Symbol hinzu. Das Symbol sollte die Datei "my_icon.png" verwenden.

```python
import sys
from PyQt5.QtGui import QIcon
from PyQt5.QtWidgets import QApplication, QMainWindow

app = QApplication(sys.argv)
window = QMainWindow()
# Füge hier deinen Code ein

window.show()
sys.exit(app.exec_())
```
Hier ist eine mögliche Lösung für die leichte Aufgabe:

```python
import sys
from PyQt5.QtGui import QIcon
from PyQt5.QtWidgets import QApplication, QMainWindow

app = QApplication(sys.argv)
window = QMainWindow()
window.setWindowTitle("Hallo Welt")
window.setWindowIcon(QIcon("my_icon.png"))
window.show()
sys.exit(app.exec_())

**Erklärung:**
Der obige Code erstellt ein einfaches PyQt5-Hauptfenster. Die **'setWindowTitle()'**-Methode wird verwendet, um den Fenstertitel festzulegen, und die **'setWindowIcon()'**-Methode wird verwendet, um das Fenster-Icon zu setzen. Stelle sicher, dass die Datei "my_icon.png" im gleichen Verzeichnis wie dein Skript vorhanden ist.

```
### Schwere Aufgabe
Erstelle einen benutzerdefinierten Schalter in der Titelleiste, der den Text "Klick mich!" anzeigt und eine Funktion my_function() aufruft, wenn er geklickt wird.
```python
import sys
from PyQt5.QtCore import Qt
from PyQt5.QtWidgets import QApplication, QMainWindow, QToolButton

app = QApplication(sys.argv)
window = QMainWindow()
# Füge hier deinen Code ein

window.show()
sys.exit(app.exec_())
```
Hier ist eine mögliche Lösung für die schwere Aufgabe:
```python
import sys
from PyQt5.QtCore import Qt
from PyQt5.QtWidgets import QApplication, QMainWindow, QToolButton

def my_function():
    print("Funktion wurde aufgerufen!")

app = QApplication(sys.argv)
window = QMainWindow()

button = QToolButton(window)
button.setText("Klick mich!")
button.clicked.connect(my_function)

window.setWindowFlags(Qt.Window | Qt.WindowTitleHint | Qt.CustomizeWindowHint)
window.setCorner(Qt.TopRightCorner, Qt.RightDockWidgetArea)
window.setCorner(Qt.TopLeftCorner, Qt.LeftDockWidgetArea)
window.setCentralWidget(button)
window.show()

sys.exit(app.exec_())
```
**Erklärung:**
Wir haben eine Funktion 'my_function()' definiert, die beim Klicken des benutzerdefinierten Schalters aufgerufen wird und eine einfache Ausgabe erzeugt. Stelle sicher, dass du den Code ausführst und den Schalter in der Titelleiste testest!

## Fazit
Herzlichen Glückwunsch! Du hast erfolgreich gelernt, wie du die Titelleiste von GUI-Fenstern in Python mit PyQt5 anpassen kannst. Du kennst nun die Grundlagen, um den Fenstertitel zu ändern, benutzerdefinierte Symbole hinzuzufügen und eigene Steuerelemente zu erstellen. Experimentiere weiter und finde heraus, wie du deine Anwendungen noch individueller gestalten kannst. Viel Spaß beim Programmieren und der Gestaltung deiner eigenen einzigartigen Benutzeroberflächen!