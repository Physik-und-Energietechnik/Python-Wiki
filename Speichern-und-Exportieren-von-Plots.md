## Einführung

In diesem Abschnitt lernst du, wie du deine erstellten Diagramme und Visualisierungen in Python mit Matplotlib speichern und exportieren kannst. Das Wissen, das du hier erlangst, wird dir helfen, deine Plots für verschiedene Zwecke zu verwenden, sei es für Präsentationen, Berichte oder sogar soziale Medien.

## Theorie

### Grundlagen der Plot-Speicherung

Bevor wir in die Praxis einsteigen, lass uns kurz die Grundlagen der Plot-Speicherung besprechen. Matplotlib bietet verschiedene Möglichkeiten, um deine Plots zu speichern. Die gängigsten Formate sind PNG, JPEG, SVG und PDF. Jedes Format hat seine eigenen Vorteile, abhängig von deinen Anforderungen. Zum Beispiel ist PNG ideal, wenn du eine hohe Bildqualität beibehalten möchtest, während SVG eine skalierbare Vektorgrafik ist, die sich gut für die spätere Bearbeitung eignet.

Hier ist ein allgemeines Code-Beispiel, das zeigt, wie du deinen Plot in Matplotlib speichern kannst:

```python
import matplotlib.pyplot as plt

# Erstelle deinen Plot
plt.plot([1, 2, 3, 4], [1, 4, 9, 16])

# Speichere den Plot als PNG-Datei
plt.savefig('mein_plot.png')
```

### Speichern von Plots mit hoher Qualität

Wenn du einen Plot mit hoher Qualität erstellen möchtest, kannst du die DPI (Dots Per Inch)-Einstellung in Matplotlib verwenden. Eine höhere DPI-Zahl bedeutet eine höhere Auflösung des gespeicherten Bildes.

Hier ist ein explizites Code-Beispiel, das zeigt, wie du die DPI-Einstellung für die Plot-Speicherung ändern kannst:

```python
import matplotlib.pyplot as plt

# Erstelle deinen Plot
plt.plot([1, 2, 3, 4], [1, 4, 9, 16])

# Setze die DPI auf 300 für eine höhere Auflösung
plt.savefig('mein_plot.png', dpi=300)
```

## Praxis

Jetzt ist es an der Zeit, dein erlangtes Wissen in die Praxis umzusetzen! Hier ist eine leichte Aufgabe, gefolgt von einer schwierigeren Aufgabe:

### Aufgabe 1

Erstelle einen einfachen Plot mit Matplotlib, der eine Linie von x = 0 bis x = 5 mit den entsprechenden y-Werten darstellt. Speichere den Plot als JPEG-Datei mit dem Namen "mein_plot.jpg".

Hier ist eine Musterlösung:

```python
import matplotlib.pyplot as plt

# Erstelle den Plot
x = [0, 1, 2, 3, 4, 5]
y = [0, 2, 4, 6, 8, 10]
plt.plot(x, y)

# Speichere den Plot als JPEG-Datei
plt.savefig('mein_plot.jpg')
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Grundlagen_des_Plottings/Speichern_und_Exportieren_von_Plots/ms_aufgabe1.png)

### Aufgabe 2

Erstelle einen fortgeschrittenen Plot mit Matplotlib, der zwei Linien darstellt: eine Sinuswelle und eine Kosinuswelle im Bereich von 0 bis 2π. Speichere den Plot als SVG-Datei mit dem Namen "fortgeschrittener_plot.svg".

Hier ist eine Musterlösung:

```python
import numpy as np
import matplotlib.pyplot as plt

# Erstelle den Plot
x = np.linspace(0, 2*np.pi, 100)
y_sin = np.sin(x)
y_cos = np.cos(x)

plt.plot(x, y_sin, label='Sinus')
plt.plot(x, y_cos, label='Kosinus')
plt.legend()

# Speichere den Plot als SVG-Datei
plt.savefig('fortgeschrittener_plot.svg')
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Grundlagen_des_Plottings/Speichern_und_Exportieren_von_Plots/ms_aufgabe2.png)

## Fazit
Herzlichen Glückwunsch! Du hast erfolgreich gelernt, wie man Plots mit Matplotlib in Python speichert und exportiert. Jetzt kannst du deine Visualisierungen auf verschiedene Weise nutzen und sie mit anderen teilen.

Viel Spaß beim Plotten und Teilen deiner Kreationen!

## Links / Weiteres Material
### Dokumentation
### W3Schools
### YouTube