## Matplotlib - Der boxplot Plot

### Einführung

Willkommen zurück, liebe Python-Neulinge! In diesem Abschnitt werden wir uns mit einem spannenden Aspekt von Matplotlib beschäftigen - dem boxplot Plot. Du fragst dich vielleicht, was das überhaupt ist und wofür man ihn benutzt. Keine Sorge, wir werden dir alles erklären!

Der boxplot Plot ist ein mächtiges Werkzeug zur Visualisierung von Daten. Er hilft uns dabei, die Verteilung und statistische Eigenschaften eines Datensatzes auf einen Blick zu erfassen. Mit diesem Wissen können wir interessante Erkenntnisse gewinnen und Muster in unseren Daten entdecken.

### Theorie

Bevor wir jedoch direkt in die Praxis eintauchen, lassen uns zunächst die Theorie hinter dem boxplot Plot verstehen. Keine Sorge, wir werden es so verständlich wie möglich erklären!

Der boxplot besteht aus einer Box und einigen Linien, die über unsere Daten "streuen". Die Box repräsentiert den Interquartilsbereich (IQR), also den Bereich, in dem die mittleren 50% unserer Daten liegen. Die Linien, die aus der Box herausragen, werden als "Whiskers" bezeichnet und zeigen uns die Streuung der Daten außerhalb des IQRs.

Um das Ganze noch anschaulicher zu machen, werfen wir einen Blick auf das allgemeine Code-Beispiel:

```python
import matplotlib.pyplot as plt

# Daten für den boxplot
data = [1, 2, 3, 3, 4, 4, 4, 5, 6, 7, 8]

# Erstellen des boxplots
plt.boxplot(data)

# Anzeigen des Plots
plt.show()
```

Siehst du? Der Code ist gar nicht so gruselig, wie er auf den ersten Blick erscheinen mag! Dieses Beispiel zeigt uns einen einfachen boxplot für eine Liste von Daten. Die y-Achse zeigt die Werte unserer Daten an, während die x-Achse nur zur Veranschaulichung der verschiedenen boxplots dient, falls wir mehrere davon haben.

Jetzt wollen wir natürlich auch ein explizites Code-Beispiel sehen, das dir die Anwendung des boxplot Plots näherbringt:

```python
import matplotlib.pyplot as plt
import numpy as np

# Generieren von zufälligen Daten für drei Gruppen
np.random.seed(42)
data1 = np.random.normal(100, 10, 200)
data2 = np.random.normal(90, 20, 200)
data3 = np.random.normal(80, 30, 200)
data = [data1, data2, data3]

# Erstellen des boxplots mit Labels für die Gruppen
plt.boxplot(data, labels=['Gruppe 1', 'Gruppe 2', 'Gruppe 3'])

# Anzeigen des Plots
plt.show()
```

In diesem Beispiel erzeugen wir drei Gruppen von zufälligen Daten und erstellen einen boxplot, der uns die Verteilung dieser Gruppen zeigt. Beachte, dass wir auch Labels für die Gruppen hinzufügen, damit wir die einzelnen Boxen besser identifizieren können.

### Praxis

Nun, da wir die Theorie hinter dem boxplot Plot kennen, wird es Zeit, unser Wissen in die Praxis umzusetzen! Lass uns mit einer leichten Aufgabe beginnen:

**Auf

gabe:** Du hast eine Liste von Noten für einen Test erhalten. Erstelle einen boxplot, um die Verteilung der Noten zu visualisieren.

Musterlösung:

```python
import matplotlib.pyplot as plt

# Liste der Noten
grades = [75, 80, 85, 90, 95, 100]

# Erstellen des boxplots für die Noten
plt.boxplot(grades)

# Anzeigen des Plots
plt.show()
```

Und voilà! Du hast erfolgreich einen boxplot erstellt, der dir die Verteilung der Noten zeigt. Du kannst jetzt auf einen Blick sehen, ob die Noten konzentriert sind oder ob es Ausreißer gibt.

Für diejenigen unter euch, die eine größere Herausforderung suchen, haben wir hier eine schwierigere Aufgabe:

**Aufgabe:** Du hast Daten über die Verkaufszahlen von drei verschiedenen Produkten. Erstelle einen boxplot, um die Verteilung der Verkaufszahlen pro Produkt zu vergleichen. Vergiss nicht, Labels für die Produkte hinzuzufügen.

Musterlösung:

```python
import matplotlib.pyplot as plt
import numpy as np

# Generieren von zufälligen Verkaufszahlen für drei Produkte
np.random.seed(42)
product1 = np.random.normal(1000, 100, 200)
product2 = np.random.normal(900, 200, 200)
product3 = np.random.normal(800, 300, 200)

# Daten für den boxplot
data = [product1, product2, product3]

# Erstellen des boxplots mit Labels für die Produkte
plt.boxplot(data, labels=['Produkt 1', 'Produkt 2', 'Produkt 3'])

# Anzeigen des Plots
plt.show()
```

Fantastisch! Du hast es geschafft, einen boxplot zu erstellen, der die Verkaufszahlen der drei Produkte vergleicht. Jetzt kannst du leicht erkennen, ob es Unterschiede in den Verteilungen gibt und wie die Verkaufszahlen für jedes Produkt variieren.

Das war's für den Abschnitt über den boxplot Plot in Matplotlib! Wir hoffen, dass du jetzt ein besseres Verständnis dafür hast, wie dieser Plot funktioniert und wie du ihn für deine eigenen Daten verwenden kannst. Also, schnapp dir deine Daten und lass uns an die Arbeit gehen!

Happy plotting! 📊