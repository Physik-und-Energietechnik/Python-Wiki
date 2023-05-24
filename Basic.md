## Scatter
Ein Scatter Plot (Streudiagramm) ist eine Art von Diagramm, das in der Datenvisualisierung verwendet wird, um die Beziehung zwischen zwei numerischen Variablen zu zeigen. In einem Scatter Plot werden Datenpunkte als einzelne Punkte auf einem Koordinatensystem dargestellt, wobei die x- und y-Koordinaten jeweils den Wert der entsprechenden Variablen repräsentieren.

Der Matplotlib Scatter Plot ist eine Funktion der Matplotlib-Bibliothek in Python, die es ermöglicht, Scatter Plots einfach zu erstellen und anzupassen. Dieses Diagramm eignet sich besonders gut, um Korrelationen, Muster oder Trends zwischen zwei Variablen zu visualisieren.

Der Scatter Plot wird oft für die folgenden Zwecke verwendet:

1. Darstellung von Zusammenhängen: Ein Scatter Plot kann verwendet werden, um die Beziehung zwischen zwei Variablen zu zeigen. Zum Beispiel kann man untersuchen, ob es einen Zusammenhang zwischen der Anzahl der Arbeitsstunden und dem erzielten Umsatz gibt.

2. Identifizierung von Ausreißern: Scatter Plots können dabei helfen, Ausreißer in den Daten zu identifizieren. Ausreißer sind Datenpunkte, die sich stark von der allgemeinen Verteilung abheben und potenziell Fehler oder ungewöhnliche Ereignisse darstellen können.

3. Gruppierung oder Klassifizierung: Scatter Plots können verwendet werden, um verschiedene Gruppen oder Klassen von Datenpunkten zu unterscheiden. Jede Gruppe kann mit einer anderen Farbe oder einem anderen Symbol dargestellt werden, um Muster oder Unterschiede zwischen den Gruppen zu visualisieren.

4. Visualisierung von mehrdimensionalen Daten: Scatter Plots können auch genutzt werden, um mehrdimensionale Daten darzustellen, indem sie zusätzliche Dimensionen durch die Größe der Datenpunkte oder durch Farben codieren.

Insgesamt ist der Scatter Plot ein leistungsstarkes Werkzeug, um Muster und Beziehungen zwischen Variablen zu erkunden und zu visualisieren. Matplotlib bietet eine einfache Möglichkeit, Scatter Plots in Python zu erstellen und anzupassen, und ist daher bei Datenanalysten und Data Scientists sehr beliebt.

Hier ist ein einfaches Beispiel, das dir zeigt, wie du mit Matplotlib einen Scatter-Graphen erstellen kannst:

```python
import matplotlib.pyplot as plt

# Beispiel-Daten
x = [1, 2, 3, 4, 5]  # X-Koordinaten
y = [2, 4, 6, 8, 10]  # Y-Koordinaten

# Scatter-Graphen erstellen
plt.scatter(x, y)

# Diagramm beschriften
plt.title('Beispiel Scatter-Graph')
plt.xlabel('X-Achse')
plt.ylabel('Y-Achse')

# Diagramm anzeigen
plt.show()
```

In diesem Beispiel werden zwei einfache Listen `x` und `y` als Beispiel-Daten verwendet. Du kannst diese Listen mit deinen eigenen Daten aktualisieren. 

Der `plt.scatter()`-Befehl erstellt den Scatter-Graphen, indem er die x- und y-Koordinaten als Argumente annimmt.

Mit den Funktionen `plt.title()`, `plt.xlabel()` und `plt.ylabel()` kannst du das Diagramm beschriften und die Titel und Achsenbeschriftungen anpassen.

Der Befehl `plt.show()` zeigt das erstellte Diagramm an.
