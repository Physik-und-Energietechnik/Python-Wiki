# Datenbank-Sharding

## Einführung

Willkommen zu unserem Tutorial über Datenbank-Sharding! In diesem Tutorial werden wir dir einen Überblick über das Konzept des Shardings geben und erklären, wie es verwendet wird, um große Datenmengen über mehrere Datenbankinstanzen zu verteilen und die Leistung zu verbessern. Aber keine Sorge, wir werden das Ganze mit einer Prise Humor und verständlichen Beispielen würzen, sodass es auch für Python-unerfahrene Menschen leicht zu verstehen ist.

Durch das Erlernen von Datenbank-Sharding wirst du in der Lage sein, Datenbanken effizient zu skalieren und die Leistung von Anwendungen zu verbessern, die große Mengen an Daten verarbeiten müssen. Du wirst verstehen, wie das Sharding-Konzept funktioniert und wie es in der Praxis angewendet werden kann.

Also lass uns gleich loslegen!

## Theorie

### Was ist Sharding?

Stell dir vor, du hast eine riesige Datenbank mit Millionen von Datensätzen. Die Verarbeitung und Abfrage dieser Datenbank wird mit der Zeit immer langsamer, da alle Daten auf einer einzigen Datenbankinstanz gespeichert sind. Hier kommt das Sharding ins Spiel.

Sharding ist eine Technik, bei der die Datenbank in mehrere Teile, sogenannte "Shards", aufgeteilt wird. Jeder Shard ist eine eigenständige Datenbankinstanz, die einen Teil der Daten enthält. Durch diese Aufteilung können die Datenbankabfragen parallel auf mehreren Shards ausgeführt werden, was zu einer besseren Leistung führt.

### Sharding-Methoden

Es gibt verschiedene Methoden, um das Sharding durchzuführen:

1. **Horizontal Sharding**: Bei dieser Methode werden die Datenzeilen basierend auf einem bestimmten Kriterium, z.B. dem Wert einer Spalte, auf verschiedene Shards aufgeteilt. Jeder Shard enthält eine Teilmenge der Datenzeilen.

   *Allgemeines Code-Beispiel:*
   ```python
   # Hier wird die Datenbanktabelle "users" horizontal auf zwei Shards aufgeteilt,
   # basierend auf dem Wert der Spalte "city".
   # Alle Benutzer aus derselben Stadt werden auf dem gleichen Shard gespeichert.
   
   Shard 1:
   SELECT * FROM users WHERE city = 'Berlin'
   
   Shard 2:
   SELECT * FROM users WHERE city = 'New York'
   ```

   *Explizites Code-Beispiel in Python:*
   ```python
   # Hier wird das "shard_key" als Kriterium für das Horizontale Sharding verwendet.
   # Der Wert des "shard_key" bestimmt, auf welchem Shard die Daten gespeichert werden.
   # In diesem Beispiel wird der "shard_key" als Hash-Wert der Benutzer-ID berechnet.
   
   shard_key = hash(user_id) % num_shards
   
   if shard_key == 1:
       # Speichere Daten auf Shard 1
       insert_into_shard1(user_data)
   elif shard_key == 2:
       # Speichere Daten auf Shard 2
       insert_into_shard2(user_data)
   else:
       # Speichere Daten auf Shard 3
       insert_into_shard3(user_data)
   ```

2. **Vertikal Sharding**: Bei dieser Methode werden die Spalten einer Tabelle auf verschiedene Shards aufgeteilt.

 Jeder Shard enthält nur einen Teil der Spalten.

   *Allgemeines Code-Beispiel:*
   ```python
   # Hier wird die Datenbanktabelle "users" vertikal auf zwei Shards aufgeteilt,
   # wobei Shard 1 die Spalten "user_id" und "username" enthält und Shard 2 die Spalten "email" und "phone".
   
   Shard 1:
   SELECT user_id, username FROM users
   
   Shard 2:
   SELECT email, phone FROM users
   ```

   *Explizites Code-Beispiel in Python:*
   ```python
   # Hier werden die Spalten "user_id" und "username" auf Shard 1 gespeichert
   # und die Spalten "email" und "phone" auf Shard 2.
   
   if shard_id == 1:
       # Speichere "user_id" und "username" auf Shard 1
       insert_into_shard1(user_id, username)
   elif shard_id == 2:
       # Speichere "email" und "phone" auf Shard 2
       insert_into_shard2(email, phone)
   ```

