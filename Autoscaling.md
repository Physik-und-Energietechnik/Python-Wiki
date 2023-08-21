# Matplotlib - Autoscaling

## Einführung
Willkommen zu diesem Python-Tutorial über Autoscaling in Matplotlib! In diesem Abschnitt wirst du lernen, wie du mithilfe von Matplotlib deine Diagramme automatisch an die Daten anpassen kannst. Aber was bedeutet das eigentlich? Stell dir vor, du hast Daten, die über einen bestimmten Bereich verteilt sind, und du möchtest ein Diagramm erstellen, das diese Daten optimal darstellt, ohne unnötig viel Platz zu verschwenden. Autoscaling hilft dir dabei, die Achsen deines Diagramms so anzupassen, dass die Daten gut sichtbar sind und gleichzeitig der verfügbare Platz effizient genutzt wird.

Autoscaling ist eine der vielen nützlichen Funktionen, die Matplotlib bietet, um die Darstellung von Daten zu optimieren. Indem du Autoscaling beherrscht, kannst du deine Diagramme professionell gestalten und deine Daten effektiv präsentieren.

## Theorie
### Allgemeines Code-Beispiel
Um das Konzept des Autoscalings zu verdeutlichen, betrachten wir zunächst ein allgemeines Code-Beispiel:

```python
import matplotlib.pyplot as plt

# Datenpunkte erstellen
x = [1, 2, 3, 4]
y = [1, 4, 9, 16]

# Diagramm erstellen
plt.plot(x, y)

# Autoscaling aktivieren
plt.autoscale()

# Diagramm anzeigen
plt.show()
```

Das obige Beispiel erzeugt ein einfaches Liniendiagramm, das die Datenpunkte `(1, 1)`, `(2, 4)`, `(3, 9)` und `(4, 16)` darstellt. Mit der Funktion `plt.autoscale()` wird das Autoscaling aktiviert, das automatisch die Achsen des Diagramms an die Daten anpasst.

### Explizites Code-Beispiel in Python
Um Autoscaling in Matplotlib noch besser zu verstehen, betrachten wir nun ein expliziteres Code-Beispiel:

```python
import matplotlib.pyplot as plt

# Datenpunkte erstellen
x = [1, 2, 3, 4]
y = [1, 4, 9, 16]

# Diagramm erstellen
plt.plot(x, y)

# Autoscaling manuell einstellen
plt.axis('scaled')

# Diagramm anzeigen
plt.show()
```

In diesem Beispiel wird die Funktion `plt.axis('scaled')` verwendet, um das Autoscaling manuell einzustellen. Das Diagramm wird so skaliert, dass die Längen der x- und y-Achsen gleich sind.

## Praxis
Jetzt ist es an der Zeit, dein neu erlerntes Wissen in die Praxis umzusetzen! Probieren wir es mit zwei Aufgaben aus:

### Aufgabe 1
Erstelle ein Liniendiagramm, das die folgenden Daten darstellt:

```python
x = [1, 2, 3, 4]
y = [2, 4, 6, 8]
```

Aktiviere das Autoscaling, um sicherzustellen, dass die Achsen des Diagramms optimal an die Daten angepasst werden.

**Musterlösung:**

```python
import matplotlib.pyplot as plt

# Datenpunkte erstellen
x = [1, 2, 3, 4]
y = [2, 4, 6, 8]

# Diagramm erstellen
plt.plot(x, y)

# Autoscaling aktivieren
plt.autoscale()

# Diagramm anzeigen
plt.show()
```

### Aufgabe 2
Erstelle ein Streudiagramm, das die folgenden Daten darstellt:

```python
x = [1, 2, 3, 4]
y = [10, 100, 1000, 10000]
```

Passe das Autoscaling manuell an, um sicherzustellen, dass die x-Achse logarithmisch skaliert wird.

**Musterlösung:**

```python
import matplotlib.pyplot as plt

# Datenpunkte erstellen
x = [1, 2, 3, 4]
y = [10, 100, 1000, 10000]

# Diagramm erstellen
plt.scatter(x, y)

# Autoscaling manuell einstellen (logarithmische Skalierung der x-Achse)
plt.xscale('log')

# Diagramm anzeigen
plt.show()
```

Herzlichen Glückwunsch! Du hast erfolgreich Autoscaling in Matplotlib angewendet. Du bist nun in der Lage, deine Diagramme automatisch an deine Daten anzupassen und sie optimal zu präsentieren.

Viel Spaß beim Erstellen beeindruckender Diagramme mit Matplotlib!