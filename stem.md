## Einführung
In diesem Abschnitt widmen wir uns einem besonders faszinierenden Werkzeug - dem "stem Plot". Klingt nach Pflanzenbiologie, oder? Nun, es ist tatsächlich so ähnlich, nur dass wir hier keine Pflanzen, sondern Daten betrachten. Der stem Plot ermöglicht es uns, diskrete Datenpunkte auf einer Achse darzustellen und Verbindungen zwischen ihnen herzustellen. Klingt cool, oder? Lass uns eintauchen und herausfinden, wie wir damit unsere Daten zum Blühen bringen können!

## Theorie

### Was ist ein stem Plot?
Ein stem Plot ist eine spezielle Art von Diagramm, das uns hilft, diskrete Daten darzustellen. Im Gegensatz zu herkömmlichen Linien- oder Balkendiagrammen, bei denen die Datenpunkte auf der Achse verschmelzen, hebt der stem Plot jeden Datenpunkt deutlich hervor. Er zeigt uns, wie die Werte entlang der Achse verteilt sind und ermöglicht es uns, Muster und Ausreißer leichter zu erkennen. Ein stem Plot ähnelt ein wenig einer Pflanze, bei der die Datenpunkte wie Stängel aussehen und die zugehörigen Werte wie Blätter daran befestigt sind.

### Code-Beispiel (allgemein)
```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [0.1, 0.3, 0.2, 0.4, 0.5]

plt.stem(x, y, markerfmt='ro', linefmt='b--', basefmt='g-')
plt.xlabel('x-Achse')
plt.ylabel('y-Achse')
plt.title('Ein einfacher stem Plot')
plt.show()
```

### Explizites Code-Beispiel (Python)
```python
import matplotlib.pyplot as plt

ages = [21, 24, 26, 28, 30, 34, 35, 40, 42, 45]
weights = [62, 68, 70, 75, 80, 82, 83, 88, 90, 92]

plt.stem(ages, weights, markerfmt='ro', linefmt='b--', basefmt='g-')
plt.xlabel('Alter')
plt.ylabel('Gewicht')
plt.title('Verteilung von Alter und Gewicht')
plt.show()
```

## Praxis
Jetzt wollen wir unser neu erworbenes Wissen in die Praxis umsetzen! Hier sind zwei Aufgaben, die dir helfen werden, den stem Plot besser zu verstehen.

### Aufgabe 1
Erstelle einen stem Plot für die folgenden Daten:
```python
x = [1, 2, 3, 4, 5]
y = [3, 1, 4, 2, 5]
```

Musterlösung:
```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [3, 1, 4, 2, 5]

plt.stem(x, y, markerfmt='ro', linefmt='b--', basefmt='g-')
plt.xlabel('x-Achse')
plt.ylabel('y-Achse')
plt.title('Mein erster stem Plot

')
plt.show()
```

### Aufgabe 2
Erstelle einen stem Plot für die folgenden Daten:
```python
months = ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun']
temperatures = [8, 10, 12, 15, 18, 20]
```

Musterlösung:
```python
import matplotlib.pyplot as plt

months = ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun']
temperatures = [8, 10, 12, 15, 18, 20]

plt.stem(months, temperatures, markerfmt='ro', linefmt='b--', basefmt='g-')
plt.xlabel('Monate')
plt.ylabel('Temperaturen')
plt.title('Temperaturverlauf')
plt.show()
```

Viel Spaß beim Experimentieren mit dem stem Plot! Lass deiner Kreativität freien Lauf und entdecke die vielfältigen Möglichkeiten der Datenvisualisierung.