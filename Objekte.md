

## Einführung

Objekte sind die Grundlage von Python. Alles in Python ist ein Objekt, von einfachen Datentypen wie Zahlen und Strings bis hin zu komplexen Datenstrukturen wie Listen und Dictionaries. Wenn du also Python lernen möchtest, solltest du dich mit Objekten vertraut machen.

In diesem Abschnitt wirst du lernen, was Objekte sind, wie man sie erstellt und manipuliert und wie sie in Python verwendet werden können. Am Ende dieses Abschnitts solltest du in der Lage sein, eigene Objekte zu erstellen und in deinem Code einzusetzen.

## Theorie

### Objekte erstellen

In Python werden Objekte erstellt, indem man eine sogenannte "Klasse" definiert. Eine Klasse ist eine Art Bauplan für ein Objekt. Sie definiert, welche Attribute ein Objekt hat und welche Methoden es ausführen kann.

Ein einfaches Beispiel für eine Klasse wäre eine Klasse für eine Person:

```python
class Person:
    def __init__(self, name, alter):
        self.name = name
        self.alter = alter
```

Hier wird eine Klasse `Person` definiert, die zwei Attribute hat: `name` und `alter`. Das Attribut `name` ist vom Typ String und das Attribut `alter` ist vom Typ Integer.Um nun ein Objekt der Klasse `Person` zu erstellen müssen den Konstruktor, also die `__init__()`funktion,  aufrufen. Diese wird als Name der Klasse geschrieben.
```python
person = Person("Daniel",24)
```

### Objekte manipulieren

Um ein Objekt zu manipulieren, kann man auf die Attribute und Methoden der Klasse zugreifen. Hier ist ein Beispiel, das zeigt, wie man das Attribut `name` einer Person ändert:

```python
person = Person("Max", 30)
person.name = "Moritz"
print(person.name)  # Ausgabe: Moritz
```

### Methoden definieren

In einer Klasse können auch Methoden definiert werden. Eine Methode ist eine Funktion, die auf ein Objekt angewendet werden kann. Hier ist ein Beispiel, das zeigt, wie man eine Methode in einer Klasse definiert:

```python
class Person:
    def __init__(self, name, alter):
        self.name = name
        self.alter = alter

    def geburtstag_feiern(self):
        self.alter += 1
        print(f"{self.name} feiert seinen {self.alter}. Geburtstag!")
```

In diesem Beispiel wird eine Methode `geburtstag_feiern()` definiert, die das Alter einer Person um eins erhöht und eine Nachricht ausgibt, die den Namen und das neue Alter enthält.

## Praxis

### Aufgabe 1

Erstelle eine Klasse `Auto`, die folgende Attribute hat:

- `Hersteller` (String)
- `Modell` (String)
- `Baujahr` (Integer)
- `Farbe` (String)

Erstelle anschließend ein Objekt der Klasse `Auto` mit den folgenden Werten:

- Hersteller: `BMW`
- Modell: `X5`
- Baujahr: `2021`
- Farbe: `Blau`

### Lösung 2

```python
class Auto:
    def __init__(self, hersteller, modell, baujahr, farbe):
        self.hersteller = hersteller
        self.modell = modell
        self.baujahr = baujahr
        self.farbe = farbe

auto = Auto("BMW", "X5", 2021, "Blau")
```