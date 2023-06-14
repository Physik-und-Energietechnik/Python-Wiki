# Skalierbarkeit

## Einführung

Willkommen zum Tutorial über Skalierbarkeit von Datenbanken! In diesem Tutorial werden wir verschiedene Ansätze zur Skalierung von Datenbanken kennenlernen und diskutieren. Skalierbarkeit bezieht sich auf die Fähigkeit einer Datenbank, mit zunehmender Datenmenge und Benutzerlast umzugehen. Wir werden uns mit zwei Hauptansätzen beschäftigen: vertikale Skalierung und horizontale Skalierung.

Durch dieses Tutorial wirst du Folgendes lernen:

- Den Unterschied zwischen vertikaler und horizontaler Skalierung verstehen
- Die Vor- und Nachteile der einzelnen Skalierungsmethoden kennenlernen
- Wissen, wie du diese Ansätze in der Praxis einsetzen kannst, um die Leistung deiner Datenbank zu verbessern

Das Wissen über Skalierbarkeit ist für jeden relevant, der mit Datenbanken arbeitet, sei es als Entwickler, Datenbankadministrator oder Systemarchitekt. Es ermöglicht dir, datenintensive Anwendungen effizienter zu gestalten und Engpässe bei steigender Benutzerlast zu vermeiden. Also lass uns loslegen und die Welt der Skalierbarkeit erkunden!

## Theorie

### Vertikale Skalierung

Bei der vertikalen Skalierung erhöhst du die Leistung einer Datenbank, indem du die Ressourcen auf einem einzelnen Server erhöhst. Das umfasst die Verbesserung der Hardware-Komponenten wie Prozessor, Arbeitsspeicher und Festplattenkapazität. Hier sind einige Vor- und Nachteile der vertikalen Skalierung:

**Vorteile der vertikalen Skalierung:**
- Einfacher zu implementieren und zu verwalten
- Keine komplexen Änderungen am Datenbankdesign oder der Anwendungslogik erforderlich
- Geringere Kosten im Vergleich zur horizontalen Skalierung bei kleineren Workloads

**Nachteile der vertikalen Skalierung:**
- Begrenzte Skalierbarkeit aufgrund von physischen Hardwarebeschränkungen
- Hohe Kosten für den Erwerb und die Wartung leistungsfähiger Hardware
- Einzelner Ausfallpunkt - Wenn der Server ausfällt, ist die Datenbank nicht verfügbar

Um die vertikale Skalierung in Python zu demonstrieren, schauen wir uns ein einfaches Beispiel an. Angenommen, wir haben eine Tabelle "users" in einer SQLite-Datenbank und möchten alle Benutzer abrufen:

```python
import sqlite3

# Verbindung zur Datenbank herstellen
conn = sqlite3.connect('database.db')

# Cursor erstellen
cursor = conn.cursor()

# Abfrage ausführen
cursor.execute('SELECT * FROM users')

# Ergebnisse abrufen
results = cursor.fetchall()

# Ergebnisse anzeigen
for row in
results:
    print(row)

# Verbindung schließen
conn.close()
```

Dies ist ein einfacher Code, um Daten aus einer SQLite-Datenbank abzurufen. Beachte jedoch, dass die vertikale Skalierung hier nicht direkt im Code implementiert ist. Stattdessen bezieht sie sich auf die Verbesserung der Hardware-Ressourcen des Servers, auf dem die Datenbank läuft.

### Horizontale Skalierung

Bei der horizontalen Skalierung verteilst du die Datenbank auf mehrere Server, um die Leistung zu verbessern. Jeder Server enthält einen Teil der Daten und bearbeitet Anfragen unabhängig voneinander. Hier sind einige Vor- und Nachteile der horizontalen Skalierung:

**Vorteile der horizontalen Skalierung:**
- Hohe Skalierbarkeit durch Hinzufügen weiterer Server bei Bedarf
- Bessere Ausfallsicherheit - Ausfall eines Servers beeinträchtigt nicht die gesamte Datenbank
- Potenziell geringere Kosten durch die Verwendung kostengünstigerer Hardware

**Nachteile der horizontalen Skalierung:**
- Komplexere Implementierung und Konfiguration erforderlich
- Aufteilung der Daten kann zu erhöhtem Aufwand bei der Datenkonsistenz führen
- Abhängigkeit von Netzwerklatenz und Kommunikation zwischen den Servern

