## Einführung
Willkommen zu unserem Python-Tutorial über Streamlit und interaktive Widgets! In diesem Tutorial werden wir dir zeigen, wie du mit Streamlit beeindruckende Webanwendungen erstellen kannst, die mit deinen Benutzern interagieren. Streamlit ist eine einfache und intuitive Bibliothek, die es dir ermöglicht, Datenvisualisierungen, Dashboards und mehr zu erstellen, ohne dich um das komplizierte Backend kümmern zu müssen. 

Am Ende dieses Tutorials wirst du in der Lage sein, interaktive Widgets wie Schieberegler, Dropdown-Menüs und Texteingabefelder zu erstellen und sie mit deinem Code zu verbinden. Du wirst auch lernen, wie du Daten anzeigen, das Layout deiner App anpassen und sogar fortgeschrittene Funktionen wie Caching nutzen kannst.

## Theorie

### Was sind interaktive Widgets?
Interaktive Widgets sind Elemente, die es deinen Benutzern ermöglichen, mit deiner Streamlit-App zu interagieren. Sie dienen dazu, Eingaben entgegenzunehmen, Optionen auszuwählen oder Parameter anzupassen, um die Ausgabe der App dynamisch zu verändern. Widgets können eine Vielzahl von Formen haben, wie Schieberegler, Auswahlmenüs, Checkboxen und mehr.

Hier ist ein allgemeines Beispiel eines Dropdown-Menüs in Streamlit:
```python
import streamlit as st

# Dropdown-Menü definieren
option = st.selectbox("Wähle eine Option", ["Option 1", "Option 2", "Option 3"])

# Ausgabe basierend auf der ausgewählten Option
if option == "Option 1":
    st.write("Du hast Option 1 ausgewählt.")
elif option == "Option 2":
    st.write("Du hast Option 2 ausgewählt.")
else:
    st.write("Du hast Option 3 ausgewählt.")
```

### Weitere interaktive Widgets
Streamlit bietet eine Vielzahl von interaktiven Widgets, die du in deiner App verwenden kannst. Hier sind einige Beispiele:

- Schieberegler: Ermöglicht es Benutzern, einen Wert innerhalb eines bestimmten Bereichs auszuwählen.
```python
import streamlit as st

# Schieberegler definieren
value = st.slider("Wähle einen Wert", min_value=0, max_value=100, value=50)

# Ausgabe basierend auf dem ausgewählten Wert
st.write("Du hast den Wert", value, "ausgewählt.")
```

- Texteingabefeld: Ermöglicht es Benutzern, Text einzugeben.
```python
import streamlit as st

# Texteingabefeld definieren
name = st.text_input("Gib deinen Namen ein")

# Ausgabe des eingegebenen Namens
st.write("Hallo", name)
```

- Radio-Buttons: Ermöglicht es Benutzern, eine Option aus einer Reihe von Optionen aus

zuwählen.
```python
import streamlit as st

# Radio-Buttons definieren
option = st.radio("Wähle eine Option", ["Option 1", "Option 2", "Option 3"])

# Ausgabe basierend auf der ausgewählten Option
st.write("Du hast", option, "ausgewählt.")
```

- Button: Ermöglicht es Benutzern, eine Aktion auszulösen.
```python
import streamlit as st

# Button definieren
button_clicked = st.button("Klick mich!")

# Ausgabe basierend auf dem Zustand des Buttons
if button_clicked:
    st.write("Der Button wurde geklickt!")
```

- Multiselect: Ermöglicht es Benutzern, mehrere Optionen aus einer Liste auszuwählen.
```python
import streamlit as st

# Multiselect definieren
selected_options = st.multiselect("Wähle mehrere Optionen", ["Option 1", "Option 2", "Option 3"])

# Ausgabe der ausgewählten Optionen
st.write("Du hast folgende Optionen ausgewählt:", selected_options)
```

- Checkbox: Ermöglicht es Benutzern, eine oder mehrere Checkboxen auszuwählen.
```python
import streamlit as st

# Checkbox definieren
checked = st.checkbox("Ich stimme den Nutzungsbedingungen zu")

# Ausgabe basierend auf dem Zustand der Checkbox
if checked:
    st.write("Vielen Dank für deine Zustimmung!")
```

