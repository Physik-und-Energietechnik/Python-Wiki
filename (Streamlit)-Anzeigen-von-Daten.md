## Einführung
Willkommen zu unserem Python-Tutorial für Streamlit! In diesem Tutorial werden wir gemeinsam lernen, wie man mit Streamlit Daten in ansprechender Weise visualisieren und präsentieren kann. Streamlit ist ein einfaches und zugängliches Framework, das uns dabei hilft, interaktive Webanwendungen zu erstellen, ohne uns mit komplexem Code herumschlagen zu müssen.

Nach Abschluss dieses Tutorials wirst du in der Lage sein, beeindruckende Datenvisualisierungen zu erstellen und diese mit anderen zu teilen. Du wirst in der Lage sein, komplexe Daten auf eine verständliche Art und Weise darzustellen und dein Publikum mit deinen fesselnden Anwendungen zu begeistern.

## Theorie
Streamlit bietet verschiedene Möglichkeiten, um Daten ansprechend darzustellen. Hier sind einige Beispiele für die Darstellung von Daten in Streamlit:

### Text anzeigen
Du kannst Text mit Streamlit anzeigen, um Informationen zu erklären oder Kontext zu geben. Verwende dazu die Funktion `st.write()` oder `st.text()`.

```python
import streamlit as st

# Text anzeigen
st.title("Willkommen zu meiner Streamlit-App")
st.write("Hier sind einige Daten, die ich mit dir teilen möchte:")
```

### Tabellen anzeigen
Mit Streamlit kannst du Daten in Tabellenform darstellen. Du kannst entweder eine Pandas-Datenframe verwenden oder eine Tabelle direkt mit `st.table()` erstellen.

```python
import streamlit as st
import pandas as pd

# Daten laden
data = pd.read_csv("data.csv")

# Tabelle anzeigen
st.table(data)
```

### Diagramme anzeigen
Streamlit bietet Unterstützung für verschiedene Diagrammtypen, einschließlich Linien-, Balken-, Säulen- und Kreisdiagrammen. Du kannst Bibliotheken wie Matplotlib oder Plotly verwenden, um Diagramme zu erstellen.

```python
import streamlit as st
import pandas as pd
import matplotlib.pyplot as plt

# Daten laden
data = pd.read_csv("data.csv")

# Diagramm anzeigen
plt.plot(data["X"], data["Y"])
st.pyplot()
```

### Karten anzeigen
Wenn du geografische Daten hast, kannst du sie mit Streamlit auf interaktiven Karten anzeigen. Du kannst Bibliotheken wie Folium oder Plotly verwenden, um Karten zu erstellen.

```python
import streamlit as st
import pandas as pd
import folium
from streamlit_folium import folium_static

# Karte erstellen
m = folium.Map(location=[51.5074, -0.1278], zoom_start=12)
folium.Marker([51.5074, -0.1278], popup="London").add_to(m)

# Karte anzeigen
folium_static(m)
```

## Praxis
Jetzt lass uns das Gelernte in die Praxis umsetzen. Du bist bereit für eine kleine Aufgabe!

### Aufgabe
Zeige mithilfe einer Karte eine beliebige Stadt an.

#### Musterlösung
Schau dir die Musterlösung an, um zu sehen, wie man die Aufgabe lösen kann:

```python
import streamlit as st
import pandas as pd
import folium
from streamlit_folium import folium_static

# Karte erstellen
m = folium.Map(location=[51.5074, -0.1278], zoom_start=12)
folium.Marker([51.5074, -0.1278], popup="London").add_to(m)

# Karte anzeigen
folium_static(m)
```

Hinweis: Stelle sicher, dass du deine eigene CSV-Datei mit dem richtigen Dateinamen in den Code einfügst.

## Fazit
Herzlichen Glückwunsch, du hast erfolgreich gelernt, wie man Daten mit Streamlit in Python visualisiert! Du kannst jetzt beeindruckende interaktive Anwendungen erstellen, die deine Daten zum Leben erwecken. Streamlit macht es einfach, deine Ideen mit anderen zu teilen und deine Präsentationen auf ein neues Level zu heben.

Wir haben in diesem Tutorial die Grundlagen von Streamlit abgedeckt, aber es gibt noch viel mehr zu entdecken. Experimentiere weiter mit den verschiedenen Funktionen und erweitere dein Wissen, um noch beeindruckendere Streamlit-Anwendungen zu erstellen.

Viel Spaß beim Programmieren und lass deiner Kreativität freien Lauf!