
## Einführung

Willkommen zu unserem Python-Tutorial über Datenvalidierung und Deserialisierung von JSON! In diesem Tutorial lernst du, wie du mit Python JSON-Daten validieren und in Python-Objekte umwandeln kannst. Die Validierung und Deserialisierung von JSON ist ein wichtiger Schritt, um sicherzustellen, dass die empfangenen Daten korrekt sind und erfolgreich verarbeitet werden können.

## Theorie

Bevor wir mit der Praxis beginnen, werfen wir einen Blick auf die Theorie und schauen uns ein allgemeines Code-Beispiel an. JSON steht für "JavaScript Object Notation" und ist ein gängiges Datenformat zum Speichern und Übertragen von strukturierten Daten. In Python können wir JSON-Daten mithilfe des `json`-Moduls verarbeiten.

Hier ist ein allgemeines Code-Beispiel, das die Validierung und Deserialisierung von JSON verdeutlicht:

```python
import json

# JSON-Daten
json_data = '''
{
    "name": "John Doe",
    "age": 30,
    "email": "john.doe@example.com"
}
'''

# Deserialisierung von JSON zu einem Python-Objekt
data = json.loads(json_data)

# Datenvalidierung
if "name" in data and "age" in data and "email" in data:
    print("Daten sind gültig!")
    name = data["name"]
    age = data["age"]
    email = data["email"]
    print("Name:", name)
    print("Alter:", age)
    print("E-Mail:", email)
else:
    print("Daten sind ungültig!")
```

In diesem Beispiel verwenden wir die `json.loads()`-Funktion, um die JSON-Daten in ein Python-Objekt umzuwandeln. Anschließend überprüfen wir, ob die erforderlichen Schlüssel in den Daten vorhanden sind, um ihre Gültigkeit zu bestätigen. Wenn die Daten gültig sind, greifen wir auf die Werte der Schlüssel zu und geben sie aus.

## Praxis

Jetzt wollen wir das Gelernte in die Praxis umsetzen. Deine Aufgabe besteht darin, eine Funktion zu implementieren, die JSON-Daten validiert und die erforderlichen Informationen extrahiert. Hier ist die Aufgabenstellung:

**Aufgabe:** Implementiere die Funktion `validate_json(json_data: str) -> dict`, die JSON-Daten validiert und die Werte der Schlüssel `"name"`, `"age"` und `"email"` zurückgibt, falls die Daten gültig sind. Andernfalls gib den Wert `None` zurück.

**Musterlösung:**

```python
import json

def validate_json(json_data: str) -> dict:
    data = json.loads(json_data)
    
    if "name" in data and "age" in data and "email" in data:
        name = data["name"]
        age = data["age"]
        email = data["email"]
        return {"name": name, "age": age, "email": email}
    else:
        return None

# Beispielaufruf
json_data = '''
{
    "name": "John Doe",
    "age": 30,
    "email": "john.doe@example.com"
}
'''

result = validate_json(json_data)
if result is not None:
    print("Daten sind gültig!")
    print("Name:", result["name"])
    print("Alter:",

 result["age"])
    print("E-Mail:", result["email"])
else:
    print("Daten sind ungültig!")
```

In dieser Musterlösung haben wir die Funktion `validate_json()` implementiert. Sie validiert die JSON-Daten und gibt ein Wörterbuch mit den Schlüssel-Wert-Paaren von `"name"`, `"age"` und `"email"` zurück, wenn die Daten gültig sind. Andernfalls wird `None` zurückgegeben.

## Fazit

Herzlichen Glückwunsch! Du hast nun gelernt, wie du JSON-Daten validieren und deserialisieren kannst. Dies ist ein wichtiger Schritt, um sicherzustellen, dass die empfangenen Daten korrekt sind und erfolgreich verarbeitet werden können.

Die Validierung und Deserialisierung von JSON-Daten ist in Python dank des `json`-Moduls einfach und effektiv. Du kannst dieses Wissen nutzen, um JSON-Daten in Python-Anwendungen zu verarbeiten, z. B. beim Arbeiten mit APIs oder beim Lesen von JSON-Dateien.

Wir hoffen, dass du dieses Tutorial informativ und unterhaltsam fandest. Nutze dein neues Wissen, um mit JSON-Daten zu experimentieren und eigene Anwendungen zu entwickeln. Viel Spaß beim Programmieren!