## Einführung

In diesem Abschnitt werden wir uns mit einem weiteren spannenden Aspekt von Matplotlib beschäftigen - dem errorbar Plot. Klingt beeindruckend, oder? Aber keine Sorge, wir werden diesen Begriff Schritt für Schritt erkunden und dabei hoffentlich jede Menge Spaß haben!

Der errorbar Plot ist eine großartige Möglichkeit, um Fehlerbalken zu visualisieren, die uns Informationen über die Genauigkeit oder Unsicherheit von Daten geben. Mit Matplotlib können wir diese Fehlerbalken ganz einfach in unsere Plots einbauen und somit unsere Daten noch aussagekräftiger machen.

In diesem Tutorial werden wir lernen, wie man den errorbar Plot in Matplotlib erstellt, was er uns über unsere Daten verrät und wie wir damit beeindruckende visuelle Darstellungen erstellen können. Egal, ob du Wissenschaftler, Datenanalyst oder einfach nur ein Python-Enthusiast bist, dieses Wissen wird dir helfen, deine Daten mit Stil zu präsentieren!

## Theorie

Bevor wir in die Praxis übergehen, werfen wir einen Blick auf die Theorie hinter dem errorbar Plot. Hier lernen wir die Konzepte kennen und sehen, wie sie in Code umgesetzt werden können.

Der errorbar Plot besteht im Wesentlichen aus drei Komponenten: den x- und y-Koordinaten für unsere Datenpunkte und den Fehlerbalken, die die Unsicherheit dieser Punkte anzeigen. Die Fehlerbalken können auf verschiedene Arten definiert werden, zum Beispiel als Standardabweichung, Konfidenzintervall oder benutzerdefinierte Werte.

Um das Ganze besser zu verstehen, werfen wir einen Blick auf ein allgemeines Beispiel. Angenommen, du hast eine Studie durchgeführt, um den Einfluss von Koffein auf die Produktivität zu untersuchen. Du hast die Durchschnittswerte der Produktivität für verschiedene Koffeindosen und möchtest nun den errorbar Plot erstellen, um die Unsicherheit der Daten zu zeigen.

Hier ist ein allgemeines Code-Beispiel, das die Struktur eines errorbar Plots zeigt:

```python
import matplotlib.pyplot as plt

# x-Koordinaten (Koffeindosen)
x = [1, 2, 3, 4, 5]

# y-Koordinaten (Produktivität)
y = [10, 15, 12, 14, 11]

# Fehlerbalken (Unsicherheit der Daten)
error = [1, 2, 1.5, 1, 1.2]

plt.errorbar(x, y, yerr=error, fmt='o')

plt.xlabel('Koffeindosis')
plt.ylabel('Produktivität')
plt.title('Einfluss von Koffein auf die Produktivität')

plt.show()
```

In diesem Beispiel haben wir eine Liste `x`, die die Koffeindosen repräsentiert, eine Liste `y`, die die Produktivitätswerte enthält, und eine Liste `error`, die die Unsicherheit dieser Werte angibt. Die `errorbar`-Funktion erzeugt dann den Plot mit den Fehlerbalken, die unsere Datenpunkte umgeben.

Lass uns nun das Ganze mit einem konkreten Beispiel in Python sehen. Angenommen, du hast eine Umfrage durchgeführt und die folgenden Daten über die Beliebtheit von Eiscreme-Sorten gesammelt:

| Eiscreme-Sorte | Beliebtheit | Fehler |
| -------------- | ----------- | ------ |
| Schokolade     | 75          | 5      |
| Erdbeere       | 60          | 8      |
| Vanille        | 80          | 7      |
| Pistazie       | 70          | 4      |
| Zitrone        | 65          | 6      |

Hier ist der entsprechende Code, um den errorbar Plot für diese Daten zu erstellen:

```python
import matplotlib.pyplot as plt

# Eiscreme-Sorten
eissorten = ['Schokolade', 'Erdbeere', 'Vanille', 'Pistazie', 'Zitrone']

# Beliebtheit der Eiscreme
beliebtheit = [75, 60, 80, 70, 65]

# Fehler der Beliebtheit
fehler = [5, 8, 7, 4, 6]

plt.errorbar(eissorten, beliebtheit, yerr=fehler, fmt='o')

plt.xlabel('Eiscreme-Sorte')
plt.ylabel('Beliebtheit')
plt.title('Beliebtheit von Eiscreme-Sorten')

plt.show()
```

## Praxis

Nun ist es Zeit für etwas Praxis! Lass uns unser erlangtes Wissen über den errorbar Plot auf die Probe stellen. Wir werden zwei Aufgaben angehen - eine leichte und eine schwierigere.

### Aufgabe 1

Stelle die Temperaturwerte eines Tagesverlaufs dar und verwende dabei den errorbar Plot, um die Unsicherheit der Messungen anzuzeigen.

Hier ist eine Musterlösung für diese Aufgabe:

```python
import matplotlib.pyplot as plt

# Zeitpunkte der Messungen
zeitpunkte = [1, 2, 3, 4, 5, 6, 7]

# Temperaturwerte
temperatur = [25, 24, 26, 23, 25, 27, 28]

# Unsicherheit der Temperaturmessungen
unsicherheit = [1, 2, 1.5, 1, 1.2, 0.5, 1]

plt.errorbar(zeitpunkte, temperatur, yerr=unsicherheit, fmt='o')

plt.xlabel('Zeit')
plt.ylabel('Temperatur')
plt.title('Tagesverlauf der Temperatur')

plt.show()
```
![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Plottypen/Array_Fields/errorbar/ms_aufgabe1.png)

### Aufgabe 2
Du hast Daten über die monatlichen Einnahmen eines Geschäfts gesammelt und möchtest den errorbar Plot verwenden, um sowohl die durchschnittlichen Einnahmen als auch die Schwankungen von Monat zu Monat zu visualisieren.

Hier ist eine Musterlösung für diese Aufgabe:

```python
import matplotlib.pyplot as plt

# Monate
monate = ['Jan', 'Feb', 'März', 'Apr', 'Mai']

# Durchschnittliche monatliche Einnahmen
einnahmen = [10000, 12000, 11000, 13000, 11500]

# Schwankungen der monatlichen Einnahmen
schwankungen = [800, 1000, 900, 1200, 950]

plt.errorbar(monate, einnahmen, yerr=schwankungen, fmt='o')

plt.xlabel('Monat')
plt.ylabel('Einnahmen')
plt.title('Monatliche Einnahmen')

plt.show()
```
![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Plottypen/Array_Fields/errorbar/ms_aufgabe2.png)

## Fazit
Herzlichen Glückwunsch! Du hast den errorbar Plot gemeistert und kannst jetzt beeindruckende visuelle Darstellungen mit Matplotlib erstellen. Nutze dieses mächtige Werkzeug, um Daten zu präsentieren und Einblicke zu gewinnen.

## Links / Weiteres Material
### Dokumentation
https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.errorbar.html