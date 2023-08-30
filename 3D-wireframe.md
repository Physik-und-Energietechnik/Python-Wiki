## Einführung

In diesem Abschnitt werden wir uns mit einem faszinierenden Feature von Matplotlib auseinandersetzen: dem 3D Wireframe. Aber was genau ist ein 3D Wireframe? Nun, lasst uns eine aufregende Reise in die dreidimensionale Welt der Datenvisualisierung antreten!

Mit dem 3D Wireframe können wir Daten in einer spannenden neuen Dimension darstellen. Stellt euch vor, ihr könntet eure Daten in einem magischen Raum betrachten, in dem sie sich nicht nur nach links und rechts bewegen, sondern auch nach oben und unten schweben können. Klingt cool, oder? Matplotlib macht das möglich!

In diesem Tutorial werdet ihr lernen, wie ihr eure eigenen 3D Wireframes erstellen könnt. Wir werden die Theorie hinter den Wireframes erkunden und dann gemeinsam einige Code-Beispiele betrachten, sowohl allgemeine als auch spezifische für Python. Am Ende werdet ihr mit einem breiten Lächeln im Gesicht in der Lage sein, beeindruckende 3D Wireframes zu erstellen und eure Daten auf eine völlig neue Art und Weise zu visualisieren.

## Theorie

Bevor wir uns in den Code stürzen, lasst uns kurz über die Theorie hinter den 3D Wireframes sprechen. Stellt euch vor, ihr habt eine Menge von Datenpunkten, die in einem dreidimensionalen Koordinatensystem verteilt sind. Ein 3D Wireframe verbindet diese Punkte mit Linien und bildet so eine dreidimensionale Struktur. Es ist wie das Gerüst eines Gebäudes, das eure Daten zusammenhält.

Um euch das besser vorstellen zu können, werfen wir einen Blick auf ein allgemeines Code-Beispiel:

```python
import matplotlib.pyplot as plt
import numpy as np

# Daten generieren
x = np.linspace(-5, 5, 50)
y = np.linspace(-5, 5, 50)
X, Y = np.meshgrid(x, y)
Z = np.sin(np.sqrt(X**2 + Y**2))

# 3D Wireframe erstellen
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.plot_wireframe(X, Y, Z)

# Achsenbeschriftungen hinzufügen
ax.set_xlabel('X-Achse')
ax.set_ylabel('Y-Achse')
ax.set_zlabel('Z-Achse')

# Titel setzen
ax.set_title('Ein fantastischer 3D Wireframe')

# Anzeigen
plt.show()
```

In diesem Beispiel erzeugen wir zunächst eine Menge von x- und y-Werten mithilfe von `np.linspace`. Dann verwenden wir `np.meshgrid`, um Gitterpunkte zu generieren, die wir für die Berechnung unserer z-Koordinaten verwenden. In diesem Fall verwenden wir die Funktion `np.sin` für einige schöne, wellenförmige Daten.

Als nächstes erstellen wir eine `figure` und eine `axis` mit `projection='3d'`, um unsere 3D-Umgebung vorzubereiten. Mit `ax.plot_wireframe` zeichnen wir schließlich unseren 3D Wireframe.

Um das Ganze noch ansprechender zu machen, fügen wir Achsenbeschriftungen und einen Titel hinzu. Und voilà! Wir haben unseren eigenen beeindruckenden 3D Wireframe erstellt.

## Praxis

Nun ist es an der Zeit, euer frisch erlerntes Wissen in die Praxis umzusetzen. Wir werden euch zwei Aufgaben geben, eine leichte und eine etwas herausforderndere. Aber keine Sorge, ihr habt das drauf!

### Aufgabe 1

Erstellt einen 3D Wireframe einer Kugel. Verwendet dazu die folgenden Code-Vorlagen:

```python
import matplotlib.pyplot as plt
import numpy as np

# Daten generieren
# ...

# 3D Wireframe erstellen
# ...

# Achsenbeschriftungen hinzufügen
# ...

# Titel setzen
# ...

# Anzeigen
plt.show()
```

Musterlösung:

```python
import matplotlib.pyplot as plt
import numpy as np

# Daten generieren
u = np.linspace(0, 2 * np.pi, 100)
v = np.linspace(0, np.pi, 100)
x = 10 * np.outer(np.cos(u), np.sin(v))
y = 10 * np.outer(np.sin(u), np.sin(v))
z = 10 * np.outer(np.ones(np.size(u)), np.cos(v))

# 3D Wireframe erstellen
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.plot_wireframe(x, y, z)

# Achsenbeschriftungen hinzufügen
ax.set_xlabel('X-Achse')
ax.set_ylabel('Y-Achse')
ax.set_zlabel('Z-Achse')

# Titel setzen
ax.set_title('Eine kugelrunde Kugel')

# Anzeigen
plt.show()
```

### Aufgabe 2
Erstellt einen 3D Wireframe einer schwingenden Funktion, wie beispielsweise einer Sinuswelle oder einer Exponentialfunktion.

Musterlösung:

```python
import matplotlib.pyplot as plt
import numpy as np

# Daten generieren
x = np.linspace(-5, 5, 100)
y = np.linspace(-5, 5, 100)
X, Y = np.meshgrid(x, y)
Z = np.sin(np.sqrt(X**2 + Y**2))

# 3D Wireframe erstellen
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.plot_wireframe(X, Y, Z)

# Achsenbeschriftungen hinzufügen
ax.set_xlabel('X-Achse')
ax.set_ylabel('Y-Achse')
ax.set_zlabel('Z-Achse')

# Titel setzen
ax.set_title('Eine wunderschöne schwingende Funktion')

# Anzeigen
plt.show()
```
## Fazit
Herzlichen Glückwunsch, ihr habt es geschafft! Ihr könnt nun eure eigenen beeindruckenden 3D Wireframes erstellen. Feiert euren Erfolg und bewundert eure Daten in ihrer ganzen räumlichen Pracht!

Das war's für diesen Abschnitt. Macht euch bereit für neue Abenteuer und spannende Möglichkeiten, eure Daten zu visualisieren.
## Links / Weiteres Material
### W3Schools
### YouTube