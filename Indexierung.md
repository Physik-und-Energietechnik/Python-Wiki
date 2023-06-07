# Indexierung

## Einführung
Willkommen zum Tutorial über Indexierung in Python! In diesem Tutorial werden wir das Geheimnis der schnellen Datenbankabfragen lüften. Du wirst lernen, was Indexierung ist, wie sie funktioniert und warum sie wichtig ist, um die Performance von Datenbankabfragen zu verbessern. Mit diesem Wissen bist du in der Lage, deine Datenbankabfragen zu beschleunigen und schneller an die gewünschten Informationen zu gelangen. Los geht's!

## Theorie
### Was ist Indexierung?
Stell dir vor, du hast ein riesiges Buch mit vielen Seiten und möchtest eine bestimmte Information finden. Es wäre sehr zeitaufwendig, Seite für Seite durchzublättern, um die gesuchte Information zu finden. Genau hier kommt die Indexierung ins Spiel. Eine Indexstruktur in einer Datenbank funktioniert wie das Inhaltsverzeichnis in einem Buch. Sie enthält vordefinierte Einträge, die auf bestimmte Datensätze in der Datenbank verweisen. Dadurch können Abfragen schneller ausgeführt werden, da die Datenbank direkt zu den relevanten Datensätzen springen kann, ohne alles von vorne durchsuchen zu müssen.

#### Allgemeines Code-Beispiel:
```python
# Index erstellen
create_index(table_name, column_name)

# Index entfernen
drop_index(table_name, index_name)
```

#### Explizites Code-Beispiel in Python:
```python
# Beispielcode für Indexierung
def search_by_name(name):
    # Index für den Namen erstellen
    create_index("employees", "name")
    
    # Abfrage mit Index verwenden
    result = execute_query("SELECT * FROM employees WHERE name = ?", [name])
    
    print("Ergebnis:", result)
```

### Vorteile der Indexierung
- Schnellere Abfragen: Durch die Verwendung von Indexen können Abfragen beschleunigt werden, da die Datenbank direkt auf die relevanten Datensätze zugreifen kann.
- Effiziente Datenverwaltung: Indexe ermöglichen eine effiziente Verwaltung von Daten in der Datenbank, da sie eine geordnete Struktur schaffen.
- Verbesserte Datenintegrität: Indexe können auch verwendet werden, um die Datenintegrität sicherzustellen, indem sie eindeutige oder bedingte Einschränkungen auf Spalten anwenden.

### Nachteile der Indexierung
- Speicherplatzbedarf: Indexe benötigen zusätzlichen Speicherplatz, da sie separate Strukturen sind, die auf die Daten verweisen.
- Aktualisierungsaufwand: Wenn Daten in der Datenbank aktualisiert werden, müssen auch die Indexe aktualisiert werden, was zusätzlichen Aufwand bedeutet.
- Beeinträchtigung der Einfügegeschwindigkeit: Da Indexe aktualisiert werden müssen, kann dies die Geschwindigkeit von Einfügeoperationen beeinflussen.

## Praxis
### Aufgabe 1 (Leicht)
Angenommen, du hast eine Datenbanktabelle mit Kundendaten und möchtest nach Kunden suchen, die in einer bestimmten Stadt leben. Erstelle einen Index für die Spalte "Stadt" und führe eine Abfrage aus, um alle Kunden aus der Stadt "Berlin" zu erhalten.

#### Musterlösung:
```python
# Index für die Spalte "Stadt" erstellen
create_index("customers", "city")

# Abfrage

 mit Index verwenden
result = execute_query("SELECT * FROM customers WHERE city = ?", ["Berlin"])

print("Ergebnis:", result)
```

### Aufgabe 2 (Schwer)
Angenommen, du entwickelst eine Anwendung zur Verwaltung von Büchern und möchtest eine schnelle Suche nach Büchern anhand ihres Titels ermöglichen. Implementiere eine Funktion `search_books(title)`, die den Titel als Parameter akzeptiert und eine Liste von Büchern mit Übereinstimmungen zurückgibt. Verwende einen Index für die Titelspalte, um die Abfrage zu beschleunigen.

#### Musterlösung:
```python
# Index für die Spalte "Titel" erstellen
create_index("books", "title")

# Funktion zur Büchersuche implementieren
def search_books(title):
    result = execute_query("SELECT * FROM books WHERE title LIKE ?", [f"%{title}%"])
    return result

# Beispielaufruf der Funktion
books = search_books("Python")
print("Gefundene Bücher:", books)
```

Herzlichen Glückwunsch! Du hast erfolgreich gelernt, wie Indexierung in Datenbanken funktioniert und wie sie zur Verbesserung der Performance von Abfragen beiträgt. Nutze dieses Wissen, um deine Datenbankanwendungen effizienter zu gestalten und schneller auf die benötigten Informationen zuzugreifen.

Viel Spaß beim Programmieren und erfolgreichen Indexieren!