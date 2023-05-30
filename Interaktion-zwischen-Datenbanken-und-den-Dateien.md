Herzlichen Glückwunsch! Du hast bereits gelernt, wie man Daten aus JSON- und CSV-Dateien liest und schreibt. Jetzt ist es an der Zeit, diese Daten in einer Datenbank zu speichern, mit ihnen zu arbeiten und sie wieder in JSON- oder CSV-Dateien zu exportieren. In diesem Abschnitt werden wir uns damit beschäftigen, wie du Daten zwischen Datenbanken und JSON-Dateien hin- und herbewegen kannst. Los geht's!

## 1. Daten in einer Datenbank speichern

Um Daten aus einer JSON- oder CSV-Datei in einer Datenbank zu speichern, musst du zuerst eine Verbindung zur Datenbank herstellen. Hier sind die grundlegenden Schritte, die du befolgen musst:

1. Importiere das entsprechende Datenbankmodul in Python.

2. Stelle eine Verbindung zur Datenbank her, indem du die Verbindungsparameter wie den Host, den Benutzernamen, das Passwort usw. bereitstellst.

3. Erstelle eine Tabelle in der Datenbank, um die Daten zu speichern. Definiere die Spalten entsprechend den Datenattributen.

4. Lese die Daten aus der JSON- oder CSV-Datei und füge sie in die Datenbank ein. Verwende SQL-Abfragen, um die Daten in die richtigen Tabellenspalten einzufügen.

5. Schließe die Verbindung zur Datenbank, sobald du mit dem Speichern der Daten fertig bist.

## 2. Daten aus einer Datenbank abrufen

Um Daten aus einer Datenbank abzurufen und in JSON- oder CSV-Dateien zu exportieren, musst du die folgenden Schritte befolgen:

1. Stelle eine Verbindung zur Datenbank her, ähnlich wie beim Speichern der Daten.

2. Führe eine SQL-Abfrage aus, um die gewünschten Daten aus der Datenbank abzurufen.

3. Verarbeite die abgerufenen Daten und formatiere sie entsprechend dem gewünschten Dateiformat (JSON oder CSV).

4. Speichere die formatierten Daten in einer Datei.

5. Schließe die Verbindung zur Datenbank.

## Aufgaben:

1. Speichere die Daten aus einer JSON-Datei in einer SQLite-Datenbank und gib die Bestätigung aus, dass die Daten erfolgreich gespeichert wurden.

2. Rufe die Daten aus der Datenbank ab und speichere sie in einer CSV-Datei.

3. Aktualisiere die Daten in der Datenbank basierend auf den Änderungen in einer JSON-Datei.

Lösungen:

1. Beispiel für das Speichern von Daten aus einer JSON-Datei in einer SQLite-Datenbank:

```python
import sqlite3
import json

# Verbindung zur Datenbank herstellen
conn = sqlite3.connect('mydatabase.db')

# Tabelle erstellen
conn.execute('''CREATE TABLE IF NOT EXISTS employees
                 (id INT PRIMARY KEY NOT NULL,
                 name TEXT NOT NULL,
                 age INT NOT NULL);''')

# Daten aus JSON-Datei lesen
with open('data.json', 'r') as file:
    data = json.load(file)

# Daten in die Datenbank einfügen
for item in data:
    conn.execute("INSERT INTO employees (id, name, age) VALUES (?, ?, ?)",
                 (item['id'], item['name'], item['age']))

# Änderungen speichern und Verbindung schließen


conn.commit()
conn.close()

print("Die Daten wurden erfolgreich in der Datenbank gespeichert.")
```

2. Beispiel für das Abrufen von Daten aus der Datenbank und Speichern in einer CSV-Datei:

```python
import sqlite3
import csv

# Verbindung zur Datenbank herstellen
conn = sqlite3.connect('mydatabase.db')

# SQL-Abfrage ausführen
cursor = conn.execute("SELECT * FROM employees")

# Daten in CSV-Datei exportieren
with open('data.csv', 'w', newline='') as file:
    writer = csv.writer(file)
    writer.writerow([i[0] for i in cursor.description])  # Überschriften schreiben
    writer.writerows(cursor)

# Verbindung schließen
conn.close()

print("Die Daten wurden erfolgreich in der CSV-Datei gespeichert.")
```

3. Beispiel für das Aktualisieren von Daten in der Datenbank basierend auf Änderungen in einer JSON-Datei:

```python
import sqlite3
import json

# Verbindung zur Datenbank herstellen
conn = sqlite3.connect('mydatabase.db')

# Daten aus JSON-Datei lesen
with open('changes.json', 'r') as file:
    changes = json.load(file)

# Daten in der Datenbank aktualisieren
for change in changes:
    conn.execute("UPDATE employees SET age = ? WHERE id = ?",
                 (change['new_age'], change['id']))

# Änderungen speichern und Verbindung schließen
conn.commit()
conn.close()

print("Die Daten in der Datenbank wurden erfolgreich aktualisiert.")
```

Viel Erfolg beim Arbeiten mit Datenbanken und dem Austausch von Daten zwischen JSON- oder CSV-Dateien und Datenbanken!