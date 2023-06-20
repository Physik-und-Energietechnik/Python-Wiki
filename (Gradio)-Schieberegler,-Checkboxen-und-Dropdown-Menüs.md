## Einführung

Herzlich willkommen zu unserem Python-Tutorial! In diesem Abschnitt werden wir uns mit Gradio, einer Bibliothek zur einfachen Erstellung von Benutzeroberflächen für maschinelles Lernen, beschäftigen. Du fragst dich vielleicht, was das mit Python zu tun hat? Nun, Gradio bietet uns eine Möglichkeit, unsere Python-Modelle interaktiv zu nutzen, indem wir Schieberegler, Checkboxen und Dropdown-Menüs verwenden.

In diesem Tutorial lernst du, wie du Schieberegler, Checkboxen und Dropdown-Menüs in Gradio erstellst und diese Funktionen effektiv einsetzt. Du wirst sehen, dass du damit deine Modelle auf eine interaktive und unterhaltsame Weise steuern kannst. Also lass uns loslegen und die Macht der Benutzeroberfläche entfesseln!

## Theorie

### Schieberegler

Schieberegler sind eine großartige Möglichkeit, Werte in einem bestimmten Bereich auszuwählen. Mit ihnen kannst du z. B. die Größe eines Bildes ändern oder den Schwellenwert eines Filters einstellen. Schauen wir uns ein allgemeines Beispiel an, um das Konzept zu verdeutlichen:

```python
# Allgemeines Beispiel - Schieberegler
def slider_example(value):
    print("Ausgewählter Wert:", value)

slider_example(0.5)
```

Das war einfach, oder? Wir haben eine Funktion `slider_example`, die einen Wert `value` akzeptiert und ihn einfach ausgibt. Hier kannst du deine eigenen Werte ausprobieren, indem du den Schieberegler verschiebst.

Jetzt wollen wir das Ganze in Gradio umsetzen:

```python
import gradio as gr

def slider_example(value):
    return f"Ausgewählter Wert: {value}"

iface = gr.Interface(fn=slider_example, inputs="slider", outputs="text")
iface.launch()
```

Führe den Code aus und sieh dir die Schieberegler-Benutzeroberfläche an! Du kannst den Wert anpassen und die Ausgabe beobachten.

### Checkboxen

Checkboxen ermöglichen es uns, Optionen auszuwählen oder abzuwählen. Sie sind besonders nützlich, wenn wir Entscheidungen treffen müssen, die verschiedene Pfade in unserem Code beeinflussen. Hier ist ein allgemeines Beispiel:

```python
# Allgemeines Beispiel - Checkboxen
def checkbox_example(option1, option2):
    if option1:
        print("Option 1 ist aktiviert!")
    if option2:
        print("Option 2 ist aktiviert!")

checkbox_example(True, False)
```

In diesem Beispiel haben wir die Funktion `checkbox_example`, die zwei Optionen `option1` und `option2` akzeptiert und basierend auf deren Zustand eine entsprechende Ausgabe liefert. Probiere es aus, indem du die Optionen änderst!

Jetzt schauen wir uns an, wie wir Checkboxen in Gradio verwenden:

```python
import gradio as gr

def checkbox_example(option1, option2):
    if option1:
        return "Option 1 ist aktiviert!"
    if option2:
        return "Option 2 ist aktiviert!"
    return "Keine Option ausgewählt."

iface = gr.Interface(fn=checkbox_example, inputs=["checkbox", "checkbox"], outputs="text")
iface.launch

()
```

Führe den Code aus und sieh dir die Checkboxen-Benutzeroberfläche an! Du kannst die Optionen an- oder abwählen und die Ausgabe überprüfen.

### Dropdown-Menüs

Dropdown-Menüs bieten uns eine Liste von Optionen, aus denen wir eine einzige Option auswählen können. Sie sind besonders praktisch, wenn wir eine begrenzte Auswahlmöglichkeit haben. Hier ist ein allgemeines Beispiel:

```python
# Allgemeines Beispiel - Dropdown-Menüs
def dropdown_example(option):
    print("Ausgewählte Option:", option)

dropdown_example("Option 2")
```

Hier haben wir die Funktion `dropdown_example`, die eine Option `option` akzeptiert und sie ausgibt. Probiere es aus, indem du verschiedene Optionen auswählst!

Jetzt sehen wir uns an, wie wir Dropdown-Menüs in Gradio verwenden:

```python
import gradio as gr

def dropdown_example(option):
    return f"Ausgewählte Option: {option}"

iface = gr.Interface(fn=dropdown_example, inputs="dropdown", outputs="text", choices=["Option 1", "Option 2", "Option 3"])
iface.launch()
```

Führe den Code aus und sieh dir die Dropdown-Menü-Benutzeroberfläche an! Du kannst eine Option auswählen und die Ausgabe überprüfen.

## Praxis

### Aufgabe 1

Jetzt bist du dran! Schreibe eine Funktion `convert_temperature`, die eine Temperatur in Celsius akzeptiert und sie in Fahrenheit umrechnet. Verwende einen Schieberegler, um die Temperatur auszuwählen, und gib das Ergebnis aus. Hier ist eine Musterlösung:

```python
import gradio as gr

def convert_temperature(celsius_temperature):
    fahrenheit_temperature = celsius_temperature * 9/5 + 32
    return f"Die Temperatur in Fahrenheit beträgt: {fahrenheit_temperature}°F"

iface = gr.Interface(fn=convert_temperature, inputs="slider", outputs="text", title="Temperaturumrechner")
iface.launch()
```

### Aufgabe 2

Jetzt wird es etwas kniffliger! Schreibe eine Funktion `calculate_discounted_price`, die den ursprünglichen Preis eines Produkts und den Rabatt in Prozent akzeptiert und den reduzierten Preis berechnet. Verwende Checkboxen, um den Rabatttyp auszuwählen (z. B. "Prozentualer Rabatt" oder "Absoluter Rabatt"). Gib den reduzierten Preis aus. Hier ist eine Musterlösung:

```python
import gradio as gr

def calculate_discounted_price(original_price, discount, is_percentage):
    if is_percentage:
        discounted_price = original_price * (1 - discount / 100)
    else:
        discounted_price = original_price - discount
    return f"Der reduzierte Preis beträgt: {discounted_price}$"

iface = gr.Interface(fn=calculate_discounted_price, inputs=["number", "text", "checkbox"], outputs="text", title="Preisrechner")
iface.launch()
```

## Fazit

Herzlichen Glückwunsch! Du hast nun die Grundlagen von Gradio kennengelernt und gelernt, wie du Schieberegler, Checkboxen und Dropdown-Menüs verwenden kannst, um deine Python-Modelle interaktiv zu machen. Mit diesen Werkzeugen kannst du eine Vielzahl von Anwendungen erstellen, von einfachen Konvertierungstools bis hin zu komplexen Entscheidungsprozessen.

Wir hoffen, dass dir dieses Tutorial geholfen hat und du jetzt motiviert bist, mit Gradio herumzuspielen und erstaunliche Projekte zu erstellen. Viel Spaß und happy coding!