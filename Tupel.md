## Einführung

Tupel sind eine Art von Datenstruktur in Python, die verwendet wird, um eine Sammlung von Elementen zu speichern. Im Gegensatz zu Listen sind Tupel unveränderlich, was bedeutet, dass sie nach ihrer Erstellung nicht mehr geändert werden können. In diesem Tutorial werden wir uns ansehen, wie Tupel in Python erstellt und verwendet werden können.

Nach diesem Tutorial wirst du wissen:
- Was Tupel sind und wie man sie erstellt
- Wie man auf Elemente in einem Tupel zugreift
- Wie man Tupel in Python manipuliert und verwendet

## Theorie

Ein Tupel wird in Python durch das Trennen von Elementen mit Kommas und das Umgeben der Elemente mit Klammern erstellt:

```python
mein_tupel = (1, 2, 3)
```

Tupel können auch Elemente unterschiedlicher Typen enthalten:

```python
mein_anderes_tupel = ("Hallo", 42, True)
```

### Elementzugriff

Auf Elemente in einem Tupel kann zugegriffen werden, indem der Index des Elements in eckigen Klammern nach dem Namen des Tupels angegeben wird. Beachten Sie, dass Indizes in Python bei 0 beginnen:

```python
mein_tupel = (1, 2, 3)
print(mein_tupel[0]) # Ausgabe: 1
```

### Tupelmanipulation

Wie bereits erwähnt, sind Tupel unveränderlich. Dies bedeutet, dass du keine Elemente hinzufügen, entfernen oder ändern kannst, nachdem du den Tupel erstellt hast. du kannst jedoch Tupel kombinieren, um neue Tupel zu erstellen:

```python
tupel_eins = (1, 2, 3)
tupel_zwei = (4, 5, 6)
tupel_drei = tupel_eins + tupel_zwei
print(tupel_drei) # Ausgabe: (1, 2, 3, 4, 5, 6)
```
 
### Der `tuple()` Konstruktor

Ein Tupel kann auf verschiedene Weise erstellt werden. Eine Möglichkeit besteht darin, den `tuple()` Konstruktor zu verwenden. Der `tuple()` Konstruktor erwartet als Argument eine Sequenz von Elementen (z. B. eine Liste oder einen anderen Tupel) und gibt ein neues Tupel mit den Elementen in derselben Reihenfolge zurück. Hier ist ein Beispiel:

```python
mein_tupel = tuple([1, 2, 3, 4])
print(mein_tupel) # Ausgabe: (1, 2, 3, 4)
```

In diesem Beispiel haben wir eine Liste `[1, 2, 3, 4]` als Argument an den `tuple()` Konstruktor übergeben, um ein neues Tupel zu erstellen. Das Ergebnis ist das Tupel `(1, 2, 3, 4)`.

### Länge von Tupeln

Wie bei Listen können wir auch die Länge eines Tupels mithilfe der `len()` Funktion ermitteln. Hier ist ein Beispiel:

```python
mein_tupel = (1, 2, 3, 4)
print(len(mein_tupel)) # Ausgabe: 4
```

In diesem Beispiel haben wir ein Tupel `(1, 2, 3, 4)` erstellt und dann seine Länge mit der `len()` Funktion ermittelt.

## Praxis

### Aufgabe 1

Erstelle ein Tupel mit deinen Lieblingsfarben und gebe die zweite Farbe in der Liste aus.

```python
meine_lieblingsfarben = ("Blau", "Grün", "Rot")
print(meine_lieblingsfarben[1]) # Ausgabe: Grün
```
#### Erklärung Musterlösung Aufgabe 1

In diesem Python-Code wird zunächst eine Tupel-Variable `meine_lieblingsfarben` definiert, welche die drei Elemente "Blau", "Grün" und "Rot" enthält. Anschließend wird mittels der Index-Notation `[1]` auf das zweite Element "Grün" zugegriffen und mittels `print` auf der Konsole ausgegeben. Die Ausgabe des Codes lautet daher `Grün`. 

Tupel in Python sind eine Art geordnete Sammlung von Elementen, ähnlich wie Listen. Der Unterschied zu Listen besteht darin, dass Tupel unveränderlich sind, d.h. ihre Elemente können nach der Definition nicht mehr hinzugefügt, entfernt oder geändert werden.

### Aufgabe 2

Erstelle ein Tupel mit den Namen deiner Lieblingsfilme. Füge dann einen weiteren Film hinzu und Speicher das Ergebnis in einer neuen Variablen. Geben die neue Variable aus.

```python
meine_lieblingsfilme = ("Star Wars", "Matrix", "Indiana Jones")
neues_tupel = meine_lieblingsfilme + ("Inception",)
print(neues_tupel) # Ausgabe: ('Star Wars', 'Matrix', 'Indiana Jones', 'Inception')
```
#### Erklärung Musterlösung Aufgabe 2

In diesem Python-Code wird zunächst eine Tupel-Variable `meine_lieblingsfilme` definiert, welche die drei Elemente "Star Wars", "Matrix" und "Indiana Jones" enthält. Anschließend wird ein neues Tupel `neues_tupel` durch Konkatenation von `meine_lieblingsfilme` und einem weiteren Tupel mit dem einzigen Element "Inception" erstellt. Hierbei ist zu beachten, dass das Tupel mit einem Komma am Ende definiert wird, um es als Tupel zu kennzeichnen. Das neue Tupel enthält nun vier Elemente. Schließlich wird das neue Tupel mittels `print` auf der Konsole ausgegeben, wobei die Ausgabe `('Star Wars', 'Matrix', 'Indiana Jones', 'Inception')` lautet.

In Python können Tupel mittels der `+`-Operator zusammengeführt werden. Hierbei wird ein neues Tupel erstellt, welches die Elemente beider ursprünglicher Tupel enthält. Dabei bleiben die ursprünglichen Tupel unverändert, da Tupel in Python unveränderlich sind.