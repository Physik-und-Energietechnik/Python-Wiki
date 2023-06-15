# XML: Die Sprache der flexiblen Daten

## Einführung

Willkommen zu unserem Tutorial über XML! Hast du dich jemals gefragt, wie Daten auf eine strukturierte und flexible Weise gespeichert und ausgetauscht werden können? XML ist die Antwort! In diesem Tutorial werden wir uns mit XML befassen, einer mächtigen Sprache zur Darstellung und Organisation von Daten. Du wirst lernen, was XML ist, wie es aufgebaut ist und wie du es in Python nutzen kannst.

Nach diesem Tutorial wirst du in der Lage sein:

- XML-Dateien zu lesen und zu verstehen.
- XML-Dateien zu erstellen und zu schreiben.
- XML-Daten in Python zu verarbeiten und zu manipulieren.

XML ist weit verbreitet und wird in vielen Anwendungen eingesetzt, darunter Webentwicklung, Datenbanken, Konfigurationsdateien und vieles mehr. Indem du XML beherrschst, wirst du in der Lage sein, Daten auf eine strukturierte und flexible Weise zu verwalten und auszutauschen. Also lass uns eintauchen und die wunderbare Welt von XML erkunden!

## Theorie

XML steht für "eXtensible Markup Language" und ist eine Auszeichnungssprache zur Darstellung strukturierter Daten. Es ähnelt HTML, aber im Gegensatz zu HTML, das für die Darstellung von Webseiten verwendet wird, ist XML allgemeiner und kann für beliebige Daten verwendet werden.

XML verwendet Tags, um die Struktur der Daten zu definieren. Ein Tag besteht aus einem Namen, der von spitzen Klammern umschlossen ist, z. B. `<tag>`. Es gibt öffnende Tags `<tag>` und schließende Tags `</tag>`, die den Anfang und das Ende eines Elements markieren.

Hier ist ein allgemeines Beispiel für XML:

```xml
<person>
    <name>John Doe</name>
    <age>30</age>
    <city>New York</city>
</person>
```

In diesem Beispiel haben wir ein Element `<person>`, das die Daten einer Person enthält. Das Element hat drei Unterelemente: `<name>`, `<age>` und `<city>`. Jedes Unterelement enthält den entsprechenden Wert.

### XML in Python

In Python können wir die Bibliothek `xml.etree.ElementTree` verwenden, um XML-Dateien zu lesen, zu schreiben und zu manipulieren. Diese Bibliothek bietet eine einfache und intuitive API für die Arbeit mit XML.

Hier ist ein allgemeines Beispiel, wie wir XML in Python verwenden können:

```python
import xml.etree.ElementTree as ET

# XML lesen
tree = ET.parse('daten.xml')
root = tree.getroot()

# Durch die XML-Struktur navigieren
for child in root:
    print(child.tag, child.text)

# XML schreiben
new_person = ET.SubElement(root, 'person')
new_name = ET.SubElement(new_person, 'name')
new_name.text = 'Jane Smith'

tree.write('neue_daten.xml')
```

In diesem Beispiel lesen wir eine XML-Datei `daten.xml`, navigieren durch die XML-Struktur und geben die Tags und Texte der Elemente aus. Dann erstellen wir ein neues Element `<person>` mit einem Unterelement `<name>` und schreiben die aktualisierte XML-Struktur in eine neue Datei `neue_daten.xml`.

## Praxis

### Leichte Aufgabe

Lies die folgende

 XML-Datei ein und gib den Namen und das Alter jeder Person aus:

```xml
<people>
    <person>
        <name>John Doe</name>
        <age>30</age>
    </person>
    <person>
        <name>Jane Smith</name>
        <age>25</age>
    </person>
</people>
```

Musterlösung:

```python
import xml.etree.ElementTree as ET

tree = ET.parse('daten.xml')
root = tree.getroot()

for person in root:
    name = person.find('name').text
    age = person.find('age').text
    print("Name:", name)
    print("Alter:", age)
```

### Schwierigere Aufgabe

Schreibe Python-Code, der eine XML-Datei erstellt und speichert, die Informationen über Bücher enthält. Jedes Buch sollte einen Titel, einen Autor und eine ISBN-Nummer haben. Denke daran, die XML-Struktur mit Tags und Unterelementen zu definieren.

Musterlösung:

```python
import xml.etree.ElementTree as ET

root = ET.Element('books')

book1 = ET.SubElement(root, 'book')
title1 = ET.SubElement(book1, 'title')
title1.text = 'The Great Gatsby'
author1 = ET.SubElement(book1, 'author')
author1.text = 'F. Scott Fitzgerald'
isbn1 = ET.SubElement(book1, 'isbn')
isbn1.text = '978-3-16-148410-0'

book2 = ET.SubElement(root, 'book')
title2 = ET.SubElement(book2, 'title')
title2.text = 'To Kill a Mockingbird'
author2 = ET.SubElement(book2, 'author')
author2.text = 'Harper Lee'
isbn2 = ET.SubElement(book2, 'isbn')
isbn2.text = '978-1-22-119678-9'

tree = ET.ElementTree(root)
tree.write('books.xml')
```

In dieser Musterlösung erstellen wir eine XML-Struktur mit dem Root-Element `<books>` und zwei Buch-Elementen `<book>`. Jedes Buch-Element enthält Unterelemente für Titel, Autor und ISBN-Nummer. Die XML-Struktur wird dann in der Datei `books.xml` gespeichert.

---

Herzlichen Glückwunsch! Du hast jetzt einen Einblick in XML bekommen. Du weißt, was XML ist, wie es aufgebaut ist und wie du es in Python verwenden kannst. XML bietet eine flexible Möglichkeit, Daten zu strukturieren und auszutauschen, und wird in vielen Anwendungen eingesetzt. Viel Spaß beim Erkunden der wunderbaren Welt von XML!