# Datenbank-Sicherheit

## Einführung

Willkommen zum Tutorial über Datenbank-Sicherheit! In diesem Tutorial werden wir grundlegende Konzepte der Datenbanksicherheit kennenlernen und erfahren, wie wir unsere Datenbanken vor Sicherheitsbedrohungen schützen können. Datenbanksicherheit ist ein äußerst wichtiges Thema, da Datenbanken oft sensible Informationen enthalten, auf die nicht autorisierte Personen keinen Zugriff haben sollten.

Durch dieses Tutorial wirst du Folgendes lernen:
- Benutzer-Authentifizierung und -Autorisierung für den sicheren Zugriff auf die Datenbank
- Verschlüsselung von Datenbanken, um die Vertraulichkeit der Informationen zu gewährleisten
- Schutz vor SQL-Injektion, einer häufigen Sicherheitsbedrohung bei Datenbanken

Das erlernte Wissen kann in verschiedenen Anwendungsbereichen eingesetzt werden, wie z.B. Webanwendungen, Unternehmenssysteme oder persönliche Projekte. Datenbanksicherheit ist von entscheidender Bedeutung, um die Integrität, Vertraulichkeit und Verfügbarkeit der Daten zu gewährleisten und den Schutz sensibler Informationen zu gewährleisten.

Also lass uns loslegen und lernen, wie wir unsere Datenbanken sicher machen können!

## Theorie

### Benutzer-Authentifizierung und -Autorisierung

Benutzer-Authentifizierung und -Autorisierung sind grundlegende Konzepte der Datenbanksicherheit. Authentifizierung bezieht sich auf die Überprüfung der Identität eines Benutzers, um sicherzustellen, dass er berechtigt ist, auf die Datenbank zuzugreifen. Autorisierung hingegen bestimmt die Berechtigungen eines authentifizierten Benutzers, d.h. welche Aktionen er auf der Datenbank ausführen darf.

#### Allgemeines Code-Beispiel

```python
import sqlite3

# Verbindung zur Datenbank herstellen
conn = sqlite3.connect('database.db')

# Cursor erstellen
cursor = conn.cursor()

# Benutzer authentifizieren
username = input("Benutzername: ")
password = input("Passwort: ")

cursor.execute('SELECT * FROM users WHERE username = ? AND password = ?', (username, password))
user = cursor.fetchone()

if user:
    print("Erfolgreich authentifiziert!")
else:
    print("Ungültige Anmeldeinformationen!")

# Benutzer autorisieren
if user and user['role'] == 'admin':
    print("Du hast Administratorberechtigungen!")
else:
    print("Du hast keine ausreichenden Berechtigungen!")

# Verbindung schließen
conn.close()
```

Dieses Code-Beispiel zeigt, wie du Benutzer-Authentifizierung und -Autorisierung in Python mit SQLite umsetzen kannst. Der Benutzer wird nach seinem Benutzernamen und Passwort gefragt. Anschließend wird überprüft, ob ein Benutzer mit den eingegebenen Anmeldeinformationen existiert. Wenn ein Benutzer gefunden wird, wird er erfolgreich authentifiziert. Anschließend wird überprüft, ob der Benutzer die Rolle "admin" hat, um zu bestimmen, ob er Administratorberechtigungen hat.

#### Explizites Code-Beispiel

```python
import sqlite3

# Verbindung zur Datenbank herstellen
conn =

 sqlite3.connect('database.db')

# Cursor erstellen
cursor = conn.cursor()

# Benutzer erstellen
cursor.execute('CREATE TABLE users (id INTEGER PRIMARY KEY, username TEXT, password TEXT, role TEXT)')

# Benutzer hinzufügen
cursor.execute('INSERT INTO users (username, password, role) VALUES (?, ?, ?)', ('alice', 'pass123', 'admin'))

# Benutzer abrufen
cursor.execute('SELECT * FROM users')
users = cursor.fetchall()

# Ergebnisse anzeigen
for user in users:
    print(user)

# Verbindung schließen
conn.close()
```

Dieses Code-Beispiel zeigt, wie du eine Datenbanktabelle für Benutzer erstellen, Benutzer hinzufügen und Benutzer abrufen kannst. Die Tabelle "users" enthält Spalten für den Benutzernamen, das Passwort und die Rolle. In diesem Beispiel fügen wir einen Benutzer mit dem Benutzernamen "alice", dem Passwort "pass123" und der Rolle "admin" hinzu.

### Verschlüsselung von Datenbanken

