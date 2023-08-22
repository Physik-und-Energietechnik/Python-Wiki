## Einführung
In diesem Abschnitt unseres Python-Tutorials werden wir uns mit einem interessanten Aspekt von Matplotlib befassen - dem step Plot.

Der step Plot ist ein nützliches Werkzeug in der Datenvisualisierung, das uns hilft, diskrete Datenpunkte zu visualisieren, als wären sie durch Schritte miteinander verbunden. Es ist wie das Hüpfen von Punkt zu Punkt, um die Daten zu präsentieren. Klingt spaßig, oder?

In diesem Tutorial wirst du lernen, wie du den step Plot in Matplotlib erstellst und wie du ihn in deinen eigenen Projekten einsetzen kannst. Sei gespannt!

## Theorie

Bevor wir in die Praxis gehen, lass uns die Theorie hinter dem step Plot verstehen. Stell dir vor, du hast eine Reihe von diskreten Datenpunkten, zum Beispiel die Anzahl der Kekse, die du pro Tag isst. Du könntest diese Daten als Diagramm darstellen, indem du jeden Datenpunkt mit dem nächsten verbindest. Und das ist der springende Punkt (im wahrsten Sinne des Wortes) des step Plots!

### Allgemeines Code-Beispiel
```python
import matplotlib.pyplot as plt

x = [0, 1, 2, 3, 4]  # x-Koordinaten
y = [1, 3, 2, 4, 2]  # y-Koordinaten

plt.step(x, y)
plt.show()
```

### Explizites Code-Beispiel in Python
```python
import matplotlib.pyplot as plt

# Diskrete Datenpunkte definieren
days = ["Montag", "Dienstag", "Mittwoch", "Donnerstag", "Freitag"]
cookies_eaten = [2, 5, 1, 4, 3]

plt.step(days, cookies_eaten, linestyle=":", marker="o", color="purple")

# Achsentitel und Diagrammtitel hinzufügen
plt.xlabel("Tage der Woche")
plt.ylabel("Verzehrte Kekse")
plt.title("Mein Kekskonsum pro Tag")

plt.show()
```

## Praxis

Jetzt ist es Zeit, das Gelernte in die Praxis umzusetzen. Mach dir keine Sorgen, es wird nicht zu knifflig! Ich habe zwei Aufgaben für dich vorbereitet - eine leichtere und eine schwerere. Viel Spaß dabei!

### Aufgabe 1
Erstelle ein step Plot-Diagramm für die folgenden Datenpunkte:

```python
x = [1, 2, 3, 4, 5, 6]
y = [2, 4, 2, 5, 3, 6]
```

Musterlösung:
```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5, 6]
y = [2, 4, 2, 5, 3, 6]

plt.step(x, y)
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Plottypen/Basic/step/ms_aufgabe1.png)

### Aufgabe 2
Stell dir vor, du verfolgst die Anzahl der Seiten, die du in verschiedenen Büchern pro Tag gelesen hast. Erstelle ein step Plot-Diagramm, um diese Datenpunkte darzustellen:

```python
books = ["Harry Potter", "Der Herr der Ringe", "1984", "Der kleine Prinz", "Moby Dick"]
pages_read = [10, 15, 5, 8, 12]
```

Musterlösung:
```python
import matplotlib.pyplot as plt

books = ["Harry Potter", "Der Herr der Ringe", "1984", "Der kleine Prinz", "Moby Dick"]
pages_read = [10, 15, 5, 8, 12]

plt.step(books, pages_read, linestyle="--", marker="o", color="green")

plt.xlabel("Buchtitel")
plt.ylabel("Gelesene Seiten")
plt.title("Mein Lesefortschritt")

plt.show()
```
![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Plottypen/Basic/step/ms_aufgabe2.png)

## Fazit
Jetzt bist du in der Lage, deine Datenpunkte mit Stil zu visualisieren und andere mit deinen schicken Diagrammen zu beeindrucken. Denke daran, dass der step Plot ein hilfreiches Werkzeug ist, um diskrete Datenpunkte auf eine interessante Art und Weise darzustellen. Viel Spaß beim Experimentieren und viel Erfolg in deinen zukünftigen Python-Projekten!

## Links / Weiteres Material
### Dokumentation
https://matplotlib.org/stable/plot_types/basic/step.html
### W3Schools
### YouTube