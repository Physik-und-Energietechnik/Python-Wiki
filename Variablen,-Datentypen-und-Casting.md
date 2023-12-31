## Einführung
In diesem Abschnitt geht es darum, wie man Variablen in Python benutzt und wie man die verschiedenen Datentypen verwendet. Das Ziel dieses Abschnitts ist es, dass du die Grundlagen von Variablen und Datentypen in Python verstehst und lernst, wie man zwischen verschiedenen Datentypen umwandelt.

## Theorie

### Variablen
Variablen sind einfach Behälter, in denen du Werte speichern kannst. Stell dir eine Schublade vor, in der du Dinge aufbewahren kannst. In Python sind Variablen case-sensitive, was bedeutet, dass Variablennamen, die sich in ihrer Groß- und Kleinschreibung unterscheiden, als unterschiedliche Variablen betrachtet werden.

Zum Beispiel sind die Variablen "name" und "Name" in Python zwei verschiedene Variablen, die unterschiedliche Werte speichern können. Das bedeutet, dass du beim Benennen von Variablen darauf achten musst, dass du die Groß- und Kleinschreibung richtig verwendest. In Python kannst du Variablen auf diese Weise definieren:

```python
name = "Max"
Name = "Lisa"
age = 30
Age = 25
print(name) # Output: Max
print(Name) # Output: Lisa
```

Hier haben wir zwei Variablen definiert. Eine namens `name` und eine andere namens `age`. Wir haben den Wert `"Max"` der Variable `name` zugewiesen und den Wert `30` der Variable `age`. Beachte, dass wir hier Anführungszeichen für den `name` verwendet haben, da es sich um einen String handelt, während wir für `age` keine Anführungszeichen verwendet haben, da es sich um eine Ganzzahl handelt. Beachte auch, dass die Variablen "name" und "Name" unterschiedliche Werte haben und dass die Groß- und Kleinschreibung in den print-Anweisungen beibehalten wird.

### Datentypen
Es gibt verschiedene Datentypen in Python. Hier sind einige der häufigsten:

* Strings: Text in Anführungszeichen, z.B. `"Hallo Welt"`
* Ganzzahlen: z.B. `42`
* Gleitkommazahlen: z.B. `3.14`
* Boolesche Werte: `True` oder `False`
* Komplexe Zahlen: z.B. `2 + 3j`

Python erkennt den Datentyp automatisch, wenn du eine Variable erstellst. Du kannst den Datentyp einer Variable auch explizit überprüfen, indem du die `type()`-Funktion verwendest:

```python

name = "Max"            # String
print(type(name))       # Output: <class 'str'>

age = 30                # Ganzzahl
print(type(age))        # Output: <class 'int'>

height = 1.80           # Gleitkommazahl
print(type(height))     # Output: <class 'float'>

is_student = True       # Boolescher Wert
print(type(is_student)) # Output: <class 'bool'>

c = 2 + 3j              # Komplexe Zahl
print(type(c))          # Output: <class 'complex'>
```

Die `type()`-Funktion ist in Python eine integrierte Funktion, die den Datentyp einer Variable zurückgibt. Sie kann auf alle Variablen angewendet werden, um ihren Datentyp zu überprüfen.
Die `type()`-Funktion kann auch nützlich sein, wenn du den Datentyp einer Variable nicht kennst und ihn überprüfen möchtest.

### Casting
Manchmal musst du den Datentyp einer Variablen ändern. Das nennt man Casting. Hier sind ein paar Beispiele:

```python
# Ganzzahl zu Gleitkommazahl
x = 1
float_x = float(x)

# Gleitkommazahl zu Ganzzahl
y = 3.14
int_y = int(y)

# String zu Ganzzahl
z = "42"
int_z = int(z)
```

Beachte, dass du möglicherweise eine Fehlermeldung erhältst, wenn du versuchst, einen ungültigen Cast durchzuführen, z.B. wenn du versuchst, einen String in eine Gleitkommazahl umzuwandeln, der keinen numerischen Wert enthält.

## Praxis
### Aufgabe 1
Erstelle eine Variable `name` und weise ihr deinen eigenen Namen als String zu. Erstelle dann eine Variable `age` und weise ihr dein Alter als Ganzzahl zu. Schließlich erstelle eine Variable `height` und weise ihr deine Größe als Gleitkommazahl zu.

```python
# Musterlösung
name = "Lisa"
age = 25
height = 1.65
```

Der gegebene Code definiert drei Variablen in Python: `name`, `age` und `height`. Die erste Variable `name` ist ein String, der den Wert `Lisa` enthält. Die zweite Variable `age` ist eine ganze Zahl (Integer), die den Wert 25 enthält. Die dritte Variable `height` ist eine Fließkommazahl (Float), die den Wert `1.65` enthält und die Höhe von Lisa in Metern darstellt.

### Aufgabe 2
Erstelle eine Variable `number` und weise ihr den Wert `5` als Ganzzahl zu. Erstelle dann eine Variable `text` und weise ihr den Wert `"10"` als String zu. Führe dann die folgenden Schritte aus:

1. Wandle die Variable `number` in eine Gleitkommazahl um und weise sie der Variable `number_float` zu.
2. Wandle die Variable `text` in eine Ganzzahl um und weise sie der Variable `text_int` zu.
3. Multipliziere die Variable `number_float` mit der Variable `text_int` und weise das Ergebnis der Variable `result` zu.
4. Gib das Ergebnis aus.

```python
# Musterlösung
number = 5
text = "10"

number_float = float(number)
text_int = int(text)
result = number_float * text_int
print(result) # Output: 50.0
```

Der gegebene Code definiert drei Variablen in Python: `number`, `text` und `result`. Die `number` hat den Wert `5`, was eine Ganzzahl (Integer) darstellt. Die Variable `text` hat den Wert `"10"`, was ein String ist, der eine Zahl in Zeichenkette darstellt.
Der Code führt dann zwei Umwandlungen durch. Zuerst wird der Wert der Variablen `number` in eine Fließkommazahl (Float) umgewandelt und der resultierende Wert wird der Variablen `number_float` zugewiesen. Dann wird der Wert der Variablen `text` in eine Ganzzahl (Integer) umgewandelt und der resultierende Wert wird der Variablen `text_int` zugewiesen. Der Code multipliziert dann die beiden umgewandelten Werte `number_float` und `text_int` und speichert das Ergebnis in der Variablen `result`.Schließlich wird das Ergebnis mithilfe der `print()`-Funktion auf der Konsole ausgegeben. Der Output zeigt das Ergebnis der Multiplikation, das `50.0` beträgt.

## Fazit
In diesem Abschnitt wurden die Grundlagen von Variablen und Datentypen in Python behandelt. Du hast gelernt, wie man Variablen definiert und zwischen verschiedenen Datentypen umwandelt. Darüber hinaus wurden die verschiedenen Datentypen in Python vorgestellt und erklärt, wie man ihren Datentyp überprüfen kann. Casting, also das Ändern des Datentyps einer Variable, wurde ebenfalls behandelt. Diese grundlegenden Konzepte sind sehr wichtig, um Python effektiv zu nutzen und zu verstehen.

## Links / Weiteres Material

* https://www.w3schools.com/python/python_variables.asp
* https://www.w3schools.com/python/python_datatypes.asp
* https://www.w3schools.com/python/python_numbers.asp
* https://www.w3schools.com/python/python_casting.asp