
## Einführung

Willkommen zu unserem Python-Tutorial über die Verwendung von HTTP-Methoden in einer RESTful API! In diesem Tutorial werden wir lernen, wie wir mit Python, Flask (FastAPI) und den gängigen HTTP-Methoden GET, POST, PUT und DELETE interagieren können, um eine RESTful API zu entwickeln. Keine Sorge, wenn du noch keine Erfahrung mit Python oder Flask hast, wir werden alles Schritt für Schritt erklären.

Bevor wir jedoch in die Praxis eintauchen, lassen uns etwas Theorie durchgehen, um ein grundlegendes Verständnis der RESTful-Architektur und der verschiedenen HTTP-Methoden zu bekommen.

## Theorie

REST (Representational State Transfer) ist ein Architekturstil für die Entwicklung von Webdiensten. Eine RESTful API verwendet die HTTP-Methoden, um auf Ressourcen zuzugreifen und Aktionen auf ihnen auszuführen.

Hier sind die gängigsten HTTP-Methoden und ihre Verwendung in einer RESTful API:

- **GET**: Wird verwendet, um Daten von einem Server abzurufen. Eine GET-Anfrage ist idempotent, was bedeutet, dass sie keine Änderungen auf dem Server verursachen soll.

- **POST**: Wird verwendet, um Daten an einen Server zu senden, um sie zu verarbeiten und neue Ressourcen zu erstellen.

- **PUT**: Wird verwendet, um Daten an einen Server zu senden, um eine vorhandene Ressource zu aktualisieren oder zu ersetzen.

- **DELETE**: Wird verwendet, um eine Ressource auf einem Server zu löschen.

## Praxis

Nun ist es an der Zeit, unser Wissen in die Praxis umzusetzen. Deine Aufgabe besteht darin, eine einfache RESTful API mit Python und Flask (FastAPI) zu erstellen und die verschiedenen HTTP-Methoden zu implementieren. Hier ist eine Beispiel-Aufgabe:

**Aufgabe:** Erstelle eine RESTful API mit den folgenden Endpunkten:
- `GET /users`: Gibt eine Liste aller Benutzer zurück.
- `GET /users/{id}`: Gibt die Informationen eines bestimmten Benutzers basierend auf seiner ID zurück.
- `POST /users`: Erstellt einen neuen Benutzer.
- `PUT /users/{id}`: Aktualisiert die Informationen eines bestimmten Benutzers basierend auf seiner ID.
- `DELETE /users/{id}`: Löscht einen bestimmten Benutzer basierend auf seiner ID.

**Musterlösung:**

```python
from fastapi import FastAPI

app = FastAPI()

users = []

@app.get("/users")
def get_users():
    return users

@app.get("/users/{id}")
def get_user(id: int):
    for user in users:
        if user["id"] == id:
            return user
    return {"message": "Benutzer nicht gefunden"}

@app.post("/users")
def create_user(user: dict):
    user["id"] = len(users) + 1
    users.append(user)
    return user

@app.put("/users/{id}")
def update_user(id: int, updated_user: dict):
    for user in users:
        if user["id"] == id:
            user.update(updated_user)
            return user
    return {"message": "Benutzer nicht gefunden"}

@app.delete("/users/{id}")


def delete_user(id: int):
    for user in users:
        if user["id"] == id:
            users.remove(user)
            return {"message": "Benutzer gelöscht"}
    return {"message": "Benutzer nicht gefunden"}

# Beispielaufrufe
print(get_users())  # Ausgabe: []
print(create_user({"name": "Max", "age": 25}))  # Ausgabe: {'name': 'Max', 'age': 25, 'id': 1}
print(get_users())  # Ausgabe: [{'name': 'Max', 'age': 25, 'id': 1}]
print(get_user(1))  # Ausgabe: {'name': 'Max', 'age': 25, 'id': 1}
print(update_user(1, {"age": 30}))  # Ausgabe: {'name': 'Max', 'age': 30, 'id': 1}
print(delete_user(1))  # Ausgabe: {'message': 'Benutzer gelöscht'}
print(get_users())  # Ausgabe: []

```

## Fazit

Herzlichen Glückwunsch! Du hast gerade gelernt, wie du die gängigen HTTP-Methoden (GET, POST, PUT, DELETE) in einer RESTful API mit Python und Flask (FastAPI) verwenden kannst. Dieses Wissen ist äußerst nützlich, wenn du robuste Webanwendungen entwickeln möchtest, die mit verschiedenen Ressourcen interagieren.

Denke daran, dass eine gut gestaltete RESTful API die Prinzipien von REST beachten sollte, wie die Verwendung der richtigen HTTP-Methoden für die entsprechenden Aktionen und die sinnvolle Strukturierung der Ressourcen-Endpunkte.

Jetzt bist du bereit, deine eigene RESTful API mit Python und Flask (FastAPI) zu entwickeln. Viel Spaß beim Codieren und Erstellen großartiger Webdienste!