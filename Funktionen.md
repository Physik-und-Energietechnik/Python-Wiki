## Einführung

Willkommen zum Python Abschnitt über Funktionen! Funktionen sind ein grundlegender Bestandteil der Programmierung und sind in jeder Sprache unerlässlich. In diesem Abschnitt lernst du, wie man Funktionen in Python definiert, aufruft und verwendet. Durch das Verständnis von Funktionen kannst du deinen Code strukturieren, wiederverwendbar machen und das Schreiben von Programmen vereinfachen.

## Theorie

Eine Funktion ist eine Gruppe von Anweisungen, die eine bestimmte Aufgabe ausführt. Funktionen werden verwendet, um Code zu strukturieren und zu organisieren, um ihn wiederverwendbar zu machen und um die Lesbarkeit und Wartbarkeit des Codes zu verbessern. Wenn du eine Funktion definierst, gibst du ihr einen Namen und fügst einen Block von Code hinzu, der ausgeführt wird, wenn die Funktion aufgerufen wird. Funktionen können Parameter akzeptieren, um Daten an die Funktion zu übergeben, und sie können Rückgabewerte zurückgeben, um Daten aus der Funktion zurückzugeben.

### Rückgabewerte

Rückgabewerte sind die Daten, die von einer Funktion zurückgegeben werden, nachdem sie ausgeführt wurde. Eine Funktion kann Null, einen einzelnen Wert oder mehrere Werte zurückgeben. Um einen Rückgabewert in Python zu definieren, verwenden wir das Schlüsselwort `return` gefolgt von dem Wert, den wir zurückgeben möchten. Wenn eine Funktion keinen Rückgabewert hat, wird das Schlüsselwort `return` ohne einen Wert verwendet.

### Aufrufen von Funktionen

Um eine Funktion in Python aufzurufen, schreibst du einfach den Namen der Funktion und fügst die Argumente (falls vorhanden) in Klammern hinzu. Hier ist ein Beispiel:

```python
def meine_funktion(name):
    print("Hallo " + name + "!")
    
meine_funktion("Max") # Ausgabe: Hallo Max!
```

In diesem Beispiel rufen wir die Funktion `meine_funktion` auf und übergeben den String "Max" als Argument. Die Funktion gibt dann "Hallo Max!" aus.

Funktionen können auch einen Rückgabewert haben, den wir in einer Variablen speichern können. Hier ist ein Beispiel:

```python
def addiere_zahlen(zahl_1, zahl_2):
    summe = zahl_1 + zahl_2
    return summe
    
ergebnis = addiere_zahlen(2, 3)
print(ergebnis) # Ausgabe: 5
```

In diesem Beispiel rufen wir die Funktion `addiere_zahlen` mit den Argumenten 2 und 3 auf und speichern das Ergebnis in der Variablen `ergebnis`. Dann geben wir das Ergebnis mit einem Print-Statement aus.

## Praxis
### Aufgabe 1

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

### Aufgabe 2

Schreibe eine Funktion `berechne_durchschnitt(werte)`, die eine Liste von Zahlen akzeptiert und den Durchschnitt zurückgibt. Hier ist ein Beispielaufruf:

```python
werte = [2, 5, 8, 11]
durchschnitt = berechne_durchschnitt(werte)
print(durchschnitt) # Ausgabe: 6.5
```

Hier ist eine Musterlösung:

```python
def berechne_durchschnitt(werte):
    summe = sum(werte)
    durchschnitt = summe / len(werte)
    return durchschnitt
``` 
## Fazit

Herzlichen Glückwunsch, du hast das Python Tutorial über Funktionen abgeschlossen! Du solltest jetzt in der Lage sein, Funktionen zu definieren und in deinem Code zu verwenden.

In diesem Tutorial hast du gelernt, wie man Funktionen in Python definiert, aufruft und verwendet. Funktionen sind ein grundlegender Bestandteil der Programmierung und helfen dabei, Code zu strukturieren, wiederverwendbar zu machen und das Schreiben von Programmen zu vereinfachen. Du hast auch gelernt, wie man Rückgabewerte definiert und wie man Funktionen mit Parametern aufruft. Am Ende hast du zwei praktische Übungen durchgeführt, um das Gelernte anzuwenden. Nun bist du in der Lage, Funktionen in Python zu definieren und in deinem Code zu verwenden.

## Links / Weiteres Material 

### [W3Schools](https://www.w3schools.com/python/python_functions.asp)

### [YouTube](https://www.youtube.com/watch?v=mgA-Ytr32Ys)