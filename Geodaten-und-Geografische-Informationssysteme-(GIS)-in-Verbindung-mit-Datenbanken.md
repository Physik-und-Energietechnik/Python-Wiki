# Geodaten und Geografische Informationssysteme (GIS) in Verbindung mit Datenbanken

## Einführung

Willkommen zu einer aufregenden Entdeckungsreise in die Kombination von Geodaten und Geografischen Informationssystemen (GIS) mit Datenbanken in Python! 🌍🗺️ In diesem Tutorial werden wir erforschen, wie Python dazu verwendet werden kann, um mit geografischen Daten zu jonglieren und wie wir diese Daten in Datenbanken speichern und abrufen können. Keine Sorge, wenn das alles neu für dich ist – wir werden das Thema Schritt für Schritt erkunden, mit einer Prise Humor!

Hast du dich jemals gefragt, wie Facebook oder Instagram wissen, wo du dich befindest, wenn du einen Beitrag teilst? Das ist alles dank Geodaten und GIS in Verbindung mit Datenbanken. Wir werden entdecken, wie diese Technologien es uns ermöglichen, nicht nur Orte zu verstehen, sondern auch, wie wir sie speichern und analysieren können.

## Theorie

### Was sind Geodaten?

Geodaten sind im Grunde genommen Informationen über Orte auf der Erde. Stell dir vor, du könntest die ganze Welt in eine riesige Datenbank stecken, in der jedes Gebäude, jede Straße und jeder Berg seinen eigenen Eintrag hat. Das sind Geodaten!

Hier ist ein einfaches Code-Beispiel in Python, um Geodaten in eine Datenbank einzufügen:

```python
import sqlite3

# Verbindung zur Datenbank herstellen
conn = sqlite3.connect('geodata.db')
cursor = conn.cursor()

# Tabelle erstellen
cursor.execute('''
    CREATE TABLE places (
        id INTEGER PRIMARY KEY,
        name TEXT,
        latitude REAL,
        longitude REAL
    )
''')

# Daten einfügen
cursor.execute('INSERT INTO places (name, latitude, longitude) VALUES (?, ?, ?)', ('Eiffel Tower', 48.8584, 2.2945))
conn.commit()
conn.close()
```

### Geografische Informationssysteme (GIS) und Datenbanken

GIS erweitert unsere Datenbanken auf Karten. Es ist wie eine Superkraft für Standortinformationen! Mit GIS können wir nicht nur Daten speichern, sondern sie auch auf Karten visualisieren und analysieren.

Hier ist ein Beispiel, wie du mit Python und `geopandas` Geodaten aus einer Datenbank abrufen und auf einer Karte anzeigen kannst:

```python
import geopandas as gpd
import matplotlib.pyplot as plt
import sqlite3

# Verbindung zur Datenbank herstellen
conn = sqlite3.connect('geodata.db')

# Daten aus der Datenbank abrufen
gdf = gpd.read_postgis('SELECT * FROM places', conn, geom_col='geometry')

# Karte anzeigen
gdf.plot()
plt.show()

# Verbindung schließen
conn.close()
```

## Praxis

### Leichte Aufgabe

Deine Aufgabe ist es, eine Tabelle in deiner Geodaten-Datenbank zu erstellen und einige Orte einzufügen. Zeige dann diese Orte auf einer Karte an, ähnlich wie im vorherigen Beispiel.

Musterlösung:

```python
import geopandas as gpd
import matplotlib.pyplot as plt
import sqlite3

# Verbindung zur Datenbank herstellen
conn = sqlite3.connect('geodata.db')
cursor = conn.cursor()

# Tabelle erstellen
cursor.execute('''
    CREATE TABLE places (
        id INTEGER PRIMARY KEY,
        name TEXT,
        latitude REAL,
        longitude REAL
    )
''')

# Daten einfügen
cursor.execute('INSERT INTO places (name, latitude, longitude) VALUES (?, ?, ?)', ('Statue of Liberty', 40.6892, -74.0445))
cursor.execute('INSERT INTO places (name, latitude, longitude) VALUES (?, ?, ?)', ('Taj Mahal', 27.1751, 78.0421))
conn.commit()

# Daten aus der Datenbank abrufen
gdf = gpd.read_postgis('SELECT * FROM places', conn, geom_col='geometry')

# Karte anzeigen
gdf.plot()
plt.show()

# Verbindung schließen
conn.close()
```

### Schwierige Aufgabe

Jetzt wird es herausfordernder! Verbinde deine Geodaten-Datenbank mit einer Online-Karte (z. B. Leaflet) und zeige die Orte interaktiv auf einer Website an.

Musterlösung:

Erstelle eine HTML-Datei mit einem Leaflet-Code, der auf die Daten in deiner Geodaten-Datenbank zugreift und die Orte auf einer Karte anzeigt.

## Fazit

Du hast es geschafft! Du hast jetzt eine spannende Kombination von Geodaten, GIS und Datenbanken in Python kennengelernt. Du kannst nicht nur Orte speichern, sondern sie auch visualisieren und analysieren. Diese Fähigkeiten sind in vielen Bereichen, von der Stadtplanung bis zur Umweltforschung, äußerst wertvoll.

