# Python Tutorial - Sets

## Einführung
In diesem Tutorial geht es um eine Datenstruktur namens Set in Python. Ein Set ist eine Sammlung von einzigartigen Elementen, die in keiner bestimmten Reihenfolge gespeichert werden. Mit Sets können Sie schnell Duplikate aus einer Liste entfernen und mathematische Operationen wie Vereinigung, Schnitt und Differenz durchführen.

## Theorie
### Erstellen eines Sets
Sie können ein Set erstellen, indem Sie geschweifte Klammern {} verwenden oder die set() Funktion aufrufen. Hier ist ein Beispiel:

```python
# Verwenden von geschweiften Klammern
my_set = {1, 2, 3, 4, 5}

# Verwenden von set()
my_set = set([1, 2, 3, 4, 5])
```

### Hinzufügen und Entfernen von Elementen
Sie können ein Element zu einem Set hinzufügen, indem Sie die add() Methode verwenden und ein Element aus einem Set entfernen, indem Sie die remove() Methode verwenden. Hier sind Beispiele:

```python
my_set = {1, 2, 3, 4, 5}
my_set.add(6) # Hinzufügen von 6 zum Set
my_set.remove(3) # Entfernen von 3 aus dem Set
```

### Vereinigung, Schnitt und Differenz von Sets
Sie können Sets mathematisch kombinieren, indem Sie die union(), intersection() und difference() Methoden verwenden. Hier sind Beispiele:

```python
set1 = {1, 2, 3}
set2 = {2, 3, 4}

# Vereinigung von set1 und set2
set3 = set1.union(set2)
# Ergebnis: {1, 2, 3, 4}

# Schnitt von set1 und set2
set4 = set1.intersection(set2)
# Ergebnis: {2, 3}

# Differenz von set1 und set2
set5 = set1.difference(set2)
# Ergebnis: {1}
```

## Praxis
### Leichte Aufgabe
Schreiben Sie eine Funktion, die eine Liste von Zahlen entgegennimmt und ein Set zurückgibt, das nur die einzigartigen Zahlen aus der Liste enthält.

```python
def unique_numbers(numbers):
    return set(numbers)
```

### Schwere Aufgabe
Schreiben Sie eine Funktion, die zwei Sets entgegennimmt und ein neues Set zurückgibt, das nur Elemente enthält, die in beiden Sets vorkommen.

```python
def common_elements(set1, set2):
    return set1.intersection(set2)
```