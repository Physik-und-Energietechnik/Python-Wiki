

# Python - Listen

## Einführung
Herzlich Willkommen zum Tutorial über Listen in Python! Listen gehören zu den grundlegenden Datenstrukturen in Python und sind ein wichtiges Werkzeug in der Programmierung. Durch dieses Tutorial lernst du, wie man Listen erstellt, sie manipuliert und darauf zugreift. Aber bevor wir loslegen, lass uns eine wichtige Frage klären: Was sind Listen überhaupt?

Stell dir vor, du bist in der Schule und musst eine Liste von Dingen machen, die du für eine Prüfung brauchst: Stifte, Radiergummi, Lineal, Taschenrechner usw. Eine Liste ist einfach eine Sammlung von Dingen, die geordnet sind und auf die man zugreifen kann. Und genau das ist es, was eine Liste in Python ist: eine geordnete Sammlung von Elementen.

Aber warum sind Listen so wichtig? Nun, sie erlauben es uns, viele Elemente auf einmal zu speichern und darauf zuzugreifen, ohne jedes einzelne Element nennen zu müssen. Wir können sie auch dynamisch verändern, Elemente hinzufügen oder entfernen und so vieles mehr. Kurz gesagt, Listen sind ein wichtiges Werkzeug in der Programmierung und ein Must-have in deinem Python-Arsenal.

## Theorie

Hier sind die grundlegenden Operationen einer Liste in Python:

### Erstellung einer Liste
Du kannst eine Liste in Python erstellen, indem du die Elemente in eckigen Klammern `[]` mit einem Komma getrennt einfügst.

```python
meine_liste = ["Apfel", "Birne", "Kirsche"]
```

### Zugriff auf Elemente in einer Liste
Du kannst auf jedes Element in der Liste zugreifen, indem du den Index des Elements verwendest. Beachte, dass in Python die Indizierung bei 0 beginnt.

```python
meine_liste = ["Apfel", "Birne", "Kirsche"]
print(meine_liste[0]) # Ausgabe: "Apfel"
```

### Ändern eines Elements in einer Liste
Du kannst ein Element in der Liste ändern, indem du auf das Element zugreifst und es überschreibst.

```python
meine_liste = ["Apfel", "Birne", "Kirsche"]
meine_liste[1] = "Orange"
print(meine_liste) # Ausgabe: ["Apfel", "Orange", "Kirsche"]
```

### Hinzufügen eines Elements zu einer Liste
Du kannst ein Element am Ende der Liste hinzufügen, indem du die `append()`-Methode verwendest.

```python
meine_liste = ["Apfel", "Birne", "Kirsche"]
meine_liste.append("Pfirsich")
print(meine_liste) # Ausgabe: ["Apfel", "Birne", "Kirsche", "Pfirsich"]
```

### Entfernen eines Elements aus einer Liste
Du kannst ein Element aus der Liste entfernen, indem du die `remove()`-Methode verwendest und den Wert des Elements übergibst.

```python
meine_liste = ["Apfel", "Birne", "Kirsche"]
meine_liste.remove("Kirsche")
print(meine_liste) # Ausgabe: ["Apfel", "Birne"]
```

### Entfernen und Rückgabe eines Elements aus einer Liste
Du kannst ein Element aus der Liste entfernen und gleichzeitig zurückgeben, indem du die `pop()`-Methode verwendest und den Index des Elements übergibst.

```python
meine_liste = ["Apfel", "Birne", "Kirsche"]
entferntes_element = meine_liste.pop(1)
print(entferntes_element) # Ausgabe: "Birne"
print(meine_liste) # Ausgabe: ["Apfel", "Kirsche"]
```

### Einfügen eines Elements an einer bestimmten Stelle
Du kannst ein Element an einer bestimmten Position in der Liste einfügen, indem du die `insert()`-Methode verwendest und den Index der Position und den Wert des Elements übergibst.

```python
meine_liste = ["Apfel", "Birne", "Kirsche"]
meine_liste.insert(1, "Orange")
print(meine_liste) # Ausgabe: ["Apfel", "Orange", "Birne", "Kirsche"]
```

###Länge einer Liste
Du kannst die Anzahl der Elemente in der Liste mit der `len()`-Funktion ermitteln.

```python
meine_liste = ["Apfel", "Birne", "Kirsche"]
print(len(meine_liste)) # Ausgabe: 3
```

###Sortieren einer Liste
Du kannst eine Liste in aufsteigender Reihenfolge mit der `sort()`-Methode sortieren.

```python
meine_liste = [3, 1, 4, 1, 5, 9, 2, 6, 5]
meine_liste.sort()
print(meine_liste) # Ausgabe: [1, 1, 2, 3, 4, 5, 5, 6, 9]
```

### Umkehren einer Liste
Du kannst die Reihenfolge der Elemente in der Liste umkehren, indem du die `reverse()`-Methode verwendest.

```python
meine_liste = ["Apfel", "Birne", "Kirsche"]
meine_liste.reverse()
print(meine_liste) # Ausgabe: ["Kirsche", "Birne", "Apfel"]
```

### Überprüfen, ob ein Element in einer Liste vorhanden ist
Du kannst prüfen, ob ein bestimmtes Element in der Liste vorhanden ist, indem du den `in`-Operator verwendest.

```python
meine_liste = ["Apfel", "Birne", "Kirsche"]
print("Apfel" in meine_liste) # Ausgabe: True
print("Pfirsich" in meine_liste) # Ausgabe: False
```

## Praxis
Nun, da du die Theorie kennst, ist es Zeit für die Praxis! Hier sind zwei Übungen für dich, um dein neues Wissen zu testen.

#### Übung 1 - Leicht
Erstelle eine Liste mit deinen Lieblingsfarben und gib sie auf der Konsole aus.

Musterlösung:

```python
lieblingsfarben = ["Rot", "Grün", "Blau"]
print(lieblingsfarben)
```

#### Übung 2 - Schwer
Erstelle ein Programm, das eine Liste mit Zahlen erstellt, die durch 3 teilbar sind, aber nicht durch 2. Die Liste soll 10 Elemente enthalten und auf der Konsole ausgegeben werden.

Musterlösung:

```python
meine_liste = []
i = 1
while len(meine_liste) < 10:
    if i % 3 == 0 and i % 2 != 0:
        meine_liste.append(i)
    i += 1
print(meine_liste)
```

Herzlichen Glückwunsch, du hast es geschafft! Du hast nun ein grundlegendes Verständnis für Listen in Python und wie man sie erstellt, manipuliert und darauf zugreift. Listen sind ein wichtiger Bestandteil der Programmierung und es gibt noch viel mehr zu entdecken. Viel Spaß beim Weiterlernen!

