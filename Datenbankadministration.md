# Datenbankadministration

## Einführung
Willkommen zum Tutorial über Datenbankadministration! In diesem Tutorial werden wir uns mit der spannenden Welt der Datenbankverwaltung beschäftigen. Du wirst lernen, was Datenbankadministration bedeutet, welche Aufgaben damit verbunden sind und wie du deine Datenbank effizient verwalten kannst. Mit diesem Wissen bist du in der Lage, deine Datenbanken reibungslos zu betreiben und ihre Leistung zu optimieren. Los geht's!

## Theorie
### Was ist Datenbankadministration?
Datenbankadministration bezieht sich auf die Verwaltung und Organisation von Datenbanken. Sie umfasst verschiedene Aufgaben wie die Installation und Konfiguration der Datenbanksoftware, das Erstellen und Verwalten von Benutzern und Berechtigungen, die Überwachung der Datenbankleistung, das Durchführen von Backups und Wiederherstellungen sowie die Optimierung der Datenbankabfragen.

#### Allgemeines Code-Beispiel:
```python
# Datenbank sichern
backup_database(database_name, backup_path)

# Datenbank wiederherstellen
restore_database(database_name, backup_path)
```

#### Explizites Code-Beispiel in Python:
```python
# Beispielcode für Datenbankadministration
def create_user(username, password):
    # Benutzer in der Datenbank anlegen
    execute_query("CREATE USER ? IDENTIFIED BY ?", [username, password])
    
    print("Benutzer erstellt:", username)
```

### Aufgabenverwaltung
- Installation und Konfiguration von Datenbanksoftware
- Erstellung und Verwaltung von Benutzern und Berechtigungen
- Überwachung der Datenbankleistung
- Durchführung von Backups und Wiederherstellungen
- Optimierung von Datenbankabfragen

## Praxis
### Aufgabe 1 (Leicht)
Erstelle einen neuen Benutzer mit dem Namen "admin" und dem Passwort "123456". Stelle sicher, dass der Benutzer alle erforderlichen Berechtigungen hat, um die Datenbank zu verwalten.

#### Musterlösung:
```python
# Benutzer "admin" erstellen
create_user("admin", "123456")

# Berechtigungen festlegen
grant_permissions("admin", "ALL PRIVILEGES")

print("Benutzer erstellt und Berechtigungen zugewiesen.")
```

### Aufgabe 2 (Schwer)
Führe eine Leistungsanalyse für deine Datenbank durch und identifiziere langsame Abfragen. Optimiere eine dieser Abfragen, um die Performance zu verbessern.

#### Musterlösung:
```python
# Leistungsanalyse durchführen
analyze_performance(database_name)

# Langsame Abfrage identifizieren
slow_query = identify_slow_query(database_name)

# Abfrage optimieren
optimized_query = optimize_query(slow_query)

print("Optimierte Abfrage:", optimized_query)
```

Herzlichen Glückwunsch! Du hast erfolgreich gelernt, wie Datenbankadministration funktioniert und welche Aufgaben damit verbunden sind. Nutze dieses Wissen, um deine Datenbanken effektiv zu verwalten und ihre Leistung zu optimieren.

Viel Spaß beim Administrieren deiner Datenbanken!