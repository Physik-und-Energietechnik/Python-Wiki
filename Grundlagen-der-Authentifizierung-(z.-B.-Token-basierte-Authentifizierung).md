
## Einführung

Willkommen zu unserem Python-Tutorial über die Grundlagen der Authentifizierung! In diesem Tutorial werden wir uns damit befassen, wie wir in Python die Identität eines Benutzers überprüfen können. Authentifizierung ist ein wichtiger Aspekt der Sicherheit, der sicherstellt, dass nur autorisierte Benutzer auf geschützte Ressourcen zugreifen können.

## Theorie

Es gibt verschiedene Arten von Authentifizierungsmethoden, und eine beliebte Methode ist die tokenbasierte Authentifizierung. Bei der tokenbasierten Authentifizierung wird dem Benutzer ein Token zugewiesen, das er bei jeder Anfrage an die API vorlegen muss, um seine Identität zu bestätigen.

Hier ist ein allgemeines Code-Beispiel, das die tokenbasierte Authentifizierung veranschaulicht:

```python
import jwt

# Funktion zur Generierung eines Tokens für einen Benutzer
def generate_token(user_id: int) -> str:
    payload = {"user_id": user_id}
    secret_key = "geheimeschluessel"
    token = jwt.encode(payload, secret_key, algorithm="HS256")
    return token

# Funktion zur Überprüfung eines Tokens
def verify_token(token: str) -> bool:
    secret_key = "geheimeschluessel"
    try:
        payload = jwt.decode(token, secret_key, algorithms=["HS256"])
        user_id = payload["user_id"]
        print("Token verifiziert! Benutzer-ID:", user_id)
        return True
    except jwt.InvalidTokenError:
        print("Ungültiges Token!")
        return False
```

In diesem Beispiel verwenden wir die `jwt`-Bibliothek, um Tokens zu generieren und zu überprüfen. Die Funktion `generate_token` generiert ein Token für einen bestimmten Benutzer, indem sie die Benutzer-ID in das Token-Payload einbettet und es mit einem geheimen Schlüssel signiert. Die Funktion `verify_token` überprüft ein erhaltenes Token, entschlüsselt es und stellt sicher, dass es gültig ist.

## Praxis

Jetzt wollen wir das Gelernte in die Praxis umsetzen. Deine Aufgabe besteht darin, eine Funktion zu implementieren, die ein Token generiert und eine Funktion, die ein erhaltenes Token überprüft. Hier ist die Aufgabenstellung:

**Aufgabe 1:** Implementiere die Funktion `generate_token(user_id: int)`, die ein Token für einen Benutzer generiert. Verwende die Benutzer-ID als Teil des Token-Payloads und den geheimen Schlüssel "geheimeschluessel".

**Aufgabe 2:** Implementiere die Funktion `verify_token(token: str)`, die ein Token überprüft und den Benutzer anhand der im Token enthaltenen Informationen identifiziert. Verwende den geheimen Schlüssel "geheimeschluessel".

**Musterlösung:**

```python
import jwt

def generate_token(user_id: int) -> str:
    payload = {"user_id": user_id}
    secret_key = "geheimeschluessel"
    token = jwt.encode(payload, secret_key, algorithm="HS256")
    return token

def verify_token(token: str) -> bool:
    secret_key = "geheimeschluessel"
    try:
        payload = jwt.decode(token

, secret_key, algorithms=["HS256"])
        user_id = payload["user_id"]
        print("Token verifiziert! Benutzer-ID:", user_id)
        return True
    except jwt.InvalidTokenError:
        print("Ungültiges Token!")
        return False

# Beispielaufrufe
user_id = 123
token = generate_token(user_id)
print("Generiertes Token:", token)

verify_token(token)
```

## Fazit

Herzlichen Glückwunsch! Du hast nun die Grundlagen der tokenbasierten Authentifizierung in Python kennengelernt. Du weißt jetzt, wie man Tokens generiert und überprüft, um die Identität eines Benutzers zu authentifizieren.

Die tokenbasierte Authentifizierung ist eine flexible und sichere Methode, um Benutzeridentitäten in deinen Python-Anwendungen zu verwalten. Du kannst diese Methode nutzen, um den Zugriff auf bestimmte Ressourcen zu beschränken und sicherzustellen, dass nur autorisierte Benutzer auf sensible Daten zugreifen können.

Wir hoffen, dass du dieses Tutorial informativ und unterhaltsam fandest. Setze dein neues Wissen ein, um sicherere und geschützte Anwendungen zu entwickeln. Viel Spaß beim Programmieren!