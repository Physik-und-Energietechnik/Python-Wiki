
## Einführung

Willkommen zu unserem Python-Tutorial über gängige API-Architekturen! In diesem Tutorial werden wir einen Einblick in zwei populäre API-Architekturen, nämlich REST und GraphQL, erhalten. Keine Sorge, wenn du noch keine Erfahrung mit Python hast, wir werden alles Schritt für Schritt erklären.

Bevor wir jedoch in die Praxis eintauchen, lassen uns etwas Theorie durchgehen, um ein grundlegendes Verständnis von REST und GraphQL zu bekommen.

## Theorie

### REST (Representational State Transfer)

REST ist ein Architekturstil, der auf dem Prinzip der Zustandslosigkeit beruht. Dabei werden Ressourcen über eindeutige URIs (Uniform Resource Identifier) repräsentiert und durch HTTP-Methoden wie GET, POST, PUT und DELETE manipuliert. RESTful APIs sind weit verbreitet und werden oft verwendet, um Daten von Servern abzurufen oder zu aktualisieren.

Hier ist ein allgemeines Beispiel für die Verwendung von REST mit Python:

```python
import requests

def get_user(user_id):
    url = f"https://api.example.com/users/{user_id}"
    response = requests.get(url)
    if response.status_code == 200:
        user_data = response.json()
        print(f"Benutzername: {user_data['username']}")
    else:
        print("Fehler beim Abrufen der Benutzerdaten.")

user_id = input("Gib die Benutzer-ID ein: ")
get_user(user_id)
```

### GraphQL

GraphQL ist eine Abfragesprache und eine Laufzeitumgebung für APIs. Im Gegensatz zu REST bietet GraphQL die Möglichkeit, genau die Daten abzurufen, die du benötigst, indem du eine spezifische Abfrage sendest. Dadurch wird Overfetching vermieden, bei dem unnötige Daten abgerufen werden, und Underfetching, bei dem nicht genügend Daten abgerufen werden.

Hier ist ein allgemeines Beispiel für die Verwendung von GraphQL mit Python:

```python
import requests

def get_user(user_id):
    url = "https://api.example.com/graphql"
    query = f"""
    query {{
        user(id: {user_id}) {{
            username
            email
        }}
    }}
    """
    response = requests.post(url, json={'query': query})
    if response.status_code == 200:
        user_data = response.json()
        user = user_data['data']['user']
        print(f"Benutzername: {user['username']}")
        print(f"E-Mail: {user['email']}")
    else:
        print("Fehler beim Abrufen der Benutzerdaten.")

user_id = input("Gib die Benutzer-ID ein: ")
get_user(user_id)
```

## Praxis

Nun ist es an der Zeit, unser Wissen in die Praxis umzusetzen. Deine Aufgabe besteht darin, eine Funktion zu erstellen, die entweder REST oder GraphQL verwendet, um Informationen über Bücher abzurufen. Du kannst die API deiner Wahl verwenden und die Daten in der Konsole ausgeben.

```python
import requests

def get_book_info(book_id):
    # TODO: Verwende REST oder GraphQL, um Informationen über das Buch abzurufen
    # Gib die Buchinformationen in der Konsole aus
    pass

book_id = input("Gib die Buch-ID ein: ")
get_book

_info(book_id)
```

## Fazit

Herzlichen Glückwunsch! Du hast gerade eine Einführung in gängige API-Architekturen wie REST und GraphQL erhalten. REST bietet eine bewährte Methode zur Kommunikation mit APIs, während GraphQL eine flexible Abfragemöglichkeit bietet.

Je nach den Anforderungen deines Projekts kannst du die geeignete Architektur wählen. Jetzt bist du bereit, die spannende Welt der APIs zu erkunden und damit in deinen Projekten zu interagieren. Viel Spaß und happy coding!