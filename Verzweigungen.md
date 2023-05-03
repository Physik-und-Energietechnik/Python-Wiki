

# Python - Verzweigungen

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

Hier ist ein explizites Code-Beispiel direkt in Python:

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

Hier ist ein explizites Code-Beispiel direkt in Python:

```python
age = 18

if age < 18:
    print("Du bist minderjährig.")
elif age == 18:
    print("Du bist gerade volljährig geworden.")
else:
    print("Du bist volljährig.")
```

### else-Anweisung
Die `else`-Anweisung wird verwendet, um eine Aktion auszuführen, wenn keine der Bedingungen erfüllt ist. Hier ist ein allgemeines Code-Beispiel:

```python
if bedingung1:
    # Aktion, wenn Bedingung 1 erfüllt ist
elif bedingung2:
    # Aktion, wenn Bedingung 2 erfüllt ist
else:
    # Aktion, wenn keine der Bedingungen erfüllt ist
```

Hier ist ein explizites Code-Beispiel direkt in Python:

```python
age = 17

if age >= 18:
    print("Du bist volljährig.")
else:
    print("Du bist minderjährig.")
```

## Praxis
Jetzt ist es an der Zeit, dein Wissen in der Praxis anzuwenden! Hier ist eine leichte Aufgabe, zu der es eine Musterlösung gibt, und eine schwerere Aufgabe, zu der es ebenfalls eine Musterlösung gibt.

### Leichte Aufgabe
Schreibe ein kleines Programm, das den Nutzer nach seinem Namen fragt und ihm dann eine personalisierte Begrüßung ausgibt. Wenn der Nutzer den Namen "Guido" eingibt, soll das Programm einen besonderen Gruß ausgeben.

Hier ist eine mögliche Lösung:

```python
name = input("Wie ist dein Name? ")

if name == "Guido":
    print("Hey Guido, willkommen zurück!")
else:
    print("Hallo " + name + ", schön dich kennenzulernen!")
```

### Schwerere Aufgabe
Schreibe ein Programm, das eine Zahlenfolge vom Nutzer entgegennimmt und dann die größte Zahl ausgibt. Das Programm sollte auch eine Fehlermeldung ausgeben, wenn der Nutzer eine ungültige Eingabe macht (z.B. einen Buchstaben statt einer Zahl eingibt).

Hier ist eine mögliche Lösung:

```python
numbers = input("Gib eine Liste von Zahlen ein, getrennt durch Leerzeichen: ")

numbers_list = numbers.split()

# Überprüfen, ob die Eingabe gültig ist
for number in numbers_list:
    if not number.isdigit():
        print("Ungültige Eingabe: " + number + " ist keine Zahl.")
        exit()

# Die größte Zahl in der Liste finden
max_number = int(numbers_list[0])
for number in numbers_list:
    if int(number) > max_number:
        max_number = int(number)

print("Die größte Zahl in der Liste ist: " + str(max_number))
```

Herzlichen Glückwunsch! Du hast erfolgreich Verzweigungen in Python gelernt und dein Wissen in der Praxis angewendet. Weiter so!