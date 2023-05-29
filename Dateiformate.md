# Einführung

Willkommen zum Python-Tutorial über Dateiformate! In diesem Tutorial lernst du, wie Python mit verschiedenen Dateiformaten umgehen kann. Dateiformate sind wie magische Schachteln, die Daten speichern und transportieren können. Indem du Python benutzt, kannst du diese Schachteln öffnen, den Inhalt lesen und sogar deinen eigenen Inhalt darin erstellen! 

In diesem Tutorial wirst du Folgendes lernen:

    Was Dateiformate sind und warum sie wichtig sind
    Wie du mit den gängigsten Dateiformaten wie CSV und JSON umgehst
    Wie du Daten aus Dateien liest und in Python nutzt
    Wie du Daten in Dateien schreibst und sie bearbeitest

Das Wissen über Dateiformate ist in vielen Bereichen nützlich, sei es beim Verarbeiten von Tabellendaten, beim Austausch von Informationen mit anderen Systemen oder beim Speichern von strukturierten Daten. Also lass uns in die wundervolle Welt der Dateiformate eintauchen!
# Theorie
## CSV (Comma-Separated Values)

CSV steht für "Comma-Separated Values" (kommagetrennte Werte). Es ist ein einfaches Dateiformat, das Tabellendaten speichert. Jeder Wert in einer CSV-Datei ist durch ein Komma getrennt. CSV-Dateien sind großartig, um Daten in Tabellenform zu speichern und zu transportieren.

Ein allgemeines Code-Beispiel:

```python

import csv

# CSV-Datei öffnen
with open('daten.csv', 'r') as file:
    reader = csv.reader(file)

    # Daten lesen und anzeigen
    for row in reader:
        print(row)
```

Ein explizites Code-Beispiel in Python:

```python

import csv

# CSV-Datei öffnen
with open('daten.csv', 'r') as file:
    reader = csv.DictReader(file)

    # Daten lesen und anzeigen
    for row in reader:
        print("Name:", row['Name'])
        print("Alter:", row['Alter'])
```

## JSON (JavaScript Object Notation)

JSON steht für "JavaScript Object Notation". Es ist ein flexibles Dateiformat, das strukturierte Daten speichert. JSON basiert auf der Syntax von JavaScript-Objekten und wird häufig verwendet, um Daten zwischen verschiedenen Systemen auszutauschen.

Ein allgemeines Code-Beispiel:

```python

import json

# JSON-Datei öffnen
with open('daten.json', 'r') as file:
    data = json.load(file)

    # Daten anzeigen
    print(data)
```
Ein explizites Code-Beispiel in Python:

```python

import json

# JSON-Datei öffnen
with open('daten.json', 'r') as file:
    data = json.load(file)

    # Daten anzeigen
    print("Name:", data['name'])
    print("Alter:", data['alter'])
```

Praxis
Aufgabe 1: Daten aus einer CSV-Datei lesen

Deine Aufgabe besteht darin, Daten aus einer CSV-Datei zu lesen und sie auf der Konsole auszugeben.

Musterlösung:

```python

import csv

# CSV-Datei öffnen
with open('daten.csv', 'r') as file:
    reader = csv.reader(file)

    # Daten lesen und anzeigen
    for row in reader:
        print(row)
```

Aufgabe 2: Daten in eine JSON-Datei schreiben

Jetzt möchtest du Daten in eine JSON-Datei schreiben. Schreibe den Python-Code, um Daten in die Datei zu speichern.

Musterlösung:

```python

import json

# Daten vorbereiten
data = {
    'name': 'Alice',
    'alter': 25
}

# JSON-Datei öffnen und Daten schreiben
with open('daten.json', 'w') as file:
    json.dump(data, file)
```

Herzlichen Glückwunsch! Du hast erfolgreich gelernt, wie du mit Dateiformaten wie CSV und JSON in Python umgehst. Du kannst Daten aus Dateien lesen, sie anzeigen und sogar neue Daten in Dateien speichern. Das ist wie Zauberei für Daten! Mach weiter so und erkunde die spannende Welt der Dateiformate mit Python!