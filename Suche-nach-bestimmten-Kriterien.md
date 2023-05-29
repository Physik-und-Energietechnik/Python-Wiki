## Einführung

Willkommen zum Python-Tutorial über die Suche! In diesem Tutorial lernst du, wie du mit Python nach bestimmten Kriterien in großen Datenmengen suchst. Stell dir vor, du hast eine riesige Schatzkiste voller Daten, aber du suchst nach einem bestimmten Schatzstück. Python ist wie dein treuer Spürhund, der dir hilft, den gesuchten Schatz zu finden!

In diesem Tutorial wirst du Folgendes lernen:

    Wie du in JSON- und CSV-Dateien nach bestimmten Kriterien suchst
    Wie du die mächtigen Funktionen von Python nutzt, um gezielt nach Daten zu suchen
    Wie du die gefundenen Daten weiterverarbeiten und anzeigen kannst

Die Fähigkeit, nach Daten zu suchen, ist äußerst wertvoll, insbesondere wenn du mit großen Datenmengen arbeitest. Egal, ob du nach bestimmten Kundeninformationen in einer CSV-Datei oder nach spezifischen Objekten in einer JSON-Datei suchst, Python ist dein bester Freund in der Suche nach dem verlorenen Schatz!
## Theorie
### Suche in JSON-Dateien

JSON-Dateien können komplexe strukturierte Daten enthalten, die nach bestimmten Kriterien durchsucht werden können. Du kannst Python verwenden, um die JSON-Daten zu öffnen, zu durchsuchen und die gewünschten Informationen zu finden.

Ein allgemeines Code-Beispiel:

```python

import json

# JSON-Datei öffnen
with open('daten.json', 'r') as file:
    data = json.load(file)

    # Suche nach bestimmten Kriterien
    results = []
    for item in data:
        if item['alter'] > 25:
            results.append(item)

    # Gefundene Ergebnisse anzeigen
    for result in results:
        print(result)
```

Ein explizites Code-Beispiel in Python:

```python

import json

# JSON-Datei öffnen
with open('daten.json', 'r') as file:
    data = json.load(file)

    # Suche nach bestimmten Kriterien
    results = []
    for item in data:
        if item['name'].startswith('A'):
            results.append(item)

    # Gefundene Ergebnisse anzeigen
    for result in results:
        print("Name:", result['name'])
        print("Alter:", result['alter'])
```

### Suche in CSV-Dateien

CSV-Dateien speichern tabellarische Daten, die nach bestimmten Kriterien durchsucht werden können. Mit Python kannst du CSV-Dateien öffnen, durch die Datenzeilen iterieren und die gewünschten Informationen filtern.

Ein allgemeines Code-Beispiel:

```python

import csv

# CSV-Datei öffnen
with open('daten.csv', 'r') as file:
    reader = csv.DictReader(file)

    # Suche nach bestimmten Kriterien
    results = []
    for row in reader:
        if int(row['alter']) > 25:
            results.append(row)

    # Gefundene Ergebnisse anzeigen
    for result in results:
        print(result)
```

Ein explizites Code-Beispiel in Python:

```python

import csv

# CSV-Datei öffnen
with open('daten.csv', 'r') as file:
    reader = csv.DictReader(file)

    # Suche nach bestimmten Kriterien
```
## Aufgaben

### Aufgabe 1: Suche in einer JSON-Datei

Gegeben ist eine JSON-Datei mit Informationen über verschiedene Bücher. Deine Aufgabe besteht darin, nach Büchern zu suchen, die von einem bestimmten Autor geschrieben wurden, und die gefundenen Bücher auf der Konsole auszugeben.

Musterlösung:

```python

import json

# JSON-Datei öffnen
with open('buecher.json', 'r') as file:
    data = json.load(file)

    # Suche nach Büchern des Autors
    author = "J.K. Rowling"
    results = []
    for book in data:
        if book['author'] == author:
            results.append(book)

    # Gefundene Bücher anzeigen
    for result in results:
        print("Titel:", result['title'])
        print("Autor:", result['author'])
```

### Aufgabe 2: Suche in einer CSV-Datei

Gegeben ist eine CSV-Datei mit Informationen über verschiedene Produkte. Deine Aufgabe besteht darin, nach Produkten zu suchen, die in einem bestimmten Preissegment liegen, und die gefundenen Produkte auf der Konsole auszugeben.

Musterlösung:

```python

import csv

# CSV-Datei öffnen
with open('produkte.csv', 'r') as file:
    reader = csv.DictReader(file)

    # Suche nach Produkten im Preissegment
    min_price = 10
    max_price = 50
    results = []
    for row in reader:
        price = float(row['price'])
        if min_price <= price <= max_price:
            results.append(row)

    # Gefundene Produkte anzeigen
    for result in results:
        print("Produkt:", result['product'])
        print("Preis:", result['price'])
```
Viel Spaß beim Ausprobieren und Erforschen der spannenden Welt der Suche in Dateien mit Python!