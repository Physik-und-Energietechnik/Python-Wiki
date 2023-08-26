# Matplotlib - streamplot

## Einführung
Willkommen zum aufregenden Teil der Matplotlib-Bibliothek: streamplot! In diesem Tutorial werden wir uns mit streamplot vertraut machen und lernen, wie man mit diesem tollen Feature Strömungsfelder in Python visualisiert. Aber keine Sorge, wir werden uns nicht mit echten Flüssigkeiten herumschlagen müssen. Stattdessen werden wir uns auf eine einfache und lustige Weise mit den Konzepten vertraut machen.

Streamplot ist ein mächtiges Werkzeug, das es uns ermöglicht, Vektorfelder grafisch darzustellen. Das hört sich kompliziert an, aber keine Sorge, ich werde es erklären. Du wirst lernen, wie man Strömungsmuster wie die Bewegung von Flüssigkeiten oder Gasen visuell darstellen kann. Klingt doch cool, oder?

Nach diesem Tutorial wirst du in der Lage sein, streamplot zu verwenden, um deine eigenen Strömungsmuster zu erstellen. Du könntest damit zum Beispiel die Bewegung von Luftströmungen, die Fahrtroute von Fischen oder sogar die Windverhältnisse in der Nähe deines Lieblingscafés darstellen. Die Möglichkeiten sind endlos, und wer weiß, vielleicht findest du in deinen Daten ja sogar das nächste große Geheimnis der Strömungsmechanik!

## Theorie
Lass uns nun etwas Theorie besprechen, bevor wir in die Praxis übergehen. Beim Visualisieren von Strömungen geht es darum, die Geschwindigkeit und Richtung der Strömung an verschiedenen Punkten in einem bestimmten Bereich zu verstehen. Um dies zu tun, verwenden wir Vektorfelder. Diese bestehen aus Vektoren, die Länge und Richtung repräsentieren.

In der Theorie wird streamplot wie folgt verwendet:
```python
import matplotlib.pyplot as plt

# Erstelle x- und y-Koordinaten
x = [1, 2, 3, 4, 5]
y = [1, 2, 3, 4, 5]

# Erstelle u- und v-Komponenten der Vektoren
u = [1, 0, -1, 0, 1]
v = [0, 1, 0, -1, 0]

# Erstelle das Strömungsfeld
plt.streamplot(x, y, u, v)

# Zeige das Diagramm an
plt.show()
```

In diesem Beispiel haben wir ein einfaches Gitter von Koordinaten erstellt. Dann haben wir die u- und v-Komponenten der Vektoren definiert, die die Strömung repräsentieren. Schließlich haben wir `plt.streamplot` verwendet, um das Strömungsfeld zu erstellen, und `plt.show`, um das Diagramm anzuzeigen.

Jetzt ist es an der Zeit, das Ganze in Aktion zu sehen! Hier ist ein Code-Beispiel speziell für dich, um den Dreh rauszubekommen:
```python
import matplotlib.pyplot as plt
import numpy as np

# Erstelle x- und y-Koordinaten
x = np.linspace(-2, 2, 100)
y = np.linspace(-2, 2, 100)

# Erstelle u- und v-Komponenten der Vektoren
X, Y = np.meshgrid(x, y)
u = -Y
v = X

# Erstelle das Strömungsfeld
plt.streamplot(X, Y, u, v)

# Zeige das Diagramm an
plt.show()
```

In diesem Beispiel haben wir eine Funktion definiert, die ein Wirbelfeld erzeugt. Die `np.meshgrid`-Funktion wird verwendet, um ein Gitter von Koordinaten zu erstellen. Dann haben wir die u- und v-Komponenten der Vektoren definiert, um das Wirbelfeld zu erzeugen. Schließlich haben wir `plt.streamplot` verwendet, um das Strömungsfeld zu erstellen, und `plt.show`, um das Diagramm anzuzeigen.

## Praxis

**Aufgabe 1**
Genug Theorie, lass uns mit der Praxis beginnen! Hier ist eine leichte Aufgabe für dich: Erstelle ein Strömungsfeld, das das Fließen eines Flusses darstellt. Verwende die folgenden Koordinaten und Vektoren:

```python
import matplotlib.pyplot as plt

# Erstelle x- und y-Koordinaten
x = [1, 2, 3, 4, 5]
y = [1, 2, 3, 4, 5]

# Erstelle u- und v-Komponenten der Vektoren
u = [1, 0, -1, 0, 1]
v = [0, 1, 0, -1, 0]

# Erstelle das Strömungsfeld
plt.streamplot(x, y, u, v)

# Zeige das Diagramm an
plt.show()
```

Probier es aus und schau dir das erzeugte Strömungsfeld an. Beachte, wie die Vektoren die Richtung und Geschwindigkeit des Flusses anzeigen.


**Aufgabe 2**
Für diejenigen, die eine größere Herausforderung suchen, hier ist eine schwierigere Aufgabe: Erstelle ein Strömungsfeld, das die Bewegung eines Tornados darstellt. Verwende den folgenden Code:

```python
import matplotlib.pyplot as plt
import numpy as np

# Erstelle x- und y-Koordinaten
x = np.linspace(-2, 2, 100)
y = np.linspace(-2, 2, 100)

# Erstelle u- und v-Komponenten der Vektoren
X, Y = np.meshgrid(x, y)
u = -Y
v = X

# Erstelle das Strömungsfeld
plt.streamplot(X, Y, u, v)

# Zeige das Diagramm an
plt.show()
```
![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Plottypen/Array_Fields/streamplot/ms_aufgabe2.png)

Versuche, das Strömungsfeld des Tornados zu interpretieren. Beachte die Drehbewegung und wie die Vektoren die Strömung anzeigen.

## Fazit
Super! Du hast es geschafft, streamplot zu meistern und bist nun in der Lage, Strömungsfelder in Python zu visualisieren. Das war nur ein kleiner Vorgeschmack auf die Möglichkeiten, die Matplotlib bietet. Also schnapp dir deine Daten und finde heraus, was noch alles mit streamplot möglich ist!

## Links / Weiteres Material
### Dokumentation
https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.streamplot.html