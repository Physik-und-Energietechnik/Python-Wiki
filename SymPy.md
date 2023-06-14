## Einführung
In diesem Abschnitt werden wir uns mit SymPy beschäftigen, einer magischen Bibliothek für symbolisches Rechnen in Python. Wenn du dich für Mathematik, Algebra oder symbolische Berechnungen interessierst, dann wirst du SymPy lieben!

Mit SymPy kannst du mathematische Ausdrücke symbolisch darstellen und manipulieren. Es hilft dir, komplexe Gleichungen zu lösen, Ableitungen und Integrationen durchzuführen und vieles mehr. Es ist wie ein Taschenrechner auf Steroiden, der sogar mit Variablen und Symbolen jonglieren kann.

In diesem Abschnitt wirst du lernen, wie du SymPy benutzt, um mathematische Probleme zu lösen und symbolische Berechnungen durchzuführen. Am Ende wirst du in der Lage sein, deine eigenen mathematischen Superkräfte mit SymPy einzusetzen!

## Theorie
### Symbolische Ausdrücke
In SymPy dreht sich alles um symbolische Ausdrücke. Du kannst Variablen definieren und damit komplexe mathematische Ausdrücke erstellen. Hier ist ein einfaches Beispiel:

```python
from sympy import symbols, Eq, solve

# Definiere Symbole
x, y = symbols('x y')

# Erstelle eine Gleichung
equation = Eq(x**2 + y, 10)

# Löse die Gleichung nach x
solution = solve(equation, x)
print("Lösung:", solution)
```
### Ableitungen und Integrationen
SymPy macht es einfach, Ableitungen und Integrationen symbolisch durchzuführen. Hier sind zwei Beispiele:

Ableitung: Berechne die Ableitung einer Funktion.
```python
from sympy import diff

# Definiere eine Funktion
f = x**3 + 2*x**2 - 5*x

# Berechne die Ableitung
derivative = diff(f, x)
print("Ableitung:", derivative)
```
Integration: Berechne das bestimmte Integral einer Funktion.
```python
from sympy import integrate

# Definiere eine Funktion
g = x**2 + 3*x + 2

# Berechne das Integral
integral = integrate(g, (x, 0, 2))
print("Integral:", integral)
```
## Praxis
### Aufgabe 1
Löse die Gleichung x^2 - 5x + 6 = 0.

Musterlösung:
Die Lösungen der Gleichung x^2 - 5x + 6 = 0 sind x = 2 und x = 3.
```python
# Definiere eine Gleichung
equation = Eq(x**2 - 5*x + 6, 0)

# Löse die Gleichung nach x
solutions = solve(equation, x)
print("Lösungen:", solutions)
```


### Aufgabe 2
Berechne das bestimmte Integral der Funktion f(x) = e^x * sin(x) von 0 bis π.

Musterlösung:
Das bestimmte Integral der Funktion f(x) = e^x * sin(x) von 0 bis π ergibt ungefähr 5.33007.
```python
from sympy import exp, sin

# Definiere eine Funktion
f = exp(x) * sin(x)

# Berechne das Integral
integral = integrate(f, (x, 0, 3.14159))
print("Integral:", integral)
```


Fantastisch! Du hast erfolgreich die Grundlagen von SymPy erlernt und kannst nun deine mathematischen Probleme elegant mit Symbolen und Ausdrücken lösen. SymPy wird dich auf deinem Weg zu mathematischer Brillanz begleiten. Viel Spaß beim Entdecken und Erkunden der Welt des symbolischen Rechnens mit SymPy!

## Weiterführende Links
### [sympy.org](https://www.sympy.org/en/features.html)