### Datenkonsistenz und Sharding

Beim Sharding ist es wichtig, die Datenkonsistenz zwischen den Shards zu gewährleisten. Änderungen an den Daten sollten korrekt über alle Shards repliziert werden, um Inkonsistenzen zu vermeiden. Es gibt verschiedene Ansätze, um die Datenkonsistenz sicherzustellen:

- **Replikation**: Jeder Shard kann mehrere Replikationen haben, um die Ausfallsicherheit und die Redundanz der Daten sicherzustellen. Änderungen an den Daten werden auf alle Replikationen angewendet.

- **Konsistenzprotokolle**: Konsistenzprotokolle wie ACID (Atomicity, Consistency, Isolation, Durability) können verwendet werden, um sicherzustellen, dass Änderungen an den Daten atomar und konsistent über alle Shards hinweg durchgeführt werden.

## Praxis

### Leichte Aufgabe

Deine Aufgabe besteht darin, eine Funktion zu implementieren, die einen Benutzer in der Shard-Datenbank speichert, basierend auf dem Wert des "shard_key". Die Shard-Datenbank besteht aus drei Shards (Shard 1, Shard 2, Shard 3), und der "shard_key" wird als Hash-Wert der Benutzer-ID berechnet.

Schreibe den Python-Code für die Funktion `save_user_to_shard(user_id, username, shard_key)`. Die Funktion sollte den Benutzer in dem entsprechenden Shard speichern.

*Musterlösung:*
```python
def save_user_to_shard(user_id, username, shard_key):
    if shard_key == 1:
        # Speichere Benutzerdaten auf Shard 1
        insert_into_shard1(user_id, username)
    elif shard_key == 2:
        # Speichere Benutzerdaten auf Shard 2
        insert_into_shard2(user_id, username)
    elif shard_key == 3:
        # Speichere Benutzerdaten auf Shard 3
        insert_into_shard3(user_id, username)
    else:
        raise ValueError("Ungültiger shard_key")
```

### Schwere Aufgabe

Deine Aufgabe besteht darin, eine Funktion zu implementieren, die einen SQL-Befehl an alle Shards der Shard-Datenbank sendet und die Ergebnisse komb

iniert. Die Funktion `execute_query_on_shards(query)` sollte den SQL-Befehl an alle Shards senden und die Ergebnisse zusammenführen.

Schreibe den Python-Code für die Funktion `execute_query_on_shards(query)`.

*Musterlösung:*
```python
def execute_query_on_shards(query):
    results = []
    for shard_id in range(1, num_shards + 1):
        result = execute_query_on_shard(query, shard_id)
        results.extend(result)
    return results
```

Herzlichen Glückwunsch! Du hast die Aufgaben erfolgreich gelöst und das Konzept des Datenbank-Shardings gemeistert.

## Fazit

In diesem Tutorial haben wir das Konzept des Datenbank-Shardings kennengelernt und gesehen, wie es verwendet wird, um große Datenmengen über mehrere Datenbankinstanzen zu verteilen und die Leistung zu verbessern. Wir haben die Methoden des Horizontalen und Vertikalen Shardings besprochen und gesehen, wie die Datenkonsistenz zwischen den Shards gewährleistet werden kann.

Durch das Erlernen des Datenbank-Shardings bist du nun in der Lage, Datenbanken effizient zu skalieren und die Leistung von Anwendungen zu verbessern. Du kannst das Sharding-Konzept in der Praxis anwenden, um mit großen Datenmengen umzugehen und gleichzeitig eine hohe Verfügbarkeit und Leistungsfähigkeit zu gewährleisten.

Wir hoffen, dass dir dieses Tutorial gefallen hat und du nun ein besseres Verständnis für das Datenbank-Sharding hast. Viel Spaß beim Skalieren und Optimieren deiner Datenbanken!