- Number Input: Ermöglicht es Benutzern, numerische Werte einzugeben.
```python
import streamlit as st

# Number Input definieren
number = st.number_input("Gib eine Zahl ein", min_value=0, max_value=100, value=50)

# Ausgabe des eingegebenen Werts
st.wrte("Du hast die Zahl", number, "eingegeben.")
```

- File Uploader: Ermöglicht es Benutzern, Dateien hochzuladen.
```python
import streamlit as st

# File Uploader definieren
uploaded_file = st.file_uploader("Lade eine Datei hoch")

# Ausgabe basierend auf der hochgeladenen Datei
if uploaded_file is not None:
    st.write("Du hast folgende Datei hochgeladen:", uploaded_file.name)
```
### Hinweis
Beachte, dass es noch weitere Widgets für Streamlit gibt, welche hier nicht aufgelistet wurden.

## Praxis

### Leichte Aufgabe: BMI-Rechner
Lass uns dein erlerntes Wissen über interaktive Widgets in die Praxis umsetzen! Deine Aufgabe besteht darin, einen einfachen BMI-Rechner zu erstellen. Der Benutzer soll sein Gewicht und seine Körpergröße eingeben können, und die App berechnet dann den BMI-Wert und gibt eine Empfehlung aus.

Hier ist eine Musterlösung für den BMI-Rechner:
```python
# Importiere das Streamlit-Modul
import streamlit as st

# Gewicht und Körpergröße eingeben
weight = st.number_input("Gib dein Gewicht in kg ein:", value=75.0, step=0.1, format="%.1f", min_value=0.1)
height = st.number_input("Gib deine Körpergröße in cm ein:", value=180, min_value=1)

# BMI berechnen
bmi = weight / ((height / 100) ** 2)

# Empfehlung basierend auf dem BMI-Wert
if bmi < 18.5:
    st.write("Du bist untergewichtig. Iss etwas mehr!")
elif bmi >= 25:
    st.write("Du bist übergewichtig. Vielleicht solltest du auf deine Ernährung achten.")
else:
    st.write("Dein Gewicht ist im normalen Bereich. Gut gemacht!")
```

### Schwierigere Aufgabe: Kreditrechner
Bist du bereit für eine etwas anspruchsvollere Aufgabe? Versuche einen Kreditrechner zu erstellen! Der Benutzer soll den Kreditbetrag, den Zinssatz und die Laufzeit eingeben können, und die App berechnet dann die monatliche Rate und die Gesamtzahlung.

Hier ist eine Musterlösung für den Kreditrechner:
```python
# Importiere das Streamlit-Modul
import streamlit as st

# Kreditbetrag, Zinssatz und Laufzeit eingeben
loan_amount = st.number_input("Gib den Kreditbetrag ein:", format="%.2f", value=1000.00, step=100.00, min_value=100.00, max_value=10000.00)
interest_rate = st.slider("Wähle den Zinssatz (%)", 0.1, 10.0, 5.0, format="%.1f")
loan_term = st.number_input("Gib die Laufzeit in Jahren ein:", format="%.1f", value=5.0, step=0.5, min_value=0.5, max_value=30.0)

# Zinssatz in Dezimalzahl umwandeln
interest_rate = interest_rate / 100

# Monatliche Rate berechnen
monthly_interest_rate = interest_rate / 12
num_payments = loan_term * 12
monthly_payment = (loan_amount * monthly_interest_rate) / (1 - (1 + monthly_interest_rate) ** -num_payments)

# Gesamtzahlung berechnen
total_payment = monthly_payment * num_payments

# Ergebnisse anzeigen
st.write("Monatliche Rate:", f'{monthly_payment:.2f} €')
st.write("Gesamtzahlung:", f'{total_payment:.2f} €')
```

## Fazit
Herzlichen Glückwunsch! Du hast es geschafft, interaktive Widgets in Streamlit zu nutzen und sogar

 einen BMI-Rechner und einen Kreditrechner zu erstellen. Du hast gelernt, wie du Eingaben von Benutzern entgegennimmst, Berechnungen durchführst und Ergebnisse präsentierst. Streamlit ist ein leistungsfähiges Werkzeug, das dir dabei helfen kann, beeindruckende Webanwendungen zu erstellen, ohne dass du dich um das Backend kümmern musst. Jetzt bist du bereit, eigene interaktive Apps zu entwickeln und deine Kreativität einzusetzen!

Wir hoffen, dass dir dieses Tutorial gefallen hat. Viel Spaß beim Entdecken und Entwickeln mit Streamlit!