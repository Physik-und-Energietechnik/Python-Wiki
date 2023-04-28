**## Einführung**

Willkommen zu unserem Python Tutorial für Anfänger! In diesem Abschnitt werden wir uns mit Operatoren in Python beschäftigen. Dabei lernst du, wie du mit Variablen und Werten rechnen und vergleichen kannst.
Das Wissen über Operatoren ist ein wichtiger Bestandteil für viele Programmieraufgaben, z.B. für die Erstellung von mathematischen Formeln, Bedingungen und Schleifen.

**## Theorie**

Es gibt verschiedene Arten von Operatoren in Python, die wir in diesem Abschnitt näher betrachten werden. Dazu gehören:

* **###Arithmetische Operatoren**

Arithmetische Operatoren dienen zur Durchführung von mathematischen Berechnungen wie Addition, Subtraktion, Multiplikation und Division.

Code-Beispiel:

a = 10
b = 5

print(a + b) # Addition
print(a - b) # Subtraktion
print(a * b) # Multiplikation
print(a / b) # Division

* **### Vergleichsoperatoren**

Vergleichsoperatoren dienen zur Überprüfung von Bedingungen. Dabei wird das Ergebnis eines Vergleichs als Wahrheitswert (True oder False) zurückgegeben.

Code-Beispiel:

a = 10
b = 5

print(a > b) # Größer als
print(a < b) # Kleiner als
print(a == b) # Gleich
print(a != b) # Ungleich

* **### Logische Operatoren**

Logische Operatoren werden verwendet, um komplexe Bedingungen zu erstellen, indem man mehrere Vergleichsoperatoren miteinander kombiniert.

Code-Beispiel:

a = 10
b = 5
c = 20

print(a > b and a < c) # Und
print(a > b or a > c) # Oder
print(not a > b) # Nicht

* ### **Zuweisungsoperatoren**

Zuweisungsoperatoren dienen zur Zuweisung von Werten zu Variablen.

Code-Beispiel:

a = 10
b = 5

a += b # a = a + b
print(a)

a -= b # a = a - b
print(a)

a *= b # a = a * b
print(a)

a /= b # a = a / b
print(a)

**## Praxis**

Lass uns nun das erlernte Wissen in der Praxis anwenden. Hier sind zwei Aufgaben für dich:

**### Aufgabe 1**

Schreibe ein kleines Programm, das den Benutzer nach seinem Alter fragt und überprüft, ob er volljährig ist. Wenn ja, soll das Programm "Du bist volljährig!" ausgeben, andernfalls "Du bist minderjährig!".

Ergebnis:

age = int(input("Wie alt bist du? "))

if age >= 18:
    print("Du bist volljährig!")
else:
    print("Du bist minderjährig!")

### **Aufgabe 2**

Schreibe ein Programm, das eine Schleife ausführt und bei jedem Durchlauf die aktuelle Zahl ausgibt. Die Schleife soll bei der Zahl 10 enden.

Ergebnis:

i = 1

while i <= 10:
    print(i)
    i += 1


