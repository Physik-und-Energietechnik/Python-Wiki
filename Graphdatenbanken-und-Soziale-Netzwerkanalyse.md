# Graphdatenbanken und Soziale Netzwerkanalyse

## Einführung

Willkommen zu einem weiteren aufregenden Kapitel in der Welt der Python-Programmierung! Heute tauchen wir in die faszinierende Welt der Graphdatenbanken und sozialen Netzwerkanalyse ein. 🌐🔍

Stell dir vor, du könntest Daten nicht nur als langweilige Tabellen sehen, sondern als ein Netzwerk von Verbindungen zwischen verschiedenen Dingen. Graphdatenbanken erlauben genau das! Wir werden lernen, wie man Daten in Knoten und Kanten organisiert, um komplexe Beziehungen darzustellen und zu analysieren.

## Theorie

### Was sind Graphen?

Graphen sind wie die beste Art von Freundschaften – sie bestehen aus Knoten und Verbindungen! In einer Graphdatenbank repräsentieren Knoten Dinge (wie Personen oder Orte) und Kanten stellen Beziehungen zwischen diesen Dingen dar.

### Warum sind Graphdatenbanken cool?

Stell dir vor, du möchtest wissen, welche Freunde deines Freundes auch deine Freunde sein könnten. Das ist eine Aufgabe für Graphdatenbanken! Sie helfen uns, Muster in Beziehungen zu finden und Verbindungen zwischen verschiedenen Entitäten zu entdecken.

### Code-Beispiel: Was ist ein Graph?

Schau dir diesen einfachen Code an, der einen kleinen sozialen Graphen erstellt:

```python
from py2neo import Graph, Node, Relationship

# Verbindung zur Datenbank herstellen
graph = Graph("bolt://localhost:7687", user="neo4j", password="your_password")

# Knoten erstellen
alice = Node("Person", name="Alice")
bob = Node("Person", name="Bob")

# Beziehung hinzufügen
friendship = Relationship(alice, "FRIENDS_WITH", bob)
graph.create(friendship)
```

### Sozialnetzwerk-Analyse mit Python

Mit Graphdatenbanken können wir sozialen Netzwerken auf den Zahn fühlen! Zum Beispiel könnten wir den "Einflussgrad" einer Person basierend auf ihren Freundschaften analysieren.

```python
# Zuerst: Verbindung zur Datenbank herstellen (siehe vorheriges Beispiel)

# Abfrage: Wie viele Freunde hat Alice?
query = '''
MATCH (p:Person {name: "Alice"})-[:FRIENDS_WITH]->(friend)
RETURN p.name, COUNT(friend) as friend_count
'''

result = graph.run(query).data()
print(result)
```

## Praxis

### Leichte Aufgabe

Deine Aufgabe ist es, einen einfachen Graphen von Personen und ihren Hobbies zu erstellen. Füge dann eine Beziehung hinzu, die zeigt, wer welches Hobby mag. Zeige die Ergebnisse an.

Musterlösung:

```python
alice = Node("Person", name="Alice")
coding = Node("Hobby", name="Coding")
likes = Relationship(alice, "LIKES", coding)
graph.create(alice | coding | likes)
```

### Schwierige Aufgabe

Jetzt wird es herausfordernd! Analysiere den Graphen, den du erstellt hast, und finde heraus, welches Hobby am beliebtesten ist. Zeige das Hobby mit den meisten Likes an.

Musterlösung:

Verwende eine ähnliche Abfrage wie im vorherigen Beispiel, aber zähle dieses Mal die Anzahl der Beziehungen vom Hobbyknoten zu Personen.

## Fazit

Bravo, du hast erfolgreich die Geheimnisse der Graphdatenbanken und sozialen Netzwerkanalyse enthüllt! Mit Python und Graphdatenbanken kannst du Beziehungen zwischen Daten visualisieren, Muster entdecken und soziale Netzwerke analysieren. Diese Fähigkeiten sind nicht nur cool, sondern auch in vielen Bereichen, von sozialen Medien bis zur Empfehlungslogik, äußerst nützlich.

Kämpfe weiter, Datenentdecker!
