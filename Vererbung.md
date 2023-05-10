## Einführung
In diesem Abschnitt werden wir uns mit einem wichtigen Konzept der objektorientierten Programmierung befassen: der Vererbung. Wenn du bisher noch keine Erfahrung mit Python hast, keine Sorge! Wir werden alles Schritt für Schritt erklären und sicherstellen, dass du die Konzepte verstehst.

Die Vererbung ermöglicht es uns, bestehenden Code wiederzuverwenden und unsere Klassen hierarchisch zu organisieren. Du wirst lernen, wie man neue Klassen erstellt, die Eigenschaften und Methoden einer bereits vorhandenen Klasse erben und diese nach Bedarf erweitern oder anpassen können.

Am Ende dieses Abschnitt wirst du in der Lage sein, Vererbung in Python zu verstehen und anzuwenden. Du wirst sehen, wie nützlich dieses Konzept ist, um deinen Code strukturierter und effizienter zu gestalten.

## Theorie
Was ist Vererbung?
Vererbung ist ein Konzept der objektorientierten Programmierung, bei dem eine Klasse die Eigenschaften und Methoden einer anderen Klasse übernimmt. Die Klasse, von der geerbt wird, wird als Elternklasse oder Basisklasse bezeichnet, während die Klasse, die erbt, als Kindklasse oder abgeleitete Klasse bezeichnet wird.

Die Kindklasse erbt alle Attribute und Methoden der Elternklasse und kann diese entweder direkt verwenden oder sie bei Bedarf überschreiben oder erweitern.

Hier ist ein allgemeines Beispiel, um das Konzept der Vererbung zu verdeutlichen:

```python
# Allgemeines Beispiel für Vererbung

# Elternklasse
class Fahrzeug:
    def __init__(self, marke):
        self.marke = marke

    def beschleunigen(self):
        print("Das Fahrzeug beschleunigt.")

# Kindklasse erbt von Fahrzeug
class Auto(Fahrzeug):
    def __init__(self, marke, modell):
        super().__init__(marke)
        self.modell = modell

    def beschleunigen(self):
        print("Das Auto beschleunigt schnell.")

# Instanz der Kindklasse erstellen
mein_auto = Auto("Toyota", "Corolla")
mein_auto.beschleunigen()
```
In diesem Beispiel haben wir eine Elternklasse namens `Fahrzeug` und eine Kindklasse namens `Auto`. Das Auto erbt die `beschleunigen()`-Methode von der Fahrzeugklasse, aber überschreibt sie, um "Das Auto beschleunigt schnell." auszugeben. Die `__init__()`-Methode der Elternklasse wird auch durch `super().__init__()` aufgerufen, um die Marke zu initialisieren.

Code-Beispiel
Schauen wir uns nun ein spezifisches Beispiel an, um die Vererbung in Python besser zu verstehen:

```python
# Spezifisches Beispiel für Vererbung

# Elternklasse
class Tier:
    def __init__(self, name):
        self.name = name

    def laut_machen(self):
        print("Ein Tier macht ein Geräusch.")

# Kindklasse erbt von Tier
class Hund(Tier):
    def __init__(self, name, rasse):
        super().init(name)
        self.rasse = rasse

    def laut_machen(self):
        print("Der Hund bellt: Wuff!")

#Instanz der Kindklasse erstellen
mein_hund = Hund("Bello", "Dackel")
mein_hund.laut_machen()    #Der Hund bellt: Wuff!
```


In diesem Beispiel haben wir eine Elternklasse namens `Tier` und eine Kindklasse namens `Hund`. Der Hund erbt die `laut_machen()`-Methode von der Tierklasse, überschreibt sie jedoch, um "Der Hund bellt: Wuff!" auszugeben. Die `__init__()`-Methode der Elternklasse wird durch `super().__init__()` aufgerufen, um den Namen des Hundes zu initialisieren.

## Praxis

Jetzt ist es an der Zeit, dein Wissen in der Praxis anzuwenden! Wir haben zwei Aufgaben für dich vorbereitet: eine leichte und eine schwerere.

### Aufgabe 1

Erstelle eine neue Kindklasse namens `Katze`, die von der Elternklasse `Tier` erbt. Die Katze soll eine Methode namens `laut_machen()` haben, die "Die Katze miaut: Miau!" ausgibt.

Lösung:

```python
# Leichte Aufgabe - Musterlösung

# Kindklasse Katze
class Katze(Tier):
    def laut_machen(self):
        print("Die Katze miaut: Miau!")

# Instanz der Kindklasse erstellen
meine_katze = Katze("Minka")
meine_katze.laut_machen()
```
## Aufgabe 2
Erstelle eine neue Kindklasse namens `Student`, die von einer Elternklasse `Person` erbt. Die Elternklasse `Person` soll eine Methode namens `vorstellen()` haben, die den Namen der Person ausgibt. Die Kindklasse `Student` soll zusätzlich zur `vorstellen()`-Methode eine Eigenschaft namens `studienfach` haben, die den Namen des Studienfachs des Studenten speichert.

Lösung:

```python
# Elternklasse Person
class Person:
    def __init__(self, name):
        self.name = name

    def vorstellen(self):
        print("Hallo, ich bin", self.name)

# Kindklasse Student
class Student(Person):
    def __init__(self, name, studienfach):
        super().__init__(name)
        self.studienfach = studienfach

# Instanz der Kindklasse erstellen
mein_student = Student("Max Mustermann", "Informatik")
mein_student.vorstellen()
print("Ich studiere", mein_student.studienfach)
```