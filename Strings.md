

# Python - Strings

## Einführung
Strings sind Textwerte in Python. Sie werden von Anführungszeichen, entweder einfache (') oder doppelte (") umgeben. In diesem Tutorial werden wir uns mit den Grundlagen von Strings beschäftigen und lernen, wie man sie manipuliert.

Nach Abschluss des Tutorials wirst du in der Lage sein:
- Strings in Python zu erstellen und zu manipulieren
- Verwendung von Methoden für Strings
- Die Unterschiede zwischen verschiedenen String-Operatoren

Und falls du dich jemals gefragt hast, was Indiana Jones auf seinem Computer benutzt hat, war es bestimmt Python – denn er hatte Python-Strings immer dabei!

## Theorie

### Erstellen von Strings
Strings werden durch Anführungszeichen erstellt, die den Text einschließen. Entweder einfache (') oder doppelte ("). Hier sind ein paar Beispiele:

```python
# einfache Anführungszeichen
mein_string = 'Hallo, Welt!'
print(mein_string)

# doppelte Anführungszeichen
mein_string_2 = "Das ist ein anderer String."
print(mein_string_2)
```

### String-Konkatenation
Strings können durch den + Operator zusammengeführt werden, um eine längere Zeichenkette zu erstellen:

```python
string_1 = "Das ist der erste Teil"
string_2 = " und das ist der zweite Teil."
ergebnis_string = string_1 + string_2
print(ergebnis_string)
```

### String-Methoden
Python bietet eine Menge von Methoden an, die auf Strings angewendet werden können. Hier sind ein paar Beispiele:

```python
mein_string = "python ist super cool"

# Großschreibung
print(mein_string.upper())

# Kleinbuchstaben
print(mein_string.lower())

# Ersetzung
print(mein_string.replace("python", "java"))

# Aufspaltung
print(mein_string.split(" "))
```

### String-Indizierung und Slicing
Jeder Buchstabe in einem String hat einen Index, beginnend mit 0. Mit Indizes können wir auf bestimmte Buchstaben im String zugreifen oder Slicing verwenden, um eine Teilzeichenfolge zu extrahieren:

```python
mein_string = "Python ist fantastisch!"
print(mein_string[0])   # P
print(mein_string[6])   # i
print(mein_string[0:6]) # Python
```

## Praxis

### Aufgabe 1
Erstelle einen String und füge den Satz "Ich lerne Python" hinzu.

Musterlösung:

```python
mein_string = "Hallo, Welt!"
mein_string += " Ich lerne Python."
print(mein_string)
```

### Aufgabe 2
Erstelle einen String und gib nur jeden zweiten Buchstaben aus.

Musterlösung:

```python
mein_string = "Dies ist ein langer String."
print(mein_string[::2])
```