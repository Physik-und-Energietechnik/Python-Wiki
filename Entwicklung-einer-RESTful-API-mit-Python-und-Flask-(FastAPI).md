# 4. Entwicklung einer RESTful API mit Python und Flask (FastAPI)

## 4.1 Einführung in das Flask-Framework

Flask ist ein beliebtes Web-Framework für Python, das die Entwicklung von Webanwendungen und RESTful APIs erleichtert. In diesem Tutorial lernst du, wie du mit Flask eine RESTful API erstellen kannst.

Flask zeichnet sich durch seine Einfachheit und Flexibilität aus und eignet sich sowohl für kleine als auch für größere Projekte. Es basiert auf dem WSGI-Toolkit Werkzeug und der Template-Engine Jinja2.

## 4.2 Erstellung von RESTful-Routen und Endpunkten

Eine RESTful API besteht aus verschiedenen Routen und Endpunkten, über die Client-Anwendungen Daten abrufen, hinzufügen, aktualisieren oder löschen können. In Flask kannst du Routen und Endpunkte einfach definieren und mit entsprechenden Funktionen verknüpfen.

Hier ist ein allgemeines Code-Beispiel, das zeigt, wie eine einfache Route mit Flask definiert wird:

```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def hello_world():
    return 'Hallo, Welt!'

if __name__ == '__main__':
    app.run()
```

In diesem Beispiel wird eine Route für den Stammendpunkt (`/`) definiert, die die Funktion `hello_world()` aufruft. Die Funktion gibt den Text "Hallo, Welt!" als Antwort zurück.

## 4.3 Verwendung von HTTP-Methoden (GET, POST, PUT, DELETE)

Eine wichtige Eigenschaft einer RESTful API ist die Verwendung von verschiedenen HTTP-Methoden, um unterschiedliche Aktionen auf den Endpunkten auszuführen. In Flask kannst du leicht festlegen, welche HTTP-Methoden von deinen Endpunkten akzeptiert werden sollen.

Hier ist ein Beispiel, das zeigt, wie du in Flask verschiedene HTTP-Methoden verwenden kannst:

```python
from flask import Flask, request

app = Flask(__name__)

@app.route('/user', methods=['GET', 'POST'])
def handle_user():
    if request.method == 'GET':
        # Logik für GET-Anfrage
        return 'Daten für Benutzer abrufen'
    elif request.method == 'POST':
        # Logik für POST-Anfrage
        return 'Neuen Benutzer erstellen'

if __name__ == '__main__':
    app.run()
```

In diesem Beispiel wird die Route `/user` definiert und festgelegt, dass sie sowohl GET- als auch POST-Anfragen akzeptiert. Je nach empfangener Methode wird die entsprechende Logik ausgeführt.

## 4.4 Datenbankintegration für die API (z. B. mit SQLAlchemy)

Für die Speicherung und Verwaltung von Daten in einer RESTful API ist oft eine Datenbankintegration erforderlich. In Flask kannst du verschiedene Datenbank-Frameworks verwenden, wie zum Beispiel SQLAlchemy, um deine Datenbankoperationen zu vereinfachen.

Eine humorvolle Erklärung dazu wäre:

Nehmen wir an, deine RESTful API ist wie ein riesiges Lagerhaus voller Daten. SQLAlchemy ist dein treuer Assistent, der dafür sorgt, dass alles organisiert und im Einklang bleibt. Egal ob du Daten hinzufügst, aktualisierst oder abrufst, SQLAlchemy kümmert sich um die schwierigen Details, damit du dich auf das Wichtige konzentrieren kannst - das Einrichten einer gemütlichen Ecke in deinem Lagerhaus, um deinen Benutzern genau das zu geben, wonach sie suchen.

Um SQLAlchemy in deine Flask-Anwendung zu integrieren, musst du zunächst die entsprechenden Module installieren und konfigurieren. Danach kannst du Modelle definieren, die deine Datenbanktabellen repräsentieren, und Datenbankoperationen durchführen.

Hier ist ein Beispiel für die Verwendung von SQLAlchemy in Flask:

```python
from flask import Flask
from flask_sqlalchemy import SQLAlchemy

app = Flask(__name__)
app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///mydatabase.db'
db = SQLAlchemy(app)

class User(db.Model):
    id = db.Column(db.Integer, primary_key=True)
    name = db.Column(db.String(50))

@app.route('/user/<int:user_id>')
def get_user(user_id):
    user = User.query.get(user_id)
    if user:
        return f'Benutzername: {user.name}'
    else:
        return 'Benutzer nicht gefunden'

if __name__ == '__main__':
    app.run()
```

In diesem Beispiel wird SQLAlchemy verwendet, um eine SQLite-Datenbank zu verwalten. Es wird ein einfaches `User`-Modell erstellt, das eine Tabelle in der Datenbank repräsentiert. Die Route `/user/<user_id>` wird definiert, um einen bestimmten Benutzer abzurufen.

## Praxis

### Leichte Aufgabe

Erstelle eine Flask-Anwendung mit einer RESTful API, die eine Route `/hello` hat und bei GET-Anfragen den Text "Hallo, API!" als Antwort zurückgibt.

Musterlösung:

```python
from flask import Flask

app = Flask(__name__)

@app.route('/hello', methods=['GET'])
def say_hello():
    return 'Hallo, API!'

if __name__ == '__main__':
    app.run()
```

### Schwerere Aufgabe

Erweitere die Flask-Anwendung, um eine Route `/user` zu erstellen, die GET-Anfragen akzeptiert und eine Liste von Benutzern aus einer Datenbank abruft. Implementiere auch eine POST-Anfrage, um einen neuen Benutzer zur Datenbank hinzuzufügen.

Musterlösung:

```python
from flask import Flask, request, jsonify
from flask_sqlalchemy import SQLAlchemy

app = Flask(__name__)
app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///mydatabase.db'
db = SQLAlchemy(app)

class User(db.Model):
    id = db.Column(db.Integer, primary_key=True)
    name = db.Column(db.String(50))

@app.route('/user', methods=['GET', 'POST'])
def handle_user():
    if request.method == 'GET':
        users = User.query.all()
        user_list = [{'id': user.id, 'name': user.name} for user in users]
        return jsonify(user_list)
    elif request.method == 'POST':
        data = request.get_json()
        new_user = User(name=data['name'])
        db.session.add(new_user)
        db.session.commit()
        return 'Benutzer erstellt'

if __name__ == '__main__':
    app.run()
```

In dieser Musterlösung wird SQLAlchemy verwendet, um Benutzerdaten in einer SQLite-Datenbank zu speichern. Die GET-Anfrage auf `/user` gibt eine Liste der vorhandenen Benutzer zurück, während die POST-Anfrage einen neuen Benutzer zur Datenbank hinzufügt.

Das waren die Abschnitte für das Python-Tutorial zur Entwicklung einer RESTful API mit Python und Flask. Viel Spaß beim Lernen und Entwickeln!