Die Verschlüsselung von Datenbanken ist ein weiterer wichtiger Aspekt der Datenbanksicherheit. Durch die Verschlüsselung können wir sicherstellen, dass die Daten vertraulich bleiben und nur von autorisierten Benutzern entschlüsselt werden können.

#### Allgemeines Code-Beispiel

```python
import sqlite3
from cryptography.fernet import Fernet

# Schlüssel generieren
key = Fernet.generate_key()

# Verbindung zur Datenbank herstellen
conn = sqlite3.connect('encrypted.db')

# Cursor erstellen
cursor = conn.cursor()

# Tabelle erstellen
cursor.execute('CREATE TABLE secrets (id INTEGER PRIMARY KEY, data TEXT)')

# Daten verschlüsseln
cipher_suite = Fernet(key)
encrypted_data = cipher_suite.encrypt(b'Sensible Informationen')

# Daten in die Datenbank einfügen
cursor.execute('INSERT INTO secrets (data) VALUES (?)', (encrypted_data,))

# Daten abrufen und entschlüsseln
cursor.execute('SELECT * FROM secrets')
row = cursor.fetchone()

if row:
    decrypted_data = cipher_suite.decrypt(row['data'])
    print("Entschlüsselte Daten:", decrypted_data.decode())

# Verbindung schließen
conn.close()
```

Dieses Code-Beispiel zeigt, wie du Datenbanken in SQLite mit Verschlüsselung verwenden kannst. Zuerst generieren wir einen Schlüssel mit der Fernet-Bibliothek. Dann stellen wir eine Verbindung zur Datenbank her und erstellen eine Tabelle für sensible Informationen. Die Daten werden mit dem generierten Schlüssel verschlüsselt und in die Datenbank eingefügt. Beim Abrufen der Daten werden sie mit dem Schlüssel entschlüsselt.

#### Explizites Code-Beispiel

```python
import sqlite3
from cryptography.fernet import Fernet

# Schlüssel generieren
key = Fernet.generate_key()

# Verbindung zur Datenbank herstellen
conn = sqlite3.connect('encrypted.db')

# Cursor erstellen
cursor = conn.cursor()

# Tabelle erstellen
cursor.execute('CREATE TABLE secrets (id INTEGER PRIMARY KEY, data TEXT)')

# Daten verschlüsseln und in die Datenbank einfügen
cipher_suite = Fernet(key)

data = b'Sensible Informationen'

encrypted_data = cipher_suite.encrypt(data)
cursor.execute('INSERT INTO secrets (data) VALUES (?)', (encrypted_data,))

# Daten abrufen und entschlüsseln
cursor.execute('SELECT * FROM secrets')
row =

 cursor.fetchone()

if row:
    decrypted_data = cipher_suite.decrypt(row['data'])
    print("Entschlüsselte Daten:", decrypted_data.decode())

# Verbindung schließen
conn.close()
```

Dieses Code-Beispiel zeigt den konkreten Ablauf der Verschlüsselung von Datenbanken mit der Fernet-Bibliothek. Der generierte Schlüssel wird verwendet, um die Daten zu verschlüsseln, bevor sie in die Datenbank eingefügt werden. Beim Abrufen der Daten werden sie mit demselben Schlüssel entschlüsselt.

### Schutz vor SQL-Injektion und anderen Sicherheitsbedrohungen

SQL-Injektion ist eine häufige Sicherheitsbedrohung bei Datenbanken. Dabei werden bösartige SQL-Befehle in Eingabeparameter eingeschleust, um unberechtigten Zugriff auf die Datenbank oder Datenmanipulation zu ermöglichen. Um solche Angriffe zu verhindern, sollten wir immer sichere Praktiken beim Schreiben von Datenbankabfragen verwenden.

#### Allgemeines Code-Beispiel

```python
import sqlite3

# Verbindung zur Datenbank herstellen
conn = sqlite3.connect('database.db')

# Cursor erstellen
cursor = conn.cursor()

# Eingabe vom Benutzer erhalten
username = input("Benutzername: ")
password = input("Passwort: ")

# Sicherer SQL-Befehl mit Platzhaltern
cursor.execute('SELECT * FROM users WHERE username = ? AND password = ?', (username, password))
user = cursor.fetchone()

if user:
    print("Erfolgreich authentifiziert!")
else:
    print("Ungültige Anmeldeinformationen!")

# Verbindung schließen
conn.close()
```

In diesem Code-Beispiel wird eine sichere Methode zur Vermeidung von SQL-Injektion verwendet. Statt die Benutzereingaben direkt in die SQL-Abfrage einzufügen, verwenden wir Platzhalter. Die tatsächlichen Werte werden separat übergeben und sicher in die Abfrage eingefügt. Dadurch wird verhindert, dass bösartiger SQL-Code in die Abfrage eingeschleust wird.

