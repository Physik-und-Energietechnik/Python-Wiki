# Python Tutorial - Syntax, Comments

## Einführung
In diesem Tutorial werden wir uns mit der grundlegenden Syntax von Python befassen und lernen, wie man Kommentare in Python schreibt. Durch dieses Tutorial wirst du in der Lage sein, grundlegende Python-Programme zu schreiben und zu verstehen.

## Theorie
### Python-Syntax
Python-Syntax bezieht sich auf die Regeln, die bestimmen, wie ein gültiges Python-Programm geschrieben wird. Hier sind einige wichtige Syntax-Regeln in Python:

#### Einrückungen
In Python wird Code-Blöcke nicht durch Klammern oder Schlüsselwörter wie "begin" und "end" begrenzt, sondern durch Einrückungen. Die Einrückungen müssen einheitlich sein, um Fehler im Code zu vermeiden. 

```python
# Ein Beispiel für korrekte Einrückungen:
if 5 > 2:
  print("Fünf ist größer als zwei")
else:
  print("Das kann nicht sein")
```

#### Kommentare
Kommentare sind Textteile im Code, die nicht ausgeführt werden, sondern dem Leser des Codes helfen sollen, diesen zu verstehen. In Python werden Kommentare mit dem `#`-Zeichen eingeleitet. Alles, was nach diesem Zeichen steht, wird von Python ignoriert.

```python
# Das ist ein Kommentar in Python
print("Dieser Code wird ausgeführt") # Das ist ein Kommentar in Python, der dem Code folgt
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
