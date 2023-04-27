# Python-Schleifen: Eine Einführung

## Einführung
Herzlich willkommen zum Python-Schleifen-Tutorial für Anfänger! In diesem Tutorial werden wir lernen, wie man Schleifen in Python schreibt. Schleifen sind sehr nützlich, um wiederholte Aufgaben auszuführen, ohne dass man den Code mehrfach schreiben muss. Wenn du jemals müde davon bist, wiederholt denselben Code zu schreiben, dann bist du hier genau richtig. Lass uns loslegen und in die Welt der Schleifen eintauchen!

## Theorie
### Was sind Schleifen?
Schleifen ermöglichen es dir, eine bestimmte Anzahl von Codezeilen immer wieder auszuführen, bis eine bestimmte Bedingung erfüllt ist. Es gibt zwei Arten von Schleifen in Python: die "for-Schleife" und die "while-Schleife".

#### for-Schleife
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

#### while-Schleife
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

## Aufgabe
Jetzt, da wir wissen, wie man Schleifen in Python schreibt, lass uns eine kleine Übung machen. Schreibe eine for-Schleife, die alle geraden Zahlen von 0 bis 10 ausdruckt. Hier ist die Musterlösung:

```python
for zahl in range(0, 11, 2):
    print(zahl)
```


Ich hoffe, dieses Tutorial hat dir geholfen, Schleifen in Python zu verstehen. Schleifen sind eine wichtige Grundlage in der Programmierung und werden dir helfen, effizienten und wiederverwendbaren Code zu schreiben. Jetzt bist du bereit, Schleifen in deinen eigenen Python-Programmen zu verwenden. Viel Spaß beim Coden!