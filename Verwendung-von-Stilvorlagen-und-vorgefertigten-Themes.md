## Einführung
Willkommen zu unserem Python-Tutorial über die Verwendung von Stilvorlagen und vorgefertigten Themes in Matplotlib! In diesem Abschnitt werden wir uns mit einem spannenden Aspekt von Matplotlib befassen - der Anpassung des Erscheinungsbilds unserer Diagramme mithilfe von Stilvorlagen und vorgefertigten Themes.

Durch die Verwendung von Stilvorlagen und vorgefertigten Themes können wir einfach und effektiv das Aussehen unserer Diagramme ändern, ohne viel Code schreiben zu müssen. Wir werden lernen, wie wir verschiedene Stile anwenden können, um unsere Diagramme zu verbessern und ihnen eine persönliche Note zu verleihen.

## Theorie
### Stilvorlagen
Stilvorlagen sind vorgefertigte Konfigurationen, mit denen wir das Erscheinungsbild unserer Diagramme anpassen können. Matplotlib bietet eine Vielzahl von Stilvorlagen, die von einfachen bis hin zu speziellen Designs reichen. Diese Stilvorlagen ändern Aspekte wie Farbschemata, Linienstile, Hintergründe und vieles mehr.

Hier ist ein allgemeines Beispiel, wie wir eine Stilvorlage in Matplotlib verwenden können:

```python
import matplotlib.pyplot as plt

plt.style.use('stylename')
```

Und hier ist ein explizites Beispiel, bei dem wir die 'ggplot'-Stilvorlage anwenden:

```python
import matplotlib.pyplot as plt

plt.style.use('ggplot')
```

### Vorgefertigte Themes
Vorgefertigte Themes sind eine weitere Möglichkeit, das Erscheinungsbild unserer Diagramme anzupassen. Ein Theme ist eine Kombination aus Stilvorlagen und weiteren Anpassungen, die auf eine bestimmte Art von Diagrammen zugeschnitten sind. Es gibt verschiedene vorgefertigte Themes in Matplotlib, wie zum Beispiel 'dark_background', 'seaborn', 'ggplot' und viele mehr.

Hier ist ein allgemeines Beispiel, wie wir ein vorgefertigtes Theme in Matplotlib verwenden können:

```python
import matplotlib.pyplot as plt

plt.style.use('theme_name')
```

Und hier ist ein explizites Beispiel, bei dem wir das 'dark_background'-Theme verwenden:

```python
import matplotlib.pyplot as plt

plt.style.use('dark_background')
```

## Praxis
Jetzt wollen wir unser erlangtes Wissen über Stilvorlagen und vorgefertigte Themes in die Praxis umsetzen. Hier sind zwei Aufgaben für dich:

### Aufgabe 1
Verwende die 'seaborn-v0_8'-Stilvorlage, um ein einfaches Liniendiagramm zu erstellen, das die Anzahl der verkauften Einheiten über einen Zeitraum von 10 Tagen darstellt. Du kannst fiktive Daten verwenden. Verleihe dem Diagramm eine Überschrift und benenne die Achsen.

Hier ist eine Musterlösung:

```python
import matplotlib.pyplot as plt
import numpy as np

plt.style.use('seaborn-v0_8')

# Daten generieren
tage = np.arange(1, 11)
verkaufte_einheiten = np.random.randint(100, 1000, size=10)

# Diagramm erstellen
plt.plot(tage, verkauf

te_einheiten)
plt.title('Verkaufte Einheiten über 10 Tage')
plt.xlabel('Tage')
plt.ylabel('Verkaufte Einheiten')

# Diagramm anzeigen
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Anpassungen_und_Stilisierung/Verwendung_von_Stilvorlagen_und_vorgefertigten_Themes/ms_aufgabe1.png)

### Aufgabe 2
Verwende das 'ggplot'-Theme, um ein gestapeltes Säulendiagramm zu erstellen, das den Umsatz nach Produktkategorien für einen bestimmten Monat darstellt. Du kannst wieder fiktive Daten verwenden. Füge eine Legende hinzu, um die Produktkategorien zu kennzeichnen.

Hier ist eine Musterlösung:

```python
import matplotlib.pyplot as plt

plt.style.use('ggplot')

# Daten generieren
produkte = ['Produkt A', 'Produkt B', 'Produkt C']
umsatz = [4000, 2500, 6000]

# Diagramm erstellen
plt.bar(produkte, umsatz)
plt.title('Umsatz nach Produktkategorien')
plt.xlabel('Produktkategorien')
plt.ylabel('Umsatz')

# Legende hinzufügen
plt.legend(['Umsatz'])

# Diagramm anzeigen
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Anpassungen_und_Stilisierung/Verwendung_von_Stilvorlagen_und_vorgefertigten_Themes/ms_aufgabe2.png)

## Fazit
Viel Spaß beim Ausprobieren und Anpassen der Stilvorlagen und vorgefertigten Themes in Matplotlib! Experimentiere und finde deinen eigenen Stil, um deine Diagramme zum Leben zu erwecken.