## Einführung
In diesem Tutorial werden wir lernen, wie wir die Achsen eines Diagramms in Matplotlib anpassen können.

Nach Abschluss dieses Tutorials wirst du in der Lage sein:
- Die Achsenbeschriftungen anzupassen, um sie besser lesbar zu machen.
- Die Skalierung der Achsen anzupassen, um die Daten optimal darzustellen.
- Achsenlimits festzulegen, um den Fokus auf bestimmte Bereiche der Daten zu legen.

Lasst uns direkt loslegen und in die faszinierende Welt der angepassten Achsen eintauchen!

## Theorie

### Achsenbeschriftungen
Die Achsenbeschriftungen sind entscheidend, um unsere Diagramme verständlich zu machen. Sie geben uns Informationen darüber, was auf den Achsen dargestellt wird. Matplotlib bietet uns die Möglichkeit, die Achsenbeschriftungen anzupassen, indem wir ihnen benutzerdefinierte Bezeichnungen geben.

Hier ist ein allgemeines Beispiel dafür, wie wir Achsenbeschriftungen in Matplotlib anpassen können:

```python
import matplotlib.pyplot as plt

# Beispieldaten
x = [1, 2, 3, 4, 5]
y = [10, 20, 30, 40, 50]

# Diagramm erstellen
plt.plot(x, y)

# Achsenbeschriftungen anpassen
plt.xlabel('Zeit')
plt.ylabel('Wert')

# Diagramm anzeigen
plt.show()
```

In diesem Beispiel haben wir die Achsenbeschriftungen für die x-Achse auf "Zeit" und für die y-Achse auf "Wert" festgelegt. Du kannst diese Beschriftungen natürlich an deine spezifischen Daten anpassen.

### Skalierung der Achsen
Manchmal sind unsere Daten auf einer Achse stark unterschiedlich skaliert, was es schwierig machen kann, sie in einem Diagramm angemessen darzustellen. Matplotlib bietet uns die Möglichkeit, die Skalierung der Achsen anzupassen, um die Daten besser sichtbar zu machen.

Hier ist ein Beispiel dafür, wie wir die Skalierung der Achsen in Matplotlib anpassen können:

```python
import matplotlib.pyplot as plt

# Beispieldaten
x = [1, 2, 3, 4, 5]
y = [1000, 2000, 3000, 4000, 5000]

# Diagramm erstellen
plt.plot(x, y)

# Skalierung der y-Achse anpassen
plt.yscale('log')

# Diagramm anzeigen
plt.show()
```

In diesem Beispiel haben wir die Skalierung der y-Achse auf eine logarithmische Skala geändert, indem wir `plt.yscale('log')` verwendet haben. Dadurch werden große Zahlen auf der y-Achse komprimiert und besser sichtbar gemacht.

### Achsenlimits festlegen
Manchmal möchten wir den Fokus auf einen bestimmten Bereich unserer Daten legen und den Rest ausblenden. Matplotlib ermöglicht es uns, die Achsenlimits festzulegen, um nur den gewünschten Bereich anzuzeigen.

Hier ist ein Beispiel dafür, wie wir die Achsenlimits in Matplotlib festlegen können:

```python
import matplotlib.pyplot as plt

# Beispieldaten
x = [1, 2, 3, 4, 5]
y = [10, 20, 30, 40, 50]

# Diagramm erstellen
plt.plot(x, y)

# Achsenlimits festlegen
plt.xlim(2, 4)
plt.ylim(20, 40)

# Diagramm anzeigen
plt.show()
```

In diesem Beispiel haben wir die Achsenlimits für die x-Achse auf den Bereich von 2 bis 4 und für die y-Achse auf den Bereich von 20 bis 40 festgelegt. Dadurch wird nur dieser Bereich in unserem Diagramm angezeigt, während der Rest ausgeblendet wird.

## Praxis

### Aufgabe 1
Versuche, die Achsenbeschriftungen in folgendem Diagramm anzupassen:

```python
import matplotlib.pyplot as plt

# Beispieldaten
x = [1, 2, 3, 4, 5]
y = [10, 20, 30, 40, 50]

# Diagramm erstellen
plt.plot(x, y)

# TODO: Achsenbeschriftungen anpassen

# Diagramm anzeigen
plt.show()
```

Musterlösung:

```python
import matplotlib.pyplot as plt

# Beispieldaten
x = [1, 2, 3, 4, 5]
y = [10, 20, 30, 40, 50]

# Diagramm erstellen
plt.plot(x, y)

# Achsenbeschriftungen anpassen
plt.xlabel('X-Achse')
plt.ylabel('Y-Achse')

# Diagramm anzeigen
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Grundlagen_des_Plottings/Anpassen_von_Achsen/ms_aufgabe1.png)

### Aufgabe 2
Versuche, die Skalierung der y-Achse in folgendem Diagramm anzupassen:

```python
import matplotlib.pyplot as plt

# Beispieldaten
x = [1, 2, 3, 4, 5]
y = [1000, 2000, 3000, 4000, 5000]

# Diagramm erstellen
plt.plot(x, y)

# TODO: Skalierung der y-Achse anpassen

# Diagramm anzeigen
plt.show()
```

Musterlösung:

```python
import matplotlib.pyplot as plt

# Beispieldaten
x = [1, 2, 3, 4, 5]
y = [1000, 2000, 3000, 4000, 5000]

# Diagramm erstellen
plt.plot(x, y)

# Skalierung der y-Achse anpassen
plt.yscale('log')

# Diagramm anzeigen
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Grundlagen_des_Plottings/Anpassen_von_Achsen/ms_aufgabe2.png)


## Fazit
Viel Spaß beim Anpassen von Achsen in Matplotlib! Lass deiner Kreativität freien Lauf und erstelle beeindruckende Diagramme.