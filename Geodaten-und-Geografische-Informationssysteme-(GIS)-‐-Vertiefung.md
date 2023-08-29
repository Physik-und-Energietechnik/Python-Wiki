# Geodaten und Geografische Informationssysteme (GIS) - Vertiefung

## Einführung

Willkommen zurück zur aufregenden Welt der Geodaten und Geografischen Informationssysteme (GIS) in Verbindung mit Datenbanken! 🌍🗺️ In diesem vertiefenden Tutorial werden wir unser Wissen erweitern und tiefer in die Anwendung von Python für die Arbeit mit räumlichen Daten eintauchen. Keine Sorge, wenn du noch nicht alles im Griff hast – wir werden Schritt für Schritt vorgehen und sicherstellen, dass du dich wie ein(e) Geo-Profi fühlst!

In der vorherigen Lektion haben wir entdeckt, wie man Orte speichert und auf Karten darstellt. Diesmal werden wir lernen, wie man räumliche Abfragen durchführt und Geodaten mit Datenbanken verknüpft, um komplexe Aufgaben zu bewältigen.

## Theorie

### Räumliche Abfragen mit Geopandas und SQL

Stell dir vor, du möchtest alle Restaurants innerhalb eines bestimmten Radius um deinen Standort finden. Mit Python und Geopandas kannst du räumliche Abfragen durchführen, um genau das zu tun! Hier ist ein Beispiel:

```python
import geopandas as gpd
from shapely.geometry import Point

# Daten aus der Datenbank abrufen
gdf = gpd.read_postgis('SELECT * FROM places', conn, geom_col='geometry')

# Unser Standort
user_location = Point(-74.006, 40.7128)

# Räumliche Abfrage
restaurants_nearby = gdf[gdf.geometry.distance(user_location) < 0.1]

print(restaurants_nearby)
```

### Geodatenanalyse mit Python

Du kannst Python verwenden, um spannende Analysen mit deinen Geodaten durchzuführen. Zum Beispiel könntest du die durchschnittliche Entfernung zwischen verschiedenen Orten berechnen:

```python
from geopy.distance import geodesic

# Koordinaten von zwei Orten
coord1 = (-74.006, 40.7128)
coord2 = (-118.2437, 34.0522)

# Entfernung berechnen
distance = geodesic(coord1, coord2).kilometers

print(f'Die Entfernung beträgt {distance} km')
```

## Praxis

### Leichte Aufgabe

Deine Aufgabe ist es, eine räumliche Abfrage mit Geopandas und SQL durchzuführen. Finde alle Orte in deiner Datenbank, die sich innerhalb eines bestimmten Bereichs um deinen Standort befinden. Zeige die Ergebnisse an.

Musterlösung:

```python
user_location = Point(-74.006, 40.7128)
places_nearby = gdf[gdf.geometry.distance(user_location) < 0.5]
print(places_nearby)
```

### Schwierige Aufgabe

Jetzt wird es herausfordernder! Erstelle eine Karte, auf der du die Orte aus deiner Datenbank darstellst. Füge dann eine interaktive Funktion hinzu, um Informationen über einen Ort anzuzeigen, wenn du darauf klickst.

Musterlösung:

Verwende die Bibliothek `folium`, um eine interaktive Karte zu erstellen und Pop-up-Informationen für Orte hinzuzufügen.

## Fazit

Herzlichen Glückwunsch, du hast es geschafft, deine Geo-Fähigkeiten auf die nächste Stufe zu heben! Mit Python, Geopandas und Datenbanken kannst du nicht nur Orte speichern und anzeigen, sondern auch räumliche Abfragen durchführen und sogar geografische Analysen erstellen. Dieses Wissen kann in zahlreichen Bereichen wie Stadtplanung, Umweltforschung und vielem mehr eingesetzt werden.

Karte weiter, Geo-Held!
