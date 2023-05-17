# Python - Lambda
## Einführung
Willkommen zu unserem Python-Tutorial über Lambdas! Wenn du dich fragst, was zum Teufel ein Lambda ist und wie es dir beim Programmieren helfen kann, dann bist du hier genau richtig. Keine Sorge, wir werden es dir in einer verständlichen und humorvollen Weise erklären.
In diesem Tutorial wirst du lernen, wie du Lambdas in Python erstellst und wie du sie in deinen eigenen Programmen einsetzen kannst. Lambdas sind eine elegante Möglichkeit, kleine anonyme Funktionen zu definieren, die oft in Verbindung mit Funktionen wie map(), filter() und reduce() verwendet werden. Sie können dir helfen, deinen Code kompakter und lesbarer zu machen.
## Theorie
### Was sind Lambdas?
Lambdas sind wie Miniatur-Versionen von Funktionen, die du "on the fly" erstellen kannst. Sie sind anonyme Funktionen, was bedeutet, dass sie keinen Namen haben. Du kannst sie direkt an der Stelle verwenden, an der du sie brauchst, ohne sie zuerst definieren zu müssen.
### Code-Beispiel: Allgemein
Um dir zu zeigen, wie Lambdas funktionieren, hier ein allgemeines Code-Beispiel:
python
add_numbers = lambda x, y: x + y
result = add_numbers(3, 5)
print(result)  # Output: 8
Hier haben wir eine Lambda-Funktion erstellt, die zwei Zahlen addiert. Das Schlüsselwort lambda zeigt an, dass es sich um eine Lambda-Funktion handelt, gefolgt von den Parametern x und y. Der Doppelpunkt : trennt die Parameter von der eigentlichen Berechnung. In diesem Fall addieren wir einfach x und y.
### Code-Beispiel: Explizit in Python
Wenn du die Lambda-Syntax nicht verwendest, könntest du dasselbe Code-Beispiel wie oben mit einer expliziten Funktion schreiben:
python
def add_numbers(x, y):
    return x + y

result = add_numbers(3, 5)
print(result)  # Output: 8
Die Lambda-Variante ist jedoch nützlich, wenn du eine Funktion benötigst, die nur an einer Stelle im Code verwendet wird und keine eigenen Namen haben muss.

## Praxis
### Leichte Aufgabe: Multipliziere Zahlen

Schreibe eine Lambda-Funktion, die zwei Zahlen multipliziert. Verwende dann die Funktion reduce(), um die Produkt aller Zahlen in einer Liste zu berechnen. Hier ist ein Musterbeispiel, um dir den Einstieg zu erleichtern:

python

from functools import reduce

numbers = [2, 3, 4, 5]
product = reduce(lambda x, y: x * y, numbers)
print(product)  # Output: 120

### Schwere Aufgabe: Sortiere Wörter nach Länge

Schreibe eine Lambda-Funktion, die die Länge eines Worts zurückgibt. Verwende dann die Funktion sorted(), um eine Liste von Wörtern nach ihrer Länge zu sortieren. Hier ist ein Musterbeispiel:

python

words = ["Python", "is", "awesome", "to", "learn"]
sorted_words = sorted(words, key=lambda word: len(word))
print(sorted_words)  # Output: ['is', 'to', 'learn', 'Python', 'awesome']

In diesem Beispiel wird die Lambda-Funktion als key-Argument an sorted() übergeben, um die Länge jedes Worts zu berechnen und die Wörter entsprechend zu sortieren.

