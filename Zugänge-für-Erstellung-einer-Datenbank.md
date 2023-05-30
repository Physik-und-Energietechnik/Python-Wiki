# Erstellen einer Datenbank mit Python

Wenn du eine Datenbank mit Python erstellen möchtest, brauchst du einige Werkzeuge und Module. Keine Sorge, ich werde dir zeigen, was du brauchst!

## 1. Datenbank-Management-System (DBMS)

Ein DBMS ist wie ein verrückter Wissenschaftler, der die Kontrolle über deine Datenbank übernimmt. Es gibt verschiedene DBMS zur Auswahl, aber für Python empfehle ich SQLite. SQLite ist wie ein kleiner Datenbank-Zauberer, der direkt in deiner Anwendung arbeitet.

## 2. SQLite-Modul

Um mit SQLite zu arbeiten, benötigst du das SQLite-Modul für Python. Keine Sorge, du musst es nicht selbst programmieren! Es ist bereits in der Python-Standardbibliothek enthalten.

## 3. Ein wenig Python-Magie

Jetzt kommt der lustige Teil! Du musst ein paar Zeilen Python-Code schreiben, um deine Datenbank zu erstellen. Hier ist ein einfaches Beispiel:

```python
import sqlite3

# Verbindung zur Datenbank herstellen
conn = sqlite3.connect('meine_datenbank.db')

# Datenbank-Cursor erstellen
cursor = conn.cursor()

# Tabelle erstellen
cursor.execute("CREATE TABLE benutzer (id INT, name TEXT, alter INT)")

# Verbindung schließen
conn.close()
```

In diesem Beispiel haben wir eine Verbindung zur Datenbank hergestellt, einen Cursor erstellt und dann eine Tabelle mit dem Namen "benutzer" und den Spalten "id", "name" und "alter" erstellt. Schließlich haben wir die Verbindung zur Datenbank geschlossen.

Jetzt hast du deine eigene Datenbank erstellt! Du kannst sie verwenden, um Daten zu speichern, abzufragen und zu manipulieren. Denke daran, dass dies nur ein einfaches Beispiel ist. Du kannst viele weitere coole Dinge mit SQLite und Python machen.

Also schnapp dir deinen Zauberstab (ähm, deinen Code-Editor) und fange an, magische Datenbanken mit Python zu erstellen!

