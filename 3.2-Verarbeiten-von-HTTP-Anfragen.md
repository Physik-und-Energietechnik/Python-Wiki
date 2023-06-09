
## Einführung

Willkommen zu unserem Python-Tutorial über das Verarbeiten von HTTP-Anfragen! In diesem Tutorial lernst du, wie du mit Python HTTP-Anfragen senden und empfangen kannst. HTTP-Anfragen sind der grundlegende Mechanismus, um mit APIs und Webseiten zu interagieren. Du wirst lernen, wie du Daten von einer URL abrufen, Anfragen an APIs senden und die erhaltenen Antworten verarbeiten kannst.

## Theorie

Bevor wir in die Praxis eintauchen, werfen wir einen Blick auf die Theorie und betrachten ein allgemeines Python-Code-Beispiel. Bei der Verarbeitung von HTTP-Anfragen verwenden wir das `requests`-Modul, das uns eine einfache und benutzerfreundliche API zur Verfügung stellt.

Hier ist ein allgemeines Code-Beispiel, das die Verarbeitung von HTTP-Anfragen verdeutlicht:

```python
import requests

# Daten von einer URL abrufen
response = requests.get('https://www.example.com')
print(response.text)

# Anfrage an eine API senden
payload = {'key1': 'value1', 'key2': 'value2'}
response = requests.post('https://api.example.com', data=payload)
print(response.json())

# Verarbeitung der erhaltenen Antwort
if response.status_code == 200:
    print('Anfrage erfolgreich')
else:
    print('Fehler bei der Anfrage: {}'.format(response.status_code))
```

In diesem Beispiel verwenden wir das `requests`-Modul, um Daten von einer URL abzurufen und eine Anfrage an eine API zu senden. Wir können Daten in der Anfrage als Parameter oder im Body angeben. Die empfangene Antwort enthält Informationen wie den Statuscode und die Antwortdaten. Je nach Statuscode können wir die Anfrage als erfolgreich oder fehlerhaft behandeln.

## Praxis

Nun wollen wir das Gelernte in die Praxis umsetzen. Deine Aufgabe besteht darin, eine einfache Python-Anwendung zu erstellen, die Daten von einer öffentlichen API abruft und die erhaltenen Informationen verarbeitet. Hier ist die Aufgabenstellung:

**Aufgabe:** Verwende das `requests`-Modul, um Daten von der [JSONPlaceholder](https://jsonplaceholder.typicode.com/) API abzurufen. Rufe die Liste der Benutzer (users) ab und gib die Anzahl der Benutzer aus.

**Musterlösung:**

```python
import requests

# Daten von der API abrufen
response = requests.get('https://jsonplaceholder.typicode.com/users')
users = response.json()

# Anzahl der Benutzer ausgeben
user_count = len(users)
print('Anzahl der Benutzer: {}'.format(user_count))
```

In dieser Musterlösung verwenden wir das `requests`-Modul, um die Benutzerdaten von der JSONPlaceholder-API abzurufen. Wir verwenden die `get`-Funktion und geben die URL der API an. Die empfangenen Daten werden als JSON interpretiert und in der Variable `users` gespeichert. Anschließend zählen wir die Anzahl der Benutzer und geben sie aus.

## Fazit

Herzlichen Glückwunsch! Du hast gelernt, wie du HTTP-Anfragen mit Python verarbeiten kannst. Du kannst Daten von URLs abrufen, Anfragen an APIs senden und die empfangenen Antworten verarbeiten. Das `requests`-

Modul ist ein leistungsstarkes Werkzeug, das dir dabei hilft, mit der HTTP-Kommunikation in Python umzugehen. Nun bist du bereit, deine eigenen Anwendungen zu entwickeln und mit verschiedenen APIs zu interagieren. Viel Spaß beim Coden!