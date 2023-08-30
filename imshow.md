## Einführung

In diesem Abschnitt tauchen wir tief in die Magie von `imshow()` ein. Klingt nach einem Geheimcode aus einem Agentenfilm, oder? Aber mach dir keine Sorgen, wir werden diesen Code knacken und verstehen, wie man damit Daten in anschauliche Bilder verwandelt.

In diesem Tutorial werden wir lernen, wie man mit `imshow()` umgeht. Das ist wie Photoshop für Zahlen, nur viel cooler. Wir werden Daten in Bildern visualisieren und herausfinden, wie wir das in verschiedenen Situationen anwenden können. Am Ende kannst du deine Freunde mit fantastischen visuellen Darstellungen beeindrucken!

In diesem Abschnitt wirst du lernen:
- Wie man den `imshow` Plot in Matplotlib verwendet, um Daten zu visualisieren.
- Wie man Farbkarten anpasst und Farblegenden hinzufügt.
- Wie man Bilder anzeigen und manipulieren kann.

Mit diesem Wissen bist du in der Lage, beeindruckende Visualisierungen zu erstellen und Daten auf eine unterhaltsame Art und Weise zu erkunden. Du kannst deine Forschungsergebnisse, deine Datenanalyse oder sogar deinen nächsten Vortrag aufpeppen. Also lass uns loslegen!

## Theorie

### Was zur Hölle ist `imshow()`?
Stell dir vor, du könntest Zahlen in Farben verwandeln und dadurch Muster und Strukturen sichtbar machen. Das ist im Grunde das, was `imshow()` tut. Es erlaubt uns, Matrizen von Zahlen als Bilder darzustellen. Und das Beste daran? Du musst kein Künstler sein, um das hinzubekommen.

### Code-Beispiel: Grundlegendes
Hier ist ein einfaches Beispiel, um dir den Geschmack von `imshow()` zu geben:

```python
import matplotlib.pyplot as plt
import numpy as np

data = np.random.random((10, 10))  # Erstelle eine zufällige 10x10 Matrix

plt.imshow(data, cmap='viridis')  # Zeige die Daten als Bild an
plt.colorbar()  # Zeige eine Farbskala zur Referenz an
plt.show()  # Zeige das Bild an
```

### Explizites Code-Beispiel: Anpassungen
Du kannst das Bild anpassen, um es episch aussehen zu lassen:

```python
plt.imshow(data, cmap='plasma', interpolation='bilinear')
plt.title("Episches Bild")
plt.xlabel("X-Achse")
plt.ylabel("Y-Achse")
plt.xticks([])  # Entferne x-Achsenbeschriftungen
plt.yticks([])  # Entferne y-Achsenbeschriftungen
plt.colorbar(label="Wertigkeit")
plt.show()
```

## Praxis

### Aufgabe 1
Zeige deine Macht, indem du eine Matrix mit aufsteigenden Werten von 0 bis 24 erstellst und sie als Bild anzeigst. Lass die Farben von cool nach warm verlaufen.

**Musterlösung:**

```python
data_light = np.arange(25).reshape(5, 5)
plt.imshow(data_light, cmap='coolwarm')
plt.colorbar()
plt.show()
```
![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Plottypen/Array_Fields/imshow/ms_aufgabe1.png)

### Aufgabe 2
Hier wird's kniffliger! Erstelle eine Matrix mit zufälligen Ganzzahlen zwischen 0 und 100 (5x5). Zeige sie als Bild an, aber lass nur die Werte über 50 in kräftigem Rot erscheinen.

**Musterlösung:**

```python
data_hard = np.random.randint(0, 101, (5, 5))
masked_data = np.ma.masked_less_equal(data_hard, 50)  # Maske Werte <= 50
plt.imshow(masked_data, cmap='Reds')
plt.colorbar()
plt.show()
```
![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Plottypen/Array_Fields/imshow/ms_aufgabe2.png)


## Fazit
Herzlichen Glückwunsch, du hast gerade die Kunst der Datenvisualisierung mit `imshow()` gemeistert! Du bist jetzt offiziell ein Picasso der Programmierung.

## Links / Weiteres Material
### Dokumentation
https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.imshow.html