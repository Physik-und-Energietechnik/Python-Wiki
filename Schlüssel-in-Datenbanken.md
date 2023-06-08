# Schlüssel in Datenbanken

## Einführung

In einer Datenbank dienen Schlüssel dazu, Datensätze eindeutig zu identifizieren und Beziehungen zwischen verschiedenen Tabellen herzustellen. Schlüssel spielen eine wichtige Rolle im Datenbankdesign und gewährleisten die Integrität und Konsistenz der Daten. In diesem Tutorial werden wir uns mit verschiedenen Arten von Schlüsseln befassen und ihre Funktionen und Anwendungen genauer betrachten.

## Theorie

### Primärschlüssel

Ein Primärschlüssel ist ein eindeutiger Identifikator für jeden Datensatz in einer Tabelle. Er stellt sicher, dass es keine doppelten oder redundante Einträge gibt. Ein Primärschlüssel kann aus einer oder mehreren Spalten bestehen und wird beim Erstellen der Tabelle definiert. Hier sind einige wichtige Punkte zu Primärschlüsseln:

- Ein Primärschlüssel darf keine doppelten Werte enthalten (eindeutig).
- Ein Primärschlüssel darf keinen NULL-Wert enthalten (not null).

Ein Beispiel für einen Primärschlüssel in Python:

```python
CREATE TABLE Benutzer (
    id INT PRIMARY KEY,
    name VARCHAR(50) NOT NULL,
    email VARCHAR(50) NOT NULL
)
```

In diesem Beispiel besteht der Primärschlüssel aus der Spalte "id". Jeder Benutzer in der Tabelle hat eine eindeutige ID, die als Primärschlüssel fungiert. Die Spalten "name" und "email" sind als "not null" definiert, um sicherzustellen, dass sie keine NULL-Werte enthalten.

### Fremdschlüssel

Ein Fremdschlüssel stellt eine Beziehung zwischen zwei Tabellen her. Er verweist auf den Primärschlüssel einer anderen Tabelle und ermöglicht es, Beziehungen zwischen den Datensätzen herzustellen. Ein Fremdschlüssel wird in der Tabelle definiert, die auf die andere Tabelle verweist. Hier sind einige wichtige Punkte zu Fremdschlüsseln:

- Ein Fremdschlüssel muss auf den Primärschlüssel einer anderen Tabelle verweisen.
- Ein Fremdschlüssel kann auch NULL-Werte enthalten, um optionale Beziehungen darzustellen.

Ein Beispiel für einen Fremdschlüssel in Python:

```python
CREATE TABLE Bestellung (
    id INT PRIMARY KEY,
    benutzer_id INT,
    produkt VARCHAR(50),
    FOREIGN KEY (benutzer_id) REFERENCES Benutzer(id)
)
```

In diesem Beispiel verweist der Fremdschlüssel "benutzer_id" auf den Primärschlüssel "id" in der Tabelle "Benutzer". Dadurch wird eine Beziehung zwischen den Tabellen "Bestellung" und "Benutzer" hergestellt. Der Fremdschlüssel "benutzer_id" kann auch NULL-Werte enthalten, um optionale Beziehungen zu ermöglichen.

### Zusammengesetzte Schlüssel

Manchmal ist es erforderlich, einen Schlüssel aus mehreren Spalten zu erstellen. Dies wird als zusammengesetzter Schlüssel bezeichnet. Ein zusammengesetzter Schlüssel besteht aus zwei oder mehr Spalten und ermöglicht es, Datensätze eindeutig zu identifizieren, indem die Kombination der Werte in den Sp

alten verwendet wird. Dies kann hilfreich sein, wenn eine einzelne Spalte nicht ausreicht, um die Eindeutigkeit sicherzustellen.

Ein Beispiel für einen zusammengesetzten Schlüssel in Python:

```python
CREATE TABLE Student (
    studiengang VARCHAR(50),
    semester INT,
    name VARCHAR(50),
    PRIMARY KEY (studiengang, semester)
)
```

In diesem Beispiel besteht der Schlüssel aus den Spalten "studiengang" und "semester". Zusammen bilden sie einen eindeutigen Schlüssel, der jeden Studenten eindeutig identifiziert. Durch die Verwendung eines zusammengesetzten Schlüssels können wir sicherstellen, dass es keine doppelten Einträge für denselben Studiengang und dasselbe Semester gibt.

## Praxis

### Aufgabe 1

Erstelle eine Tabelle mit dem Namen "Produkt" mit den folgenden Spalten:

- id: Eine eindeutige ID für das Produkt (Primärschlüssel).
- name: Der Name des Produkts.
- preis: Der Preis des Produkts.

```python
CREATE TABLE Produkt (
    id INT PRIMARY KEY,
    name VARCHAR(50) NOT NULL,
    preis DECIMAL(8,2) NOT NULL
)
```

### Aufgabe 2

Erstelle eine Tabelle mit dem Namen "Bestellung" mit den folgenden Spalten:

- id: Eine eindeutige ID für die Bestellung (Primärschlüssel).
- benutzer_id: Die ID des Benutzers, der die Bestellung aufgegeben hat (Fremdschlüssel).
- produkt_id: Die ID des bestellten Produkts (Fremdschlüssel).
- menge: Die Anzahl der bestellten Produkte.

```python
CREATE TABLE Bestellung (
    id INT PRIMARY KEY,
    benutzer_id INT,
    produkt_id INT,
    menge INT,
    FOREIGN KEY (benutzer_id) REFERENCES Benutzer(id),
    FOREIGN KEY (produkt_id) REFERENCES Produkt(id)
)
```

Das waren zwei Beispiele, wie Tabellen mit Primärschlüsseln und Fremdschlüsseln erstellt werden können.

Ich hoffe, dieses Tutorial hilft dir dabei, Schlüssel in Datenbanken besser zu verstehen und ihre Bedeutung im Datenbankdesign zu erkennen. Viel Spaß beim Experimentieren und Entdecken neuer Möglichkeiten!