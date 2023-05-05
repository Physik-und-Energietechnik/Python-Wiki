# Python - Ein- und Ausgabe in der Konsole

## Einführung
In diesem Tutorial werden wir uns damit beschäftigen, wie man Daten in der Konsole ausgibt und wie man Daten von Benutzern in der Konsole einliest. Am Ende dieses Tutorials solltest du in der Lage sein, einfache Programme zu schreiben, die Benutzereingaben akzeptieren und Ausgaben in der Konsole anzeigen. 

## Theorie

### Ausgabe in der Konsole
Um Daten in der Konsole auszugeben, können wir die Funktion `print()` verwenden. Die Funktion `print()` gibt Daten als Text in der Konsole aus. Hier ist ein allgemeines Beispiel:

```
print("Hello World!")
```

Dieser Code gibt den Text "Hello World!" in der Konsole aus.

Hier ist ein explizites Beispiel mit Variablen:

```python
name = "Alice"
age = 25
print("Mein Name ist", name, "und ich bin", age, "Jahre alt.")
```

Dieser Code gibt den Text "Mein Name ist Alice und ich bin 25 Jahre alt." in der Konsole aus.

### Eingabe in der Konsole
Um Daten von Benutzern in der Konsole einzulesen, können wir die Funktion `input()` verwenden. Die Funktion `input()` fordert den Benutzer auf, einen Text in der Konsole einzugeben. Der eingegebene Text wird als Zeichenkette (String) zurückgegeben. Hier ist ein Beispiel:

```python
name = input("Gib deinen Namen ein: ")
print("Hallo", name)
```

Dieser Code fordert den Benutzer auf, einen Namen in der Konsole einzugeben. Der eingegebene Name wird in der Variablen `name` gespeichert und dann als Teil der Ausgabe "Hallo `name`" in der Konsole angezeigt.

## Praxis
Lass uns das Gelernte in die Praxis umsetzen! Hier ist eine einfache Übung:

### Übung 1
Schreibe ein Programm, das den Benutzer nach seinem Alter fragt und dann das Jahr berechnet, in dem der Benutzer 100 Jahre alt wird. Gib das Ergebnis in der Konsole aus.

Hier ist eine mögliche Lösung:

```python
age = int(input("Wie alt bist du? "))
year = 2023 + 100 - age
print("Du wirst im Jahr", year, "100 Jahre alt.")
```
Die Aufgabe fordert den Benutzer auf, sein Alter einzugeben, um dann das Jahr zu berechnen, in dem er 100 Jahre alt wird. Dafür wird zuerst das Alter des Benutzers mit der `input()`-Funktion eingelesen und als Ganzzahl (`int`) in der Variable `age` gespeichert. Anschließend wird das Jahr berechnet, in dem der Benutzer 100 Jahre alt wird. Hierfür wird das aktuelle Jahr 2023 (als Beispieljahr) mit 100 subtrahiert und das Alter des Benutzers addiert. Das Ergebnis wird in der Variablen `year` gespeichert. Schließlich wird die berechnete Information mit der `print()`-Funktion in der Konsole ausgegeben. 

In der zweiten Übungsaufgabe wird der Benutzer aufgefordert, eine Zahl einzugeben, um dann die Fakultät dieser Zahl zu berechnen. Hierfür wird zuerst die Zahl mit der `input()`-Funktion eingelesen und als Ganzzahl in der Variable `num` gespeichert. Anschließend wird die Fakultät dieser Zahl mit einer Schleife berechnet und in der Variable `factorial` gespeichert. Das Ergebnis wird dann mit der `print()`-Funktion in der Konsole ausgegeben.

Ich hoffe, das hilft dir weiter!

### Übung 2
Schreibe ein Programm, das den Benutzer nach einer Zahl fragt und dann die Fakultät dieser Zahl berechnet. Gib das Ergebnis in der Konsole aus.

Hier ist eine mögliche Lösung:

```python
num = int(input("Gib eine Zahl ein: "))
factorial = 1
for i in range(1, num+1):
    factorial *= i
print("Die Fakultät von", num, "ist", factorial)
```

Herzlichen Glückwunsch, du hast erfolgreich Ein- und Ausgabe in der Konsole gelernt!