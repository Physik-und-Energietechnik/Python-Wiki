## Einführung
In diesem Tutorial geht es um Lambda Funktionen in Python. Mit Lambda Funktionen kann man schnell und einfach kleine, anonyme Funktionen erstellen. Dies kann sehr nützlich sein, wenn man z.B. eine Funktion nur einmal benötigt oder wenn eine Funktion als Argument an eine andere Funktion übergeben werden soll.

## Theorie
Eine Lambda Funktion in Python wird mit dem Schlüsselwort `lambda` definiert und hat die folgende Syntax:
```python
lambda argumente: ausdruck
```
Dabei sind `argumente` die Parameter der Funktion und `ausdruck` der Ausdruck, der von der Funktion zurückgegeben wird.

Ein allgemeines Code-Beispiel:
```python
# Eine einfache Lambda Funktion, die zwei Zahlen addiert
addieren = lambda a, b: a + b
print(addieren(3, 4)) # Ausgabe: 7
```

Ein explizites Code-Beispiel:
```python
# Eine Lambda Funktion, die das Quadrat einer Zahl berechnet
quadrat = lambda x: x*x
print(quadrat(5)) # Ausgabe: 25
```

## Praxis
### Leichte Aufgabe
Schreibe eine Lambda Funktion, die das Produkt zweier Zahlen berechnet und speichere sie in der Variablen `produkt`.
```python
produkt = lambda x, y: x * y
```
### Schwerere Aufgabe
Schreibe eine Lambda Funktion, die eine Liste von Zahlen als Argument nimmt und die Summe aller ungeraden Zahlen in der Liste zurückgibt. Speichere diese Funktion in der Variablen `summe_ungerade`.
```python
summe_ungerade = lambda lst: sum(filter(lambda x: x%2 != 0, lst))
```
Beachte, dass hier die `filter` Funktion verwendet wird, um nur die ungeraden Zahlen aus der Liste auszuwählen. Die `sum` Funktion addiert dann alle ausgewählten Zahlen zusammen.