Um die horizontale Skalierung zu verdeutlichen, betrachten wir ein Beispiel mit einer MongoDB-Datenbank, die über mehrere Server repliziert wird. Hier ist ein Codebeispiel, wie du mit Python auf die replizierte Datenbank zugreifen kannst:

```python
from pymongo import MongoClient

# Verbindung zur Datenbank herstellen
client = MongoClient("mongodb://server1,server2,server3")

# Datenbank auswählen
db = client.mydatabase

# Dokumente abrufen
results = db.mycollection.find()

# Ergebnisse anzeigen
for doc in results:
    print(doc)

# Verbindung schließen
client.close()
```

In diesem Beispiel verwenden wir die PyMongo-Bibliothek, um auf eine replizierte MongoDB-Datenbank zuzugreifen. Beachte, dass wir mehrere Server in der Verbindungs-URL angeben, um auf die horizontal skalierte Datenbank zuzugreifen.

## Praxis

Nun, da wir die Theorie der vertikalen und horizontalen Skalierung kennen, wollen wir unser Wissen in die Praxis umsetzen. Hier sind zwei Aufgaben, die dir helfen werden, dein Verständnis zu überprüfen:

### Leichte Aufgabe

Du arbeitest an einer Webanwendung, die eine große Anzahl von Benutzern verwaltet. Die Datenbankabfragen dauern jedoch immer länger, je mehr Benutzer hinzukommen. Um die Leistung zu verbessern, möchtest du einen geeigneten Index für eine Tabelle hinzufügen.

Deine Aufgabe besteht darin, einen geeigneten Index für die Spalte "username" in der Tabelle "users" zu erstellen.

#### Musterlösung

```python
import sqlite3

# Verbindung zur Datenbank herstellen
conn = sqlite3.connect('database.db')

# Cursor erstellen
cursor = conn.cursor()

# Index erstellen
cursor.execute('CREATE INDEX idx_username ON users(username)')

# Index bestätigen
conn.commit()

# Verbindung schließen
conn.close()
```

In diesem Beispiel verwenden wir SQLite

, um den Index für die Spalte "username" in der Tabelle "users" zu erstellen. Der Index verbessert die Abfrageleistung, indem er den Zugriff auf die Daten beschleunigt.

### Schwierige Aufgabe

Du arbeitest an einer skalierbaren E-Commerce-Anwendung, bei der täglich Tausende von Bestellungen verarbeitet werden. Du hast festgestellt, dass die Datenbankleistung während der Spitzenzeiten beeinträchtigt ist und möchtest das Problem durch horizontale Skalierung angehen.

Deine Aufgabe besteht darin, die Datenbank in eine Clusterumgebung mit mehreren Servern zu replizieren und die Anwendung so zu konfigurieren, dass sie auf den replizierten Cluster zugreift.

#### Musterlösung

```python
from pymongo import MongoClient

# Verbindung zur Primärinstanz herstellen
client = MongoClient("mongodb://primary-server")

# Replica Set-Optionen festlegen
replica_set_options = {
    'replicaSet': 'myreplicaset',
    'readPreference': 'secondaryPreferred'
}

# Verbindung zur replizierten Datenbank herstellen
client = MongoClient("mongodb://server1,server2,server3", **replica_set_options)

# Datenbank auswählen
db = client.mydatabase

# Dokumente abrufen
results = db.mycollection.find()

# Ergebnisse anzeigen
for doc in results:
    print(doc)

# Verbindung schließen
client.close()
```

In diesem Beispiel verwenden wir PyMongo, um auf eine replizierte MongoDB-Datenbank zuzugreifen. Wir verwenden die Optionen "replicaSet" und "readPreference", um auf den replizierten Cluster zuzugreifen und die Lesevorlieben zu konfigurieren.

## Fazit

Herzlichen Glückwunsch! Du hast nun einen Überblick über Skalierbarkeit von Datenbanken erhalten. Wir haben die Konzepte der vertikalen und horizontalen Skalierung untersucht und ihre Vor- und Nachteile diskutiert. Darüber hinaus hast du praktische Beispiele gesehen, wie du Skalierbarkeit in Python implementieren kannst.

Durch das Verständnis der Skalierbarkeit kannst du die Leistung deiner Datenbank verbessern und sicherstellen, dass sie mit steigender Datenmenge und Benutzerlast umgehen kann. Also nutze dieses Wissen, um deine Anwendungen auf die nächste Stufe zu bringen!

Happy scaling!