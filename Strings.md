## Einführung
Strings sind Textwerte in Python. Sie werden von Anführungszeichen, entweder einfachen (') oder doppelten (") umgeben. In diesem Tutorial werden wir uns mit den Grundlagen von Strings beschäftigen und lernen, wie man sie manipuliert.

Nach Abschluss des Tutorials wirst du in der Lage sein:
- Strings in Python zu erstellen und zu manipulieren
- Verwendung von Methoden für Strings
- Die Unterschiede zwischen verschiedenen String-Operatoren

Und falls du dich jemals gefragt hast, was Indiana Jones auf seinem Computer benutzt hat, war es bestimmt Python – denn er hatte Python-Strings immer dabei!

## Theorie

### Erstellen von Strings
Strings werden durch Anführungszeichen erstellt, die den Text einschließen. Entweder einfachen (') oder doppelten ("). Hier sind ein paar Beispiele:

```python
# einfache Anführungszeichen
mein_string = 'Hallo, Welt!'
print(mein_string)  # Hallo, Welt!

# doppelte Anführungszeichen
mein_string_2 = "Das ist ein anderer String."
print(mein_string_2)  # Das ist ein anderer String.
```

### String-Konkatenation
Strings können durch den + Operator zusammengeführt werden, um eine längere Zeichenkette zu erstellen:

```python
string_1 = "Das ist der erste Teil"
string_2 = " und das ist der zweite Teil."
ergebnis_string = string_1 + string_2
print(ergebnis_string)  # Das ist der erste Teil und das ist der zweite Teil.
```

### Länge von Strings
Die Länge eines Strings kann mit der Funktion `len()` bestimmt werden:

```python
mein_string = "Hallo, Welt!"
print(len(mein_string))  # 12
```

### String-Methoden
Python bietet eine Vielzahl von Methoden an, die auf Strings angewendet werden können. Hier sind ein paar Beispiele:

#### `strip()`
Die Methode `strip()` entfernt Leerzeichen am Anfang und Ende eines Strings:

```python
mein_string = "   Hallo, Welt!   "
print(mein_string.strip())  # Hallo, Welt!
```

#### `replace()`
Die Methode `replace()` ersetzt einen Teil eines Strings durch einen anderen Teil:

```python
mein_string = "python ist super cool"
print(mein_string.replace("python", "java"))  # java ist super cool
```

#### `format()`
Die Methode `format()` kann verwendet werden, um Variablen in einen String einzufügen:

```python
name = "Max"
alter = 30
print("Mein Name ist {} und ich bin {} Jahre alt.".format(name, alter))  # Mein Name ist Max und ich bin 30 Jahre alt.
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

## Fazit

In diesem Tutorial haben wir uns mit den Grundlagen von Strings in Python beschäftigt und gelernt, wie man sie erstellt, manipuliert und auf sie zugreift. Wir haben auch verschiedene Methoden für Strings kennengelernt, wie z.B. `strip()`, `replace()` und `format()`. Durch Übungen wie das Erstellen eines Strings und das Ausgeben jedes zweiten Buchstabens haben wir das Gelernte in die Praxis umgesetzt. Nun bist du in der Lage, Strings in Python zu erstellen und zu manipulieren und die verschiedenen Methoden und Operatoren, die dafür zur Verfügung stehen, zu nutzen.

## Links / Weiteres Material 

### [W3Schools](https://www.w3schools.com/python/python_strings.asp)

### [YouTube](https://www.youtube.com/watch?v=sTEf4_mrLvw)