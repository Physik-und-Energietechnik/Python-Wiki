## Einführung
Willkommen zum Abschnitt über API-Dokumentation und Testen! In diesem Tutorial lernst du, wie du API-Dokumentation erstellst und deine APIs mit Python-Bibliotheken testest. API-Dokumentation ist von entscheidender Bedeutung, um anderen Entwicklern zu zeigen, wie sie deine API nutzen können. Darüber hinaus ist das Testen von APIs ein wichtiger Schritt, um sicherzustellen, dass sie wie erwartet funktionieren.

In diesem Abschnitt werden wir uns mit dem Erstellen von API-Dokumentation mithilfe von OpenAPI/Swagger befassen. OpenAPI ist ein weit verbreitetes Framework zur Beschreibung von APIs, während Swagger ein Toolset zur Generierung von interaktiver Dokumentation aus OpenAPI-Spezifikationen ist. Wir werden auch lernen, wie wir unsere APIs mit Python-Bibliotheken wie pytest und requests testen können, um sicherzustellen, dass sie ordnungsgemäß funktionieren.

## Theorie

### 8.1 Erstellen von API-Dokumentation mit OpenAPI/Swagger
OpenAPI bietet eine standardisierte Möglichkeit, APIs zu beschreiben und zu dokumentieren. Mit OpenAPI können wir die Struktur unserer API definieren, einschließlich der verfügbaren Endpunkte, unterstützten HTTP-Methoden, Anfragedaten und Antwortformaten. Swagger wiederum ermöglicht es uns, aus den OpenAPI-Spezifikationen automatisch interaktive API-Dokumentation zu generieren.

Hier ist ein allgemeines Code-Beispiel für eine OpenAPI-Spezifikation:

```yaml
openapi: 3.0.0
info:
  title: Mein API
  version: 1.0.0
paths:
  /users:
    get:
      summary: Ruft eine Liste von Benutzern ab
      responses:
        '200':
          description: Erfolgreiche Antwort
```

Und hier ist ein explizites Code-Beispiel für die Verwendung von OpenAPI/Swagger mit Flask:

```python
from flask import Flask
from flask_swagger_ui import get_swaggerui_blueprint

app = Flask(__name__)

# OpenAPI-Spezifikation bereitstellen
@app.route("/swagger.json")
def provide_swagger_json():
    return app.send_static_file("swagger.json")

# Swagger-UI-Blueprint konfigurieren
SWAGGER_URL = "/swagger"
API_URL = "/swagger.json"
swagger_ui_blueprint = get_swaggerui_blueprint(
    SWAGGER_URL,
    API_URL,
    config={"app_name": "Mein API"}
)
app.register_blueprint(swagger_ui_blueprint, url_prefix=SWAGGER_URL)

if __name__ == "__main__":
    app.run()
```

### 8.2 Testen von APIs mit Python-Bibliotheken (z. B. pytest, requests)
Das Testen von APIs ist ein wichtiger Teil des Entwicklungsprozesses, um sicherzustellen, dass sie wie erwartet funktionieren und die gewünschten Ergebnisse liefern. In Python gibt es verschiedene Bibliotheken, die uns beim Testen von APIs unterstützen, wie z. B. pytest und requests.

Mit pytest können wir Testfälle schreiben und Assertions verwenden, um sicherzustellen, dass die API die erwarteten Antworten zurückgibt. Requests ist eine leistungsstarke Bibliothek zur Vereinfachung von HTTP-Anfragen und ermöglicht es uns, An

fragen an unsere API zu senden und die erhaltenen Antworten zu überprüfen.

Hier ist ein allgemeines Code-Beispiel für einen API-Test mit pytest und requests:

```python
import requests

def test_get_users():
    response = requests.get("https://api.example.com/users")
    assert response.status_code == 200
    assert len(response.json()) > 0

def test_create_user():
    data = {"name": "John Doe", "email": "johndoe@example.com"}
    response = requests.post("https://api.example.com/users", json=data)
    assert response.status_code == 201
    assert response.json()["name"] == "John Doe"
```

## Praxis

### Leichte Aufgabe: API-Dokumentation erstellen
Erstelle eine OpenAPI-Spezifikation für eine einfache Blog-API. Definiere die verfügbaren Endpunkte, unterstützten HTTP-Methoden und Anfrage-/Antwortformate. Verwende Swagger, um aus der Spezifikation interaktive API-Dokumentation zu generieren.

### Musterlösung - Leichte Aufgabe:
```yaml
openapi: 3.0.0
info:
  title: Blog-API
  version: 1.0.0
paths:
  /posts:
    get:
      summary: Ruft eine Liste von Blog-Posts ab
      responses:
        '200':
          description: Erfolgreiche Antwort
  /posts/{id}:
    get:
      summary: Ruft einen einzelnen Blog-Post ab
      parameters:
        - name: id
          in: path
          required: true
          description: ID des Blog-Posts
          schema:
            type: integer
      responses:
        '200':
          description: Erfolgreiche Antwort
```

### Schwere Aufgabe: API-Testen mit pytest und requests
Schreibe Testfälle für eine vorhandene API. Überprüfe, ob die API die erwarteten Antworten für verschiedene Endpunkte und Anfragen liefert. Verwende pytest und requests, um die Tests durchzuführen.

### Musterlösung - Schwere Aufgabe:
```python
import requests

def test_get_posts():
    response = requests.get("https://api.example.com/posts")
    assert response.status_code == 200
    assert len(response.json()) > 0

def test_get_single_post():
    response = requests.get("https://api.example.com/posts/1")
    assert response.status_code == 200
    assert response.json()["id"] == 1
```

Das war eine großartige Einführung in die API-Dokumentation und das Testen von APIs. Du hast gelernt, wie man API-Dokumentation mithilfe von OpenAPI/Swagger erstellt und APIs mit pytest und requests testet. Viel Spaß beim Erstellen und Testen deiner eigenen APIs!