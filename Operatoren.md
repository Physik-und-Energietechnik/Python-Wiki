## **Einführung**
Willkommen zu diesem Python-Tutorial über Operatoren. In diesem Tutorial werden wir uns mit den verschiedenen Arten von Operatoren in Python befassen und wie man sie benutzt. Wir werden uns auch einige praktische Anwendungen ansehen, um zu verstehen, wie Operatoren in der Praxis verwendet werden können.

## **Theorie**
Operatoren sind Symbole oder Schlüsselwörter in Python, die verwendet werden, um arithmetische oder logische Operationen auf Variablen und Werten durchzuführen. In Python gibt es verschiedene Arten von Operatoren, darunter:

* ### **Arithmetische Operatoren** 
Diese Operatoren werden verwendet, um mathematische Berechnungen durchzuführen, wie **Addition(+), Subtraktion(-), Multiplikation(*), Division(/), Potenz(**) und Modulo(%)**.
Hier ist **ein allgemeines Code-Beispiel**:

    a = 10
    b = 5
    c = a + b
    print(c) # Ausgabe: 15


**Explizites Code-Beispiel**:

    # Addition
    a = 10
    b = 5
    c = a + b
    print(c)  # Ausgabe: 15

    # Subtraktion
    a = 10
    b = 5
    c = a - b
    print(c)  # Ausgabe: 5

    # Multiplikation
    a = 10
    b = 5
    c = a * b
    print(c)  # Ausgabe: 50

    # Division
    a = 10
    b = 5
    c = a / b
    print(c)  # Ausgabe: 2.0

    # Modulo
    a = 10
    b = 3
    c = a % b
    print(c)  # Ausgabe: 1

    # Exponentiation
    a = 2
    b = 3
    c = a ** b
    print(c)  # Ausgabe: 8

* ### **Logische Operatoren**
Logische Operatoren werden verwendet, um logische Aussagen zu kombinieren und auszuwerten. Dazu gehören **AND (und), OR (oder) und NOT (nicht)**.

**Allgemeines Code-Beispiel:**

    a = True
    b = False
    c = a and b
    print(c) # Ausgabe: False

**Explizites Code-Beispiel:**

    # AND
    a = True
    b = False
    c = a and b
    print(c)  # Ausgabe: False

    # OR
    a = True
    b = False
    c = a or b
    print(c)  # Ausgabe: True

    # NOT
    a = True
    b = False
    c = not a
    print(c)  # Ausgabe: False

* ### **Vergleichsoperatoren**
Vergleichsoperatoren werden verwendet, um den Vergleich von Variablen oder Ausdrücken durchzuführen. Dazu gehören **!= (ungleich), == (gleich), > (größer als), < (kleiner als), >= (größer oder gleich) und <= (kleiner oder gleich)**.

**Allgemeines Code-Beispiel**:

    a = 10
    b = 5
    c = (a == b)
    print(c) #Ausgabe: False

**Explizites Code-Beispiel:**

    a = 10
    b = 5

    print(a == b)  # Ausgabe: False
    print(a != b)  # Ausgabe: True
    print(a > b)   # Ausgabe: True
    print(a < b)   # Ausgabe: False
    print(a >= b)  # Ausgabe: True
    print(a <= b)  # Ausgabe: False

* ### **Zuweisungs-Operatoren:**
Zuweisungs-Operatoren werden verwendet, um Werte einer Variablen zuzuweisen.

**Allgemeines Code-Beispiel:**

    a = b   # Wert von b an a zuweisen
    a += b  # Äquivalent zu a = a + b
    a -= b  # Äquivalent zu a = a - b
    a *= b  # Äquivalent zu a = a * b
    a /= b  # Äquivalent zu a = a / b
    a %= b  # Äquivalent zu a = a % b

**Explizites Code-Beispiel:**

    a = 10
    b = 5

    a = b      
    print(a)   # Ausgabe: 5

    a += b
    print(a)   # Ausgabe: 15

    a -= b  
    print(a)   # Ausgabe: 5

    a *= b  
    print(a)   # Ausgabe: 50

    a /= b  
    print(a)   # Ausgabe: 2.0

    a %= b  
    print(a)   # Ausgabe: 0







