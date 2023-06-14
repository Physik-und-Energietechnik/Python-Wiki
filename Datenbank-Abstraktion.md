## 1. Datenbank-Abstraktion

### 2. Einführung

Willkommen zu unserem Tutorial über Datenbank-Abstraktion! In diesem Tutorial werden wir uns damit beschäftigen, wie wir mit Datenbanken interagieren können, ohne uns um die spezifischen Details der zugrunde liegenden Datenbankplattform kümmern zu müssen. Wir werden uns auf die Verwendung von Datenbank-Abstraktionsbibliotheken oder -frameworks konzentrieren, die es uns ermöglichen, auf eine höhere Ebene der Datenbankinteraktion zuzugreifen.

Aber Moment mal, was genau ist Datenbank-Abstraktion? Stell dir vor, du möchtest ein Haus bauen. Anstatt jedes Detail des Bauprozesses selbst zu erledigen, könntest du einen Architekten beauftragen, der die spezifischen Details für dich abstrahiert. Du musst dich nicht mit dem genauen Aufbau der Wände, der Elektrik oder der Rohrleitungen befassen. Stattdessen arbeitest du mit den Entwürfen des Architekten und lässt ihn den Rest erledigen. Ähnlich funktioniert auch die Datenbank-Abstraktion.

Durch die Verwendung von Datenbank-Abstraktionsbibliotheken oder -frameworks können wir uns auf die Logik und die Anforderungen unserer Anwendung konzentrieren, ohne uns um die spezifischen Datenbankdetails kümmern zu müssen. Die Datenbank-Abstraktion übernimmt das Mapping von Objekten in unserer Anwendung auf Datenbanktabellen und ermöglicht uns, Daten zu speichern, abzufragen und zu aktualisieren, ohne uns um die genaue Syntax oder die spezifischen Datenbankabfragen kümmern zu müssen.

In diesem Tutorial werden wir uns auf zwei beliebte Datenbank-Abstraktionsframeworks in Python konzentrieren: SQLAlchemy und Django ORM. Diese Frameworks bieten eine Vielzahl von Funktionen und Werkzeugen, um die Datenbank-Abstraktion zu erleichtern und uns bei der effizienten Interaktion mit Datenbanken zu unterstützen.

Nach Abschluss dieses Tutorials wirst du in der Lage sein, die Grundlagen der Datenbank-Abstraktion zu verstehen und in der Lage sein, Datenbanken in deinen Python-Anwendungen effektiv zu nutzen. Du wirst die Vorteile der Datenbank-Abstraktion erkennen und in der Lage sein, Code zu schreiben, der unabhängig von der zugrunde liegenden Datenbankplattform ist.

### 3. Theorie

#### Was ist SQLAlchemy?

SQLAlchemy ist eine leistungsstarke und flexible Python-Bibliothek für die Datenbankabstraktion. Sie ermöglicht uns, mit Datenbanken auf einer höheren Ebene zu arbeiten und Objekte in unserer Anwendung direkt mit Datenbanktabellen zu verknüpfen. SQLAlchemy bietet eine Vielzahl von Funktionen, die uns bei der Datenmodellierung, dem Datenbankzugriff und der Abfrageerstellung unterstützen.

##### Allgemeines Code-Beispiel:

Hier ist ein allgemeines Code-Beispiel, das die Verwendung von SQLAlchemy demonstriert:

```python
from sqlalchemy import create_engine, Column, Integer, String
from sqlalchemy.orm import sessionmaker
from sqlalchemy.ext.declarative import declarative_base

# Verbindung zur Datenbank herstellen
engine = create_engine('sqlite:///mydatabase.db

')

# Session erstellen
Session = sessionmaker(bind=engine)
session = Session()

# Basis-Klasse für unsere Datenmodelle
Base = declarative_base()

# Datenmodell definieren
class User(Base):
    __tablename__ = 'users'
    id = Column(Integer, primary_key=True)
    name = Column(String)
    email = Column(String)

# Datenbanktabelle erstellen
Base.metadata.create_all(engine)

# Ein neues Benutzerobjekt erstellen
user = User(name='John Doe', email='john@example.com')

# Das Benutzerobjekt zur Datenbank hinzufügen
session.add(user)
session.commit()

# Eine Abfrage erstellen
query = session.query(User).filter_by(name='John Doe')

# Die Abfrage ausführen und Ergebnisse erhalten
results = query.all()

# Ergebnisse anzeigen
for user in results:
    print(user.name, user.email)
```

