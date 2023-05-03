# Python Tutorial: Variablen, Datentypen und Casting

## Einführung
Hey du, willkommen zum Python-Tutorial für Anfänger! In diesem Abschnitt geht es darum, wie man Variablen in Python benutzt und wie man die verschiedenen Datentypen verwendet. Das Ziel dieses Tutorials ist es, dass du die Grundlagen von Variablen und Datentypen in Python verstehst und lernst, wie man zwischen verschiedenen Datentypen umwandelt. Mit diesem Wissen wirst du in der Lage sein, komplexe Probleme zu lösen und deine eigenen Programme zu schreiben!

## Theorie

### Variablen
Variablen sind einfach Behälter, in denen du Werte speichern kannst. Stell dir eine Schublade vor, in der du Dinge aufbewahren kannst. In Python kannst du Variablen auf diese Weise definieren:

```python
name = "Max"
age = 30
```

Hier haben wir zwei Variablen definiert. Eine namens `name` und eine andere namens `age`. Wir haben den Wert `"Max"` der Variable `name` zugewiesen und den Wert `30` der Variable `age`. Beachte, dass wir hier Anführungszeichen für den `name` verwendet haben, da es sich um einen String handelt, während wir für `age` keine Anführungszeichen verwendet haben, da es sich um eine Ganzzahl handelt.

### Datentypen
Es gibt verschiedene Datentypen in Python. Hier sind einige der häufigsten:

* Strings: Text in Anführungszeichen, z.B. `"Hallo Welt"`
* Ganzzahlen: z.B. `42`
* Gleitkommazahlen: z.B. `3.14`
* Boolesche Werte: `True` oder `False`

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

```

Die type()-Funktion ist in Python eine integrierte Funktion, die den Datentyp einer Variable zurückgibt. Sie kann auf alle Variablen angewendet werden, um ihren Datentyp zu überprüfen.

Hier ist ein Beispiel:

python

name = "Max"
age = 30

print(type(name)) # Output: <class 'str'>
print(type(age))  # Output: <class 'int'>

In diesem Beispiel gibt die type()-Funktion den Datentyp des Strings "Max" und der Ganzzahl 30 zurück. Der Datentyp eines Strings ist in Python str und der Datentyp einer Ganzzahl ist int.

Die type()-Funktion kann auch nützlich sein, wenn du den Datentyp einer Variable nicht kennst und ihn überprüfen möchtest.

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

### Aufgabe 2
Erstelle eine Variable `number` und weise ihr den Wert `5` als Ganzzahl zu. Natürlich, hier ist der Text als normaler Text und der Python-Code als Codeblock:

Erstelle eine Variable number und weise ihr den Wert 5 als Ganzzahl zu. Erstelle dann eine Variable text und weise ihr den Wert "10" als String zu. Führe dann die folgenden Schritte aus:

1. Wandle die Variable number in eine Gleitkommazahl um und weise sie der Variable number_float zu.
2. Wandle die Variable text in eine Ganzzahl um und weise sie der Variable text_int zu.
3. Multipliziere die Variable number_float mit der Variable text_int und weise das Ergebnis der Variable result zu.
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