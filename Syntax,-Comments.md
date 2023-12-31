## Einführung
In diesem Abschnitt werden wir uns mit der grundlegenden Syntax von Python befassen und lernen, wie man Kommentare in Python schreibt. Durch diesen Abschnitt wirst du in der Lage sein, grundlegende Python-Programme zu schreiben und zu verstehen.

## Theorie
Hier sind einige Python-Syntax-Regeln und Beispiele:

### Kommentare

Kommentare in Python beginnen mit einem Rautezeichen `#` und werden vom Interpreter ignoriert. Sie werden verwendet, um den Code zu erklären und Hinweise für andere Entwickler zu geben.

```python
# Dies ist ein Kommentar
print("Hallo Welt")  # Dies ist ein Kommentar nach einem Code
```

### Anweisungen und Zeilen

In Python wird jede Anweisung in einer eigenen Zeile geschrieben. Eine Zeile kann mehrere Anweisungen enthalten, die durch Semikolons getrennt sind, aber dies ist nicht empfohlen.

```python
print("Hallo"); print("Welt")  # funktioniert, aber nicht empfohlen

print("Hallo")
print("Welt")  # besser und lesbarer
```

### Einrückungen

Python verwendet Einrückungen, um Blöcke von Code anzuzeigen. Einrückungen sind wichtiger Bestandteil der Python-Syntax und werden verwendet, um Codeblöcke in Funktionen, Schleifen und Bedingungen zu definieren.

```python
if 5 > 2:
    print("Fünf ist größer als zwei")
```

### Variablenzuweisung

In Python werden Variablen durch Zuweisung erstellt und müssen nicht vorher deklariert werden. Der Zuweisungsoperator ist das Gleichheitszeichen `=`.

```python
x = 5
y = "Hallo"
```

### Variablen-Namen

Variablen in Python müssen mit einem Buchstaben oder Unterstrich beginnen und können Buchstaben, Zahlen und Unterstriche enthalten. Es gibt einige reservierte Schlüsselwörter, die nicht als Variablennamen verwendet werden können.

```python
# Gültige Variablen-Namen
name = "Max"
age = 28
_height = 1.85

# Ungültige Variablen-Namen
2fast = "too fast"  # beginnt mit einer Zahl
for = "foreach"  # reserviertes Schlüsselwort
my-name = "Max"  # Bindestrich ist nicht erlaubt
```

## Praxis
Nun wollen wir das erlernte Wissen in der Praxis umsetzen! 

### Aufgabe 1
Schreibe ein Python-Programm, das "Hallo Welt!" auf der Konsole ausgibt und füge einen Kommentar hinzu, der erklärt, was das Programm tut.

```python
# Ein einfaches Programm, das "Hallo Welt!" ausgibt
print("Hallo Welt!")
```

Erklärung: Dieser Python-Code ist ein einfaches Programm, das "Hallo Welt!" ausgibt. Die `print`-Funktion gibt den Text "Hallo Welt!" auf der Konsole aus. Das `#`-Zeichen markiert den Beginn eines Kommentars im Code. Kommentare dienen dazu, den Code zu dokumentieren und zu erklären. Alles, was nach dem `#`-Zeichen folgt, wird vom Python-Interpreter ignoriert und hat keinen Einfluss auf die Ausführung des Codes. In diesem Fall gibt der Kommentar an, was das Programm tut.

### Aufgabe 2
Schreibe ein Python-Programm, das den Nutzer nach seinem Namen fragt und dann eine personalisierte Begrüßung ausgibt. Füge einen Kommentar hinzu, der erklärt, was das Programm tut.

```python
# Ein Programm, das den Nutzer nach seinem Namen fragt und eine personalisierte Begrüßung ausgibt
name = input("Wie ist dein Name? ")
print("Hallo " + name + "! Willkommen in der Welt von Python!")
```

Das obige Python-Programm verwendet die `input()`-Funktion, um den Nutzer nach seinem Namen zu fragen. Der eingegebene Name wird in der Variablen `name` gespeichert. Dann wird eine personalisierte Begrüßung mit dem eingegebenen Namen ausgegeben. Die `print()`-Funktion gibt den Text "Hallo ", den eingegebenen Namen und den Text "! Willkommen in der Welt von Python!" aus. Die `+`-Operatoren werden verwendet, um die Texte miteinander zu verketten.

## Fazit 

In diesem Abschnitt haben wir die grundlegende Syntax von Python kennengelernt und gelernt, wie man Kommentare in Python schreibt. Wir haben gelernt, dass Kommentare in Python mit dem Rautezeichen `#` beginnen und vom Interpreter ignoriert werden. Sie sind nützlich, um den Code zu dokumentieren und Hinweise für andere Entwickler zu geben.

Wir haben auch gelernt, dass Python Einrückungen verwendet, um Blöcke von Code anzuzeigen, und dass Variablen in Python durch Zuweisung erstellt werden und nicht vorher deklariert werden müssen. Wir haben auch die Regeln für Variablennamen in Python besprochen.

Abschließend haben wir zwei praktische Übungen durchgeführt, um das Gelernte anzuwenden. Mit diesem Wissen sollte es dir nun möglich sein, grundlegende Python-Programme zu schreiben und zu verstehen.
 

## Links / Weiteres Material 

### [W3Schools Syntax](https://www.w3schools.com/python/python_syntax.asp)
### [W3Schools Comments](https://www.w3schools.com/python/python_comments.asp)

### [YouTube](https://www.youtube.com/watch?v=ewu4x0eXVt8)
