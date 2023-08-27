## Einführung

Herzlich willkommen zum Python-Tutorial über die Anpassung der Plot Interaktion und Navigation mit Matplotlib! In diesem Abschnitt lernst du, wie du deine Plots interaktiv gestalten und die Navigation in den Plots verbessern kannst.

In diesem Tutorial werden wir uns darauf konzentrieren, wie du die Interaktion und Navigation in deinen Plots anpassen kannst. Du wirst lernen, wie du Zoomen, Verschieben und andere interaktive Funktionen in deine Plots einbaust.

## Theorie

### Interaktive Funktionen in Matplotlib

Matplotlib bietet eine Vielzahl von Funktionen, mit denen du die Interaktion mit deinen Plots anpassen kannst. Hier sind einige der wichtigsten Funktionen:

- Zoomen: Du kannst bestimmte Bereiche deines Plots vergrößern, um Details genauer zu betrachten.

- Verschieben: Du kannst den angezeigten Bereich deines Plots verschieben, um unterschiedliche Teile deiner Daten zu betrachten.

- Markierungen: Du kannst bestimmte Datenpunkte in deinem Plot markieren, um ihre Bedeutung hervorzuheben.

- Anmerkungen: Du kannst Text oder Pfeile hinzufügen, um bestimmte Merkmale oder Trends in deinen Daten zu kennzeichnen.

### Code-Beispiel - Zoomen und Verschieben

Hier ist ein allgemeines Code-Beispiel, das zeigt, wie du Zoomen und Verschieben in Matplotlib nutzen kannst:

```python
import matplotlib.pyplot as plt

# Daten generieren
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

# Plot erstellen
plt.plot(x, y)

# Zoomen und Verschieben aktivieren
plt.zoom(True)
plt.pan(True)

# Plot anzeigen
plt.show()
```

Das obige Beispiel zeigt einen einfachen Plot mit den Datenpunkten `(1, 2)`, `(2, 4)`, `(3, 6)`, `(4, 8)` und `(5, 10)`. Durch Aktivierung der Zoom- und Verschiebefunktionen kannst du den Plot vergrößern und den angezeigten Bereich verschieben, um bestimmte Bereiche genauer zu betrachten.

### Explizites Code-Beispiel - Anmerkungen hinzufügen

Hier ist ein explizites Code-Beispiel, das zeigt, wie du Anmerkungen zu deinem Plot hinzufügen kannst:

```python
import matplotlib.pyplot as plt

# Daten generieren
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

# Plot erstellen
plt.plot(x, y)

# Anmerkung hinzufügen
plt.annotate('Hier ist ein interessanter Punkt!', xy=(3, 6), xytext=(4, 8),
             arrowprops=dict(facecolor='black', arrowstyle='->'))

# Plot anzeigen
plt.show()
```

Das obige Beispiel fügt eine Anmerkung zu einem bestimmten Punkt im Plot hinzu. Die Anmerkung enthält den Text "Hier ist ein interessanter Punkt!" und wird mit einem Pfeil markiert, der auf den Punkt zeigt.

## Praxis

### Aufgabe 1

Deine Aufgabe besteht darin, einen einfachen Plot zu erstellen und die Zoom- und Verschiebefunktionen zu aktivieren. Du kannst deine eigenen Daten verwenden oder die folgenden Daten verwenden:

```python
import matplotlib.pyplot as plt

# Daten generieren
x = [1, 2, 3, 4, 5]
y = [1, 4, 9, 16, 25]

# Plot erstellen
plt.plot(x, y)

# Zoomen und Verschieben aktivieren
plt.zoom(True)
plt.pan(True)

# Plot anzeigen
plt.show()
```

Musterlösung:

```python
import matplotlib.pyplot as plt

# Daten generieren
x = [1, 2, 3, 4, 5]
y = [1, 4, 9, 16, 25]

# Plot erstellen
plt.plot(x, y)

# Zoomen und Verschieben aktivieren
plt.zoom(True)
plt.pan(True)

# Plot anzeigen
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Fortgeschrittene_Plot_Techniken/Anpassung_der_Plot-Interaktion_und_Navigation/ms_aufgabe1.png)

Du kannst den Plot vergrößern und den angezeigten Bereich verschieben, um verschiedene Aspekte der Daten genauer zu betrachten.

### Aufgabe 2

Deine schwierigere Aufgabe besteht darin, einen Plot zu erstellen und eine Anmerkung hinzuzufügen, um einen bestimmten Punkt zu markieren. Verwende deine eigenen Daten oder die folgenden Daten:

```python
import matplotlib.pyplot as plt

# Daten generieren
x = [1, 2, 3, 4, 5]
y = [1, 4, 9, 16, 25]

# Plot erstellen
plt.plot(x, y)

# Anmerkung hinzufügen
plt.annotate('Maximaler Wert', xy=(5, 25), xytext=(3, 15),
             arrowprops=dict(facecolor='black', arrowstyle='->'))

# Plot anzeigen
plt.show()
```

Musterlösung:

Hier ist eine mögliche Musterlösung für die schwierigere Aufgabe:

```python
import matplotlib.pyplot as plt

# Daten generieren
x = [1, 2, 3, 4, 5]
y = [1, 4, 9, 16, 25]

# Plot erstellen
plt.plot(x, y)

# Anmerkung hinzufügen
plt.annotate('Maximaler Wert', xy=(5, 25), xytext=(3, 15),
             arrowprops=dict(facecolor='black', arrowstyle='->'))

# Plot anzeigen
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Fortgeschrittene_Plot_Techniken/Anpassung_der_Plot-Interaktion_und_Navigation/ms_aufgabe2.png)

Die Anmerkung markiert den Punkt `(5, 25)` im Plot und enthält den Text "Maximaler Wert".

## Fazit
Herzlichen Glückwunsch! Du hast erfolgreich gelernt, wie du die Interaktion und Navigation in deinen Plots mit Matplotlib anpassen kannst. Experimentiere weiter mit den verschiedenen Funktionen, um deine Plots noch interessanter und aussagekräftiger zu gestalten.

## Links / Weiteres Material
### Dokumentation
### W3Schools
### YouTube