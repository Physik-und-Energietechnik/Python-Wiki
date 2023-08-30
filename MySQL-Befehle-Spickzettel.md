## MySQL Befehle Spickzettel

### Datenbanken verwalten

1. **CREATE DATABASE** *databasename*;
   Beispiel: `CREATE DATABASE mydb;`
   Erstellt eine neue Datenbank mit dem angegebenen Namen.

2. **USE** *databasename*;
   Beispiel: `USE mydb;`
   Wählt die angegebene Datenbank für zukünftige Operationen aus.

3. **SHOW DATABASES;**
   Zeigt eine Liste aller vorhandenen Datenbanken an.

4. **DROP DATABASE** *databasename*;
   Beispiel: `DROP DATABASE mydb;`
   Löscht die angegebene Datenbank und alle darin enthaltenen Daten.

### Tabellen erstellen und verwalten

1. **CREATE TABLE** *tablename* (
     *column1 datatype*,
     *column2 datatype*,
     ...
   );
   Beispiel: `CREATE TABLE users (id INT, name VARCHAR(50));`
   Erstellt eine neue Tabelle mit den angegebenen Spalten und Datentypen.

2. **ALTER TABLE** *tablename* **ADD** *columnname datatype*;
   Beispiel: `ALTER TABLE users ADD email VARCHAR(100);`
   Fügt eine neue Spalte zur angegebenen Tabelle hinzu.

3. **ALTER TABLE** *tablename* **MODIFY COLUMN** *columnname datatype*;
   Beispiel: `ALTER TABLE users MODIFY COLUMN age INT;`
   Ändert den Datentyp einer vorhandenen Spalte.

4. **ALTER TABLE** *tablename* **DROP COLUMN** *columnname*;
   Beispiel: `ALTER TABLE users DROP COLUMN email;`
   Entfernt eine Spalte aus der Tabelle.

5. **SELECT** *columns* **FROM** *tablename* **WHERE** *condition*;
   Beispiel: `SELECT name, email FROM users WHERE age > 25;`
   Wählt bestimmte Spalten aus einer Tabelle basierend auf einer Bedingung aus.

6. **UPDATE** *tablename* **SET** *column=value* **WHERE** *condition*;
   Beispiel: `UPDATE users SET age=30 WHERE id=1;`
   Aktualisiert Daten in einer Tabelle basierend auf einer Bedingung.

7. **DELETE FROM** *tablename* **WHERE** *condition*;
   Beispiel: `DELETE FROM users WHERE age < 18;`
   Löscht Datensätze aus einer Tabelle basierend auf einer Bedingung.

### Daten abfragen

1. **SELECT** *columns* **FROM** *tablename*;
   Beispiel: `SELECT name, age FROM users;`
   Wählt bestimmte Spalten aus allen Datensätzen einer Tabelle aus.

2. **SELECT** *function(column)* **FROM** *tablename*;
   Beispiel: `SELECT AVG(age) FROM users;`
   Führt eine Funktion (z. B. AVG, SUM) auf einer Spalte aus.

3. **SELECT** *columns* **FROM** *tablename* **JOIN** *othertable* **ON** *condition*;
   Beispiel: `SELECT orders.order_id, customers.name FROM orders JOIN customers ON orders.customer_id = customers.id;`
   Verknüpft Daten aus mehreren Tabellen basierend auf einer Bedingung.

### Datenbank sichern und wiederherstellen

1. **mysqldump -u** *username* -p *databasename* **> backup.sql**
   Beispiel: `mysqldump -u root -p mydb > backup.sql`
   Erstellt eine Sicherungskopie der Datenbank in eine Datei.

2. **mysql -u** *username* -p *databasename* **< backup.sql**
   Beispiel: `mysql -u root -p mydb < backup.sql`
   Stellt eine zuvor gesicherte Datenbank aus einer Datei wieder her.
   
3. **SHOW TABLES;**
   Zeigt eine Liste aller Tabellen in der aktuellen Datenbank an.

4. **DESCRIBE** *tablename*;
   Beispiel: `DESCRIBE users;`
   Zeigt die Struktur der angegebenen Tabelle an, einschließlich Spaltennamen und Datentypen.

5. **COUNT(*) FROM** *tablename*;
   Beispiel: `SELECT COUNT(*) FROM users;`
   Zählt die Anzahl der Datensätze in einer Tabelle.

6. **ORDER BY** *column* **ASC/DESC**;
   Beispiel: `SELECT name, age FROM users ORDER BY age DESC;`
   Sortiert die Ergebnisse nach einer bestimmten Spalte in aufsteigender oder absteigender Reihenfolge.

7. **GROUP BY** *column* **HAVING** *condition*;
   Beispiel: `SELECT country, COUNT(*) FROM customers GROUP BY country HAVING COUNT(*) > 5;`
   Gruppiert Datensätze nach einer Spalte und wendet eine Bedingung auf die Gruppen an.
