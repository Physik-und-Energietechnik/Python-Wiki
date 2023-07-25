## Einführung
Willkommen zum aufregenden Abenteuer in die wunderbare Welt der Python-Programmierung mit PyQt5! In diesem Tutorial tauchen wir ein in die faszinierende Welt der Popups Dialogfenster. Du wirst lernen, wie man diese praktischen kleinen Fenster erstellt, die es dir ermöglichen, Informationen anzuzeigen, Daten einzugeben und Entscheidungen zu treffen, ohne das Hauptfenster zu verlassen.

Nach diesem Tutorial wirst du in der Lage sein, deine eigenen Popups zu erstellen und sie in deinen PyQt5-Anwendungen einzusetzen. Diese Fähigkeit ist äußerst nützlich, wenn du Benutzernachrichten anzeigen, Bestätigungen einholen oder Daten abfragen möchtest.

## Theorie
### Was sind Popups Dialogfenster?
Popups Dialogfenster sind kleine, temporäre Fenster, die auf dem Hauptfenster deiner Anwendung erscheinen. Sie erlauben es, Informationen anzuzeigen oder Aktionen auszulösen, ohne den Fluss der Hauptanwendung zu unterbrechen. Popups sind wie kurze, aber wichtige Unterhaltungen zwischen deiner Anwendung und dem Benutzer - ein bisschen wie ein Chat mit einem freundlichen Roboter!

### Allgemeines Code-Beispiel
Bevor wir in den Code eintauchen, lass mich dir ein einfaches Beispiel geben, um das Konzept zu verdeutlichen. Stell dir vor, du hast eine Einkaufsliste-Anwendung, und du möchtest ein Popup anzeigen, wenn der Benutzer auf den "Hinzufügen" -Button klickt, um zu bestätigen, dass das Element zur Liste hinzugefügt wurde.

```python
def show_popup():
    popup = QMessageBox()
    popup.setWindowTitle("Erfolg!")
    popup.setText("Das Element wurde zur Einkaufsliste hinzugefügt.")
    popup.exec_()
```
### Explizites Code-Beispiel
Jetzt schauen wir uns das Beispiel spezifisch für PyQt5 an. Stelle sicher, dass du PyQt5 installiert hast, bevor du loslegst.

```python
import sys
from PyQt5.QtWidgets import QApplication, QMainWindow, QPushButton, QMessageBox

def show_popup():
    popup = QMessageBox()
    popup.setWindowTitle("Erfolg!")
    popup.setText("Das Element wurde zur Einkaufsliste hinzugefügt.")
    popup.exec_()

app = QApplication(sys.argv)
main_window = QMainWindow()
main_window.setGeometry(100, 100, 400, 200)

button = QPushButton("Hinzufügen", main_window)
button.setGeometry(150, 80, 100, 30)
button.clicked.connect(show_popup)

main_window.show()
sys.exit(app.exec_())
```
## Praxis
### Aufgabe 1
Erstelle ein kleines Programm, das ein Popup Dialogfenster anzeigt und den Benutzer nach seinem Namen fragt. Zeige dann eine Nachricht mit der Begrüßung "Hallo [Name]!" an.

### Musterlösung:
```python
import sys
from PyQt5.QtWidgets import QApplication, QMessageBox, QLineEdit

app = QApplication(sys.argv)

input_box = QLineEdit()
input_box.setPlaceholderText("Gib deinen Namen ein...")

msg_box = QMessageBox()
msg_box.setText("Wie heißt du?")
msg_box.setStandardButtons(QMessageBox.Ok)
msg_box.setLineEdit(input_box)

result = msg_box.exec_()

if result == QMessageBox.Ok:
    name = input_box.text()
    QMessageBox.information(None, "Begrüßung", f"Hallo {name}!")
```
**Erklärung:**
* Zunächst werden die benötigten Bibliotheken importiert: sys für die Kommandozeilenargumente und **'QApplication, QMessageBox und QLineEdit' **aus PyQt5.QtWidgets für die Erstellung der Anwendung und der Dialogfenster.
*Eine Qt-Anwendung wird erstellt, indem QApplication mit den Kommandozeilenargumenten initialisiert wird.
* Es wird ein Eingabefeld (**'QLineEdit'**) erstellt, das als Platzhaltertext "Gib deinen Namen ein..." hat.
* Ein Popup Dialogfenster (**'QMessageBox'**) wird erstellt und mit dem Text "Wie heißt du?" versehen. Es enthält einen OK-Button als Standard-Button und das zuvor erstellte Eingabefeld.
* Das Popup wird mit msg_box.exec_() angezeigt, und die Ausführung des Programms wird angehalten, bis der Benutzer das Popup schließt.
* Nachdem der Benutzer das Popup geschlossen hat, wird überprüft, ob der Benutzer den OK-Button ausgewählt hat (indem der result-Wert mit **'QMessageBox.Ok'** verglichen wird).
* Wenn der Benutzer OK ausgewählt hat, wird der eingegebene Name aus dem Eingabefeld abgerufen und eine Informationsmeldung angezeigt, die den Benutzer mit "Hallo [Name]!" begrüßt.