Dieses Beispiel zeigt die grundlegende Verwendung von SQLAlchemy. Wir definieren unser Datenmodell mithilfe von SQLAlchemy-Klassen, die von `declarative_base()` abgeleitet sind. Wir können dann Instanzen dieser Klassen erstellen und sie der Datenbank hinzufügen. Wir können auch Abfragen erstellen, sie ausführen und die Ergebnisse anzeigen.

##### Explizites Code-Beispiel:

Hier ist ein explizites Code-Beispiel, das die Verwendung von SQLAlchemy zum Erstellen einer einfachen Datenbankanwendung zeigt:

```python
from sqlalchemy import create_engine, Column, Integer, String
from sqlalchemy.orm import sessionmaker
from sqlalchemy.ext.declarative import declarative_base

# Verbindung zur Datenbank herstellen
engine = create_engine('sqlite:///mydatabase.db')

# Session erstellen
Session = sessionmaker(bind=engine)
session = Session()

# Basis-Klasse für unsere Datenmodelle
Base = declarative_base()

# Datenmodell definieren
class User(Base):
    __tablename__ = 'users'
    id = Column(Integer, primary_key=True)
    name = Column(String)
    email = Column(String)

# Datenbanktabelle erstellen
Base.metadata.create_all(engine)

# Ein neues Benutzerobjekt erstellen
user = User(name='John Doe', email='john@example.com')

# Das Benutzerobjekt zur Datenbank hinzufügen
session.add(user)
session.commit()

# Eine Abfrage erstellen
query = session.query(User).filter_by(name='John Doe')

# Die Abfrage ausführen und Ergebnisse erhalten
results = query.all()

# Ergebnisse anzeigen
for user in results:
    print(user.name, user.email)
```

Dieses Beispiel zeigt die Verwendung von SQLAlchemy zur Erstellung einer einfachen Datenbankanwendung. Wir definieren unser Datenmodell in der Klasse `User`, die von `Base` abgeleitet ist. Wir erstellen eine Verbindung zur Datenbank, erstellen eine Session, fügen einen neuen Benutzer hinzu und führen eine Abfrage aus, um die Benutzerdaten abzurufen.

#### Was ist Django ORM?

Django ORM ist ein leistungsfähiges und benutzerfreundliches Datenbank-Abstraktionsframework, das in das Django-Webframework integriert ist. Es ermöglicht uns, mit Datenbanken zu arbeiten, indem wir unsere Datenmodelle als Klassen definieren und dann auf sie zugreifen und mit ihnen interagieren. Django ORM bietet eine intuitive API und viele integrierte Funktionen für die Datenbankinteraktion.

##### Allgemeines Code-Beispiel:

Hier ist ein allgemeines Code-Beispiel, das die

 Verwendung von Django ORM demonstriert:

```python
from django.db import models

# Datenmodell definieren
class User(models.Model):
    name = models.CharField(max_length=100)
    email = models.EmailField()

# Ein neues Benutzerobjekt erstellen und in die Datenbank speichern
user = User(name='John Doe', email='john@example.com')
user.save()

# Eine Abfrage erstellen und Ergebnisse erhalten
query = User.objects.filter(name='John Doe')
results = query.all()

# Ergebnisse anzeigen
for user in results:
    print(user.name, user.email)
```

Dieses Beispiel zeigt die Verwendung von Django ORM. Wir definieren unser Datenmodell, indem wir eine Klasse `User` erstellen, die von `models.Model` abgeleitet ist. Wir können dann Instanzen dieser Klasse erstellen und sie in die Datenbank speichern. Wir können auch Abfragen erstellen, sie ausführen und die Ergebnisse anzeigen.

##### Explizites Code-Beispiel:

Hier ist ein explizites Code-Beispiel, das die Verwendung von Django ORM zum Erstellen einer einfachen Datenbankanwendung zeigt:

```python
from django.db import models

# Datenmodell definieren
class User(models.Model):
    name = models.CharField(max_length=100)
    email = models.EmailField()

# Ein neues Benutzerobjekt erstellen und in die Datenbank speichern
user = User(name='John Doe', email='john@example.com')
user.save()

# Eine Abfrage erstellen und Ergebnisse erhalten
query = User.objects.filter(name='John Doe')
results = query.all()

# Ergebnisse anzeigen
for user in results:
    print(user.name, user.email)
```

