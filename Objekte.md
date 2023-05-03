

# Python - Objekte

## Einführung

Objekte sind die Grundlage von Python. Alles in Python ist ein Objekt, von einfachen Datentypen wie Zahlen und Strings bis hin zu komplexen Datenstrukturen wie Listen und Dictionaries. Wenn du also Python lernen möchtest, solltest du dich mit Objekten vertraut machen.

In diesem Tutorial wirst du lernen, was Objekte sind, wie man sie erstellt und manipuliert und wie sie in Python verwendet werden können. Am Ende dieses Tutorials solltest du in der Lage sein, eigene Objekte zu erstellen und in deinem Code einzusetzen.

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

Hier wird eine Klasse "Person" definiert, die zwei Attribute hat: "name" und "alter". Das Attribut "name" ist vom Typ String und das Attribut "alter" ist vom Typ Integer.

### Objekte manipulieren

Um ein Objekt zu manipulieren, kann man auf die Attribute und Methoden der Klasse zugreifen. Hier ist ein Beispiel, das zeigt, wie man das Attribut "name" einer Person ändert:

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

In diesem Beispiel wird eine Methode "geburtstag_feiern" definiert, die das Alter einer Person um eins erhöht und eine Nachricht ausgibt, die den Namen und das neue Alter enthält.

### Vererbung

Eine der nützlichsten Funktionen von Klassen in Python ist die Vererbung. Vererbung ermöglicht es, eine Klasse zu erstellen, die von einer anderen Klasse abgeleitet ist und alle Attribute und Methoden der Basisklasse erbt. Hier ist ein Beispiel, das zeigt, wie man eine abgeleitete Klasse erstellt:

```python
class Student(Person):
    def __init__(self, name, alter, matrikelnummer):
        super().__init__(name, alter)
        self.matrikelnummer = matrikelnummer
```

In diesem Beispiel wird eine Klasse "Student" definiert, die von der Klasse "Person" abgeleitet ist. Die Klasse "Student" hat ein zusätzliches Attribut "matrikelnummer". Der Konstruktor der Klasse "Student" ruft den Konstruktor der Basisklasse "Person" auf, um die Attribute "name" und "alter" zu initialisieren.

## Praxis

### Aufgabe 1

Erstelle eine Klasse "Auto", die folgende Attribute hat:

- Hersteller (String)
- Modell (String)
- Baujahr (Integer)
- Farbe (String)

Erstelle anschließend ein Objekt der Klasse "Auto" mit den folgenden Werten:

- Hersteller: "BMW"
- Modell: "X5"
- Baujahr: 2021
- Farbe: "Blau"

### Lösung 1

```python
class Auto:
    def __init__(self, hersteller, modell, baujahr, farbe):
        self.hersteller = hersteller
        self.modell = modell
        self.baujahr = baujahr
        self.farbe = farbe

auto = Auto("BMW", "X5", 2021, "Blau")
```

### Aufgabe 2

Erstelle eine abgeleitete Klasse "Elektroauto", die von der Klasse "Auto" abgeleitet ist und ein zusätzliches Attribut "reichweite" (Integer) hat. Definiere auch eine Methode "laden", die die Reichweite des Elektroautos um einen bestimmten Betrag erhöht.

Erstelle anschließend ein Objekt der Klasse "Elektroauto" mit den folgenden Werten:

- Hersteller: "Tesla"
- Modell: "Model S"
- Baujahr: 2022
- Farbe: "Rot"
- Reichweite: 500

Rufe dann die Methode "laden" auf, um die Reichweite um 100 zu erhöhen.

### Lösung 2

```python
class Elektroauto(Auto):
    def __init__(self, hersteller, modell, baujahr, farbe, reichweite):
        super().__init__(hersteller, modell, baujahr, farbe)
        self.reichweite = reichweite

    def laden(self, betrag):
        self.reichweite += betrag

elektroauto = Elektroauto("Tesla", "Model S", 2022, "Rot", 500)
elektroauto.laden(100)
print(elektroauto.reichweite)  # Ausgabe: 600
``` 