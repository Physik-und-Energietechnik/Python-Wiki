## Einführung

Willkommen zum Python-Tutorial über Abfragen! Hier wirst du lernen, wie du mit Python Datenbanken durchsuchen und nach bestimmten Kriterien filtern kannst. Stell dir vor, du hast eine riesige Datenbank voller Informationen, aber du suchst nach einer bestimmten Nadel im Heuhaufen. Python ist wie dein talentierter Detektiv, der dir hilft, die gesuchten Daten zu finden!

In diesem Tutorial wirst du Folgendes lernen:
- Wie du mit Python eine Verbindung zu einer Datenbank herstellst
- Wie du Abfragen formulierst, um bestimmte Daten aus der Datenbank abzurufen
- Wie du Kriterien und Bedingungen festlegst, um gezielt nach Daten zu suchen
- Wie du die Ergebnisse deiner Abfragen weiterverarbeitest und darstellst

Die Fähigkeit, Datenbanken zu durchsuchen und Abfragen zu erstellen, ist äußerst nützlich, insbesondere wenn du mit großen Datenmengen arbeitest. Ob du nach Kundeninformationen in einer Kundendatenbank oder nach Produktdetails in einem E-Commerce-System suchst, Python steht bereit, um dir bei deinen Ermittlungen zu helfen!

## Theorie

### Verbindung zur Datenbank herstellen

Bevor du mit Abfragen beginnen kannst, musst du eine Verbindung zu deiner Datenbank herstellen. Python bietet verschiedene Module und Treiber, um mit verschiedenen Datenbanken zu kommunizieren. Du musst das entsprechende Modul installieren und importieren, um loszulegen.

*Ein allgemeines Code-Beispiel für eine Verbindung zu einer SQLite-Datenbank:*
```python
import sqlite3

# Verbindung zur Datenbank herstellen
conn = sqlite3.connect('datenbank.db')
```

### Abfragen formulieren

Nachdem du die Verbindung hergestellt hast, kannst du Abfragen formulieren, um bestimmte Daten aus der Datenbank abzurufen. Du kannst SQL (Structured Query Language) verwenden, um deine Abfragen zu erstellen. SQL ist wie die Geheimsprache der Datenbanken, die Python verstehen kann.

*Ein allgemeines Code-Beispiel für eine einfache Abfrage:*
```python
# Abfrage formulieren
query = "SELECT * FROM tabelle"

# Abfrage ausführen und Ergebnisse erhalten
cursor = conn.execute(query)
results = cursor.fetchall()

# Gefundene Ergebnisse anzeigen
for row in results:
    print(row)
```

### Kriterien und Bedingungen festlegen

Um gezielt nach Daten zu suchen, kannst du Kriterien und Bedingungen in deine Abfragen integrieren. Du kannst Filter festlegen, um nur die Daten abzurufen, die bestimmten Kriterien entsprechen. Das ist wie das Einstellen eines Sichtfilters für deine Datenbank!

*Ein allgemeines Code-Beispiel für eine Abfrage mit Kriterien:*
```python
# Abfrage mit Kriterien formulieren
query = "SELECT * FROM tabelle WHERE bedingung"

# Abfrage ausführen und Ergebnisse erhalten
cursor = conn.execute(query)
results = cursor.fetchall()

# Gefundene Ergebnisse anzeigen
for row in results:
    print(row)
```

## Praxis

### Aufgabe 1: Daten aus der Datenbank abrufen
Gegeben ist eine Datenbank mit Informationen über verschiedene Bü

cher. Deine Aufgabe besteht darin, alle Bücher aus der Datenbank abzurufen und auf der Konsole auszugeben.

*Musterlösung:*
```python
# Abfrage formulieren
query = "SELECT * FROM books"

# Abfrage ausführen und Ergebnisse erhalten
cursor = conn.execute(query)
results = cursor.fetchall()

# Gefundene Bücher anzeigen
for row in results:
    print("Titel:", row['title'])
    print("Autor:", row['author'])
    print("ISBN:", row['isbn'])
    print()
```

### Aufgabe 2: Datenbank nach bestimmten Kriterien durchsuchen
Gegeben ist eine Datenbank mit Informationen über verschiedene Produkte. Deine Aufgabe besteht darin, nach Produkten zu suchen, die einen bestimmten Preis überschreiten, und die gefundenen Produkte auf der Konsole auszugeben.

*Musterlösung:*
```python
# Preisgrenze festlegen
min_price = 50

# Abfrage mit Kriterien formulieren
query = "SELECT * FROM products WHERE price > " + str(min_price)

# Abfrage ausführen und Ergebnisse erhalten
cursor = conn.execute(query)
results = cursor.fetchall()

# Gefundene Produkte anzeigen
for row in results:
    print("Produkt:", row['product'])
    print("Preis:", row['price'])
    print()
```

### Aufgabe 3: Multiple-Choice-Frage
Welche SQL-Anweisung wird verwendet, um eine Abfrage in Python auszuführen?

A) `SELECT`
B) `UPDATE`
C) `DELETE`
D) `INSERT`

*Musterlösung: A) `SELECT`