#### Explizites Code-Beispiel

```python
import sqlite3

# Verbindung zur Datenbank herstellen
conn = sqlite3.connect('database.db')

# Cursor erstellen
cursor = conn.cursor()

# Eingabe vom Benutzer erhalten
username = input("Benutzername: ")
password = input("Passwort: ")

# Unsicherer SQL-Befehl ohne Platzhalter (anfällig für SQL-Injektion)
query = "SELECT * FROM users WHERE username = '" + username + "' AND password = '" + password + "'"
cursor.execute(query)
user = cursor.fetchone()

if user:
    print("Erfolgreich authentifiziert!")
else:
    print("Ungültige Anmeldeinformationen!")

# Verbindung schließen
conn.close()
```

Dieses Code-Beispiel zeigt, wie eine unsichere Methode zur SQL-Abfrage verwendet wird, die anfällig für SQL-Injektion ist. Die Benutzereingaben werden direkt in die Abfrage eingefügt, ohne Platzhalter zu verwenden. Dadurch wird es Angreifern ermöglicht, bösartigen SQL-Code einzuschleusen und die Datenbank unerlaubt zu manipulieren.

## Praxis

### Leichte Auf

gabe: Benutzerregistrierung

Deine Aufgabe besteht darin, eine Benutzerregistrierungsfunktion zu implementieren. Die Funktion sollte den Benutzernamen und das Passwort des Benutzers entgegennehmen, sie sicher in die Datenbank einfügen und den Benutzer erfolgreich registrieren.

**Musterlösung:**

```python
import sqlite3

# Verbindung zur Datenbank herstellen
conn = sqlite3.connect('database.db')

# Cursor erstellen
cursor = conn.cursor()

def register_user(username, password):
    # Benutzer in die Datenbank einfügen
    cursor.execute('INSERT INTO users (username, password) VALUES (?, ?)', (username, password))
    conn.commit()
    print("Benutzer erfolgreich registriert!")

# Benutzer registrieren
register_user('bob', 'pass123')

# Verbindung schließen
conn.close()
```

In dieser Musterlösung wird die Funktion `register_user` erstellt, die den Benutzernamen und das Passwort entgegennimmt. Die Funktion fügt den Benutzer sicher in die Datenbank ein und bestätigt die erfolgreiche Registrierung.

### Schwere Aufgabe: Datenbankverschlüsselung

Deine Aufgabe besteht darin, eine Funktion zu implementieren, die eine SQLite-Datenbank verschlüsselt. Die Funktion sollte einen Schlüssel generieren, die Datenbankdatei verschlüsseln und die verschlüsselte Datei speichern.

**Musterlösung:**

```python
import sqlite3
from cryptography.fernet import Fernet

def encrypt_database(database_file):
    # Schlüssel generieren
    key = Fernet.generate_key()

    # Verbindung zur unverschlüsselten Datenbank herstellen
    conn = sqlite3.connect(database_file)

    # Cursor erstellen
    cursor = conn.cursor()

    # Verschlüsselung der Datenbank aktivieren
    cursor.execute('PRAGMA key = ?', (key,))
    conn.commit()

    # Datenbankdatei verschlüsseln
    conn.close()

    # Verschlüsselten Schlüssel speichern
    with open('key.key', 'wb') as key_file:
        key_file.write(key)

    print("Datenbank erfolgreich verschlüsselt!")

# Datenbank verschlüsseln
encrypt_database('database.db')
```

In dieser Musterlösung wird die Funktion `encrypt_database` erstellt, die die Datenbankdatei mit Hilfe der Fernet-Bibliothek verschlüsselt. Zuerst wird ein Schlüssel generiert. Dann wird eine Verbindung zur unverschlüsselten Datenbank hergestellt und die Verschlüsselung aktiviert. Anschließend wird die Datenbankdatei verschlüsselt und der verschlüsselte Schlüssel in einer separaten Datei gespeichert.

Herzlichen Glückwunsch! Du hast erfolgreich die Praxisaufgaben abgeschlossen und dein Wissen über Datenbanksicherheit erweitert.

Das war eine ausführliche Erklärung zum Thema "Datenbank-Sicherheit" in einer für Python-unerfahrene Menschen verständlichen, jedoch humorvollen Ausdrucksweise. Du kannst den obigen Markdown-Code verwenden, um den Text mit den Code-Beispielen anzuzeigen. Viel Spaß beim Lernen und Entdecken der Datenbanksicherheit!