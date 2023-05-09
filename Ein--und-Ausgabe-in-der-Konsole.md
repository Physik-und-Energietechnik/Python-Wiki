# Python - Ein- und Ausgabe in der Konsole

## Einführung
In diesem Tutorial werden wir uns damit beschäftigen, wie man Daten in der Konsole ausgibt und wie man Daten von Benutzern in der Konsole einliest. Am Ende dieses Tutorials solltest du in der Lage sein, einfache Programme zu schreiben, die Benutzereingaben akzeptieren und Ausgaben in der Konsole anzeigen. 

## Theorie

### Ausgabe in der Konsole
Um Daten in der Konsole auszugeben, können wir die Funktion `print()` verwenden. Die Funktion `print()` gibt Daten als Text in der Konsole aus. Hier ist ein allgemeines Beispiel:

```
print("Hello World!") # Ausgabe: Hello World!
```

Dieser Code gibt den Text "Hello World!" in der Konsole aus.

Hier ist ein explizites Beispiel mit Variablen:

```python
name = "Alice"
age = 25
print("Mein Name ist", name, "und ich bin", age, "Jahre alt.") # Ausgabe: Mein Name ist Alice und ich bin 25 Jahre alt
```

Dieser Code gibt den Text "Mein Name ist Alice und ich bin 25 Jahre alt." in der Konsole aus.

### Eingabe in der Konsole
Um Daten von Benutzern in der Konsole einzulesen, können wir die Funktion `input()` verwenden. Die Funktion `input()` fordert den Benutzer auf, einen Text in der Konsole einzugeben. Der eingegebene Text wird als Zeichenkette (String) zurückgegeben. Hier ist ein Beispiel:

```python
name = input("Gib deinen Namen ein: ") # Ausgabe Gib deinen Namen ein:
print("Hallo", name) # Ausgabe: Hallo `name`
```

Dieser Code fordert den Benutzer auf, einen Namen in der Konsole einzugeben. Der eingegebene Name wird in der Variablen `name` gespeichert und dann als Teil der Ausgabe "Hallo `name`" in der Konsole angezeigt.

## Praxis
Lass uns das Gelernte in die Praxis umsetzen! Hier ist eine einfache Übung:

### Übung 1
Schreibe ein Programm, das den Benutzer nach seinem Alter fragt und dann das Jahr berechnet, in dem der Benutzer 100 Jahre alt wird. Gib das Ergebnis in der Konsole aus.

Hier ist eine mögliche Lösung:

```python
age = int(input("Wie alt bist du? ")) # Ausgabe: Wie alt bist du?
year = 2023 + 100 - age
print("Du wirst im Jahr", year, "100 Jahre alt.") # Ausgabe Du wirst im Jahr `year` 100 Jahre alt.
```
Die Aufgabe fordert den Benutzer auf, sein Alter einzugeben, um dann das Jahr zu berechnen, in dem er 100 Jahre alt wird. Dafür wird zuerst das Alter des Benutzers mit der `input()`-Funktion eingelesen und als Ganzzahl (`int`) in der Variable `age` gespeichert. Anschließend wird das Jahr berechnet, in dem der Benutzer 100 Jahre alt wird. Hierfür wird das aktuelle Jahr 2023 (als Beispieljahr) mit `100` subtrahiert und `age` addiert. Das Ergebnis wird in der Variablen `year` gespeichert. Schließlich wird die berechnete Information mit der `print()`-Funktion in der Konsole ausgegeben. 

### Übung 2
Schreibe ein Programm, das den Benutzer nach einer Zahl fragt und dann die Fakultät dieser Zahl berechnet. Gib das Ergebnis in der Konsole aus.

Hier ist eine mögliche Lösung:

```python
num = int(input("Gib eine Zahl ein: ")) # Ausgabe: Gib eine Zahl ein:
factorial = 1
for i in range(1, num+1):
    factorial *= i
print("Die Fakultät von", num, "ist", factorial) # Ausgabe: Die Fakultät von `num` ist `factorial`
```
Diese Aufgabe fordert den Benutzer auf, eine Zahl einzugeben, um dann die Fakultät dieser Zahl zu berechnen. Hierfür wird zuerst die Zahl mit der `input()`-Funktion eingelesen und als Ganzzahl in der Variable `num` gespeichert. Anschließend wird die Fakultät dieser Zahl mit einer Schleife berechnet und in der Variable `factorial` gespeichert. Das Ergebnis wird dann mit der `print()`-Funktion in der Konsole ausgegeben.
Keine Sorge, wenn du die Lösung zu Beginn noch nicht verstehst, ist das nicht schlimm, was Schleifen sind und wie die `range()`-Funktion funktioniert erklären wir dir noch später.

Falls du es dennoch jetzt verstehen möchtest, klappe einfach das nächste Dropdown Fenster auf.

# [Drop Down im Ilias dann]

Eine Schleife ist eine Kontrollstruktur in der Programmierung, mit der man eine Anweisung oder eine Gruppe von Anweisungen wiederholt ausführen kann. Schleifen sind besonders nützlich, wenn man denselben Codeblock mehrmals ausführen muss, oder wenn man eine Liste von Elementen oder eine Sammlung von Objekten durchlaufen möchte.

In Python gibt es zwei Arten von Schleifen: die `while`-Schleife und die `for`-Schleife. In der `while`-Schleife wird die Schleife solange ausgeführt, wie eine bestimmte Bedingung erfüllt ist. In der `for`-Schleife wird die Schleife für jedes Element in einer Sequenz ausgeführt.

In der zweiten Übungsaufgabe wird eine `for`-Schleife verwendet, um die Fakultät einer Zahl zu berechnen. Die `range()`-Funktion erzeugt eine Sequenz von Ganzzahlen von 1 bis zur eingegebenen Zahl `num`. Innerhalb der Schleife wird die Variable `factorial` mit jedem Durchlauf der Schleife mit dem Wert der Multiplikation von `factorial` mit dem jeweiligen Zähler der Schleife aktualisiert.

Hier ein Beispiel: Wenn der Benutzer die Zahl 5 eingibt, wird die Schleife 5-mal durchlaufen und `factorial` wird wie folgt aktualisiert:

1. In der ersten Schleifendurchlauf hat der Zähler den Wert 1. `factorial` wird mit dem Wert 1 initialisiert. Das erste Element in der Sequenz (1) wird ausgewählt und `factorial` wird mit diesem Wert multipliziert: `factorial` = 1 * 1 = 1.
2. In der zweiten Schleifendurchlauf hat der Zähler den Wert 2. Das zweite Element in der Sequenz (2) wird ausgewählt und `factorial` wird mit diesem Wert multipliziert: `factorial` = 1 * 2 = 2.
3. In der dritten Schleifendurchlauf hat der Zähler den Wert 3. Das dritte Element in der Sequenz (3) wird ausgewählt und `factorial` wird mit diesem Wert multipliziert: `factorial` = 2 * 3 = 6.
4. In der vierten Schleifendurchlauf hat der Zähler den Wert 4. Das vierte Element in der Sequenz (4) wird ausgewählt und `factorial` wird mit diesem Wert multipliziert: `factorial` = 6 * 4 = 24.
5. In der fünften Schleifendurchlauf hat der Zähler den Wert 5. Das fünfte Element in der Sequenz (5) wird ausgewählt und `factorial` wird mit diesem Wert multipliziert: `factorial` = 24 * 5 = 120.

Am Ende der Schleife hat `factorial` den Wert 120, der die Fakultät von 5 ist.

[Drop Down Ende]


Herzlichen Glückwunsch, du hast erfolgreich Ein- und Ausgabe in der Konsole gelernt!