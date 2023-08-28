## Einführung

In diesem Abschnitt unseres Tutorials werden wir uns mit einem spannenden Thema befassen: dem hist Plot in Matplotlib. 

Der hist Plot, oder wie ich ihn gerne nenne, der "Histinator", ist ein mächtiges Werkzeug in der Datenvisualisierung. Mit ihm kannst du deine Daten in Form von Histogrammen darstellen. Moment mal, Histogramm? Klingt wie ein gruseliger Kuchen, oder? Aber nein, das hat nichts mit Gebäck zu tun. Ein Histogramm ist einfach eine Art, Daten in verschiedene Gruppen einzuteilen und zu zeigen, wie viele Elemente in jede Gruppe fallen. Ganz ähnlich wie eine Ladung Gummibären, die in verschiedenen Farben in einer Schüssel verteilt sind.

Warum ist das wichtig? Nun, Histogramme helfen uns dabei, Datenmuster und Verteilungen zu verstehen. Sie ermöglichen es uns, die Häufigkeit von Werten in einem Datensatz zu visualisieren und wichtige Informationen daraus abzuleiten. Wenn du jemals vor einem Haufen Zahlen gesessen hast und dachtest: "Mann, ich wünschte, ich könnte das besser verstehen", dann ist der Histinator dein neuer bester Freund!

In diesem Tutorial werden wir lernen, wie man den Histinator benutzt, um Daten zu visualisieren und interessante Erkenntnisse zu gewinnen. Also schnall dich an und lass uns loslegen!

## Theorie

#### Die Grundlagen

Bevor wir in den Code eintauchen, lass uns die grundlegenden Konzepte hinter dem hist Plot verstehen. Ein Histogramm besteht aus Säulen, die verschiedene Bereiche der Daten repräsentieren. Jede Säule zeigt die Anzahl der Datenpunkte an, die in diesem Bereich liegen. Es ist wie eine Art Zählmaschine für Daten!

Um ein Histogramm zu erstellen, müssen wir zuerst unsere Daten in sogenannte "Bins" aufteilen. Ein Bin ist ein Bereich, in dem die Daten gruppiert werden. Zum Beispiel könnten wir Bins für verschiedene Altersgruppen festlegen, wenn wir Daten über Menschen haben. Der Histinator wird dann die Daten zählen, die in jeden Bin fallen, und die Höhe der Säule entsprechend anpassen.

#### Code-Beispiel: Einfaches Histogramm

Um das Ganze besser zu verstehen, werfen wir einen Blick auf ein einfaches Code-Beispiel. Angenommen, wir haben eine Liste von Noten, die wir in einem Kurs erhalten haben:

```python
noten = [85, 92, 78, 89, 95, 88, 76, 82, 90, 93, 87, 84, 79, 91]
```

Nun wollen wir diese Noten in einem Histogramm darstellen. Hier ist der Code, um das zu erreichen:

```python
import matplotlib.pyplot as plt

plt.hist(noten)

plt.xlabel('Noten')
plt.ylabel('Anzahl der Schüler')
plt.title('Verteilung der Noten')

plt.show()
```

Schau dir das an! Mit nur wenigen Zeilen Code haben wir ein schickes Histogramm unserer Noten erstellt. Die X-Achse zeigt die Noten an, während die Y-Achse die Anzahl der Schüler angibt, die diese Note erhalten haben. Das ist doch ziemlich cool, oder?

#### Code-Beispiel: Angepasstes Histogramm

Aber warte, es gibt noch mehr! Der Histinator bietet uns viele Möglichkeiten, unsere Histogramme anzupassen. Zum Beispiel können wir die Anzahl der Bins ändern, um die Genauigkeit unserer Darstellung zu beeinflussen. Schau dir dieses Beispiel an:

```python
plt.hist(noten, bins=5)  # Nur 5 Bins diesmal

plt.xlabel('Noten')
plt.ylabel('Anzahl der Schüler')
plt.title('Verteilung der Noten')

plt.show()
```

Hier haben wir die Anzahl der Bins auf 5 reduziert. Dadurch werden die Daten in weniger Gruppen aufgeteilt, und die Säulen werden breiter. Es ist wie die Verwendung von größeren Schüsseln für die Gummibären – jede Schüssel enthält mehr, aber wir haben weniger Schüsseln insgesamt.

Du kannst auch die Farbe der Säulen ändern, Beschriftungen hinzufügen und noch viele andere Anpassungen vornehmen. Die Möglichkeiten sind nahezu endlos!

## Praxis

Jetzt bist du dran, deine neu gewonnenen Fähigkeiten unter Beweis zu stellen! Hier sind zwei Aufgaben für dich:

### Aufgabe 1
Gegeben ist eine Liste von Temperaturen an verschiedenen Tagen: `[24, 26, 22, 28, 27, 25, 23]`. Erstelle ein Histogramm, um die Verteilung der Temperaturen darzustellen.

Musterlösung:

```python
temperaturen = [24, 26, 22, 28, 27, 25, 23]

plt.hist(temperaturen)

plt.xlabel('Temperaturen')
plt.ylabel('Anzahl der Tage')
plt.title('Verteilung der Temperaturen')

plt.show()
```
![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Plottypen/Statistiken/hist/ms_aufgabe1.png)

### Aufgabe 2
Du hast Zugriff auf eine Datei mit den Gehältern von 1000 Mitarbeitern eines Unternehmens. Lade die Gehaltsdaten aus der Datei und erstelle ein Histogramm, um die Gehaltsverteilung zu visualisieren.

Musterlösung:

```python
import pandas as pd

gehaelter = pd.read_csv('gehaelter.csv')['Gehalt']

plt.hist(gehaelter, bins=20)

plt.xlabel('Gehalt')
plt.ylabel('Anzahl der Mitarbeiter')
plt.title('Gehaltsverteilung')

plt.show()
```
![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Plottypen/Statistiken/hist/ms_aufgabe2.png)

## Fazit
Du hast es geschafft! Du hast den Histinator gemeistert und kannst nun Daten wie ein echter Python-Profi visualisieren. Feiere deinen Erfolg mit einem Gummibärenfest – du hast es verdient!

Das war's für den Abschnitt über den hist Plot. Wir hoffen, du hattest Spaß beim Lernen und bist jetzt bereit, deine Daten in beeindruckenden Histogrammen zum Leben zu erwecken. Bis zum nächsten Mal!

## Links / Weiteres Material
### Dokumentation
https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.hist.html