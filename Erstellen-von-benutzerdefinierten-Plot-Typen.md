## Matplotlib - Erstellen von benutzerdefinierten Plot Typen

### Einführung

Herzlich willkommen zum Python-Tutorial über das Erstellen von benutzerdefinierten Plot-Typen mit Matplotlib! In diesem Abschnitt werden wir lernen, wie wir über die Standardplots hinausgehen können, um unsere eigenen einzigartigen Diagramme zu erstellen. 

Neben den bereits vorhandenen Plot-Typen bietet Matplotlib auch die Möglichkeit, eigene benutzerdefinierte Plot-Typen zu erstellen, die unseren spezifischen Anforderungen entsprechen.

### Theorie

Bevor wir uns in die Praxis stürzen, lassen Sie uns einige grundlegende theoretische Konzepte verstehen. 

#### 1. Die `plot`-Funktion

Die `plot`-Funktion ist eine der wichtigsten Funktionen in Matplotlib. Sie ermöglicht uns das Erstellen von Linien- und Punktplots. Schauen wir uns ein einfaches Beispiel an:

```python
import matplotlib.pyplot as plt

# Daten für die x- und y-Koordinaten
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

# Plot erstellen
plt.plot(x, y)

# Plot anzeigen
plt.show()
```

In diesem Beispiel erstellen wir einen einfachen Linienplot. Die `plot`-Funktion nimmt die x- und y-Koordinaten als Argumente entgegen und zeichnet eine Linie durch die angegebenen Punkte. Anschließend verwenden wir `plt.show()`, um den Plot anzuzeigen.

#### 2. Benutzerdefinierte Plot-Typen

Matplotlib ermöglicht es uns, eigene benutzerdefinierte Plot-Typen zu erstellen, indem wir die vorhandenen Plot-Typen erweitern. Dies kann besonders nützlich sein, wenn wir spezielle Anforderungen haben oder neue Visualisierungen entwerfen möchten.

Hier ist ein einfaches Beispiel, wie wir einen "Hupenplot" erstellen können:

```python
import matplotlib.pyplot as plt

class HupenPlot(plt.plot):
    def __init__(self, *args, **kwargs):
        super().__init__(*args, **kwargs)
        self.horn_sound = "Honk! Honk!"

    def honk(self):
        print(self.horn_sound)

# Daten für die x- und y-Koordinaten
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

# HupenPlot erstellen
hp = HupenPlot(x, y)

# Hupen!
hp.honk()
```

In diesem Beispiel erstellen wir eine Klasse namens `HupenPlot`, die von `plt.plot` erbt. Wir fügen der Klasse eine Methode namens `honk` hinzu, die einen lustigen Hupen-Sound ausgibt. Durch das Erstellen einer benutzerdefinierten Klasse können wir unsere eigenen Methoden und Eigenschaften hinzufügen und so den Plot-Typ anpassen.

### Praxis

Jetzt ist es Zeit, unser erlangtes Wissen in die Praxis umzusetzen!

#### Aufgabe 1

Erstellen Sie einen benutzerdefinierten Plot-Typ namens "WackelPlot", der die gegebenen x- und y-Koordinaten durch eine wackelnde Linie verbindet. Die Wackelbewegung soll einen humorvollen Effekt erzeugen. Führen Sie dann den Plot aus.

Hier ist eine Musterlösung:

```python
import matplotlib.pyplot as plt

class WackelPlot(plt.plot):
    def __init__(self, *args, **kwargs):
        super().__init__(*args, **kwargs)
        self.wiggle_factor = 0.2

    def plot(self):
        x, y = self.get_data()
        y = [yi + self.wiggle_factor * i for i, yi in enumerate(y)]
        super().plot(x, y)

# Daten für die x- und y-Koordinaten
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

# WackelPlot erstellen
wp = WackelPlot(x, y)

# Wackeln!
wp.plot()

# Plot anzeigen
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Fortgeschrittene_Plot_Techniken/Erstellen_von_benutzerdefinierten_Plot-Typen/ms_aufgabe1.png)

#### Aufgabe 2

Erstellen Sie einen benutzerdefinierten Plot-Typ namens "Farbenexplosion", der die gegebenen x- und y-Koordinaten als Punkte darstellt. Jeder Punkt soll eine zufällige Farbe haben, um eine spannende und farbenfrohe Visualisierung zu erzeugen. Führen Sie dann den Plot aus.

Hier ist eine Musterlösung:

```python
import matplotlib.pyplot as plt
import random

class Farbenexplosion(plt.plot):
    def __init__(self, *args, **kwargs):
        super().__init__(*args, **kwargs)

    def plot(self):
        x, y = self.get_data()
        colors = [self.get_random_color() for _ in range(len(x))]
        super().plot(x, y, marker='o', color=colors)

    @staticmethod
    def get_random_color():
        r = random.random()
        g = random.random()
        b = random.random()
        return (r, g, b)

# Daten für die x- und y-Koordinaten
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

# Farbenexplosion erstellen
fe = Farbenexplosion(x, y)

# Farbenexplosion!
fe.plot()

# Plot anzeigen
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Fortgeschrittene_Plot_Techniken/Erstellen_von_benutzerdefinierten_Plot-Typen/ms_aufgabe2.png)

Herzlichen Glückwunsch! Sie haben erfolgreich eigene benutzerdefinierte Plot-Typen erstellt und Ihre Daten auf kreative und unterhaltsame Weise visualisiert.

Ich hoffe, dieses Tutorial hat Ihnen geholfen, Matplotlib besser zu verstehen und Ihre Python-Fähigkeiten zu erweitern. Viel Spaß beim Erstellen Ihrer eigenen einzigartigen Plots!