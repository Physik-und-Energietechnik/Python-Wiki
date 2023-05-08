# Python Tutorial - Syntax, Comments

## Einführung
In diesem Tutorial werden wir uns mit der grundlegenden Syntax von Python befassen und lernen, wie man Kommentare in Python schreibt. Durch dieses Tutorial wirst du in der Lage sein, grundlegende Python-Programme zu schreiben und zu verstehen.

## Theorie
Klar, hier sind einige Python-Syntax-Regeln und Beispiele:

### Grundlagen der Syntax

#### Kommentare

Kommentare in Python beginnen mit einem Rautezeichen `#` und werden vom Interpreter ignoriert. Sie werden verwendet, um den Code zu erklären und Hinweise für andere Entwickler zu geben.

```python
# Dies ist ein Kommentar
print("Hallo Welt")  # Dies ist ein Kommentar nach einem Code
```

#### Anweisungen und Zeilen

In Python wird jede Anweisung in einer eigenen Zeile geschrieben. Eine Zeile kann mehrere Anweisungen enthalten, die durch Semikolons getrennt sind, aber dies ist nicht empfohlen.

```python
print("Hallo"); print("Welt")  # funktioniert, aber nicht empfohlen

print("Hallo")
print("Welt")  # besser und lesbarer
```

#### Einrückungen

Python verwendet Einrückungen, um Blöcke von Code anzuzeigen. Einrückungen sind wichtiger Bestandteil der Python-Syntax und werden verwendet, um Codeblöcke in Funktionen, Schleifen und Bedingungen zu definieren.

```python
if 5 > 2:
    print("Fünf ist größer als zwei")
```

#### Variablenzuweisung

In Python werden Variablen durch Zuweisung erstellt und müssen nicht vorher deklariert werden. Der Zuweisungsoperator ist das Gleichheitszeichen `=`.

```python
x = 5
y = "Hallo"
```

#### Variablen-Namen

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

### Praxis
Nun wollen wir das erlernte Wissen in der Praxis umsetzen! 

#### Aufgabe 1
Schreibe ein Python-Programm, das "Hallo Welt!" auf der Konsole ausgibt und füge einen Kommentar hinzu, der erklärt, was das Programm tut.

```python
# Ein einfaches Programm, das "Hallo Welt!" ausgibt
print("Hallo Welt!")
```

#### Aufgabe 2
Schreibe ein Python-Programm, das den Nutzer nach seinem Namen fragt und dann eine personalisierte Begrüßung ausgibt. Füge einen Kommentar hinzu, der erklärt, was das Programm tut.

```python
# Ein Programm, das den Nutzer nach seinem Namen fragt und eine personalisierte Begrüßung ausgibt
name = input("Wie ist dein Name? ")
print("Hallo " + name + "! Willkommen in der Welt von Python!")
```
