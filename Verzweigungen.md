## Einführung
In diesem Abschnitt werden wir uns mit der Logik hinter Verzweigungen und deren Anwendung in Python beschäftigen. Verzweigungen helfen uns, unseren Code dynamischer zu gestalten und Entscheidungen in Abhängigkeit von verschiedenen Bedingungen zu treffen. Am Ende des Abschnitts wirst du in der Lage sein, Python-Code zu schreiben, der automatisch Entscheidungen trifft und unterschiedliche Aktionen ausführt, abhängig von bestimmten Bedingungen.

## Theorie
Verzweigungen in Python werden mit den Schlüsselwörtern `if`, `elif` und `else` umgesetzt. Mit diesen Schlüsselwörtern können wir Entscheidungen treffen und Aktionen ausführen, je nachdem, ob bestimmte Bedingungen erfüllt sind oder nicht.

### if-Anweisung
Die `if`-Anweisung wird verwendet, um eine Aktion auszuführen, wenn eine Bedingung erfüllt ist. Wenn die Bedingung nicht erfüllt ist, wird die Aktion übersprungen. Hier ist ein allgemeines Code-Beispiel:

```python
if bedingung:
    # Aktion, wenn Bedingung erfüllt ist
```

Hier ist ein explizites Code-Beispiel:

```python
age = 18

if age >= 18:
    print("Du bist volljährig.")
```

### elif-Anweisung
Die `elif`-Anweisung wird verwendet, um eine weitere Bedingung zu prüfen, wenn die erste Bedingung nicht erfüllt ist. Wenn die Bedingung erfüllt ist, wird die zugehörige Aktion ausgeführt. Hier ist ein allgemeines Code-Beispiel:

```python
if bedingung1:
    # Aktion, wenn Bedingung 1 erfüllt ist
elif bedingung2:
    # Aktion, wenn Bedingung 2 erfüllt ist
```

Nochmal als explizites Code-Beispiel direkt in Python:

```python
age = 18

if age < 18:
    print("Du bist minderjährig.")
elif age == 18:
    print("Du bist gerade volljährig geworden.")
```

### else-Anweisung
Die `else`-Anweisung wird verwendet, um eine Aktion auszuführen, wenn keine der Bedingungen erfüllt ist. Hier ist ein Pseudocode:

```python
if bedingung1:
    # Aktion, wenn Bedingung 1 erfüllt ist
elif bedingung2:
    # Aktion, wenn Bedingung 2 erfüllt ist
else:
    # Aktion, wenn keine der Bedingungen erfüllt ist
```

In Python:

```python
age = 17
if age >= 18:
    print("Du bist volljährig.")
else:
    print("Du bist minderjährig.")
```
### match-case (nur ab Python 3.10)
Der Python `match`-Operator ist eine nützliche Erweiterung der `if-elif-else`-Verzweigung, die in Python 3.10 eingeführt wurde. Er erlaubt es, einen Wert mit verschiedenen Mustern zu vergleichen und eine Aktion auszuführen, die auf das passende Muster zutrifft. Dies kann die Lesbarkeit von Code verbessern und die Anzahl der verschachtelten Bedingungen reduzieren.

Hier ist ein Beispiel, das den `match`-Operator verwendet, um eine Funktion zu schreiben, die einen Wochentag als Parameter akzeptiert und eine Nachricht zurückgibt, die auf dem übergebenen Tag basiert:

```python
def weekday_message(weekday):
    match weekday:
        case "Montag":
            return "Guten Start in die Woche!"
        case "Dienstag":
            return "Es ist Dienstag, die Woche ist schon halb vorbei!"
        case "Mittwoch":
            return "Halbzeit! Es ist Mittwoch."
        case "Donnerstag", "Freitag":
            return "Fast Wochenende!"
        case _:
            return "Kein gültiger Wochentag eingegeben."
```

In diesem Beispiel wird der `match`-Operator verwendet, um den eingegebenen Wochentag mit verschiedenen Mustern zu vergleichen. Jedes Muster wird durch eine `case`-Anweisung definiert, gefolgt von einem Doppelpunkt und der auszuführenden Aktion. Wenn keines der Muster passt, wird das Standardmuster `_` ausgewählt und die zugehörige Aktion ausgeführt.

## Praxis
Jetzt ist es an der Zeit, dein Wissen in der Praxis anzuwenden! Hier ist eine leichte und eine schwerere Aufgabe, zu der es Musterlösungen gibt.

### Aufgabe 1
Schreibe ein kleines Programm, das den Nutzer nach seinem Namen fragt und ihm dann eine personalisierte Begrüßung ausgibt. Wenn der Nutzer den Namen "Guido" eingibt, soll das Programm einen besonderen Gruß ausgeben.

Hier ist eine mögliche Lösung:

```python
name = input("Wie ist dein Name? ")

if name == "Guido":
    print("Hey Guido, willkommen zurück!")
else:
    print("Hallo " + name + ", schön dich kennenzulernen!")
```
Erklärung: In dieser Aufgabe wird der Benutzer nach seinem Namen gefragt und speichert die eingegebene Antwort in der Variablen "name". Dann überprüft das Programm, ob der eingegebene Name "Guido" ist. Wenn ja, gibt das Programm "Hey Guido, willkommen zurück!" in der Konsole aus. Wenn der eingegebene Name jedoch nicht "Guido" ist, gibt das Programm "Hallo [eingegebener Name], schön dich kennenzulernen!" aus, wobei der eingegebene Name in die Ausgabe eingefügt wird.


### Aufgabe 2

Schreibe eine Funktion in Python, die eine Ganzzahl als Parameter erhält und den FizzBuzz-Algorithmus anwendet. Das heißt, wenn die Zahl durch 3 ohne Rest teilbar ist, geben Sie "Fizz" aus, wenn sie durch 5 teilbar ist, geben Sie "Buzz" aus und wenn sie durch 3 und 5 teilbar ist, geben Sie "FizzBuzz" aus. Wenn keine dieser Bedingungen erfüllt ist, geben Sie die Zahl selbst aus.

Musterlösung:
```python
def fizzbuzz(num):
    if num % 3 == 0 and num % 5 == 0:
        return "FizzBuzz"
    elif num % 3 == 0:
        return "Fizz"
    elif num % 5 == 0:
        return "Buzz"
    else:
        return num
```
Erklärung:

Diese Funktion verwendet Verzweigungen, um den FizzBuzz-Algorithmus anzuwenden. Zunächst wird geprüft, ob die Zahl durch 3 und 5 ohne Rest teilbar ist, indem die Modulo-Operation für beide Zahlen durchgeführt wird. Wenn dies der Fall ist, gibt die Funktion "FizzBuzz" aus. Andernfalls wird geprüft, ob die Zahl nur durch 3 teilbar ist, indem nur die Modulo-Operation für 3 durchgeführt wird. Wenn dies der Fall ist, gibt die Funktion "Fizz" aus. Andernfalls wird geprüft, ob die Zahl nur durch 5 teilbar ist, indem nur die Modulo-Operation für 5 durchgeführt wird. Wenn dies der Fall ist, gibt die Funktion "Buzz" aus. Schließlich, wenn keiner der vorherigen Fälle erfüllt ist, gibt die Funktion die ursprüngliche Zahl selbst aus.

## Fazit
Herzlichen Glückwunsch! Du hast erfolgreich Verzweigungen in Python gelernt und dein Wissen in der Praxis angewendet. Weiter so!

## Links / Weiteres Material
### W3Schools
### YouTube