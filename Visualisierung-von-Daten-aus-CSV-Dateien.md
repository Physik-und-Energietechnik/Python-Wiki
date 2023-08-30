## Einführung
In diesem Abschnitt lernst du, wie du Daten aus einer CSV-Datei lesen und sie mithilfe der Matplotlib-Bibliothek in Diagrammen darstellen kannst. 

Visualisierung ist ein mächtiges Werkzeug, um Daten zu verstehen und Muster oder Trends zu erkennen. Mit Matplotlib kannst du Diagramme wie Linien-, Balken- und Streudiagramme erstellen, um deine Daten visuell darzustellen. Dieses Wissen kann in vielen Bereichen nützlich sein, wie z.B. der Analyse von Finanzdaten, dem Verständnis von Klimatrends oder der Visualisierung von Ergebnissen wissenschaftlicher Studien.

Also lasst uns loslegen und die Welt der Datenvisualisierung mit Matplotlib erkunden!

## Theorie

### CSV-Dateien
CSV steht für "Comma Separated Values" und ist ein gängiges Dateiformat zur Speicherung tabellarischer Daten. Eine CSV-Datei besteht aus Zeilen, in denen die Werte durch Kommas getrennt sind. Jede Zeile repräsentiert einen Datensatz, und jede Spalte enthält einen bestimmten Wert oder eine bestimmte Eigenschaft.

Hier ist ein einfaches Beispiel für eine CSV-Datei, die Daten zu verschiedenen Obstsorten enthält:

```python
Obstsorte,Preis,Verfügbarkeit
Apfel,0.5,Ja
Banane,0.3,Ja
Orange,0.4,Nein
```

### Matplotlib
Matplotlib ist eine Python-Bibliothek zur Erstellung von Diagrammen und Visualisierungen. Sie bietet eine Vielzahl von Funktionen und Einstellungen, mit denen du Diagramme anpassen und deine Daten anschaulich präsentieren kannst.

### Code-Beispiel - CSV-Daten einlesen
Um Daten aus einer CSV-Datei in Python einzulesen, können wir die `csv`-Bibliothek verwenden. Hier ist ein allgemeines Beispiel, wie du dies tun kannst:

```python
import csv

with open('deine_datei.csv', 'r') as file:
    csv_reader = csv.reader(file)
    
    for row in csv_reader:
        print(row)
```

Und hier ist ein spezifisches Beispiel, das die Daten aus der vorherigen Obst-CSV-Datei einliest:

```python
import csv

with open('obst.csv', 'r') as file:
    csv_reader = csv.reader(file)
    
    for row in csv_reader:
        obstsorte = row[0]
        preis = float(row[1])
        verfuegbarkeit = row[2]
        
        print(obstsorte, preis, verfuegbarkeit)
```

### Code-Beispiel - Diagramm mit Matplotlib erstellen
Nun, da wir wissen, wie wir Daten aus einer CSV-Datei einlesen können, können wir sie mithilfe von Matplotlib visualisieren. Hier ist ein Beispiel, wie du ein einfaches Balkendiagramm erstellen kannst:

```python
import matplotlib.pyplot as plt

obstsorten = ['Apfel', 'Banane', 'Orange']
preise = [0.5, 0.3, 0.4]

plt.bar(obstsorten, preise)
plt.xlabel('Obstsorte')
plt.ylabel('Preis')
plt.title('Preise von Obstsorten')

plt.show()
```

## Praxis

###  Aufgabe 1
Lass uns mit einer einfachen Aufgabe beginnen. Angenommen, du hast eine CSV-Datei mit dem Namen "temperatur.csv", die die monatlichen Durchschnittstemperaturen eines Jahres enthält. Deine Aufgabe besteht darin, die Temperaturen in einem Linienplot mit Matplotlib zu visualisieren.

Inhalt temperatur.csv:

```csv
Januar,5.3
Februar,6.8
März,10.2
April,15.7
Mai,20.5
Juni,24.3
Juli,26.8
August,25.6
September,21.4
Oktober,15.9
November,10.7
Dezember,6.2
```

Musterlösung:

```python
import csv
import matplotlib.pyplot as plt

monate = []
temperaturen = []

with open('temperaur.csv', 'r') as file:
    csv_reader = csv.reader(file)
    
    for row in csv_reader:
        monat = row[0]
        temperatur = float(row[1])
        
        monate.append(monat)
        temperaturen.append(temperatur)

plt.plot(monate, temperaturen)
plt.xlabel('Monat')
plt.ylabel('Durchschnittstemperatur (°C)')
plt.title('Monatliche Durchschnittstemperaturen')

# Manuelle Anpassung der x-Achsenticks
plt.xticks(rotation=45, ha='right')

plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Fortgeschrittene_Plot_Techniken/Visualisierung_von_Daten_aus_CSV-Dateien/ms_aufgabe1.png)

### Aufgabe 2
Für die schwierigere Aufgabe nehmen wir an, dass wir eine CSV-Datei mit dem Namen "aktien.csv" haben, die die Schlusskurse verschiedener Aktien für jeden Tag enthält. Deine Aufgabe besteht darin, die Schlusskurse von zwei Aktien in einem Streudiagramm mit Matplotlib darzustellen.

Musterlösung:

```python
import csv
import matplotlib.pyplot as plt

aktie1_kurse = []
aktie2_kurse = []

with open('aktien.csv', 'r') as file:
    csv_reader = csv.reader(file)
    
    for row in csv_reader:
        datum = row[0]
        aktie1_kurs = float(row[1])
        aktie2_kurs = float(row[2])
        
        aktie1_kurse.append(aktie1_kurs)
        aktie2_kurse.append(aktie2_kurs)

plt.scatter(aktie1_kurse, aktie2_kurse)
plt.xlabel('Aktie 1 Schlusskurs')
plt.ylabel('Aktie 2 Schlusskurs')
plt.title('Korrelation zwischen Aktie 1 und Aktie 2')

plt.show()
```
![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Fortgeschrittene_Plot_Techniken/Visualisierung_von_Daten_aus_CSV-Dateien/ms_aufgabe2.png)

## Fazit
Das war's! Du hast gerade gelernt, wie du Daten aus CSV-Dateien einliest und sie mit Matplotlib visualisierst. Jetzt kannst du mit dieser neuen Fähigkeit Daten analysieren und präsentieren. Viel Spaß beim Erkunden der Welt der Datenvisualisierung mit Python und Matplotlib!

## Links / Weiteres Material
### Dokumentation
### W3Schools
### YouTube