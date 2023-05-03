2.0 Sets

2.1 Einführung
Sets in Python sind eine Datenstruktur, die eine Sammlung einzigartiger Elemente enthält. Die Elemente in einem Set sind nicht geordnet und nicht indiziert, was bedeutet, dass man nicht auf sie mit einem Index zugreifen kann. Sets können mit geschweiften Klammern {} oder mit der set()-Funktion erstellt werden.

2.2 Theorie

Die Vorteile von Sets sind, dass sie schnell und einfach zu durchsuchen sind, und dass sie keine Duplikate enthalten. Das kann die Verarbeitung von Daten beschleunigen und vereinfachen.

Beim Umgang mit Sets sollte man sich jedoch bewusst sein, dass sie nicht indiziert sind und keine Reihenfolge haben. Das bedeutet, dass die Elemente in einem Set bei jeder Iteration in einer anderen Reihenfolge zurückgegeben werden können. Darüber hinaus sind Sets unveränderlich, was bedeutet, dass sie nach ihrer Erstellung nicht mehr geändert werden können. Wenn man Elemente hinzufügen oder entfernen muss, muss man ein neues Set erstellen.

2.2.0 Beispiele

2.2.1 Entfernung von Duplikaten - Wenn man eine Liste mit wiederholten Elementen hat, kann man sie in ein Set umwandeln, um die Duplikate zu entfernen:

my_list = [1, 2, 3, 3, 4, 4, 5]
my_set = set(my_list)
print(my_set) # Output: {1, 2, 3, 4, 5}

2.2.2 Set-Operationen - Sets unterstützen Operationen wie Union, Intersection, Difference und Symmetric Difference:

set1 = {1, 2, 3}
set2 = {2, 3, 4}

union_set = set1.union(set2)
print(union_set) # Output: {1, 2, 3, 4}

intersection_set = set1.intersection(set2)
print(intersection_set) # Output: {2, 3}

difference_set = set1.difference(set2)
print(difference_set) # Output: {1}

symmetric_difference_set = set1.symmetric_difference(set2)
print(symmetric_difference_set) # Output: {1, 4}

2.2.3 Membership-Test - Sets können verwendet werden, um zu überprüfen, ob ein Element in einer Sammlung vorhanden ist:

my_set = {1, 2, 3, 4, 5}
print(2 in my_set) # Output: True
print(6 in my_set) # Output: False



2.3 Aufgaben

2.4.1 Schreibe eine Funktion, die eine Liste von Zahlen als Eingabe nimmt und eine Liste von nur den einzigartigen Zahlen zurückgibt.
2.4.2 Schreibe eine Funktion, die zwei Listen als Eingabe nimmt und eine Liste von Elementen zurückgibt, die in beiden Listen vorkommen.
2.4.3 Schreibe eine Funktion, die eine Liste von Wörtern als Eingabe nimmt und ein Set von Wörtern zurückgibt, die in der Liste doppelt vorkommen.
