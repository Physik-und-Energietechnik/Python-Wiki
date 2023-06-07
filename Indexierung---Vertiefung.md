# Indexierung - Vertiefung

## Einführung
Willkommen zum vertiefenden Tutorial über Indexierung! In diesem Tutorial erfährst du mehr über die spannende Welt der Datenbankindizes. Du wirst verstehen, wie Indizes funktionieren und warum sie wichtig sind, um die Abfrageleistung deiner Datenbank zu verbessern. Mit diesem Wissen bist du bestens gerüstet, um effiziente Abfragen durchzuführen und deine Datenbank wie ein Profi zu optimieren. Lass uns loslegen!

## Theorie
### Was sind Indizes?
Indizes sind wie ein schnelles Adressbuch für deine Datenbank. Sie ermöglichen es der Datenbank, den Zugriff auf bestimmte Daten effizienter zu gestalten, ähnlich wie du schneller eine Seite in einem Buch findest, wenn du das Inhaltsverzeichnis verwendest. Hier ist ein Beispiel, wie du einen Index erstellst und nutzt:

#### Allgemeines Code-Beispiel:
```python
# Index erstellen
create_index(table_name, column_name)

# Index verwenden
use_index(table_name, column_name, search_value)
```

#### Explizites Code-Beispiel in Python:
```python
# Beispielcode für Index erstellen und verwenden
def create_index(table_name, column_name):
    # Code zum Erstellen des Index
    print("Index für Tabelle", table_name, "und Spalte", column_name, "erstellt.")

def use_index(table_name, column_name, search_value):
    # Code zum Verwenden des Index
    print("Suche nach Wert", search_value, "in Tabelle", table_name, "mit Hilfe des Index auf Spalte", column_name)
```

### Arten von Indizes
Es gibt verschiedene Arten von Indizes, die du in deiner Datenbank verwenden kannst, je nachdem welche Art von Abfragen du durchführst. Hier sind einige gängige Arten von Indizes:

- B-Tree-Index: Dies ist der Standardindex und eignet sich gut für gleichmäßig verteilte Daten.
- Hash-Index: Dieser Index ist ideal für Gleichheitsabfragen, bei denen der genaue Wert gesucht wird.
- Bitmap-Index: Dieser Index wird verwendet, um binäre Informationen zu indizieren, wie zum Beispiel True/False-Angaben.

### Indexierung in Python
In Python kannst du die Indexierungsfunktionen deiner Datenbank nutzen, um Indizes zu erstellen und zu verwenden. Hier ist ein Beispiel, wie du die Indexierung in Python durchführen kannst:

```python
# Index erstellen
create_index("my_table", "my_column")

# Index verwenden
use_index("my_table", "my_column", "search_value")
```

## Praxis
### Aufgabe (Leicht)
Erstelle einen B-Tree-Index für die Spalte "Nachname" in der Tabelle "Kunden". Führe dann eine Suche nach dem Nachnamen "Müller" mit Hilfe des Indexes durch.

#### Musterlösung:
```python
# B-Tree-Index für "Nachname" in "Kunden" erstellen
create_index("Kunden", "Nachname")

# Suche nach "Müller" mit Hilfe des Indexes
use_index("Kunden", "Nachname", "Müller")
```

### Aufgabe (Schwer)
Erstelle einen Hash-Index für die Spalte "Postleitzahl" in der Tabelle "Adressen". Führe dann eine