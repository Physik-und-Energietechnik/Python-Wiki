# Python Tutorial für Anfänger - Trigonometrische Funktionen mit Python.math

## Einführung
Willkommen zu unserem lustigen und spannenden Tutorial über trigonometrische Funktionen mit Python! In diesem Tutorial wirst du lernen, wie du mithilfe der `python.math`-Bibliothek trigonometrische Funktionen wie Sinus, Kosinus und Tangens berechnen kannst. Aber was genau sind eigentlich trigonometrische Funktionen und wofür sind sie gut?

Trigonometrische Funktionen sind mathematische Funktionen, die sich mit den Beziehungen zwischen den Seiten und Winkeln von Dreiecken beschäftigen. Sie finden Anwendung in vielen Bereichen wie Geometrie, Physik, Maschinenbau, Astronomie und sogar in der Computergrafik. Mit Python und der `python.math`-Bibliothek kannst du diese Funktionen einfach und präzise berechnen.

In diesem Tutorial lernst du, wie du die trigonometrischen Funktionen Sinus, Kosinus und Tangens verwendest, um Winkel zu berechnen und Probleme zu lösen, die Dreiecke betreffen. Du wirst überrascht sein, wie nützlich diese Funktionen in der realen Welt sein können!

## Theorie
### Sinus
Der Sinus einer Winkelmaßzahl ist das Verhältnis der Länge der Seite gegenüber dem Winkel zum Verhältnis der Länge der Hypotenuse eines rechtwinkligen Dreiecks. 

Hier ist ein Beispiel, das den Sinus eines Winkels berechnet:

```python
import math

angle = 45  # Winkel in Grad
radians = math.radians(angle)  # Konvertiere Grad in Bogenmaß
sin_value = math.sin(radians)  # Berechne den Sinus

print(f"Der Sinus von {angle} Grad ist {sin_value}")
```

### Kosinus
Der Kosinus einer Winkelmaßzahl ist das Verhältnis der Länge der Seite neben dem Winkel zur Länge der Hypotenuse eines rechtwinkligen Dreiecks.

Hier ist ein Beispiel, das den Kosinus eines Winkels berechnet:

```python
import math

angle = 60  # Winkel in Grad
radians = math.radians(angle)  # Konvertiere Grad in Bogenmaß
cos_value = math.cos(radians)  # Berechne den Kosinus

print(f"Der Kosinus von {angle} Grad ist {cos_value}")
```

### Tangens
Der Tangens einer Winkelmaßzahl ist das Verhältnis der Länge der Seite gegenüber dem Winkel zur Länge der Seite neben dem Winkel eines rechtwinkligen Dreiecks.

Hier ist ein Beispiel, das den Tangens eines Winkels berechnet:

```python
import math

angle = 30  # Winkel in Grad
radians = math.radians(angle)  # Konvertiere Grad in Bogenmaß
tan_value = math.tan(radians)  # Berechne den Tangens

print(f"Der Tangens von {angle} Grad ist {tan_value}")
```

## Praxis
### Aufgabe 1
Berechne den Sinus des Winkels 90 Grad.

Musterlösung:

```python
import math

angle = 90  # Winkel in Grad
radians = math.radians(angle)  # Konvertiere Grad in Bogenmaß
sin_value = math.sin(radians)  # Berechne den Sinus

print(f"Der Sinus von {angle} Grad ist {sin_value}")
```

### Aufgabe 2
Berechne den Tangens des Winkels 60 Grad.

Musterlösung:

```python
import math

angle = 60  # Winkel in Grad
radians = math.radians(angle)  # Konvertiere Grad in Bogenmaß
tan_value = math.tan(radians)  # Berechne den Tangens

print(f"Der Tangens von {angle} Grad ist {tan_value}")
```

Herzlichen Glückwunsch! Du hast gerade gelernt, wie du trigonometrische Funktionen in Python verwendest. Mit diesen Funktionen kannst du Winkel berechnen, Dreiecke analysieren und viele andere interessante Probleme lösen. Nutze dieses Wissen, um die Welt der Trigonometrie zu erforschen und weiterhin lustige und faszinierende mathematische Abenteuer mit Python zu erleben!