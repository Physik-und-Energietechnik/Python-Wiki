
## Einführung
Willkommen zu diesem spannenden Python Tutorial! Heute werden wir uns damit beschäftigen, wie du Datenbanken in deine API integrieren kannst. Stell dir vor, du hast eine Schatztruhe voller wertvoller Informationen, die du in deiner API nutzen möchtest. Eine Datenbank ist wie diese Schatztruhe, in der du deine Daten sicher und organisiert aufbewahren kannst. In diesem Tutorial lernst du, wie du die Kraft der Datenbankintegration nutzen kannst, um deine API noch leistungsfähiger zu machen!

Du wirst lernen, wie du mit Python eine Datenbank in deine API einbindest, um Daten abzurufen, zu erstellen, zu aktualisieren und zu löschen. Wir werden das SQLAlchemy-Framework verwenden, das uns dabei hilft, mit verschiedenen Datenbanken zu interagieren. Das erlernte Wissen kann in verschiedenen Szenarien eingesetzt werden, wie zum Beispiel beim Erstellen von Webanwendungen, APIs oder Backend-Services, bei denen Daten persistent gespeichert werden müssen. Also schnall dich an und mach dich bereit, deine Daten in die Datenbankwelt einzutauchen!

## Theorie
### Datenbankintegration mit SQLAlchemy
SQLAlchemy ist ein beliebtes Python-Toolkit, das uns hilft, mit Datenbanken zu interagieren. Es bietet eine abstrakte Schnittstelle zur Datenbank, sodass wir mit Python-Objekten arbeiten können, anstatt uns mit komplexen SQL-Abfragen herumschlagen zu müssen. SQLAlchemy unterstützt verschiedene Datenbanken wie MySQL, PostgreSQL, SQLite und mehr.

Hier ist ein allgemeines Beispiel, wie wir SQLAlchemy verwenden können, um eine Verbindung zur Datenbank herzustellen und Daten abzurufen:

```python
from sqlalchemy import create_engine, Column, Integer, String
from sqlalchemy.orm import sessionmaker
from sqlalchemy.ext.declarative import declarative_base

# Datenbankverbindung herstellen
engine = create_engine("sqlite:///database.db")
Session = sessionmaker(bind=engine)
session = Session()

# Model für eine Tabelle definieren
Base = declarative_base()

class User(Base):
    __tablename__ = "users"

    id = Column(Integer, primary_key=True)
    name = Column(String)

# Daten abrufen
users = session.query(User).all()
for user in users:
    print(user.name)
```

In diesem Beispiel haben wir eine Verbindung zur SQLite-Datenbank hergestellt und ein Model für die Tabelle "users" definiert. Mit der Methode `query` können wir Daten aus der Datenbank abrufen und mit Python-Objekten arbeiten.

## Praxis
Jetzt ist es Zeit, dein erlangtes Wissen in die Praxis umzusetzen! Hier ist eine Aufgabe für dich: Schreibe eine Python-Funktion, die einen Benutzer in die Datenbank einfügt. Hier ist eine Beispiel-Lösung mit SQLAlchemy:

```python
from sqlalchemy import create_engine, Column, Integer, String
from sqlalchemy.orm import sessionmaker
from sqlalchemy.ext.declarative import declarative_base

# Datenbankverbindung herstellen
engine = create_engine("sqlite:///database.db")
Session = sessionmaker(bind=engine)
session = Session()

# Model für eine Tabelle definieren
Base = declarative_base()

class User(Base):
    __tablename__ = "users"

    id = Column(Integer, primary_key=True)
    name = Column(String)

#

 Funktion zum Hinzufügen eines Benutzers
def add_user(name):
    new_user = User(name=name)
    session.add(new_user)
    session.commit()
    print("Benutzer wurde hinzugefügt!")

# Funktion aufrufen
add_user("Max Mustermann")
```

Diese Funktion `add_user` erstellt ein neues `User`-Objekt mit dem gegebenen Namen und fügt es der Datenbank hinzu. Nach dem Hinzufügen wird die Änderung mit `session.commit()` in der Datenbank gespeichert.

## Fazit
Herzlichen Glückwunsch! Du hast erfolgreich gelernt, wie du Datenbanken in deine API integrieren kannst. Durch die Verwendung von SQLAlchemy hast du die Macht, mit Datenbanken zu interagieren, ohne dich mit komplexen SQL-Abfragen auseinandersetzen zu müssen. Du kannst jetzt Daten abrufen, erstellen, aktualisieren und löschen, indem du deine Python-Objekte mit der Datenbank synchronisierst.

Die Datenbankintegration ist ein unverzichtbarer Bestandteil vieler Anwendungen, da sie uns ermöglicht, Daten dauerhaft zu speichern und effizient darauf zuzugreifen. Mit SQLAlchemy und Python bist du bestens gerüstet, um anspruchsvolle Webanwendungen, APIs oder Backend-Services zu entwickeln, die Datenbanken nutzen.

Nutze dieses erlernte Wissen, um deine eigenen datenbankgestützten Anwendungen zu erstellen und die Datenbankwelt zu erobern! Viel Spaß und happy coding!