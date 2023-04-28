

# Python Tutorial - Funktionen

## Einführung

Willkommen zum Python Tutorial über Funktionen! Funktionen sind ein grundlegender Bestandteil der Programmierung und sind in jeder Sprache unerlässlich. In diesem Tutorial lernst du, wie man Funktionen in Python definiert, aufruft und verwendet. Durch das Verständnis von Funktionen kannst du deinen Code strukturieren, wiederverwendbar machen und das Schreiben von Programmen vereinfachen.

## Theorie

Eine Funktion ist eine Gruppe von Anweisungen, die eine bestimmte Aufgabe ausführt. Funktionen werden verwendet, um Code zu strukturieren und zu organisieren, um ihn wiederverwendbar zu machen und um die Lesbarkeit und Wartbarkeit des Codes zu verbessern. Wenn du eine Funktion definierst, gibst du ihr einen Namen und fügst einen Block von Code hinzu, der ausgeführt wird, wenn die Funktion aufgerufen wird. Funktionen können Parameter akzeptieren, um Daten an die Funktion zu übergeben, und sie können Rückgabewerte zurückgeben, um Daten aus der Funktion zurückzugeben.

Um eine Funktion in Python zu definieren, verwenden wir das Schlüsselwort `def` gefolgt von dem Funktionsnamen und den Parameterklammern. Hier ist ein allgemeines Beispiel:

```python
def meine_funktion():
    print("Hallo Welt!")
```

In diesem Beispiel definieren wir die Funktion `meine_funktion`, die einfach nur "Hallo Welt!" ausgibt, wenn sie aufgerufen wird.

Funktionen können auch Parameter akzeptieren, die als Eingabe für die Funktion dienen. Hier ist ein Beispiel, das eine Funktion definiert, die zwei Zahlen addiert:

```python
def addiere_zahlen(zahl_1, zahl_2):
    summe = zahl_1 + zahl_2
    return summe
```

In diesem Beispiel haben wir die Parameter `zahl_1` und `zahl_2` definiert und dann die Summe berechnet und zurückgegeben.

## Aufgabe

Schreibe eine Funktion `berechne_mehrwertsteuer(preis, steuersatz)`, die den Preis eines Artikels und den Steuersatz akzeptiert und den Preis inklusive Mehrwertsteuer zurückgibt. Hier ist ein Beispielaufruf:

```python
preis_ohne_mwst = 100
steuersatz = 19 # 19%
preis_mit_mwst = berechne_mehrwertsteuer(preis_ohne_mwst, steuersatz)
print(preis_mit_mwst) # Ausgabe: 119.0
```

Hinweis: Der Steuersatz wird in Prozent angegeben. Um den Steuersatz in einen Faktor umzuwandeln, musst du ihn durch 100 dividieren und eins addieren. Zum Beispiel entspricht ein Steuersatz von 19% einem Faktor von 1,19.

Hier ist eine Musterlösung:

```python
def berechne_mehrwertsteuer(preis, steuersatz):
    faktor = steuersatz / 100 + 1
    preis_mit_mwst = preis * faktor
    return preis_mit_mwst
``` 

Herzlichen Glückwunsch, du hast das Python Tutorial über Funktionen abgeschlossen! Du solltest jetzt in der Lage sein, Funktionen zu definieren und in deinem Code zu verwenden.