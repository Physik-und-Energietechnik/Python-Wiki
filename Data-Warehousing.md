# Data Warehousing

## Einführung
Willkommen zum Tutorial über Data Warehousing! In diesem Tutorial werden wir uns mit dem Konzept des Data Warehousing beschäftigen und lernen, wie man Daten extrahiert, transformiert und lädt, um eine optimale Leistung für Analyse- und Berichterstattungsanwendungen zu erzielen.

Data Warehousing bezieht sich auf den Prozess der Erfassung, Organisation und Speicherung großer Mengen strukturierter Daten aus verschiedenen Quellen, um Entscheidungsunterstützungssysteme und Business Intelligence-Anwendungen zu unterstützen. Durch die Konsolidierung von Daten aus verschiedenen Quellen in einem zentralen Repository ermöglicht uns das Data Warehousing, umfassende Analysen und Berichte zu erstellen, die bei strategischen Geschäftsentscheidungen helfen können.

In diesem Tutorial werden wir die Grundlagen des Data Warehousing kennenlernen, die Schritte des ETL-Prozesses (Extraktion, Transformation, Laden) verstehen und bewährte Methoden für die Implementierung eines Data Warehouses erkunden. Am Ende des Tutorials wirst du in der Lage sein, Daten aus verschiedenen Quellen zu extrahieren, zu transformieren und in einem Data Warehouse zu laden, um aussagekräftige Analysen und Berichte zu generieren.

## Theorie

### Data Warehousing-Grundlagen
Bevor wir uns in die Details stürzen, schauen wir uns einige grundlegende Konzepte des Data Warehousing an.

Ein Data Warehouse ist eine speziell entworfene Datenbank, die Daten aus verschiedenen Quellen integriert und in einer optimierten Form für Analysezwecke speichert. Im Data Warehouse werden Daten in einem speziellen Datenmodell organisiert, das auf die Analyse und Berichterstattung abzielt. 

Typischerweise folgt ein Data Warehouse einem sogenannten **Star-Schema** oder **Snowflake-Schema**, bei dem eine zentrale Faktentabelle von dimensionalen Tabellen umgeben ist. Die dimensionalen Tabellen enthalten Attribute, die die verschiedenen Aspekte der analysierten Daten beschreiben, während die Faktentabelle die Messwerte oder Kennzahlen enthält, auf die sich die Analysen beziehen.

Hier ist ein allgemeines Code-Beispiel für ein Star-Schema:

```python
# Dimensionale Tabelle: Produkt
product_dimension = {
    "product_id": int,
    "product_name": str,
    "category": str,
    "price": float
}

# Dimensionale Tabelle: Zeit
time_dimension = {
    "date": str,
    "year": int,
    "month": int,
    "day": int
}

# Faktentabelle: Verkauf
sales_fact_table = {
    "product_id": int,
    "date": str,
    "quantity": int,
    "revenue": float
}
```

### ETL-Prozess: Extraktion, Transformation, Laden
Der ETL-Prozess ist ein wesentlicher Bestandteil des Data Warehousing. Er umfasst die Extraktion von Daten aus verschiedenen Quellen, die Transformation der Daten, um sie für die Analyse geeignet zu machen, und das Laden der Daten in das Data Warehouse.

#### Extraktion
Die Extraktion bezieht sich auf den Prozess der Erfassung von Daten aus verschiedenen Quellen, wie z.B. relationalen Datenbanken, Excel-Dateien oder APIs. Die Daten können aus internen Systemen oder externen Quellen stammen. Die Extraktion

 kann je nach Quelle und Datenformat unterschiedliche Methoden erfordern.

Hier ist ein Beispiel für die Extraktion von Daten aus einer CSV-Datei:

```python
import pandas as pd

# Daten aus CSV-Datei extrahieren
data = pd.read_csv("daten.csv")
```

#### Transformation
Die Transformation beinhaltet die Bereinigung, Zusammenführung und Umwandlung der extrahierten Daten, um sie für die Analyse geeignet zu machen. Während der Transformation können Daten bereinigt, fehlende Werte behandelt, Duplikate entfernt und Datentypen geändert werden.

Hier ist ein Beispiel für die Transformation von Daten mit pandas:

```python
# Daten bereinigen und transformieren
cleaned_data = data.dropna()  # Entfernen von Zeilen mit fehlenden Werten
transformed_data = cleaned_data.groupby("category")["revenue"].sum()  # Gruppierung und Aggregation der Daten
```

