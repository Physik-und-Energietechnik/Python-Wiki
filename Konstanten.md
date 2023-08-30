## Einführung
Willkommen zu unserem unterhaltsamen Python-Tutorial über die Konstanten von `math.py`! In diesem Tutorial werden wir uns mit den verschiedenen mathematischen Konstanten befassen, die in der `math.py`-Bibliothek von Python integriert sind. Aber welche Konstanten sind das und wie können wir sie nutzen, um unsere Python-Programme zu verbessern?

Mathematische Konstanten sind feste Werte, die in vielen mathematischen Bereichen von großer Bedeutung sind. Sie repräsentieren wichtige mathematische Konzepte und Eigenschaften, die uns helfen, komplexe Berechnungen durchzuführen und Probleme in verschiedenen mathematischen Disziplinen wie Geometrie, Trigonometrie, Statistik und mehr zu lösen.

In diesem Tutorial wirst du die verschiedenen mathematischen Konstanten kennenlernen, die in der `math.py`-Bibliothek verfügbar sind. Du wirst erfahren, wie du auf diese Konstanten zugreifen kannst und wie du sie in deinen Python-Programmen verwenden kannst, um interessante mathematische Operationen durchzuführen und faszinierende Ergebnisse zu erzielen.

## Theorie
Die `math.py`-Bibliothek bietet eine Vielzahl von mathematischen Konstanten, auf die du zugreifen kannst. Hier sind einige der wichtigsten Konstanten:

### Pi (π)
Pi ist eine der bekanntesten mathematischen Konstanten und repräsentiert das Verhältnis des Umfangs eines Kreises zu seinem Durchmesser. In Python kannst du auf den Wert von Pi zugreifen, indem du `math.pi` verwendest.

```python
import math

pi_value = math.pi

print(pi_value)
```

### Eulersche Zahl (e)
Die Eulersche Zahl ist eine weitere bedeutende mathematische Konstante und die Basis des natürlichen Logarithmus. Mit `math.e` kannst du auf den Wert der Eulerschen Zahl in Python zugreifen.

```python
import math

e_value = math.e

print(e_value)
```

### Unendlichkeit (inf)
Die Konstante `math.inf` repräsentiert den positiven unendlichen Wert. Du kannst sie verwenden, um auf unendliche oder unbegrenzte mathematische Werte hinzuweisen.

```python
import math

infinity = math.inf

print(infinity)
```

### NaN (nan)
Die Konstante `math.nan` steht für "Not a Number" und wird verwendet, um ungültige oder undefinierte mathematische Operationen anzugeben.

```python
import math

nan_value = math.nan

print(nan_value)
```

### Tau (τ)
Tau ist eine mathematische Konstante, die dem doppelten Wert von Pi entspricht. Sie wird manchmal anstelle von Pi verwendet, um bestimmte mathematische Formeln und Berechnungen zu vereinfachen.

```python
import math

tau_value = 2 * math.pi

print(tau_value)
```

## Praxis
Lass uns nun das erlernte Wissen in die Praxis umsetzen!

### Aufgabe 1
Schreibe ein Python-Programm, das den Umfang und die Fläche eines Kreises berechnet. Verwende dazu die Konstante Pi aus der `math.py`-Bibliothek. Gib die berechneten Werte anschließend aus.

```python
import math

radius = 5

# Umfang des Kreises berechnen
umfang = 2 * math.pi * radius

# Fläche des Kreises berechnen
flaeche = math.pi * radius**2

print("Umfang:", umfang)
print("Fläche:", flaeche)
```

### Aufgabe 2
Schreibe ein Python-Programm, das den Sinus, den Kosinus und den Tangens eines gegebenen Winkels berechnet. Verwende dazu die trigonometrischen Funktionen und die Konstante Pi aus der `math.py`-Bibliothek. Gib die berechneten Werte anschließend aus.

```python
import math

winkel = 45

# Sinus des Winkels berechnen
sinus = math.sin(math.radians(winkel))

# Kosinus des Winkels berechnen
kosinus = math.cos(math.radians(winkel))

# Tangens des Winkels berechnen
tangens = math.tan(math.radians(winkel))

print("Sinus:", sinus)
print("Kosinus:", kosinus)
print("Tangens:", tangens)
```

## Fazit
Herzlichen Glückwunsch! Du hast nun gelernt, wie du auf wichtige mathematische Konstanten in Python zugreifen und sie in deinen Programmen verwenden kannst. Diese Konstanten ermöglichen es dir, komplexe Berechnungen durchzuführen und mathematische Probleme zu lösen.

Die Verwendung mathematischer Konstanten eröffnet dir neue Möglichkeiten, um faszinierende mathematische Operationen durchzuführen und spannende Ergebnisse zu erzielen. Du kannst sie in verschiedenen Bereichen wie Geometrie, Trigonometrie, Statistik und vielen anderen einsetzen.

Jetzt bist du bereit, dein mathematisches Wissen in die Praxis umzusetzen und beeindruckende Python-Programme zu schreiben. Viel Spaß beim Programmieren und beim Entdecken der faszinierenden Welt der mathematischen Konstanten!

## Links / Weiteres Material
https://docs.python.org/3/library/math.html#constants