### Aufgabe 2
Erstelle ein Programm, das eine kritische Warnung als Popup Dialogfenster anzeigt, wenn der Benutzer versucht, eine bestimmte Aktion auszuführen. Der Benutzer muss dann bestätigen, dass er die Warnung verstanden hat und fortfahren möchte.

### Musterlösung:
```python
import sys
from PyQt5.QtWidgets import QApplication, QMessageBox

app = QApplication(sys.argv)

msg_box = QMessageBox()
msg_box.setIcon(QMessageBox.Warning)
msg_box.setText("Achtung! Diese Aktion kann nicht rückgängig gemacht werden!")
msg_box.setStandardButtons(QMessageBox.Ok | QMessageBox.Cancel)

result = msg_box.exec_()

if result == QMessageBox.Ok:
    print("Aktion wird ausgeführt...")
else:
    print("Aktion abgebrochen.")
```
**Erklärung:**

* Import der benötigten Bibliotheken:

**'sys'**: Dieses Modul wird für den Zugriff auf das Betriebssystem und die Befehlszeilenargumente verwendet.

**'QApplication'**: Eine Klasse aus PyQt5, die eine Qt-Anwendung initialisiert.

* Erstellen einer Anwendung:

**'app** = **QApplication(sys.argv)'**: Hier wird eine Qt-Anwendung initialisiert.
 
**'sys.argv'** sind die Befehlszeilenargumente, die von der Anwendung verwendet werden.

* Erstellen eines Popup-Dialogfensters:

**'msg_box = QMessageBox()**': Hier wird ein Objekt der 'QMessageBox'-Klasse erstellt, das das Popup-Dialogfenster repräsentiert.

**'msg_box.setIcon(QMessageBox.Warning)'**: Setzt das Icon des Dialogfensters auf ein Warnungssymbol.

**'msg_box.setText("Achtung! Diese Aktion kann nicht rückgängig gemacht werden!")**': Setzt den Haupttext der Warnung.

* Festlegen der verfügbaren Buttons:

**'msg_box.setStandardButtons(QMessageBox.Ok | QMessageBox.Cancel)'**: Hier werden die Schaltflächen festgelegt, die im Dialogfenster angezeigt werden sollen. In diesem Fall gibt es "OK" und "Abbrechen".

* Anzeigen des Popup-Dialogfensters und Warten auf Benutzerentscheidung:

**'result** = **msg_box.exec_()'**: Mit dieser Methode wird das Dialogfenster angezeigt, und die Anwendung wartet auf die Entscheidung des Benutzers.

* Auswerten der Benutzerentscheidung:

Wenn der Benutzer die "OK"-Schaltfläche auswählt (**'QMessageBox.Ok'**), wird die Meldung "Aktion wird ausgeführt..." ausgegeben.
Andernfalls wird die Meldung "Aktion abgebrochen." ausgegeben.

### Fazit
Herzlichen Glückwunsch! Ihr habt gelernt, wie man mit PyQt5 Popup Dialogfenster in Python erstellt und verwendet. Ihr könnt nun Benutzern wichtige Informationen anzeigen oder sie nach ihrer Meinung fragen, indem ihr diese nützlichen kleinen Popups nutzt. Macht weiter so und programmiert mit Freude! Happy coding! 😊