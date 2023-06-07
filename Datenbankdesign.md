# Datenbankdesign

## Einführung
Willkommen zum Tutorial über Datenbankdesign! In diesem Tutorial werden wir uns mit den Grundlagen des Datenbankdesigns befassen. Du wirst lernen, wie du eine Datenbank strukturiert aufbaust, Tabellen erstellst und Beziehungen zwischen ihnen herstellst. Das Wissen über Datenbankdesign ist von entscheidender Bedeutung, um effizient mit Daten zu arbeiten und die Integrität deiner Daten zu gewährleisten. Nach Abschluss dieses Tutorials wirst du in der Lage sein, Datenbanken zu entwerfen, Primärschlüssel richtig einzusetzen und die Normalisierung von Datenbanken zu verstehen.

## Theorie

### Grundlagen des Datenbankdesigns
Ein gut gestaltetes Datenbankdesign beruht auf einigen grundlegenden Konzepten. Hier sind die wichtigsten:

- **Datenbank:** Eine Datenbank ist eine strukturierte Sammlung von Daten, die in Tabellen organisiert sind. Sie ermöglicht es uns, Daten effizient zu speichern, abzurufen und zu verwalten.

- **Tabelle:** Eine Tabelle ist eine Datenstruktur, die aus Zeilen und Spalten besteht. Jede Tabelle repräsentiert eine Entität oder ein Objekt, das wir speichern möchten.

- **Spalte:** Eine Spalte, auch Attribut genannt, repräsentiert eine einzelne Informationseinheit in einer Tabelle. Jede Spalte hat einen Namen und einen Datentyp, der angibt, welche Art von Daten in der Spalte gespeichert werden kann.

- **Primärschlüssel:** Ein Primärschlüssel ist ein eindeutiger Identifikator für jede Zeile in einer Tabelle. Er stellt sicher, dass jede Zeile eindeutig identifiziert werden kann. Der Primärschlüssel kann aus einer oder mehreren Spalten bestehen.

### Normalisierung von Datenbanken
Die Normalisierung ist ein wichtiger Prozess im Datenbankdesign, der uns hilft, Daten effizient zu organisieren und die Datenintegrität zu gewährleisten. Hier sind die verschiedenen Normalformen:

- **Erste Normalform (1NF):** In der 1NF müssen alle Werte einer Tabelle atomar sein, das heißt, keine wiederholten Werte oder mehrere Werte in einem Feld sind erlaubt. Jede Spalte sollte nur einen einzelnen Wert enthalten.

- **Zweite Normalform (2NF):** In der 2NF müssen alle Nicht-Schlüssel-Spalten funktional von der gesamten Primärschlüssel abhängen. Es dürfen keine funktionalen Abhängigkeiten zwischen Nicht-Schlüssel-Spalten bestehen.

- **Dritte Normalform (3NF):** In der 3NF dürfen keine transitive Abhängigkeiten zwischen Nicht-Schlüssel-Spalten bestehen. Das bedeutet, dass keine Nicht-Schlüssel-Spalte von einer anderen Nicht-Schlüssel-Spalte abhängen darf.

### Beispiele

#### Beispiel 1: Tabelle "Kunden"
| KundenID | Name    | Alter | Stadt     |
|----------|---------|-------|-----------|
| 1        | Max     | 25    | Berlin    |
| 2        | Anna    | 32    | München   |
| 3        | Peter   | 40    |

 Hamburg   |

In diesem Beispiel haben wir eine Tabelle "Kunden" mit den Spalten "KundenID", "Name", "Alter" und "Stadt". Die "KundenID" dient als Primärschlüssel, um jede Zeile eindeutig zu identifizieren.

#### Beispiel 2: Tabelle "Bestellungen"
| BestellungsID | KundenID | Produkt   | Menge |
|---------------|----------|-----------|-------|
| 1             | 1        | Handy     | 2     |
| 2             | 2        | Laptop    | 1     |
| 3             | 1        | Fernseher | 1     |

