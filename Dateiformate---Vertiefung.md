Herzlichen Glückwunsch! Du hast bereits einen soliden Grundstein im Umgang mit JSON, CSV und anderen Dateiformaten gelegt. Wenn du bereit bist, tiefer in die Materie einzutauchen und dein Wissen zu erweitern, dann bist du hier genau richtig. In diesem Abschnitt werden wir uns mit fortgeschrittenen Konzepten und Techniken rund um Dateiformate beschäftigen. Lass uns loslegen!

## 1. Datenmanipulation

Neben dem Lesen und Schreiben von Dateien gibt es viele weitere Möglichkeiten, wie du Dateiformate manipulieren kannst. Hier sind einige fortgeschrittene Techniken, die dir dabei helfen, deine Daten optimal zu verwalten und zu verarbeiten:

- **Filtern von Daten:** Du kannst bestimmte Daten basierend auf Filterkriterien auswählen und extrahieren. Zum Beispiel kannst du nur die Datensätze auswählen, die bestimmte Bedingungen erfüllen.

- **Datenbearbeitung:** Du kannst Daten in Dateiformaten verändern, indem du Werte aktualisierst, hinzufügst oder löschst. Das ermöglicht dir, deine Daten entsprechend deinen Anforderungen anzupassen.

- **Datenaggregation:** Du kannst Daten zusammenfassen und aggregieren, um Informationen auf höherer Ebene zu erhalten. Du kannst zum Beispiel die Summe einer bestimmten Spalte berechnen oder den Durchschnitt von Werten ermitteln.

## 2. Datenvalidierung und Fehlerbehandlung

Die Qualität deiner Daten ist wichtig, daher ist es ratsam, Datenvalidierungstechniken zu verwenden, um sicherzustellen, dass deine Daten korrekt sind. Hier sind einige Methoden, die du anwenden kannst:

- **Datenüberprüfung:** Du kannst sicherstellen, dass die Daten in deinen Dateien bestimmte Kriterien erfüllen, wie z.B. Datentypen, Wertebereiche oder spezifische Formate. Dadurch kannst du Fehler und Inkonsistenzen frühzeitig erkennen.

- **Fehlerbehandlung:** Wenn du auf Fehler während des Verarbeitungsprozesses stößt, ist es wichtig, diese ordnungsgemäß zu behandeln. Du kannst Fehlerprotokolle erstellen, um Informationen über auftretende Fehler zu sammeln und möglicherweise automatisierte Korrekturmaßnahmen durchführen.

## Aufgaben:

1. Filtere die Daten in einer JSON-Datei, um nur die Personen anzuzeigen, die älter als 30 Jahre sind.

2. Aktualisiere eine CSV-Datei, um fehlende Werte mit einem Standardwert zu füllen.

3. Berechne den Durchschnitt der Verkaufspreise in einer JSON-Datei und speichere das Ergebnis in einer neuen Datei.



## Musterlösungen

Aufgabe 1: Extrahieren von Daten aus einer JSON-Datei und Speichern in einer CSV-Datei

```python
import json
import csv

# Daten aus JSON-Datei lesen
with open('data.json', 'r') as file:
    data = json.load(file)

# Daten in CSV-Datei speichern
with open('data.csv', 'w', newline='') as file:
    writer = csv.writer(file)
    writer.writerow(['Name', 'Alter', 'Stadt'])  # Überschriften schreiben
    for item in data:
        writer.writerow([item['name'], item['age'], item['city']])

print("Die Daten wurden erfolgreich in der CSV-Datei gespeichert.")
```

Aufgabe 2: Extrahieren von Daten aus einer CSV-Datei und Speichern in einer JSON-Datei

```python
import csv
import json

# Daten aus CSV-Datei lesen
with open('data.csv', 'r') as file:
    reader = csv.DictReader(file)
    data = [row for row in reader]

# Daten in JSON-Datei speichern
with open('data.json', 'w') as file:
    json.dump(data, file, indent=4)

print("Die Daten wurden erfolgreich in der JSON-Datei gespeichert.")
```



Viel Spaß beim Vertiefen deiner Kenntnisse über Dateiformate und deren Manipulation!