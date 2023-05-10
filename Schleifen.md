## Einführung
In diesem Abschnitt werden wir lernen, wie man Schleifen in Python schreibt. Schleifen sind sehr nützlich, um wiederholte Aufgaben auszuführen, ohne dass man den Code mehrfach schreiben muss. Wenn du jemals müde davon bist, wiederholt denselben Code zu schreiben, dann bist du hier genau richtig. Lass uns loslegen und in die Welt der Schleifen eintauchen!

## Theorie
### Was sind Schleifen?
Schleifen ermöglichen es dir, eine bestimmte Anzahl von Codezeilen immer wieder auszuführen, bis eine bestimmte Bedingung erfüllt ist. Es gibt zwei Arten von Schleifen in Python: die "for-Schleife" und die "while-Schleife".

### for-Schleife
Die for-Schleife wird verwendet, wenn du eine Anzahl von Schritten ausführen möchtest, die bereits im Voraus bekannt sind. Zum Beispiel, wenn du alle Elemente in einer Liste durchgehen möchtest, kannst du eine for-Schleife verwenden. Ein allgemeines Codebeispiel für eine for-Schleife sieht so aus:

```python
for element in liste:
    # Code zum Ausführen für jedes Element in der Liste
```

Hier ist "element" eine Variable, die bei jedem Durchlauf der Schleife auf das nächste Element in der Liste gesetzt wird. Das spezifische Codebeispiel unten zeigt, wie du eine for-Schleife verwenden kannst, um alle Elemente in einer Liste auszudrucken:

```python
meine_liste = [1, 2, 3, 4, 5]

for element in meine_liste:
    print(element)
```

### while-Schleife
Die while-Schleife wird verwendet, wenn du eine Schleife ausführen möchtest, bis eine bestimmte Bedingung erfüllt ist. Ein allgemeines Codebeispiel für eine while-Schleife sieht so aus:

```python
while bedingung:
    # Code zum Ausführen, solange die Bedingung erfüllt ist
```

Hier ist "bedingung" eine Ausdrucksanweisung, die jedes Mal ausgewertet wird, wenn die Schleife durchläuft. Wenn die Bedingung "True" ergibt, wird der Code in der Schleife ausgeführt. Wenn die Bedingung "False" ergibt, wird die Schleife beendet. Das spezifische Codebeispiel unten zeigt, wie du eine while-Schleife verwenden kannst, um die Zahlen von 1 bis 5 auszudrucken:

```python
i = 1

while i <= 5:
    print(i)
    i += 1
```

### range
`range()` ist eine Python-Funktion, die eine Folge von Zahlen erzeugt. Sie wird häufig in Schleifen verwendet, um den Schleifenindex zu steuern. 

Die `range()`-Funktion kann auf verschiedene Arten aufgerufen werden. Hier sind zwei Beispiele:

```python
range(5)
```

Dieser Aufruf erzeugt eine Folge von Zahlen von 0 bis 4. Der Startwert ist standardmäßig 0 und der Schritt ist standardmäßig 1. Das heißt, die erzeugte Folge enthält alle ganzen Zahlen von 0 bis 4, aber nicht einschließlich 5.

```python
range(2, 8, 2)
```

Dieser Aufruf erzeugt eine Folge von Zahlen von 2 bis 6, in Schritten von 2. Das heißt, die erzeugte Folge enthält die Zahlen 2, 4 und 6.

In Schleifen wird `range()` oft verwendet, um die Anzahl der Iterationen zu steuern. Hier ist ein Beispiel:

```python
for i in range(5):
    print(i)
```

Dieser Code gibt die Zahlen 0 bis 4 aus. `i` nimmt in jeder Iteration der Schleife den nächsten Wert aus der von `range(5)` erzeugten Folge an.

### 'continue' und 'break'
Klar, gerne erkläre ich auch die Anweisungen `continue` und `break`.

`continue` und `break` sind Kontrollstrukturen, die in Schleifen verwendet werden, um den Programmfluss zu steuern.

Die Anweisung `continue` wird innerhalb einer Schleife verwendet, um den aktuellen Schleifendurchlauf zu überspringen und zur nächsten Iteration überzugehen. Hier ist ein Beispiel:

```python
for zahl in range(10):
    if zahl % 2 == 0:
        continue
    print(zahl)
```

Dieser Code gibt die ungeraden Zahlen von 1 bis 9 aus, indem er bei geraden Zahlen die `continue`-Anweisung verwendet, um die Ausführung der Schleife in diesem Durchlauf zu überspringen.

Die Anweisung `break` wird innerhalb einer Schleife verwendet, um die Schleife vorzeitig zu beenden. Hier ist ein Beispiel:

```python
for zahl in range(10):
    if zahl == 5:
        break
    print(zahl)
```

Dieser Code gibt die Zahlen von 0 bis 4 aus und bricht dann die Schleife ab, wenn `zahl` den Wert 5 erreicht.

## Praxis

### Aufgabe 1
Jetzt, da wir wissen, wie man Schleifen in Python schreibt, lass uns eine kleine Übung machen. Schreibe eine for-Schleife, die alle geraden Zahlen von 0 bis 10 ausdruckt. Hier ist die Musterlösung:

```python
for zahl in range(0, 11, 2):
    print(zahl)
```

### Aufgabe 2
Klar, hier ist eine etwas anspruchsvollere Aufgabe:

Schreibe eine Python-Funktion `finde_primzahlen`, die eine positive ganze Zahl als Parameter erhält und eine Liste aller Primzahlen bis zu dieser Zahl zurückgibt. Verwende eine while-Schleife, um alle Zahlen von 2 bis zur gegebenen Zahl zu überprüfen, ob sie Primzahlen sind oder nicht.

Eine Zahl ist eine Primzahl, wenn sie nur durch 1 und sich selbst teilbar ist. Hier ist ein Codebeispiel, wie man überprüft, ob eine Zahl eine Primzahl ist:

```python
def ist_primzahl(zahl):
    if zahl < 2:
        return False
    for divisor in range(2, zahl):
        if zahl % divisor == 0:
            return False
    return True
```

Diese Funktion gibt "True" zurück, wenn die gegebene Zahl eine Primzahl ist, andernfalls gibt sie "False" zurück.

Hier ist die Musterlösung für die `finde_primzahlen`-Funktion:

```python
def finde_primzahlen(obergrenze):
    primzahlen = []
    for zahl in range(2, obergrenze + 1):
        if ist_primzahl(zahl):
            primzahlen.append(zahl)
    return primzahlen
```

Diese Funktion verwendet die `ist_primzahl`-Funktion, um alle Primzahlen von 2 bis zur gegebenen Obergrenze zu finden. Die Funktion gibt eine Liste aller gefundenen Primzahlen zurück.

## Fazit
Ich hoffe, dieser Abschnnitt hat dir geholfen, Schleifen in Python zu verstehen. Schleifen sind eine wichtige Grundlage in der Programmierung und werden dir helfen, effizienten und wiederverwendbaren Code zu schreiben. Jetzt bist du bereit, Schleifen in deinen eigenen Python-Programmen zu verwenden. Viel Spaß beim Coden!

## Links / Weiteres Material
### W3Schools
### YouTube