
## Einführung

Willkommen zu unserem Python-Tutorial über das Testen von APIs mit Python-Bibliotheken! In diesem Tutorial lernst du, wie du deine Python-APIs effektiv testen kannst, um sicherzustellen, dass sie korrekt funktionieren und die erwarteten Ergebnisse liefern. Wir werden die Python-Bibliotheken pytest und requests verwenden, um unsere API-Tests durchzuführen.

## Theorie

Bevor wir mit der praktischen Umsetzung beginnen, wollen wir kurz die Theorie betrachten und ein allgemeines Python-Code-Beispiel anschauen. Die Bibliothek pytest bietet eine einfache und effektive Möglichkeit, Tests für deine Python-Codebasis zu schreiben. Die Bibliothek requests ermöglicht es uns, HTTP-Anfragen an unsere APIs zu senden und die erhaltenen Antworten zu überprüfen.

Hier ist ein allgemeines Code-Beispiel, das die Verwendung von pytest und requests demonstriert:

```python
import requests

def test_get_books():
    response = requests.get('https://api.example.com/books')
    assert response.status_code == 200
    assert len(response.json()) > 0

def test_add_book():
    book = {'title': 'Python Testing 101', 'author': 'Jane Doe'}
    response = requests.post('https://api.example.com/books', json=book)
    assert response.status_code == 201
    assert response.json()['message'] == 'Book added successfully'
```

In diesem Beispiel haben wir zwei Testfälle definiert. Der erste Testfall überprüft, ob wir eine erfolgreiche Antwort erhalten, wenn wir eine GET-Anfrage an den `/books`-Endpunkt senden, und ob die Antwort eine Liste von Büchern enthält. Der zweite Testfall überprüft, ob wir eine erfolgreiche Antwort erhalten, wenn wir eine POST-Anfrage mit einem Buch an den `/books`-Endpunkt senden, und ob die Antwort die erwartete Erfolgsmeldung enthält.

## Praxis

Jetzt wollen wir das Gelernte in die Praxis umsetzen. Deine Aufgabe besteht darin, API-Tests für eine vorhandene Python-API zu schreiben. Hier ist die Aufgabenstellung:

**Aufgabe:** Schreibe API-Tests für eine vorhandene Python-API. Die API enthält einen Endpunkt `/users`, der Informationen über Benutzer zurückgibt. Du solltest mindestens zwei Testfälle schreiben: einen Testfall, der überprüft, ob eine erfolgreiche Antwort erhalten wird, wenn eine GET-Anfrage an den `/users`-Endpunkt gesendet wird, und einen Testfall, der überprüft, ob eine erfolgreiche Antwort erhalten wird, wenn eine POST-Anfrage mit Benutzerdaten an den `/users`-Endpunkt gesendet wird.

**Musterlösung:**

```python
import requests

def test_get_users():
    response = requests.get('https://api.example.com/users')
    assert response.status_code == 200
    assert len(response.json()) > 0

def test_add_user():
    user = {'name': 'John Doe', 'email': 'john.doe@example.com'}
    response = requests.post('https://api.example.com/users', json=user)
    assert response.status_code == 201
    assert response.json()['message'] == 'User added successfully'
```

In diesem Beispiel haben wir zwei Testfälle geschrieben. Der erste Testfall überprüft, ob wir eine erfolgreiche Antwort erhalten

, wenn wir eine GET-Anfrage an den `/users`-Endpunkt senden, und ob die Antwort eine Liste von Benutzern enthält. Der zweite Testfall überprüft, ob wir eine erfolgreiche Antwort erhalten, wenn wir eine POST-Anfrage mit Benutzerdaten an den `/users`-Endpunkt senden, und ob die Antwort die erwartete Erfolgsmeldung enthält.

## Fazit

Herzlichen Glückwunsch! Du hast gelernt, wie du APIs mit Python-Bibliotheken wie pytest und requests testen kannst. Durch das Testen deiner APIs kannst du sicherstellen, dass sie korrekt funktionieren und die erwarteten Ergebnisse liefern. Das Testen ist ein wichtiger Schritt, um qualitativ hochwertige und zuverlässige APIs zu entwickeln.

Wir hoffen, dass dir dieses Tutorial geholfen hat und dass du nun bereit bist, deine eigenen API-Tests zu schreiben. Viel Spaß beim Testen deiner APIs und beim Erstellen robuster Python-Anwendungen!