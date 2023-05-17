# Python - Sets
## Einführung

Willkommen zu unserem Python-Tutorial über Sets! Hast du jemals davon geträumt, eine Sammlung von einzigartigen Gegenständen zu haben? Nun, Sets in Python machen genau das möglich! In diesem Tutorial werden wir dir erklären, was Sets sind, wie du sie erstellst und welche magischen Kräfte sie besitzen.

Du wirst lernen, wie du Sets verwenden kannst, um Elemente ohne Duplikate zu speichern und Operationen wie Vereinigung, Schnittmenge und Differenz durchzuführen. Sets sind wie die Zauberkünstler der Python-Welt - sie lassen Duplikate verschwinden und zaubern dir ein Lächeln ins Gesicht!
## Theorie
### Was sind Sets?

Sets sind wie unsichtbare Käfige für einzigartige Objekte. Sie sind Sammlungen von Elementen, bei denen jedes Element einzigartig ist und keine bestimmte Reihenfolge hat. Stell dir vor, du hast eine Sammlung von magischen Zaubertricks - jedes Trick ist einzigartig und in deinem Set sicher verwahrt.
### Code-Beispiel: Allgemein

Hier ist ein allgemeines Code-Beispiel, um dir zu zeigen, wie Sets funktionieren:



```python
magic_tricks = {"Verschwindende Münze", "Schwebender Ball", "Zersägte Dame"}
print(magic_tricks)  # Output: {'Schwebender Ball', 'Verschwindende Münze', 'Zersägte Dame'}

````

In diesem Beispiel haben wir ein Set namens magic_tricks erstellt und drei Zaubertricks hinzugefügt. Beachte, dass die Reihenfolge der Tricks nicht erhalten bleibt und jedes Element einzigartig ist. Sets sorgen dafür, dass deine magischen Tricks niemals langweilig werden!
### Code-Beispiel: Explizit in Python

Wenn du kein Fan von Unsichtbarkeit bist und lieber direkte Dinge magst, hier ist dasselbe Beispiel mit einer expliziten Methode:


```python
magic_tricks = set(["Verschwindende Münze", "Schwebender Ball", "Zersägte Dame"])
print(magic_tricks)  # Output: {'Schwebender Ball', 'Verschwindende Münze', 'Zersägte Dame'}

````

Siehst du den Unterschied? Die Set-Version ist kompakt und mysteriös, während die explizite Methode dir zeigt, was genau passiert. Beide Wege führen dich zu einem Set voller magischer Elemente!
Praxis

Jetzt wird es Zeit, deine eigene Magie zu entfesseln! Wir haben eine leichte und eine schwere Aufgabe vorbereitet, um deine Fähigkeiten mit Sets zu testen.
## Aufgaben
### Aufgabe 1

Hier ist eine leichte Aufgabe für dich. Gegeben sind zwei Sets von Zaubertricks. Schreibe Code, um die Tricks zu finden, die in beiden Sets enthalten sind. Das wird deine Zaubertrick-Superkraft demonstrieren!


```python
set1 = {"Verschwindende Münze", "Schwebender Ball", "Zersägte Dame"}
set2 = {"Zersägte Dame", "Schwebender Ball", "Durchbohrter Apfel"}
common_tricks = set1.intersection(set2)
common_tricks = set1.intersection(set2)
print(common_tricks)  # Output: {'Schwebender Ball', 'Zersägte Dame'}

````

### Aufgabe 2

Jetzt wird es etwas schwieriger. Gegeben sind mehrere Sets von Zaubertricks. Schreibe Code, um alle einzigartigen Tricks zu finden, die in den Sets enthalten sind. Zeige uns, dass du der Meister der Einzigartigkeit bist!



```python
set1 = {"Verschwindende Münze", "Schwebender Ball", "Zersägte Dame"}
set2 = {"Zersägte Dame", "Schwebender Ball", "Durchbohrter Apfel"}
set3 = {"Schwebender Ball", "Schwebendes Tuch", "Levitierender Zauberstab"}

unique_tricks = set1.union(set2, set3)
print(unique_tricks)  # Output: {'Verschwindende Münze', 'Levitierender Zauberstab', 'Schwebendes Tuch', 'Zersägte Dame', 'Durchbohrter Apfel', 'Schwebender Ball'}


````

In diesem Beispiel verwenden wir die Methode union(), um alle einzigartigen Tricks aus set1, set2 und set3 zu finden. Das Ergebnis ist ein neues Set mit allen Tricks, ohne Duplikate. Zeige uns deine Meistermagie und finde alle einzigartigen Tricks!