# Datenbankadministration - Vertiefung

## Einführung
Willkommen zurück zum Thema Datenbankadministration! In diesem vertiefenden Tutorial werden wir uns mit den grundlegenden Aufgaben der Datenbankadministration befassen. Du wirst lernen, wie du Datenbanken erstellst und löschst, Benutzer anlegst und ihnen Berechtigungen zuweist, deine Datenbanken sicherst und wiederherstellst sowie die Leistung deiner Datenbank überwachst. Mit diesem vertieften Wissen bist du bestens gerüstet, um deine Datenbanken zu verwalten und zu schützen. Los geht's!

## Theorie
### Datenbank erstellen und löschen
Die Erstellung und Löschung von Datenbanken ist eine grundlegende Aufgabe der Datenbankadministration. Hier ein Beispiel, wie du eine Datenbank erstellen und löschen kannst:

#### Allgemeines Code-Beispiel:
```python
# Datenbank erstellen
create_database(database_name)

# Datenbank löschen
delete_database(database_name)
```

#### Explizites Code-Beispiel in Python:
```python
# Beispielcode für Datenbank erstellen und löschen
def create_database(database_name):
    # Code zum Erstellen der Datenbank
    print("Datenbank", database_name, "erstellt.")

def delete_database(database_name):
    # Code zum Löschen der Datenbank
    print("Datenbank", database_name, "gelöscht.")
```

### Benutzer anlegen und Berechtigungen vergeben
Die Erstellung von Benutzern und die Vergabe von Berechtigungen ermöglicht es, den Zugriff auf die Datenbank zu steuern. Hier ein Beispiel, wie du Benutzer anlegst und ihnen Berechtigungen zuweist:

#### Allgemeines Code-Beispiel:
```python
# Benutzer anlegen
create_user(username, password)

# Berechtigungen vergeben
grant_permissions(username, permissions)
```

#### Explizites Code-Beispiel in Python:
```python
# Beispielcode für Benutzer anlegen und Berechtigungen vergeben
def create_user(username, password):
    # Code zum Anlegen des Benutzers
    print("Benutzer", username, "erstellt.")

def grant_permissions(username, permissions):
    # Code zum Vergeben von Berechtigungen
    print("Berechtigungen für Benutzer", username, "vergeben:", permissions)
```

### Datenbank sichern und wiederherstellen
Das regelmäßige Sichern und Wiederherstellen deiner Datenbanken ist wichtig, um Datenverlust zu vermeiden. Hier ein Beispiel, wie du deine Datenbank sichern und wiederherstellen kannst:

#### Allgemeines Code-Beispiel:
```python
# Datenbank sichern
backup_database(database_name, backup_path)

# Datenbank wiederherstellen
restore_database(database_name, backup_path)
```

#### Explizites Code-Beispiel in Python:
```python
# Beispielcode für Datenbank sichern und wiederherstellen
def backup_database(database_name, backup_path):
    # Code zum Sichern der Datenbank
    print("Datenbank", database_name, "gesichert. Sicherungspfad:", backup_path)

def restore_database(database_name, backup_path):
    # Code zum Wiederherstellen der Datenbank
    print("Datenbank", database_name, "wiederhergestellt aus Sicherung:", backup_path)
```

### Datenbankleistung überwachen
Die Überwachung der Datenbankleistung hilft dir,

 Engpässe zu erkennen und die Performance zu optimieren. Hier ein Beispiel, wie du die Datenbankleistung überwachen kannst:

#### Allgemeines Code-Beispiel:
```python
# Datenbankleistung überwachen
monitor_performance(database_name)
```

#### Explizites Code-Beispiel in Python:
```python
# Beispielcode für Überwachung der Datenbankleistung
def monitor_performance(database_name):
    # Code zur Überwachung der Leistung
    print("Überwache Leistung der Datenbank", database_name)
```

## Praxis
### Aufgabe (Leicht)
Erstelle eine neue Datenbank mit dem Namen "Einkaufsliste". Anschließend lege einen Benutzer "Benutzer1" mit dem Passwort "Passwort123" an und weise ihm alle Berechtigungen für die "Einkaufsliste"-Datenbank zu.

#### Musterlösung:
```python
# Datenbank "Einkaufsliste" erstellen
create_database("Einkaufsliste")

# Benutzer "Benutzer1" anlegen
create_user("Benutzer1", "Passwort123")

# Berechtigungen vergeben
grant_permissions("Benutzer1", "ALL PRIVILEGES")
```

### Aufgabe (Schwer)
Führe eine Sicherung der Datenbank "Kundendaten" durch und speichere die Sicherungsdatei unter dem Pfad "/backup/kundendaten.bak". Anschließend stelle die Datenbank aus der Sicherungsdatei wieder her.

#### Musterlösung:
```python
# Datenbank "Kundendaten" sichern
backup_database("Kundendaten", "/backup/kundendaten.bak")

# Datenbank "Kundendaten" wiederherstellen
restore_database("Kundendaten", "/backup/kundendaten.bak")
```

Herzlichen Glückwunsch! Du hast erfolgreich gelernt, wie man Datenbanken erstellt, Benutzer anlegt und Berechtigungen vergibt, Datenbanken sichert und wiederherstellt sowie die Datenbankleistung überwacht. Mit diesem Wissen kannst du deine Datenbanken effektiv verwalten und schützen.

Viel Spaß beim Administrieren deiner Datenbanken!