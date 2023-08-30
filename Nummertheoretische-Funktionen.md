## Einführung

Hallo und herzlich willkommen zum Python-Tutorial über Nummertheoretische Funktionen! In diesem Abschnitt werden wir uns mit Funktionen befassen, die uns helfen, mit Zahlen und deren Repräsentation in Python zu arbeiten. Du wirst lernen, wie du Zahlen runden kannst, wie du den größten gemeinsamen Teiler findest und wie du feststellst, ob Zahlen gleich oder nahe beieinander sind.

Lasst uns eintauchen und diese spannenden Funktionen erkunden!

## Theorie

### Runden von Zahlen - math.ceil() und math.floor()

Manchmal möchten wir eine Zahl aufrunden oder abrunden. Python bietet uns dafür die Funktionen `math.ceil()` und `math.floor()`.

- `math.ceil(x)` gibt die kleinste Ganzzahl zurück, die größer oder gleich der gegebenen Zahl `x` ist.
- `math.floor(x)` gibt die größte Ganzzahl zurück, die kleiner oder gleich der gegebenen Zahl `x` ist.

Hier sind Beispiele:

```python
import math

x = 3.7
y = 5.2

rounded_up = math.ceil(x)  # Ergebnis: 4
rounded_down = math.floor(y)  # Ergebnis: 5
```

### Größter gemeinsamer Teiler - math.gcd()

Manchmal müssen wir den größten gemeinsamen Teiler (ggT) von Zahlen finden. Das ist besonders nützlich, wenn wir Brüche kürzen wollen. Python bietet die Funktion `math.gcd()` für diese Aufgabe.

```python
import math

num1 = 48
num2 = 18

gcd = math.gcd(num1, num2)  # Ergebnis: 6
```

### Überprüfung von Annäherung - math.isclose()

Oft müssen wir feststellen, ob zwei Zahlen nahe beieinander liegen, trotz möglicher Rundungsfehler. Hier kommt `math.isclose()` ins Spiel:

```python
import math

a = 0.1 + 0.1 + 0.1
b = 0.3

close = math.isclose(a, b)  # Ergebnis: True
```

## Praxis

### Aufgabe 1

Gegeben sind die Zahlen 5.6 und 5.601. Überprüfe, ob sie nahe beieinander liegen und gib das Ergebnis aus.

```python
import math

num1 = 5.6
num2 = 5.601

close = math.isclose(num1, num2)
print(close)  # Ergebnis: True
```

### Aufgabe 2

Berechne den ggT von 24, 36 und 48.

```python
import math

num1 = 24
num2 = 36
num3 = 48

gcd = math.gcd(num1, num2, num3)
print(gcd)  # Ergebnis: 12
```

Herzlichen Glückwunsch! Du hast nun gelernt, wie du mit diesen praktischen Funktionen in Python arbeiten kannst. Mit diesem Wissen kannst du Zahlen besser verarbeiten und mathematische Probleme elegant lösen.

## Links / Weiteres Material
https://docs.python.org/3/library/math.html