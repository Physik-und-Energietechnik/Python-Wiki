Herzlichen Glückwunsch, du hast den Grundstein der Datenbanken gelegt! Wenn du bereit bist, noch tiefer in die faszinierende Welt der Datenbanken einzutauchen, dann bist du hier genau richtig. In diesem Abschnitt werden wir uns mit fortgeschritteneren Konzepten und Techniken befassen, um deine Datenbank-Skills auf das nächste Level zu bringen. Bereit für das Datenbanken-Abenteuer? Lass uns starten!

##  Indizes

Indizes sind wie das Inhaltsverzeichnis eines Buches. Sie helfen der Datenbank dabei, Informationen schneller zu finden. Wenn du eine Tabelle hast, die auf bestimmte Spalten häufig abgefragt wird, kannst du Indizes erstellen, um die Abfragegeschwindigkeit zu verbessern. Das ist wie ein Turbo-Boost für deine Datenbank!

Hier ist ein Beispiel, wie du einen Index in einer Tabelle erstellen kannst:

```python
import sqlite3

conn = sqlite3.connect('meine_datenbank.db')
cursor = conn.cursor()

# Index erstellen
cursor.execute("CREATE INDEX index_name ON meine_tabelle (spalte)")

# Verbindung schließen
conn.close()
```

## Transaktionen

Transaktionen sind wie der Sicherheitsgurt deiner Datenbank. Sie helfen dabei, Datenänderungen atomar und konsistent durchzuführen. Mit Transaktionen kannst du sicherstellen, dass alle Änderungen entweder vollständig ausgeführt werden oder gar nicht. Wenn etwas schief geht, wird die Transaktion rückgängig gemacht, als wäre nichts passiert. Das ist wie Magie!

Hier ist ein Beispiel für die Verwendung von Transaktionen:

```python
import sqlite3

conn = sqlite3.connect('meine_datenbank.db')
cursor = conn.cursor()

# Transaktion starten
conn.begin()

try:
    # Daten ändern
    cursor.execute("UPDATE meine_tabelle SET spalte = 'neuer_wert' WHERE bedingung")

    # Weitere Änderungen...

    # Transaktion bestätigen
    conn.commit()

except:
    # Bei einem Fehler die Transaktion abbrechen
    conn.rollback()

# Verbindung schließen
conn.close()
```

##  Join-Abfragen

Joins sind wie das Verbinden von Puzzleteilen in deiner Datenbank. Mit Joins kannst du Daten aus mehreren Tabellen zusammenführen und komplexe Abfragen durchführen. Du kannst Verknüpfungen zwischen Tabellen herstellen und Daten aus beiden Tabellen in einer Abfrage anzeigen. Das ist wie ein Tanz der Daten!

Hier ist ein Beispiel für eine Join-Abfrage:

```python
import sqlite3

conn = sqlite3.connect('meine_datenbank.db')
cursor = conn.cursor()

# Join-Abfrage ausführen
cursor.execute("SELECT tabelle1.spalte1, tabelle2.spalte2 FROM tabelle1 JOIN tabelle2 ON tabelle1.id = tabelle2.id")

# Ergebnis abrufen
ergebnis = cursor.fetchall()

# Ergebnis anzeigen
for datensatz in ergebnis:
    print(datensatz)

# Verbindung schließen
conn.close()
```

## Aufgaben:

1. Erstelle einen Index für eine bestimmte Spalte in deiner Tabelle und vergleiche die Geschwindigkeit der Abfragen vor und nach der Erstellung des Indexes.

2. Führe eine Transaktion durch, um mehrere Datenänderungen atomar auszuführen. Stelle sicher, dass alle Änderungen entweder vollständig übernommen oder abgebrochen werden, wenn ein Fehler auftritt.

3. Führe eine Join-Abfrage durch, um Daten aus zwei Tabellen zusammenzuführen und die Ergebnisse anzuzeigen.

Viel Spaß beim Vertiefen deiner Datenbankkenntnisse!


## Musterlösungen

Aufgabe 1: Speichern von Daten aus einer JSON-Datei in einer SQLite-Datenbank

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

Aufgabe 2: Abrufen von Daten aus der Datenbank und Speichern in einer CSV-Datei

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

Aufgabe 3: Aktualisieren von Daten in der Datenbank basierend auf Änderungen in einer JSON-Datei

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

