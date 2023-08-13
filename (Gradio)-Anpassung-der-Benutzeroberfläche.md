## Einführung

Willkommen zu unserem Python-Tutorial für unerfahrene Python-Nutzer! In diesem Tutorial werden wir uns mit der Anpassung der Benutzeroberfläche in Python befassen, insbesondere mit der Verwendung des Gradio-Frameworks. Gradio ermöglicht es uns, interaktive Benutzeroberflächen für unsere Python-Anwendungen zu erstellen und diese an unsere eigenen Bedürfnisse anzupassen.

Bevor wir jedoch tiefer in die Materie eintauchen, lassen Sie uns zunächst einen kurzen Blick darauf werfen, was Sie durch dieses Tutorial lernen werden und wie Sie dieses Wissen nutzen können.

In diesem Tutorial werden wir lernen, wie wir die Farben, das Layout und sogar mehrere Tabs unserer Benutzeroberfläche in Python anpassen können. Sie werden verstehen, wie Sie mit Gradio arbeiten und wie Sie die verschiedenen Stile, Eigenschaften und Funktionalitäten Ihrer Benutzeroberfläche anpassen können. Dieses Wissen kann Ihnen dabei helfen, ansprechende und benutzerfreundliche Anwendungen zu entwickeln, die sowohl funktional als auch ästhetisch ansprechend sind. Denn wer sagt, dass Code nicht auch schön sein kann?

## Theorie

### Farbanpassung

Ein wichtiger Aspekt der Benutzeroberfläche ist die Farbwahl. Mit Gradio können Sie die Farben Ihrer Anwendung anpassen, um eine einzigartige und ansprechende Benutzererfahrung zu schaffen. Hier ist ein allgemeines Code-Beispiel, das Ihnen zeigt, wie Sie die Hintergrundfarbe Ihrer Benutzeroberfläche ändern können:

```python
import gradio as gr

def greet(name):
    return f"Hallo {name}!"

iface = gr.Interface(fn=greet, inputs="text", outputs="text")
iface.interface_style = "brick"  # Ändern Sie den Stil der Benutzeroberfläche
iface.launch()
```

Das obige Beispiel zeigt, wie wir den `interface_style` von Gradio verwenden, um den Stil unserer Benutzeroberfläche anzupassen. Es gibt verschiedene vordefinierte Stile wie "default", "bricks", "neon" und viele mehr, aus denen Sie wählen können. Probieren Sie sie aus und sehen Sie, welcher Stil Ihnen am besten gefällt!

### Layout-Anpassung

Neben der Farbanpassung können wir auch das Layout unserer Benutzeroberfläche anpassen, um sie unseren Vorlieben anzupassen. Hier ist ein Code-Beispiel, das zeigt, wie Sie das Layout Ihrer Benutzeroberfläche ändern können:

```python
import gradio as gr

def greet(name):
    return f"Hallo {name}!"

iface = gr.Interface(fn=greet, inputs="text", outputs="text")
iface.layout = "vertical"  # Ändern Sie das Layout der Benutzeroberfläche
iface.launch()
```

Im obigen Beispiel verwenden wir die Eigenschaft `layout` von Gradio, um das Layout der Benutzeroberfläche anzupassen. Standardmäßig verwendet Gradio das horizontale Layout, aber Sie können es einfach auf "vertical" oder "unaligned" setzen, um das Aussehen Ihrer Anwendung zu ändern.

### Erstellung von Tabs

Wenn Sie mehrere Funktionen oder Optionen in Ihrer Benutzeroberfläche haben möchten, können Sie Tabs verwenden, um diese übersichtlich

 zu organisieren. Hier ist ein Code-Beispiel, das zeigt, wie Sie mehrere Tabs in Ihrer Benutzeroberfläche erstellen können:

```python
import gradio as gr

def greet(name):
    return f"Hallo {name}!"

def goodbye(name):
    return f"Auf Wiedersehen, {name}!"

iface_1 = gr.Interface(
    fn=greet,
    inputs=gr.inputs.Textbox(label="Name"),
    outputs="text",
    title="Begrüßung"
)

iface_2 = gr.Interface(
    fn=goodbye,
    inputs=gr.inputs.Textbox(label="Name"),
    outputs="text",
    title="Verabschiedung"
)

gr.Interface.Tabbed([iface_1, iface_2]).launch()
```

In der obigen Musterlösung haben wir zwei Funktionen `greet` und `goodbye`, die jeweils einen Gruß und eine Verabschiedung zurückgeben. Indem wir die Funktionen als Liste an die `fn`-Eigenschaft übergeben und die entsprechenden Titel für die Tabs angeben, erstellen wir eine Benutzeroberfläche mit zwei Tabs. Sie können weitere Funktionen und Tabs hinzufügen, um Ihre Anwendung weiter anzupassen.

## Praxis

Jetzt, da Sie die Grundlagen der Farbanpassung, Layout-Anpassung und Tab-Erstellung kennen, ist es Zeit, Ihr Wissen in die Praxis umzusetzen!

### Aufgabe

Erstellen Sie eine Benutzeroberfläche mit drei Tabs, die verschiedene Funktionen für lustige Sprüche enthält. Jeder Tab soll einen anderen Spruch anzeigen, wenn der Benutzer seinen Namen eingibt.

**Musterlösung:**

```python
import gradio as gr

def joke_1(name):
    return f"Hallo {name}! Warum hat der Python-Entwickler die Kobra nicht benutzt? Weil sie Python war!"

def joke_2(name):
    return f"Hallo {name}! Warum surfen Programmierer nie? Weil sie immer im Code hängenbleiben!"

def joke_3(name):
    return f"Hallo {name}! Warum hat der Informatiker immer eine Brille auf? Weil er nicht C#!"

iface_1 = gr.Interface(
    fn=joke_1,
    inputs=gr.inputs.Textbox(label="Name"),
    outputs="text",
    title="Witz 1"
)

iface_2 = gr.Interface(
    fn=joke_2,
    inputs=gr.inputs.Textbox(label="Name"),
    outputs="text",
    title="Witz 2"
)

iface_3 = gr.Interface(
    fn=joke_3,
    inputs=gr.inputs.Textbox(label="Name"),
    outputs="text",
    title="Witz 3"
)

gr.TabbedInterface([iface_1, iface_2, iface_3], title="Witzmaschine").launch()
```

## Fazit

In diesem Tutorial haben Sie gelernt, wie Sie die Benutzeroberfläche Ihrer Python-Anwendungen mithilfe von Gradio anpassen können. Sie haben gesehen, wie Sie Farben, das Layout und sogar Tabs ändern können, um eine einzigartige Benutzererfahrung zu schaffen. Nun liegt es an Ihnen, Ihre Kreativität einzusetzen und Ihre eigenen benutzerdefinierten Benutzeroberflächen zu gestalten. Viel Spaß beim Coden, und denken Sie daran, dass auch Code eine Prise Schönheit vertragen kann!