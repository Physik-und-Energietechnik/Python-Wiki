# Normalisierung von Datenbanken

## 1. Einführung

In diesem Tutorial werden wir uns mit dem Thema "Normalisierung von Datenbanken" befassen. Du wirst lernen, was Normalisierung ist, warum sie wichtig ist und wie sie zur Verbesserung der Datenbankstruktur beiträgt. Das Wissen über die Normalisierung von Datenbanken ist für jeden, der mit der Gestaltung und Verwaltung von Datenbanken zu tun hat, unerlässlich.

Durch dieses Tutorial wirst du folgendes lernen:
- Die Grundlagen der Normalisierung von Datenbanken
- Die verschiedenen Normalformen und ihre Bedeutung
- Die Vorteile der Normalisierung
- Wie du deine Datenbanktabellen normalisieren kannst

Die Normalisierung von Datenbanken hilft dabei, die Daten effizienter zu speichern, die Integrität der Daten zu gewährleisten und Redundanzen zu vermeiden. Dieses Wissen kann in der Praxis angewendet werden, um Datenbanken zu entwerfen, bestehende Datenbanken zu optimieren und die Leistung von Abfragen zu verbessern.

## 3. Theorie

### Grundlagen der Normalisierung

Die Normalisierung ist ein Prozess, bei dem Datenbanktabellen so organisiert werden, dass sie die Anforderungen der Normalformen erfüllen. Dabei werden die Daten in logisch zusammenhängende Tabellen aufgeteilt, um Redundanzen zu reduzieren und die Datenintegrität zu verbessern.

Es gibt verschiedene Normalformen, die von der ersten Normalform (1NF) bis zur höchsten Normalform, der Boyce-Codd-Normalform (BCNF), reichen. Jede Normalform hat bestimmte Anforderungen an die Struktur der Datenbanktabellen.

### Erste Normalform (1NF)

Die erste Normalform (1NF) stellt die grundlegenden Anforderungen an eine Datenbanktabelle. Um die 1NF zu erfüllen, müssen folgende Kriterien erfüllt sein:

1. Jede Zelle in der Tabelle sollte atomare Werte enthalten, d.h. sie darf keine mehrwertigen Attribute enthalten.
2. Jede Zeile in der Tabelle muss eindeutig identifizierbar sein, z.B. durch Verwendung eines Primärschlüssels.

Hier ist ein allgemeines Beispiel, um die erste Normalform zu verdeutlichen:

| StudentID | Name            | Fach1   | Fach2   | Fach3   |
|-----------|-----------------|---------|---------|---------|
| 1         | John Doe        | Math    | Physik  | Geschichte |
| 2         | Jane Smith      | Englisch | Math    | Geographie |
| 3         | Michael Johnson | Physik  | Chemie  | Math    |

Dieses Beispiel erfüllt bereits die Anforderungen der 1NF, da jede Zelle atomare Werte enthält und jede Zeile durch die StudentID eindeutig identifizierbar ist.

Hier ist ein Python-Code-Beispiel, das die Daten aus der obigen Tabelle darstellt:

```python
students = [
    {"StudentID": 1, "Name": "John Doe", "Fach1": "Math", "Fach2": "Physik", "Fach3": "Geschichte"},
    {"StudentID": 2, "Name": "Jane Smith", "

Fach1": "Englisch", "Fach2": "Math", "Fach3": "Geographie"},
    {"StudentID": 3, "Name": "Michael Johnson", "Fach1": "Physik", "Fach2": "Chemie", "Fach3": "Math"}
]
```

### Zweite Normalform (2NF)

Die zweite Normalform (2NF) stellt zusätzliche Anforderungen an die Struktur der Datenbanktabellen. Um die 2NF zu erfüllen, müssen folgende Kriterien erfüllt sein:

1. Die Tabelle muss die Anforderungen der 1NF erfüllen.
2. Jedes Nichtschlüsselattribut in der Tabelle muss funktional von jedem Kandidatenschlüssel abhängig sein.

Hier ist ein allgemeines Beispiel, um die zweite Normalform zu verdeutlichen:

| BestellungsID | ProduktID | Produktname | Kategorie    | Bestellmenge |
|---------------|-----------|-------------|--------------|--------------|
| 1             | 101       | T-Shirt     | Kleidung     | 2            |
| 1             | 102       | Jeans       | Kleidung     | 1            |
| 2             | 101       | T-Shirt     | Kleidung     | 3            |
| 2             | 103       | Schuhe      | Schuhe       | 1            |

In diesem Beispiel ist "BestellungsID" der Primärschlüssel und "ProduktID" ist ein Kandidatenschlüssel. Die Spalten "Produktname" und "Kategorie" sind funktional abhängig vom Kandidatenschlüssel "ProduktID".

Hier ist ein Python-Code-Beispiel, das die Daten aus der obigen Tabelle darstellt:

