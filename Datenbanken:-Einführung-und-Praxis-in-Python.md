# Einführung
Willkommen zum Python-Tutorial über Datenbanken! Hier wirst du lernen, wie du Daten effizient speichern, abrufen und verarbeiten kannst. Datenbanken sind wie das Schrankbett der Programmierwelt - sie bieten Platz für eine Vielzahl von Informationen und lassen sich bei Bedarf blitzschnell wieder hervorzaubern. In diesem Tutorial werden wir die Grundlagen von Datenbanken kennenlernen und uns speziell auf relationale Datenbanken konzentrieren, da sie in Python besonders weit verbreitet sind.
Nach Abschluss dieses Tutorials wirst du in der Lage sein, Datenbanken zu erstellen, sie mit Python zu verbinden und grundlegende Operationen wie das Einfügen, Abrufen und Aktualisieren von Daten durchzuführen. Datenbanken sind überall und werden in den verschiedensten Anwendungen eingesetzt - von Webanwendungen über Datenanalyse bis hin zur Verwaltung von Benutzerinformationen. Mit den erlernten Fähigkeiten bist du bestens gerüstet, um in der Welt der Daten durchzustarten!
# Theorie
## Was sind Datenbanken?
Datenbanken sind wie Wunderkisten für Informationen. Stell dir vor, du hast eine riesige Sammlung von Büchern und möchtest sie ordentlich verwalten. Anstatt die Bücher wild durcheinander auf dem Boden herumliegen zu lassen, kannst du sie in einer Bücherdatenbank organisieren. Eine Datenbank ist im Grunde genommen ein elektronisches Speichersystem, das strukturierte Informationen enthält.
## Datenbankarten
Es gibt verschiedene Arten von Datenbanken, aber wir werden uns auf zwei Haupttypen konzentrieren:
1.	Relationale Datenbanken: Diese Art von Datenbanken basiert auf dem Konzept von Tabellen. Sie sind ideal für den Umgang mit strukturierten Daten geeignet, bei denen die Beziehungen zwischen den verschiedenen Tabellen von Bedeutung sind. Das Verknüpfen und Abfragen von Daten ist in relationalen Datenbanken recht einfach. SQL (Structured Query Language) ist die Sprache, die zur Kommunikation mit relationalen Datenbanken verwendet wird.
Ein Beispiel:
```python
# Python-Code
import sqlite3

# Verbindung zur Datenbank herstellen
conn = sqlite3.connect('meine_datenbank.db')

# SQL-Code ausführen
conn.execute('CREATE TABLE books (id INTEGER PRIMARY KEY, title TEXT, author TEXT)')
sql
•  -- SQL-Code
CREATE TABLE books (
    id INTEGER PRIMARY KEY,
    title TEXT,
    author TEXT
);
```
2.  Nicht-relationale Datenbanken: Diese Art von Datenbanken wird auch als NoSQL-Datenbanken bezeichnet. Im Gegensatz zu relationalen Datenbanken haben sie keine festen Tabellenstrukturen und erlauben eine flexiblere Speicherung von Daten. Sie sind gut geeignet, um unstrukturierte Daten zu verwalten und große Mengen an Daten effizient zu verarbeiten. Beispiele für nicht-relationale Datenbanken sind MongoDB und Cassandra. <br>
Ein Beispiel:
```python
# Python-Code
from pymongo import MongoClient

# Verbindung zur Datenbank herstellen
client = MongoClient('mongodb://localhost:27017/')

# Daten in die Datenbank einfügen
db = client['meine_datenbank']
collection = db['meine_sammlung']
collection.insert_one({'title': 'Python for Beginners', 'author': 'John Smith'})
javascript
2.	// MongoDB-Code
3.	db.meine_sammlung.insertOne({ title: 'Python for Beginners', author: 'John Smith' });
4.	
```
## Relationale vs. nicht-relationale Datenbanken
Der Hauptunterschied zwischen relationalen und nicht-relationale Datenbanken liegt in der Art und Weise, wie sie Daten speichern und abrufen. Relationale Datenbanken sind ideal für strukturierte Daten, bei denen die Beziehungen zwischen den Tabellen wichtig sind. Nicht-relationale Datenbanken eignen sich hingegen besser für unstrukturierte oder stark variierende Daten. <br>
Wenn du also deine Büchersammlung mit klaren Kategorien und einer festen Beziehung zwischen den Büchern organisieren möchtest, ist eine relationale Datenbank die richtige Wahl. Wenn deine Sammlung jedoch eher wie ein wilder Bücherdschungel aussieht und du flexibelere Möglichkeiten zur Speicherung und Skalierung benötigst, solltest du dich für eine nicht-relationale Datenbank entscheiden. <br>
# Praxis
## Aufgabe 1: Einfügen von Daten
Deine Aufgabe besteht darin, eine Tabelle mit dem Namen "employees" in einer relationalen Datenbank zu erstellen und einige Mitarbeiterdaten einzufügen. Verwende die Python-Bibliothek "sqlite3" für diese Aufgabe. <br>

Musterlösung:

```python
import sqlite3

# Verbindung zur Datenbank herstellen
conn = sqlite3.connect('meine_datenbank.db')

# Tabelle erstellen
conn.execute('CREATE TABLE employees (id INTEGER PRIMARY KEY, name TEXT, age INTEGER)')

# Daten einfügen
conn.execute("INSERT INTO employees (name, age) VALUES ('Alice', 28)")
conn.execute("INSERT INTO employees (name, age) VALUES ('Bob', 35)")
conn.execute("INSERT INTO employees (name, age) VALUES ('Charlie', 42)")

# Änderungen speichern
conn.commit()

# Verbindung schließen
conn.close()
```

## Aufgabe 2: Daten abrufen
Jetzt möchtest du die gespeicherten Mitarbeiterdaten abrufen und anzeigen. Schreibe den Python-Code, um alle Datensätze aus der Tabelle "employees" abzurufen. <br>

Musterlösung: 

```python
import sqlite3

# Verbindung zur Datenbank herstellen
conn = sqlite3.connect('meine_datenbank.db')

# Daten abrufen
cursor = conn.execute('SELECT * FROM employees')

# Ergebnisse anzeigen
for row in cursor:
    print(f"ID: {row[0]}, Name: {row[1]}, Alter: {row[2]}")

# Verbindung schließen
conn.close()
```
Herzlichen Glückwunsch! Du hast erfolgreich Grundlagen über Datenbanken in Python gelernt. Mit diesem Wissen kannst du nun Datenbanken erstellen, mit ihnen interagieren und komplexe Anwendungen entwickeln. Datenbanken sind wie magische Schatztruhen für deine Informationen, und du bist jetzt in der Lage, sie zu öffnen und ihren wertvollen Inhalt zu nutzen. Happy coding!