## Einführung

Willkommen in der aufregenden Welt von Streamlit! Hast du jemals davon geträumt, beeindruckende Datenvisualisierungen zu erstellen oder interaktive Webanwendungen zu entwickeln? Nun, Streamlit ist der Superheld, der dir dabei hilft, deine Träume wahr werden zu lassen.

In diesem Tutorial werden wir Schritt für Schritt lernen, wie man Streamlit verwendet, um benutzerfreundliche Anwendungen zu erstellen. Du wirst lernen, wie du Widgets einsetzen kannst, um mit deinen Benutzern zu interagieren, wie du Daten präsentierst und sogar wie du deine App bereitstellst. Am Ende dieses Tutorials wirst du in der Lage sein, atemberaubende Streamlit-Anwendungen zu erstellen und der Welt zu zeigen, was du drauf hast!

## Theorie

### Streamlit-Grundlagen

Bevor wir richtig loslegen, lass uns kurz über einige grundlegende Konzepte sprechen, die du verstehen musst, um Streamlit zu nutzen. 

Streamlit basiert auf dem Konzept von "Scripts". Ein Streamlit-Skript ist ein einfaches Python-Skript, in dem du deine App erstellst. Es folgt einem einfachen sequentiellen Ablauf, in dem du den Code von oben nach unten schreibst.

Hier ist ein allgemeines Code-Beispiel, das dir eine Vorstellung davon gibt, wie ein Streamlit-Skript aussieht:

```python
# Importiere das Streamlit-Modul
import streamlit as st

# Erstelle eine Überschrift
st.title("Meine erste Streamlit-App")

# Eingabe einer Zahl
number = st.number_input("Gib eine Zahl ein:")

# Zahl ausgeben
st.write(f"Deine Zahl: {number:.2f}")
```
Dieses Beispiel soll dir einen ersten Eindruck davon geben, wie Streamlit funktioniert. Nun lass uns weitermachen und einige praktische Übungen machen!

In Streamlit kannst du verschiedene Widgets verwenden, um mit deinen Benutzern zu interagieren. Widgets sind Elemente wie Schieberegler, Auswahlmenüs oder Texteingabefelder. Du kannst sie verwenden, um Eingaben von deinen Benutzern zu erhalten und entsprechend darauf zu reagieren.

## Praxis

### Aufgabe: BMI-Rechner

Für unsere erste Übung werden wir einen einfachen BMI-Rechner erstellen. Du wirst in der Lage sein, dein Gewicht und deine Größe einzugeben, und Streamlit wird deinen BMI berechnen. Versuche, diesen Code in deinem Streamlit-Skript auszuführen und spiele mit verschiedenen Gewichts- und Größenwerten herum, um den BMI zu berechnen.

**Musterlösung:**

```python
# Importiere das Streamlit-Modul
import streamlit as st

# Erstelle eine Überschrift
st.title("BMI-Rechner")

# Frage den Benutzer nach Gewicht und Größe
weight = st.number_input("Gib dein Gewicht in kg ein:")
height = st.number_input("Gib deine Größe in cm ein:")

# Berechne den BMI
bmi = weight / ((height/100) ** 2)

# Zeige den berechneten BMI an
st.write(f"Dein BMI beträgt: {bmi:.2f}")
```

## Fazit

Herzlichen Glückwunsch! Du hast erfolgreich die Grundlagen von Streamlit gelernt und gesehen, wie einfach es ist, interaktive Webanwendungen zu erstellen. Du hast gelernt, wie man Widgets verwendet, Daten präsentiert und sogar Verkaufsprognosen erstellt.

Streamlit bietet dir viele weitere Möglichkeiten, deine Apps zu erweitern und anzupassen. Experimentiere mit verschiedenen Widgets, füge weitere Diagramme hinzu und werde kreativ! Die Möglichkeiten sind endlos.

Ich hoffe, dieses Tutorial hat dir Spaß gemacht und dich inspiriert, Streamlit weiter zu erkunden. Viel Erfolg bei deinen zukünftigen Streamlit-Projekten!