## Einführung
In diesem Abschnitt werden wir uns mit einer leistungsstarken Bibliothek namens NumPy beschäftigen, die uns dabei hilft, Daten effizient zu verarbeiten und komplexe Berechnungen durchzuführen. Konkret werden wir uns auf n-dimensionale Arrays konzentrieren, die uns erlauben, Daten in Form von Tabellen oder Matrizen zu speichern.

Nachdem du diesen Abschnitt abgeschlossen hast, wirst du in der Lage sein, n-dimensionale Arrays zu erstellen, darauf zuzugreifen und verschiedene Operationen damit durchzuführen. Du wirst feststellen, dass NumPy eine unverzichtbare Bibliothek für viele wissenschaftliche und datenverarbeitende Anwendungen ist. Ob du nun Daten analysieren, Bilder bearbeiten oder komplexe mathematische Berechnungen durchführen möchtest – n-dimensionale Arrays werden dir dabei helfen, diese Aufgaben auf elegante Weise zu lösen.

Also, lass uns loslegen und das Potenzial von NumPy n-dimensionalen Arrays erkunden!

## Theorie
Bevor wir uns in die Praxis stürzen, wollen wir ein bisschen Theorie betrachten. N-dimensionale Arrays sind wie Superhelden für Daten – sie können riesige Mengen von Informationen speichern und verarbeiten. Denk an ein n-dimensionales Array wie an eine riesige Schachtel voller Werte. Diese Werte können Zahlen, Texte oder sogar Bilder sein!

Lass uns zuerst ein allgemeines Code-Beispiel betrachten, um das Konzept zu verdeutlichen:

```python
# Allgemeines Code-Beispiel
array = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
```
Das ist ein zweidimensionales Array, das wie eine Tabelle aussieht. Es hat drei Zeilen und drei Spalten. Du kannst auf die einzelnen Werte zugreifen, indem du den Index der Zeile und den Index der Spalte angibst. Zum Beispiel gibt array[0][0] den Wert 1 zurück.

Jetzt wollen wir uns ein explizites Code-Beispiel direkt in Python anschauen:

```python
# Explizites Code-Beispiel
import numpy as np

array = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
```
Hier haben wir NumPy importiert und ein n-dimensionales Array erstellt. Beachte, dass wir den np.array()-Befehl verwenden, um die Liste in ein NumPy-Array umzuwandeln. NumPy bietet uns viele praktische Funktionen und Methoden, um mit n-dimensionalen Arrays zu arbeiten.

## Aufgabe 1
Jetzt ist es Zeit, unser erlangtes Wissen in die Praxis umzusetzen! Hier ist eine leichte Aufgabe für dich:

Erstelle ein n-dimensionales Array mit den Zahlen von 1 bis 10 und gib die Summe aller Zahlen aus.

Lösung:

```python
import numpy as np

array = np.arange(1, 11)
summe = np.sum(array)

print(f"Die Summe aller Zahlen beträgt: {summe}")
```
## Aufgabe 2

Erstelle ein 3x3 n-dimensionales Array und multipliziere es mit einem Vektor [1, 2, 3]. Gib das Ergebnis aus.

Hier ist eine mögliche Lösung:

```python
import numpy as np

matrix = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
vector = np.array([1, 2, 3])
result = np.dot(matrix, vector)

print("Das Ergebnis der Matrix-Vektor-Multiplikation ist:")
print(result)
```
Herzlichen Glückwunsch! Du hast erfolgreich n-dimensionale Arrays in NumPy kennengelernt und zwei Aufgaben gelöst. Du kannst nun komplexere Datenstrukturen erstellen und damit fortgeschrittene Berechnungen durchführen. NumPy ist wirklich ein mächtiges Werkzeug für jeden Python-Enthusiasten!

Viel Spaß beim Experimentieren mit n-dimensionalen Arrays in NumPy!

## Weiterführende Links
