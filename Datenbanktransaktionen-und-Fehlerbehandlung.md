# Datenbanktransaktionen und Fehlerbehandlung

Willkommen zu unserem Python-Tutorial über Datenbanktransaktionen und Fehlerbehandlung! In diesem Tutorial werden wir lernen, wie wir sicherstellen können, dass unsere Datenbankoperationen zuverlässig ausgeführt werden und wie wir mit auftretenden Fehlern umgehen können. Aber bevor wir starten, lassen Sie uns zunächst eine kurze Einführung geben.

## Einführung

Datenbanktransaktionen sind wie eine Reise in die Bank. Du möchtest Geld einzahlen und sicherstellen, dass alles korrekt abläuft. Wenn du das Geld einzahlst und dein Konto aktualisiert wird, möchtest du sicher sein, dass der Vorgang erfolgreich war. Wenn etwas schief geht, möchtest du wissen, wie du mit der Situation umgehen kannst. In diesem Tutorial werden wir genau das lernen!

Durch das Erlernen von Datenbanktransaktionen und Fehlerbehandlung in Python können wir:

- Sicherstellen, dass unsere Datenbankoperationen atomar (unteilbar) ausgeführt werden.
- Transaktionen bei Bedarf rückgängig machen oder wiederholen.
- Mit auftretenden Fehlern umgehen und alternative Aktionen ausführen.
- Die Integrität unserer Daten sicherstellen und Dateninkonsistenzen vermeiden.

Jetzt, da Sie wissen, was wir durch dieses Tutorial erlernen können, lass uns direkt in die Theorie eintauchen!

## Theorie

In diesem Abschnitt werden wir uns mit den grundlegenden Konzepten von Datenbanktransaktionen und Fehlerbehandlung in Python befassen.

### Datenbanktransaktionen

Eine Datenbanktransaktion ist wie ein Keksbacken. Du benötigst eine Reihe von Schritten, um sicherzustellen, dass der Backvorgang erfolgreich ist. Wenn einer der Schritte fehlschlägt, möchtest du sicherstellen, dass du den Backvorgang rückgängig machst und nichts beschädigt ist.

Hier ist ein allgemeines Code-Beispiel, wie man eine Datenbanktransaktion in Python durchführt:

```python
import mysql.connector

# Verbindung zur Datenbank herstellen
connection = mysql.connector.connect(
    host="localhost",
    user="benutzername",
    password="passwort",
    database="datenbankname"
)

# Transaktion starten
connection.start_transaction()

try:
    # Datenbankoperationen ausführen
    # ...

    # Transaktion bestätigen
    connection.commit()
except:
    # Transaktion abbrechen
    connection.rollback()

# Verbindung schließen
connection.close()
```

### Fehlerbehandlung

Manchmal läuft nicht alles nach Plan. Fehler können auftreten, sei es aufgrund von Netzwerkproblemen, ungültigen Eingaben oder anderen unvorhergesehenen Ereignissen. Es ist wichtig, dass wir wissen, wie wir mit diesen Fehlern umgehen können, um unsere Anwendung widerstandsfähiger zu machen.

Hier ist ein Code-Beispiel, wie man Fehler in Python abfängt und damit umgeht:

```python
import mysql.connector

try:
    # Verbindung zur Datenbank herstellen
    connection = mysql.connector.connect(
        host="localhost",
        user="benutzername",
        password="passwort",
        database="datenbankname"
    )

    # Datenbankoperationen ausführen
    # ...

    # Verbindung schließen
    connection

.close()
except mysql.connector.Error as error:
    # Fehler behandeln
    print("Ein Fehler ist aufgetreten:", error)
```

## Praxis

Jetzt, da wir die Theorie kennen, lassen Sie uns das erlangte Wissen mit einer praktischen Aufgabe überprüfen.

**Aufgabe:** Erstelle eine Tabelle namens "Kunden" in deiner Datenbank mit den Spalten "ID", "Name" und "Guthaben". Füge dann einen neuen Kunden mit einem Startguthaben von 100 Euro hinzu. Führe anschließend einen Code aus, der das Guthaben des Kunden um 50 Euro erhöht. Überprüfe, ob der Code erfolgreich war und das Guthaben korrekt aktualisiert wurde. Wenn nicht, setze das Guthaben auf den vorherigen Wert zurück.

**Musterlösung:**

```python
import mysql.connector

try:
    # Verbindung zur Datenbank herstellen
    connection = mysql.connector.connect(
        host="localhost",
        user="benutzername",
        password="passwort",
        database="datenbankname"
    )

    # Transaktion starten
    connection.start_transaction()

    try:
        # Cursor erstellen
        cursor = connection.cursor()

        # Tabelle erstellen
        cursor.execute("CREATE TABLE Kunden (ID INT AUTO_INCREMENT PRIMARY KEY, Name VARCHAR(255), Guthaben DECIMAL(10, 2))")

        # Kunden hinzufügen
        cursor.execute("INSERT INTO Kunden (Name, Guthaben) VALUES ('Max Mustermann', 100.00)")

        # Guthaben erhöhen
        cursor.execute("UPDATE Kunden SET Guthaben = Guthaben + 50.00 WHERE ID = 1")

        # Transaktion bestätigen
        connection.commit()

        # Verbindung und Cursor schließen
        cursor.close()
        connection.close()
    except:
        # Transaktion abbrechen
        connection.rollback()
except mysql.connector.Error as error:
    # Fehler behandeln
    print("Ein Fehler ist aufgetreten:", error)
```

## Fazit

Herzlichen Glückwunsch! Du hast gerade gelernt, wie man Datenbanktransaktionen in Python durchführt und mit Fehlern umgeht. Du weißt jetzt, wie du sicherstellen kannst, dass deine Datenbankoperationen zuverlässig sind und wie du mit auftretenden Fehlern umgehen kannst. Dies hilft dir, die Integrität deiner Daten sicherzustellen und unerwünschte Nebenwirkungen zu vermeiden. Denke daran, dass dies nur der Anfang ist und es noch viele weitere Aspekte der Datenbankkommunikation zu entdecken gibt. Viel Spaß beim Erkunden und Experimentieren!