## Einführung

In diesem Tutorial wirst du lernen, wie du Legenden zu deinen Diagrammen hinzufügen kannst, um sie besser verständlich und ansprechender zu machen. 

Eine Legende ist eine kurze Erklärung, die den Inhalt eines Diagramms erläutert. Sie zeigt, welche Linien oder Markierungen zu welchen Daten gehören. Das ist besonders hilfreich, wenn du mehrere Datenreihen in einem Diagramm darstellst.

Nach diesem Tutorial wirst du in der Lage sein, deine Diagramme aufzupeppen und anderen zu zeigen, wie toll du mit deinen Daten umgehen kannst! Also schnall dich an und lass uns loslegen!

## Theorie

### Was ist eine Legende?

Eine Legende ist wie ein Kompass für dein Diagramm. Sie erklärt, was die verschiedenen Farben, Linien und Symbole bedeuten. Stell dir vor, du zeigst jemandem dein Diagramm und er sagt: "Wow, das ist ja ein wunderschönes Diagramm! Aber was bedeuten denn die verschiedenen Linien?" Anstatt eine lange Erklärung abzugeben, kannst du einfach auf deine Legende verweisen und alle sind glücklich.

### Wie füge ich eine Legende hinzu?

Um eine Legende in Matplotlib hinzuzufügen, gibt es verschiedene Möglichkeiten. Eine einfache Methode besteht darin, jedem Element in deinem Diagramm eine Beschriftung zu geben und dann die Funktion `legend()` aufzurufen. Diese Funktion wird automatisch eine Legende erstellen, basierend auf den Beschriftungen der Elemente.

Hier ist ein allgemeines Code-Beispiel, um dir eine Vorstellung davon zu geben:

```python
import matplotlib.pyplot as plt

# Daten für das Diagramm
x = [1, 2, 3, 4]
y1 = [1, 4, 9, 16]
y2 = [1, 2, 3, 4]

# Diagramm zeichnen
plt.plot(x, y1, label='Datenreihe 1')
plt.plot(x, y2, label='Datenreihe 2')

# Legende hinzufügen
plt.legend()

# Diagramm anzeigen
plt.show()
```

Und hier ist das explizite Code-Beispiel für dieses Tutorial:

```python
import matplotlib.pyplot as plt

# Daten für das Diagramm
x = [1, 2, 3, 4]
y1 = [1, 4, 9, 16]
y2 = [1, 2, 3, 4]

# Diagramm zeichnen
plt.plot(x, y1, label='Datenreihe 1')
plt.plot(x, y2, label='Datenreihe 2')

# Legende hinzufügen
plt.legend()

# Diagramm anzeigen
plt.show()
```

## Praxis

### Aufgabe 1

Zeichne ein einfaches Linien-Diagramm mit zwei Datenreihen: x = [1, 2, 3, 4] und y1 = [1, 3, 5, 7], y2 = [2, 4, 6, 8]. Füge dann eine passende Legende hinzu, um die Datenreihen zu kennzeichnen.

#### Musterlösung

```python
import matplotlib.pyplot as plt

# Daten für das Diagramm
x = [1, 2, 3, 4]
y1 = [1, 3, 5, 7]
y2 = [2, 4, 6, 8]

# Diagramm zeichnen
plt.plot(x, y1, label='Datenreihe 1')
plt.plot(x, y2, label='Datenreihe 2')

# Legende hinzufügen
plt.legend()

# Diagramm anzeigen
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Grundlagen_des_Plottings/Hinzufuegen_von_Legenden/ms_aufgabe1.png)

### Aufgabe 2

Zeichne ein Streudiagramm mit den folgenden Datenpunkten: x = [1, 2, 3, 4] und y = [4, 7, 2, 6]. Verwende verschiedene Farben und Formen für die Datenpunkte und füge eine aussagekräftige Legende hinzu.

#### Musterlösung

```python
import matplotlib.pyplot as plt

# Daten für das Diagramm
x = [1, 2, 3, 4]
y = [4, 7, 2, 6]

# Diagramm zeichnen
plt.scatter(x, y, color='red', marker='o', label='Datenpunkte')

# Legende hinzufügen
plt.legend()

# Diagramm anzeigen
plt.show()
```

![](https://github.com/janehlenb/Projektarbeit-ChatGPT-Python/blob/main/Images/Darstellung/Grundlagen_des_Plottings/Hinzufuegen_von_Legenden/ms_aufgabe2.png)

## Fazit
Herzlichen Glückwunsch! Du hast erfolgreich gelernt, wie man Legenden zu Diagrammen in Matplotlib hinzufügt. Jetzt kannst du deine Daten visualisieren und anderen zeigen, wie cool du bist!

## Links / Weiteres Material
### Dokumentation
### W3Schools
### YouTube