Dieses Beispiel zeigt die Verwendung von Django ORM zur Erstellung einer einfachen Datenbankanwendung. Wir definieren unser Datenmodell in der Klasse `User`, die von `models.Model` abgeleitet ist. Wir erstellen ein neues Benutzerobjekt, speichern es in die Datenbank und führen dann eine Abfrage aus, um die Benutzerdaten abzurufen.

### 4. Praxis

#### Leichte Aufgabe:

Erstelle eine Python-Anwendung, die das SQLAlchemy-Framework verwendet, um eine einfache Aufgabenverwaltung zu implementieren. Das Datenmodell soll eine Klasse `Task` mit den Attributen `id`, `title` und `status` umfassen. Implementiere Funktionen, um neue Aufgaben hinzuzufügen, bestehende Aufgaben zu aktualisieren und alle Aufgaben anzuzeigen.

Musterlösung:

```python
from sqlalchemy import create_engine, Column, Integer, String
from sqlalchemy.orm import sessionmaker
from sqlalchemy.ext.declarative import declarative_base

engine = create_engine('sqlite:///tasks.db')
Session = sessionmaker(bind=engine)
session = Session()
Base = declarative_base()

class Task(Base):
    __tablename__ = 'tasks'
    id = Column(Integer, primary_key=True)
    title = Column(String)
    status = Column(String)

Base.metadata.create_all(engine)

def add_task(title, status):
    task = Task(title=title, status=status)
    session.add(task)
    session.commit()

def update_task(id, status):
    task = session.query(Task).filter_by(id=id).first()
    if task:
        task.status = status
        session.commit()

def get_all_tasks():
    tasks = session.query(Task).all()
    for task in tasks:
        print(task.title, task.status)

add_task('Buy groceries', 'pending')
add_task('Finish homework', 'in

 progress')
update_task(1, 'completed')
get_all_tasks()
```

Diese Musterlösung verwendet SQLAlchemy, um eine einfache Aufgabenverwaltung zu implementieren. Wir definieren das Datenmodell `Task` und implementieren Funktionen zum Hinzufügen neuer Aufgaben, Aktualisieren bestehender Aufgaben und Anzeigen aller Aufgaben.

#### Schwerere Aufgabe:

Erstelle eine Django-Anwendung, die das Django ORM verwendet, um eine Blog-Plattform zu implementieren. Das Datenmodell soll eine Klasse `Post` mit den Attributen `id`, `title`, `content` und `created_at` umfassen. Implementiere Funktionen, um neue Blog-Posts hinzuzufügen, bestehende Posts zu aktualisieren, alle Posts anzuzeigen und Posts nach dem Erstellungsdatum zu filtern.

Musterlösung:

```python
from django.db import models
from datetime import datetime

class Post(models.Model):
    title = models.CharField(max_length=100)
    content = models.TextField()
    created_at = models.DateTimeField(default=datetime.now)

def add_post(title, content):
    post = Post(title=title, content=content)
    post.save()

def update_post(id, title, content):
    post = Post.objects.get(id=id)
    if post:
        post.title = title
        post.content = content
        post.save()

def get_all_posts():
    posts = Post.objects.all()
    for post in posts:
        print(post.title, post.content)

def filter_posts_by_date(date):
    posts = Post.objects.filter(created_at__date=date)
    for post in posts:
        print(post.title, post.content)

add_post('Hello World', 'This is my first blog post.')
add_post('Python Tips', 'Here are some useful Python tips.')
update_post(1, 'New Title', 'Updated content goes here.')
get_all_posts()
filter_posts_by_date(datetime.now().date())
```

Diese Musterlösung verwendet das Django ORM, um eine einfache Blog-Plattform zu implementieren. Wir definieren das Datenmodell `Post` und implementieren Funktionen zum Hinzufügen neuer Blog-Posts, Aktualisieren bestehender Posts, Anzeigen aller Posts und Filtern der Posts nach dem Erstellungsdatum.

Das waren nur einige Beispiele für Datenbank-Abstraktionsframeworks in Python. Es gibt noch viele weitere Bibliotheken und Frameworks, die du erkunden kannst, wie zum Beispiel Peewee oder Pony ORM. Die Wahl des richtigen Frameworks hängt von den Anforderungen deines Projekts und deinen persönlichen Vorlieben ab. Viel Spaß beim Entdecken und Experimentieren mit Datenbank-Abstraktion in Python!