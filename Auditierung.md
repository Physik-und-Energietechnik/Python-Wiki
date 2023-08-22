# 1. Titel - Datenbank-Auditierung

## 2. Einführung

Willkommen zu unserem lustigen Tutorial über Datenbank-Auditierung! In diesem Tutorial werden wir das spannende Thema der Auditierung von Datenbanken erkunden. Du wirst lernen, wie man die Aktivitäten und Änderungen in einer Datenbank überwacht, als ob du ein Geheimagent wärst, der die Vorgänge im Hintergrund beobachtet.

Durch dieses Tutorial wirst du Folgendes lernen:

- Was ist Datenbank-Auditierung und warum ist sie wichtig?
- Unterschiedliche Arten der Auditierung, wie z.B. Zugriffs- und Änderungsauditierung.
- Wie du Audit-Logs erstellst, um wichtige Informationen über Datenbankaktivitäten festzuhalten.
- Wie du Audit-Events abfragst, um verdächtige Aktivitäten oder Sicherheitsverletzungen zu identifizieren.

Die Fähigkeit zur Auditierung von Datenbanken ist entscheidend, um die Sicherheit und Integrität deiner Daten zu gewährleisten. Du wirst lernen, wie du unerwünschte Zugriffe auf deine Daten erkennen und potenzielle Bedrohungen abwehren kannst.

Also schnall dich an und lass uns den Datenbank-Auditierungsagenten in dir erwecken!

## 3. Theorie

### Was ist Datenbank-Auditierung?

Datenbank-Auditierung ist der Prozess der Überwachung und Aufzeichnung von Datenbankaktivitäten, um Sicherheitsrisiken zu minimieren und die Einhaltung von Richtlinien zu gewährleisten. Sie ermöglicht es dir, Zugriffe, Änderungen und andere Ereignisse in deiner Datenbank zu überwachen und zu protokollieren.

#### Zugriffsauditierung

Bei der Zugriffsauditierung werden Informationen über den Zugriff auf die Datenbank erfasst. Dies beinhaltet Benutzeranmeldungen, fehlgeschlagene Anmeldeversuche und privilegierte Operationen. Durch die Überwachung von Zugriffsereignissen kannst du potenzielle Sicherheitsbedrohungen identifizieren und auf verdächtige Aktivitäten reagieren.

Hier ist ein allgemeines Code-Beispiel, das zeigt, wie du Zugriffsauditierung in einer Datenbank konfigurierst:

```python
-- Aktiviere die Zugriffsauditierung für die Datenbank
ALTER DATABASE mydb SET AUDIT ALL;

-- Überwache Anmeldungen und privilegierte Operationen
CREATE AUDIT POLICY access_policy ACTIONS LOGON, PRIVILEGED;

-- Weise die Audit-Politik Benutzern zu
AUDIT POLICY access_policy BY alice, bob;
```

In diesem Beispiel aktivieren wir die Zugriffsauditierung für die Datenbank "mydb" und definieren eine Audit-Politik, die Anmeldungen und privilegierte Operationen überwacht. Die Audit-Politik wird dann den Benutzern Alice und Bob zugewiesen.

#### Änderungsauditierung

Bei der Änderungsauditierung werden Informationen über Änderungen an Datenbankobjekten erfasst. Dies umfasst das Hinzufügen, Ändern oder Löschen von Datensätzen, Tabellen oder anderen Datenbankobjekten. Durch die Überwachung von Änderungsereignissen kannst du die Integrität de

iner Daten überwachen und nachvollziehen, wer Änderungen vorgenommen hat.

Hier ist ein explizites Code-Beispiel, das zeigt, wie du Änderungsauditierung in einer Datenbank implementierst:

```python
-- Aktiviere die Änderungsauditierung für eine Tabelle
ALTER TABLE mytable ENABLE ROW LEVEL AUDIT;

-- Überwache Änderungen an bestimmten Spalten
AUDIT UPDATE, INSERT, DELETE ON mytable COLUMN (column1, column2);
```

In diesem Beispiel aktivieren wir die Änderungsauditierung auf Zeilenebene für die Tabelle "mytable" und definieren, dass Änderungen an den Spalten "column1" und "column2" überwacht werden sollen.

## 4. Praxis

### Leichte Aufgabe

Angenommen, du hast eine Datenbank "Customers" mit der Tabelle "Orders". Führe eine Auditierung durch, um alle Anmeldeversuche zu protokollieren und Änderungen an der Tabelle "Orders" zu überwachen.

Musterlösung:

```python
-- Aktiviere Zugriffsauditierung für die Datenbank
ALTER DATABASE Customers SET AUDIT ALL;

-- Überwache Anmeldeversuche
CREATE AUDIT POLICY login_policy ACTIONS LOGON;

-- Weise die Audit-Politik Benutzern zu
AUDIT POLICY login_policy BY alice, bob;

-- Aktiviere Änderungsauditierung für die Tabelle "Orders"
ALTER TABLE Orders ENABLE ROW LEVEL AUDIT;

-- Überwache Änderungen an der Tabelle "Orders"
AUDIT UPDATE, INSERT, DELETE ON Orders;
```

### Schwierigere Aufgabe

Angenommen, du hast eine Datenbank "Inventory" mit der Tabelle "Products". Implementiere eine Änderungsauditierung, die alle Änderungen an der Tabelle "Products" auf Spaltenebene überwacht und protokolliert.

Musterlösung:

```python
-- Aktiviere Änderungsauditierung für die Tabelle "Products"
ALTER TABLE Products ENABLE ROW LEVEL AUDIT;

-- Überwache Änderungen an allen Spalten der Tabelle "Products"
AUDIT UPDATE, INSERT, DELETE ON Products ALL COLUMNS;
```

Fantastisch! Du hast nun erfolgreich gelernt, wie man Datenbank-Auditierung durchführt. Du bist bereit, als Geheimagent in der Welt der Datenbanken zu agieren und verdächtige Aktivitäten aufzudecken.

Vielen Dank für deine Teilnahme an diesem unterhaltsamen Tutorial!