

# Python - Variablen und Datentypen

## Einführung
Hey! Herzlich willkommen zum Python Tutorial für Anfänger:innen! In diesem Tutorial wirst du lernen, wie du in Python Variablen deklarierst und mit verschiedenen Datentypen arbeitest. Warum ist das wichtig? Nun ja, Variablen sind grundlegende Bausteine in der Programmierung. Mit ihnen kannst du Daten speichern, auf sie zugreifen und sie manipulieren. Und Datentypen definieren, welche Art von Daten du speichern kannst und wie du sie verwenden kannst. Aber genug der Theorie, lass uns anfangen!

## Theorie
### Variablen
Eine Variable in Python ist ein Speicherbereich, der einen Namen hat und in dem du Daten speichern kannst. In Python musst du keine Typen für Variablen definieren, Python erkennt den Typ automatisch. Du kannst eine Variable deklarieren, indem du einfach einen Namen für sie vergibst und ihr dann einen Wert zuweist.

```python
# Allgemeines Beispiel
x = 42
```

Hier haben wir eine Variable namens "x" deklariert und ihr den Wert 42 zugewiesen.

```python
# Spezifisches Beispiel
name = "Max"
```

In diesem Beispiel haben wir eine Variable namens "name" deklariert und ihr den Wert "Max" zugewiesen.

### Datentypen
In Python gibt es verschiedene Datentypen, die dir helfen, Daten in deinem Code zu organisieren. Die gängigsten Datentypen sind:

- Integer: Ganzzahlen (z.B. 42)
- Float: Gleitkommazahlen (z.B. 3.14)
- String: Zeichenketten (z.B. "Hallo, Welt!")
- Boolean: Wahrheitswerte (True oder False)

```python
# Allgemeine Beispiele
zahl = 42        # Integer
kommazahl = 3.14  # Float
name = "Max"     # String
ist_sonne_sichtbar = True  # Boolean
```

Hier haben wir Beispiele für jede Art von Datentyp. Du kannst den Typ jeder Variable überprüfen, indem du die Funktion "type()" verwendest.

```python
# Beispiele zur Typüberprüfung
print(type(zahl))              # Ausgabe: <class 'int'>
print(type(kommazahl))         # Ausgabe: <class 'float'>
print(type(name))              # Ausgabe: <class 'str'>
print(type(ist_sonne_sichtbar)) # Ausgabe: <class 'bool'>
```

## Aufgabe
Okay, jetzt wo du die Grundlagen von Variablen und Datentypen kennst, bist du bereit für eine kleine Aufgabe. Schreibe ein Programm, das den Benutzer nach seinem Namen, Alter und Lieblingsfarbe fragt und dann diese Informationen auf der Konsole ausgibt.

```python
# Musterlösung
name = input("Wie ist dein Name? ")
alter = input("Wie alt bist du? ")
farbe = input("Was ist deine Lieblingsfarbe? ")

print("Dein Name ist " + name + ", du bist " + alter + " Jahre alt und deine Lieblingsfarbe ist " + farbe + ".")
```

Herzlichen Glückwunsch! Du hast die erste Aufgabe erfolgreich gemeistert!