```python
orders = [
    {"BestellungsID": 1, "ProduktID": 101, "Produktname": "T-Shirt", "Kategorie": "Kleidung", "Bestellmenge": 2},
    {"BestellungsID": 1, "ProduktID": 102, "Produktname": "Jeans", "Kategorie": "Kleidung", "Bestellmenge": 1},
    {"BestellungsID": 2, "ProduktID": 101, "Produktname": "T-Shirt", "Kategorie": "Kleidung", "Bestellmenge": 3},
    {"BestellungsID": 2, "ProduktID": 103, "Produktname": "Schuhe", "Kategorie": "Schuhe", "Bestellmenge": 1}
]
```

### Dritte Normalform (3NF)

Die dritte Normalform (3NF) stellt weitere Anforderungen an die Struktur der Datenbanktabellen. Um die 3NF zu erfüllen, müssen folgende Kriterien erfüllt sein:

1. Die Tabelle muss die Anforderungen der 2NF erfüllen.
2. Es dürfen keine transitiven Abhängigkeiten zwischen Nichtschlüsselattributen auftreten.

Hier ist ein allgemeines Beispiel, um die dritte Normalform zu verdeutlichen:

| AutorID | Autorname      | Buchtitel          | Genre    | Verlag           |
|---------|----------------|--------------------|----------|------------------|
| 1       | Mark Twain     | Die Abenteuer...   | Abenteuer |

 Verlag A          |
| 2       | Jane Austen    | Stolz und Voru... | Roman    | Verlag B          |
| 3       | J.R.R. Tolkien | Der Herr der R...  | Fantasy  | Verlag C          |

In diesem Beispiel sind "AutorID" und "Buchtitel" gemeinsam der Primärschlüssel. Die Spalten "Genre" und "Verlag" sind funktional abhängig vom Primärschlüssel und nicht voneinander abhängig.

Hier ist ein Python-Code-Beispiel, das die Daten aus der obigen Tabelle darstellt:

```python
books = [
    {"AutorID": 1, "Autorname": "Mark Twain", "Buchtitel": "Die Abenteuer...", "Genre": "Abenteuer", "Verlag": "Verlag A"},
    {"AutorID": 2, "Autorname": "Jane Austen", "Buchtitel": "Stolz und Voru...", "Genre": "Roman", "Verlag": "Verlag B"},
    {"AutorID": 3, "Autorname": "J.R.R. Tolkien", "Buchtitel": "Der Herr der R...", "Genre": "Fantasy", "Verlag": "Verlag C"}
]
```

## 4. Praxis

### Leichte Aufgabe

Gegeben ist die folgende Tabelle, die Informationen über Studenten und ihre Kurse enthält:

| StudentID | Name       | Fach      | Dozent    |
|-----------|------------|-----------|-----------|
| 1         | John Doe   | Math      | Prof. X   |
| 1         | John Doe   | Physik    | Prof. Y   |
| 2         | Jane Smith | Englisch  | Prof. Z   |
| 3         | Michael J. | Chemie    | Prof. W   |

Deine Aufgabe ist es, die Tabelle in die erste Normalform (1NF) zu überführen.

**Musterlösung:**

| StudentID | Name       |
|-----------|------------|
| 1         | John Doe   |
| 2         | Jane Smith |
| 3         | Michael J. |

| StudentID | Fach      | Dozent    |
|-----------|-----------|-----------|
| 1         | Math      | Prof. X   |
| 1         | Physik    | Prof. Y   |
| 2         | Englisch  | Prof. Z   |
| 3         | Chemie    | Prof. W   |

### Schwere Aufgabe

Gegeben ist die folgende Tabelle, die Informationen über Bestellungen und Produkte enthält:

| BestellungsID | Produktname | Kategorie | Preis |
|---------------|-------------|-----------|-------|
| 1             | T-Shirt     | Kleidung  | 10.00 |
| 1             | Jeans       | Kleidung  | 30.00 |
| 2             | T-Shirt     | Kleidung  | 10.00 |
| 2             | Schuhe      | Schuhe    | 50.00 |

Deine Aufgabe ist es, die Tabelle in die dritte Normalform (3NF) zu überführen.

**Musterlösung:**

| BestellungsID | ProduktID |
|---------------|-----------|
| 1             | 1         |
| 1             | 2         |
| 2             | 1         |
| 2             | 3         |

| ProduktID

 | Produktname | Kategorie |
|-----------|-------------|-----------|
| 1         | T-Shirt     | Kleidung  |
| 2         | Jeans       | Kleidung  |
| 3         | Schuhe      | Schuhe    |

| ProduktID | Preis |
|-----------|-------|
| 1         | 10.00 |
| 2         | 30.00 |
| 3         | 50.00 |

Ich hoffe, dieses Tutorial hat dir geholfen, die Grundlagen der Normalisierung von Datenbanken zu verstehen. Die Normalisierung ist ein wichtiger Schritt bei der Gestaltung effizienter und gut strukturierter Datenbanken. Indem du die Normalisierungstechniken beherrschst, kannst du sicherstellen, dass deine Datenbanken optimale Leistung und Integrität bieten.

Happy Coding!