# 1. Datenbank-Abstraktion: Vertiefung

### Peewee

Peewee ist ein einfaches und benutzerfreundliches ORM-Framework für Python. Es bietet eine intuitive Syntax und eine gute Performance. Peewee unterstützt verschiedene Datenbank-Backends wie MySQL, PostgreSQL, SQLite und mehr.

Ein allgemeines Code-Beispiel für Peewee:

```python
from peewee import *

# Verbindung zur Datenbank herstellen
db = SqliteDatabase('mydatabase.db')

# Datenmodell definieren
class User(Model):
    name = CharField()
    email = CharField()

    class Meta:
        database = db

# Verbindung zur Datenbank herstellen
db.connect()

# Datenbanktabellen erstellen
db.create_tables([User])

# Ein neues Benutzerobjekt erstellen und in die Datenbank speichern
user = User(name='John Doe', email='john@example.com')
user.save()

# Eine Abfrage erstellen und Ergebnisse erhalten
query = User.select().where(User.name == 'John Doe')
results = query.execute()

# Ergebnisse anzeigen
for user in results:
    print(user.name, user.email)
```

In diesem Code-Beispiel verwenden wir Peewee, um eine Verbindung zur Datenbank herzustellen, ein Datenmodell zu definieren und Daten abzufragen. Peewee bietet eine einfache und intuitive Syntax, um mit Datenbanken in Python zu interagieren.


### Pony ORM

Pony ORM ist ein benutzerfreundliches und leistungsstarkes ORM-Framework für Python. Es ermöglicht eine einfache und intuitive Interaktion mit Datenbanken. Pony ORM unterstützt verschiedene Datenbank-Backends wie SQLite, MySQL, PostgreSQL und Oracle.

Ein allgemeines Code-Beispiel für Pony ORM:

```python
from pony.orm import *

# Verbindung zur Datenbank herstellen
db = Database()

# Datenbank-Konfiguration festlegen
db.bind(provider='sqlite', filename='database.sqlite', create_db=True)

# Datenmodell definieren
class User(db.Entity):
    name = Required(str)
    email = Required(str)

# Datenbanktabellen erstellen
db.generate_mapping(create_tables=True)

# Ein neues Benutzerobjekt erstellen und in die Datenbank speichern
with db_session:
    user = User(name='John Doe', email='john@example.com')

# Eine Abfrage erstellen und Ergebnisse erhalten
with db_session:
    users = select(u for u in User if u.name == 'John Doe')[:]

# Ergebnisse anzeigen
for user in users:
    print(user.name, user.email)
```

In diesem Code-Beispiel verwenden wir Pony ORM, um eine Verbindung zur Datenbank herzustellen, ein Datenmodell zu definieren und Datenbankoperationen durchzuführen. Pony ORM bietet eine benutzerfreundliche Syntax und eine einfache Handhabung von Datenbankabfragen.

### Tortoise ORM

Tortoise ORM ist ein asynchrones ORM-Framework für Python, das speziell für asynchrone Anwendungen entwickelt wurde. Es basiert auf dem AIOHTTP-Framework und bietet eine intuitive API zum Arbeiten mit Datenbanken. Tortoise ORM unterstützt verschiedene Datenbank-Backends wie SQLite, PostgreSQL, MySQL und mehr.

Ein allgemeines Code-Beispiel für Tortoise ORM:

```python
from tortoise import Model, fields, Tortoise

# Verbindung zur Datenbank herstellen
async def init():
    await Tortoise.init(
        db_url='sqlite://database.sqlite',
        modules={'models': ['__main__']},
    )
    await Tortoise.generate_schemas()

# Datenmodell definieren
class User(Model):
    id = fields.IntField(pk=True)
    name = fields.CharField(max_length=100)
    email = fields.CharField(max_length=100)

# Ein neues Benutzerobjekt erstellen und in die Datenbank speichern
async def create_user():
    user = User(name='John Doe', email='john@example.com')
    await user.save()

# Eine Abfrage erstellen und Ergebnisse erhalten
async def get_users():
    users = await User.filter(name='John Doe')
    return users

# Ergebnisse anzeigen
async def print_users():
    users = await get_users()
    for user in users:
        print(user.name, user.email)

# Beispielverwendung
async def main():
    await init()
    await create_user()
    await print_users()

# Asynchrone Schleife ausführen
import asyncio
asyncio.run(main())
```

In diesem Code-Beispiel verwenden wir Tortoise ORM, um eine Verbindung zur Datenbank herzustellen, ein Datenmodell zu definieren und Datenbankoperationen asynchron auszuführen. Tortoise ORM unterstützt asynchrone Anwendungen und bietet eine einfache Möglichkeit, mit Datenbanken umzugehen.

Das waren drei weitere Datenbank-Abstraktionsframeworks, die du in Python verwenden kannst. Jedes Framework hat seine eigenen Vor- und Nachteile, daher ist es wichtig, das beste Framework für deine spezifischen Anforderungen zu wählen. Experimentiere mit den Frameworks und entdecke, welches am besten zu deinem Projekt passt!
