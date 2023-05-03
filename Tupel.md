

# Python Tutorial: Tupel

## Einführung

Tupel sind eine Art von Datenstruktur in Python, die verwendet wird, um eine Sammlung von Elementen zu speichern. Im Gegensatz zu Listen sind Tupel unveränderlich, was bedeutet, dass sie nach ihrer Erstellung nicht mehr geändert werden können. In diesem Tutorial werden wir uns ansehen, wie Tupel in Python erstellt und verwendet werden können.

Nach diesem Tutorial werden Sie wissen:
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

Wie bereits erwähnt, sind Tupel unveränderlich. Dies bedeutet, dass Sie keine Elemente hinzufügen, entfernen oder ändern können, nachdem Sie das Tupel erstellt haben. Sie können jedoch Tupel kombinieren, um neue Tupel zu erstellen:

```python
tupel_eins = (1, 2, 3)
tupel_zwei = (4, 5, 6)
tupel_drei = tupel_eins + tupel_zwei
print(tupel_drei) # Ausgabe: (1, 2, 3, 4, 5, 6)
```

## Praxis

### Aufgabe 1

Erstellen Sie ein Tupel mit Ihren Lieblingsfarben und geben Sie die zweite Farbe in der Liste aus.

```python
meine_lieblingsfarben = ("Blau", "Grün", "Rot")
print(meine_lieblingsfarben[1]) # Ausgabe: Grün
```

### Aufgabe 2

Erstellen Sie ein Tupel mit den Namen Ihrer Lieblingsfilme. Fügen Sie dann einen weiteren Film hinzu und speichern Sie das Ergebnis in einer neuen Variablen. Geben Sie die neue Variable aus.

```python
meine_lieblingsfilme = ("Star Wars", "Matrix", "Indiana Jones")
neues_tupel = meine_lieblingsfilme + ("Inception",)
print(neues_tupel) # Ausgabe: ('Star Wars', 'Matrix', 'Indiana Jones', 'Inception')
```
