1.0 Lambda

1.1	Einführung

In Python ist Lambda ein Schlüsselwort, das zur Erstellung anonymer Funktionen verwendet wird. Eine anonyme Funktion ist eine Funktion, die keinen Namen hat und normalerweise nur einmal verwendet wird.
Ein Lambda Ausdruck hat die folgende Syntax:
lambda arguments: expression
Hierbei sind arguments die Eingabevariablen der Funktion und expression ist der Ausdruck, der ausgeführt wird, wenn die Funktion aufgerufen wird. Der Rückgabewert wird implizit zurückgegeben.
Lambda Funktionen werden häufig als Argumente an höherwertige Funktionen (wie map, filter und reduce) übergeben, die eine Funktion als Argument akzeptieren. Diese Funktionen können auf eine einfache und elegante Weise verwendet werden, um Listen, Tupel, Dictionaries und andere Datenstrukturen zu verarbeiten.

1.2	Theorie

Lambda Funktionen sind in Situationen nützlich, in denen eine kleine Funktion benötigt wird, die nur einmal verwendet wird und keinen aussagekräftigen Namen benötigt. Hier sind einige Situationen, in denen Lambda Funktionen besonders nützlich sein können:
1.	Filtern von Daten: Wenn wir eine Liste oder eine andere Datenstruktur haben und nur bestimmte Elemente davon behalten möchten, können wir filter() verwenden und eine Lambda Funktion als Filterkriterium angeben.
2.	Zuweisen von Funktionen als Argumente: Wenn wir eine Funktion als Argument an eine andere Funktion übergeben müssen, können wir eine Lambda Funktion anstelle einer vollständigen Funktion definieren, um eine kürzere und einfachere Syntax zu erhalten.
3.	Erstellen von anonymen Funktionen: Wenn wir eine kleine, einmalige Funktion benötigen, können wir eine Lambda Funktion anstelle einer benannten Funktion erstellen, um den Code kompakter zu gestalten.
4.	Sortieren von Daten: Wenn wir eine Liste oder eine andere Datenstruktur haben und diese nach einem bestimmten Kriterium sortieren müssen, können wir sorted() oder sort() verwenden und eine lambda Funktion als Schlüssel angeben.
Es ist jedoch wichtig zu beachten, dass lambda Funktionen nicht für alle Situationen geeignet sind. Insbesondere wenn Funktionen komplexer werden oder mehrere Zeilen Code benötigen, kann es schwierig sein, den Code in einer lambda Funktion lesbar und wartbar zu halten. In diesen Fällen ist es oft besser, eine benannte Funktion zu definieren.

1.2.0 Beispiele 

# Beispiel 1: Quadrat einer Zahl berechnen
square = lambda x: x**2
print(square(4)) # Output: 16

# Beispiel 2: Filtern einer Liste mit einer Lambda-Funktion
numbers = [1, 2, 3, 4, 5, 6]
even_numbers = list(filter(lambda x: x % 2 == 0, numbers))
print(even_numbers) # Output: [2, 4, 6]

# Beispiel 3: Sortieren einer Liste von Wörtern nach Länge
words = ['apple', 'banana', 'cherry', 'date', 'elderberry']
sorted_words = sorted(words, key=lambda word: len(word))
print(sorted_words) # Output: ['date', 'apple', 'banana', 'cherry', 'elderberry']



1.3 Aufgaben

Hier sind ein paar Aufgaben, um das Verständnis von Lambda zu üben:
1.	Schreibe eine lambda Funktion, die das Maximum von zwei Zahlen zurückgibt.
2.	Verwende eine lambda Funktion, um alle negativen Zahlen in einer Liste zu finden und sie in eine separate Liste zu filtern.
3.	Schreibe eine lambda Funktion, um das Quadratwurzel einer Zahl zu berechnen.