#### Laden
Nach der Extraktion und Transformation müssen die Daten in das Data Warehouse geladen werden. Dieser Schritt beinhaltet das Schreiben der transformierten Daten in die entsprechenden Tabellen und Spalten des Data Warehouses.

Hier ist ein Beispiel für das Laden von Daten in eine SQL-Datenbank mit pandas:

```python
import sqlalchemy

# Verbindung zur Datenbank herstellen
engine = sqlalchemy.create_engine("sqlite:///data_warehouse.db")

# Daten in die Datenbank laden
transformed_data.to_sql("sales_fact_table", engine, if_exists="replace")
```

### Implementierung eines Data Warehouses
Die Implementierung eines Data Warehouses erfordert sorgfältige Planung und Berücksichtigung verschiedener Faktoren wie Datenmodellierung, Leistungsoptimierung und Skalierbarkeit. Es gibt verschiedene Datenbanktechnologien und Werkzeuge, die bei der Implementierung eines Data Warehouses eingesetzt werden können.

Ein bewährtes Vorgehen bei der Implementierung eines Data Warehouses ist die Verwendung eines schrittweisen Ansatzes, bei dem zunächst ein kleiner Teil des Data Warehouses entwickelt und getestet wird, bevor das gesamte System umgesetzt wird. Dies ermöglicht eine iterative Entwicklung und Anpassung an die Anforderungen der Benutzer.

## Praxis

### Leichte Aufgabe
Extrahiere Daten aus einer CSV-Datei, gruppiere sie nach Kategorie und berechne die Gesamtsumme der Einnahmen für jede Kategorie. Speichere die transformierten Daten in einer SQLite-Datenbank mit dem Namen "data_warehouse.db" und einer Tabelle "revenue_by_category".

Musterlösung:

```python
import pandas as pd
import sqlalchemy

# Daten aus CSV-Datei extrahieren
data = pd.read_csv("daten.csv")

# Daten bereinigen und transformieren
cleaned_data = data.dropna()
transformed_data = cleaned_data.groupby("category")["revenue"].sum()

# Verbindung zur Datenbank herstellen
engine = sqlalchemy.create_engine("sqlite:///data_warehouse.db")

# Daten in die Datenbank laden
transformed_data.to_sql("revenue_by_category", engine, if_exists="replace")
```

### Schwere Aufgabe
Extrahiere Daten aus zwei verschiedenen Datenbanktabellen, führe eine komplexe Transformation durch, um eine kombinierte Tabelle zu erstellen, und lade die transformierten Daten in das Data Warehouse. Verwende SQL-Abfragen, um die Daten zu extrahieren und zu transformieren.

Musterl

ösung:

```python
import pandas as pd
import sqlalchemy

# Verbindung zur Quelldatenbank herstellen
source_engine = sqlalchemy.create_engine("sqlite:///source.db")

# Daten aus zwei Tabellen extrahieren
query = """
SELECT orders.order_id, customers.customer_name, products.product_name
FROM orders
JOIN customers ON orders.customer_id = customers.customer_id
JOIN products ON orders.product_id = products.product_id
"""
data = pd.read_sql(query, source_engine)

# Daten transformieren
transformed_data = data.groupby("customer_name")["order_id"].count()

# Verbindung zur Zieldatenbank herstellen
target_engine = sqlalchemy.create_engine("sqlite:///data_warehouse.db")

# Daten in das Data Warehouse laden
transformed_data.to_sql("order_count_by_customer", target_engine, if_exists="replace")
```

Herzlichen Glückwunsch! Du hast erfolgreich Daten aus verschiedenen Quellen extrahiert, transformiert und in ein Data Warehouse geladen. Jetzt kannst du diese Daten nutzen, um umfassende Analysen und Berichte zu erstellen.

## Fazit
In diesem Tutorial hast du die Grundlagen des Data Warehousing kennengelernt und gelernt, wie man Daten extrahiert, transformiert und in ein Data Warehouse lädt. Du verstehst den ETL-Prozess und hast praktische Erfahrung mit der Verwendung von Python-Tools wie pandas und sqlalchemy gesammelt.

Data Warehousing ist ein mächtiges Konzept, das Unternehmen dabei unterstützt, fundierte Entscheidungen zu treffen und wertvolle Erkenntnisse aus ihren Daten zu gewinnen. Indem du Daten aus verschiedenen Quellen in einem zentralen Repository zusammenführst, kannst du umfassende Analysen durchführen und Geschäftsberichte generieren.

Jetzt liegt es an dir, dein neu erlangtes Wissen anzuwenden und Data Warehousing in deinen eigenen Projekten einzusetzen. Viel Erfolg und happy warehousing!