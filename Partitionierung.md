# 1. Titel - Datenbank-Partitionierung

## 2. Einführung

Willkommen zu unserem Tutorial über Datenbank-Partitionierung! In diesem Tutorial werden wir uns mit einem wichtigen Konzept der Datenbankverwaltung befassen, nämlich der Partitionierung von Daten. Partitionierung ist wie das Organisieren deiner Schränke zuhause, um deine Kleidung besser zu sortieren. Es hilft dabei, große Datenmengen effizienter zu verwalten und abzufragen.

In diesem Tutorial lernst du:

- Was Datenbank-Partitionierung ist und warum sie nützlich ist.
- Unterschiedliche Arten der Partitionierung, wie Bereichspartitionierung und Listenpartitionierung.
- Wie du Datenbanktabellen partitionierst und welche Faktoren du dabei berücksichtigen solltest.
- Wie du Partitionen in Abfragen einbeziehst, um schnellere Ergebnisse zu erzielen.

Die Kenntnis von Datenbank-Partitionierungstechniken ist sowohl für Datenbankadministratoren als auch für Entwickler von großer Bedeutung. Du wirst lernen, wie du die Leistung deiner Datenbank verbessern und effizienter mit großen Datenmengen umgehen kannst.

Also schnall dich an und lass uns die Welt der Datenbank-Partitionierung erkunden!

## 3. Theorie

### Was ist Datenbank-Partitionierung?

Datenbank-Partitionierung ist der Prozess der Aufteilung großer Datenmengen in kleinere, handhabbare Teile, die als Partitionen bezeichnet werden. Jede Partition enthält einen bestimmten Teil der Daten basierend auf einem Partitionierungsschlüssel, wie zum Beispiel einem Zeitstempel oder einer geografischen Region. Durch die Aufteilung der Daten in Partitionen wird die Datenverwaltung und -abfrage optimiert.

#### Bereichspartitionierung

Bei der Bereichspartitionierung werden die Daten basierend auf einem numerischen oder zeitlichen Wert in Bereiche unterteilt. Jeder Bereich wird dann einer Partition zugeordnet. Dies ist nützlich, wenn du Daten basierend auf bestimmten Kriterien wie Datum oder Größe gruppieren möchtest.

Hier ist ein allgemeines Code-Beispiel, das die Idee der Bereichspartitionierung verdeutlicht:

```python
CREATE TABLE Sales (
    id INT,
    product_name VARCHAR(50),
    sale_date DATE,
    amount DECIMAL(10, 2)
)
PARTITION BY RANGE (YEAR(sale_date)) (
    PARTITION p0 VALUES LESS THAN (2020),
    PARTITION p1 VALUES LESS THAN (2021),
    PARTITION p2 VALUES LESS THAN (2022)
);
```

In diesem Beispiel wird die Tabelle "Sales" basierend auf dem Verkaufsdatum in drei Partitionen aufgeteilt: p0 für Verkäufe vor 2020, p1 für Verkäufe im Jahr 2021 und p2 für Verkäufe im Jahr 2022.

#### Listenpartitionierung

Die Listenpartitionierung erfolgt anhand einer festgelegten Liste von Werten. Jeder Wert wird einer bestimmten Partition zugeordnet. Dies ist hilfreich, wenn du Daten basierend auf bestimmten Kategorien wie Produkttyp oder geografischer Region gruppieren möchtest.

Hier ist ein allgemeines Code-Beispiel, das die Idee der Listenpartitionierung verdeutlicht:

```python
CREATE TABLE Customers

 (
    id INT,
    name VARCHAR(50),
    country VARCHAR(50)
)
PARTITION BY LIST (country) (
    PARTITION p_europe VALUES IN ('Germany', 'France', 'Italy'),
    PARTITION p_asia VALUES IN ('China', 'Japan', 'India'),
    PARTITION p_others VALUES IN (DEFAULT)
);
```

In diesem Beispiel wird die Tabelle "Customers" basierend auf dem Land in drei Partitionen aufgeteilt: p_europe für europäische Länder, p_asia für asiatische Länder und p_others für alle anderen Länder.

### Code-Beispiel für die Partitionierung

Hier ist ein explizites Code-Beispiel, das zeigt, wie du Daten in Partitionen einfügst und abfragst:

```python
-- Einfügen von Daten in eine partitionierte Tabelle
INSERT INTO Sales (id, product_name, sale_date, amount)
VALUES (1, 'Product A', '2020-05-10', 100.50);

-- Abfrage von Daten aus einer bestimmten Partition
SELECT * FROM Sales PARTITION (p1);
```

In diesem Beispiel fügst du einen Verkaufseintrag in die Tabelle "Sales" ein und fragst dann Daten nur aus der Partition "p1" ab.

## 4. Praxis

### Leichte Aufgabe

Gegeben ist eine Tabelle "Students" mit den Spalten "id", "name" und "grade". Die Tabelle enthält Daten für Schüler verschiedener Schuljahre. Partitioniere die Tabelle basierend auf dem Schuljahr, sodass Schüler des gleichen Schuljahres in derselben Partition gruppiert werden.

Musterlösung:

```python
CREATE TABLE Students (
    id INT,
    name VARCHAR(50),
    grade INT
)
PARTITION BY RANGE (grade) (
    PARTITION p1 VALUES LESS THAN (6),
    PARTITION p2 VALUES LESS THAN (9),
    PARTITION p3 VALUES LESS THAN (12)
);
```

### Schwierigere Aufgabe

Angenommen, du hast eine große Tabelle "Logs" mit den Spalten "id", "timestamp" und "message". Die Tabelle enthält Protokolldaten für verschiedene Anwendungskomponenten. Partitioniere die Tabelle basierend auf dem Monat des Zeitstempels, um die Abfrageleistung zu verbessern.

Musterlösung:

```python
CREATE TABLE Logs (
    id INT,
    timestamp TIMESTAMP,
    message VARCHAR(100)
)
PARTITION BY RANGE (MONTH(timestamp)) (
    PARTITION p1 VALUES LESS THAN (2),
    PARTITION p2 VALUES LESS THAN (3),
    ...
    PARTITION p12 VALUES LESS THAN (13)
);
```

In dieser Lösung wird die Tabelle "Logs" basierend auf dem Monat des Zeitstempels in 12 Partitionen aufgeteilt.

Herzlichen Glückwunsch! Du hast erfolgreich Datenbank-Partitionierungstechniken gelernt und zwei Aufgaben gelöst.

Nun bist du bereit, deine Datenbanken zu partitionieren und sie effizienter zu verwalten!