In diesem Beispiel haben wir eine Tabelle "Bestellungen", die mit der Tabelle "Kunden" durch die Spalte "KundenID" verbunden ist. Die "KundenID" in der Tabelle "Bestellungen" ist ein Fremdschlüssel, der auf den Primärschlüssel "KundenID" in der Tabelle "Kunden" verweist.

## Praxis

### Aufgabe
Entwerfe eine Datenbanktabelle für ein Musikgeschäft, das Informationen über Künstler, Alben und Songs speichert. Jeder Künstler kann mehrere Alben haben, und jedes Album kann mehrere Songs enthalten. Jedes Album hat einen eindeutigen Namen, und jeder Song hat einen eindeutigen Titel.

### Musterlösung
Hier ist eine mögliche Lösung für die Datenbanktabelle:

#### Tabelle "Künstler"
| KünstlerID | Name         |
|------------|--------------|
| 1          | Taylor Swift |
| 2          | Ed Sheeran   |
| 3          | Beyoncé      |

#### Tabelle "Alben"
| AlbumID | KünstlerID | Name            |
|---------|------------|-----------------|
| 1       | 1          | Lover           |
| 2       | 1          | 1989            |
| 3       | 2          | ÷ (Divide)      |
| 4       | 3          | Lemonade        |

#### Tabelle "Songs"
| SongID | AlbumID | Titel         |
|--------|---------|---------------|
| 1      | 1       | Lover         |
| 2      | 1       | You Need To Calm Down |
| 3      | 2       | Shake It Off   |
| 4      | 3       | Shape of You   |
| 5      | 3       | Perfect        |
| 6      | 4       | Formation     |

In diesem Beispiel haben wir drei Tabellen: "Künstler", "Alben" und "Songs". Die Tabelle "Alben" ist über die Spalte "KünstlerID" mit der Tabelle "Künstler" verknüpft, und die Tabelle "Songs" ist über die Spalte "AlbumID" mit der Tabelle "Alben" verknüpft. Jede Tabelle hat einen Primärschlüssel, um die Eindeutigkeit der Datensätze sicherzustellen.

Herzlichen Glückwunsch! Du hast erfolgreich eine Datenbank für ein Musikgeschäft entworfen.

### Schwerere Aufgabe
Erweitere die Datenbank für das Musikgeschäft um eine weitere Tabelle "Genre", die Informationen über verschiedene Musikgenres enthält. Jedes Album kann einem oder mehreren Genres zugeordnet werden.

### Musterlösung
Hier ist

 eine mögliche Lösung für die erweiterte Datenbank:

#### Tabelle "Genre"
| GenreID | Name      |
|---------|-----------|
| 1       | Pop       |
| 2       | Rock      |
| 3       | R&B       |
| 4       | Hip Hop   |

#### Tabelle "Alben_Genres"
| AlbumID | GenreID |
|---------|---------|
| 1       | 1       |
| 1       | 3       |
| 2       | 1       |
| 3       | 2       |
| 4       | 3       |
| 4       | 4       |

In dieser erweiterten Lösung haben wir eine neue Tabelle "Genre" hinzugefügt, die Informationen über verschiedene Musikgenres enthält. Die Tabelle "Alben_Genres" stellt die Beziehung zwischen den Tabellen "Alben" und "Genre" her, indem sie die Album-IDs und Genre-IDs speichert.

Fantastische Arbeit! Du hast erfolgreich eine Datenbank für ein Musikgeschäft entworfen und um eine weitere Tabelle erweitert.

Das war eine Einführung in das Thema Datenbankdesign. Du hast gelernt, wie man Tabellen erstellt, Primärschlüssel und Fremdschlüssel einsetzt und die Normalisierung von Datenbanken versteht. Das Wissen über Datenbankdesign ist von großer Bedeutung, um effizient mit Daten zu arbeiten und die Integrität deiner Daten zu gewährleisten. Viel Spaß beim Gestalten deiner eigenen Datenbanken!