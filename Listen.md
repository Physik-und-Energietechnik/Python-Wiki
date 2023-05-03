

# Python - Listen

## Einführung
Herzlich Willkommen zum Tutorial über Listen in Python! Listen gehören zu den grundlegenden Datenstrukturen in Python und sind ein wichtiges Werkzeug in der Programmierung. Durch dieses Tutorial lernst du, wie man Listen erstellt, sie manipuliert und darauf zugreift. Aber bevor wir loslegen, lass uns eine wichtige Frage klären: Was sind Listen überhaupt?

Stell dir vor, du bist in der Schule und musst eine Liste von Dingen machen, die du für eine Prüfung brauchst: Stifte, Radiergummi, Lineal, Taschenrechner usw. Eine Liste ist einfach eine Sammlung von Dingen, die geordnet sind und auf die man zugreifen kann. Und genau das ist es, was eine Liste in Python ist: eine geordnete Sammlung von Elementen.

Aber warum sind Listen so wichtig? Nun, sie erlauben es uns, viele Elemente auf einmal zu speichern und darauf zuzugreifen, ohne jedes einzelne Element nennen zu müssen. Wir können sie auch dynamisch verändern, Elemente hinzufügen oder entfernen und so vieles mehr. Kurz gesagt, Listen sind ein wichtiges Werkzeug in der Programmierung und ein Must-have in deinem Python-Arsenal.

## Theorie
### Erstellung von Listen
Eine Liste in Python wird mit eckigen Klammern definiert und die einzelnen Elemente werden durch Kommas getrennt. Hier ist ein Beispiel:

```python
meine_liste = [1, 2, 3, 4, 5]
```

### Zugriff auf Listenelemente
Wir können auf Elemente in einer Liste zugreifen, indem wir den Index des Elements angeben. Der Index ist die Position des Elements in der Liste und beginnt immer mit 0. Hier ist ein Beispiel:

```python
meine_liste = [1, 2, 3, 4, 5]
print(meine_liste[0])  # gibt 1 aus
print(meine_liste[2])  # gibt 3 aus
```

### Manipulation von Listen
Wir können eine Liste auch dynamisch manipulieren, indem wir Elemente hinzufügen, entfernen oder ersetzen. Hier sind einige Beispiele:

#### Element hinzufügen
```python
meine_liste = [1, 2, 3, 4, 5]
meine_liste.append(6)
print(meine_liste)  # gibt [1, 2, 3, 4, 5, 6] aus
```

#### Element entfernen
```python
meine_liste = [1, 2, 3, 4, 5]
meine_liste.remove(3)
print(meine_liste)  # gibt [1, 2, 4, 5] aus
```

#### Element ersetzen
```python
meine_liste = [1, 2, 3, 4, 5]
meine_liste[2] = 6
print(meine_liste)  # gibt [1, 2, 6, 4, 5] aus
```

### Listenverarbeitung
Wir können auch verschiedene Operationen auf Listen anwenden, wie zum Beispiel das Sortieren oder Zählen von Elementen. Hier ist ein Beispiel:

#### Sortieren
```python
zahlen = [4, 2, 1, 3, 5]
zahlen.sort()
print(zahlen)   # Ausgabe: [1, 2, 3, 4, 5]
```
### Praxis
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

