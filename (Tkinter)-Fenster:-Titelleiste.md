## Einführung
Herzlich willkommen zu unserem Python-Tutorial für unerfahrene Nutzer! In diesem Abschnitt werden wir uns mit der Anpassung der Titelleiste von grafischen Benutzeroberflächen (GUIs) in Python beschäftigen. Du wirst lernen, wie du den Titel eines Fensters ändern und ihm eine persönliche Note verleihen kannst. Dieses Wissen wird dir dabei helfen, ansprechende und individuelle GUIs für deine Python-Anwendungen zu erstellen.

## Theorie
Was ist die Titelleiste?
Bevor wir loslegen, lassen uns kurz klären, was die Titelleiste ist. Die Titelleiste befindet sich oben in einem Fenster und zeigt den Namen oder den Titel der Anwendung an, die gerade ausgeführt wird. In den meisten Fällen enthält sie auch die Schaltflächen zum Minimieren, Maximieren und Schließen des Fensters.


### Code-Beispiel: Anpassung der Titelleiste
Um die Titelleiste anzupassen, können wir die title()-Methode des Fensters verwenden und ihr einen neuen Namen übergeben. Hier ist ein Code-Beispiel, das zeigt, wie du den Titel eines Fensters ändern kannst:

```python
import tkinter as tk

# Fenster erstellen
window = tk.Tk()
window.title("Mein erstes GUI-Fenster")

# Titelleiste anpassen
window.title("Ein individueller Titel")

# Fenster ausführen
window.mainloop()
```
## Praxis
### Aufgabe 1
Ändere den Titel des Fensters in "Hello World GUI" und führe den Code aus. Überprüfe, ob der Titel in der Titelleiste des Fensters angezeigt wird.

### Musterlösung:
```python
import tkinter as tk

# Fenster erstellen
window = tk.Tk()
window.title("Hello World GUI")

# GUI-Code hier einfügen

# Fenster ausführen
window.mainloop()
```

### Aufgabe 2
Jetzt wird es etwas kniffliger! Ändere den Titel des Fensters in deinen eigenen Namen und füge eine persönliche Botschaft hinzu. Führe dann den Code aus und bewundere dein individuell gestaltetes Fenster!

### Musterlösung:
```python
import tkinter as tk

# Fenster erstellen
window = tk.Tk()
window.title("Mein individuelles Fenster")
window.title("Willkommen, [Dein Name]!")

# GUI-Code hier einfügen

# Fenster ausführen
window.mainloop()
```
## Fazit
Herzlichen Glückwunsch! Du hast erfolgreich gelernt, wie du die Titelleiste eines GUI-Fensters in Python anpassen kannst. Du kannst nun deiner Kreativität freien Lauf lassen und individuelle Titel für deine Anwendungen erstellen. Dies ist nur der Anfang deiner spannenden Python-Reise, also bleib dran und lass uns gemeinsam weiterentdecken!
