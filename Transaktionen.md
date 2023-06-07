# Transaktionen

## Einführung
Willkommen zum Tutorial über Transaktionen in Python! In diesem Tutorial werden wir die Welt der Transaktionen in Datenbanken erkunden. Du wirst lernen, was Transaktionen sind, wie sie funktionieren und warum sie so wichtig sind, um die Datenkonsistenz und Datenintegrität zu gewährleisten. Mit diesem Wissen bist du in der Lage, sicher und zuverlässig mit Datenbanken umzugehen und mögliche Fehler zu vermeiden. Los geht's!

## Theorie
### Was sind Transaktionen?
Transaktionen sind wie kleine magische Zauber in der Welt der Datenbanken. Sie helfen uns dabei, Daten sicher und zuverlässig zu verwalten, sodass unsere Datenbanken nicht in ein chaotisches Durcheinander ausbrechen. Eine Transaktion ist eine Sammlung von Datenbankoperationen, die zusammengefasst werden, um als eine einzige logische Einheit ausgeführt zu werden. Entweder werden alle Operationen erfolgreich ausgeführt, oder keine davon. Es ist ein Alles-oder-Nichts-Deal!

#### Allgemeines Code-Beispiel:
```python
# Start einer Transaktion
start_transaction()

# Datenbankoperationen

# Erfolgreicher Abschluss der Transaktion
commit_transaction()

# Fehlschlag der Transaktion
rollback_transaction()
```

#### Explizites Code-Beispiel in Python:
```python
# Beispielcode für eine Transaktion
def transfer_funds(from_account, to_account, amount):
    try:
        # Start der Transaktion
        start_transaction()
        
        # Abhebung vom Konto A
        withdraw(from_account, amount)
        
        # Einzahlung auf Konto B
        deposit(to_account, amount)
        
        # Transaktion erfolgreich
        commit_transaction()
        
        print("Geldüberweisung erfolgreich!")
    except Exception as e:
        # Transaktion fehlgeschlagen
        rollback_transaction()
        
        print("Fehler bei der Geldüberweisung:", str(e))
```

### ACID-Prinzip
Transaktionen werden nach dem ACID-Prinzip durchgeführt, um ihre Eigenschaften zu gewährleisten.

- Atomicity: Eine Transaktion wird als atomar betrachtet. Entweder werden alle Operationen erfolgreich ausgeführt, oder keine davon. Wenn eine Operation fehlschlägt, werden alle vorherigen Operationen rückgängig gemacht, um sicherzustellen, dass die Datenbank in einem konsistenten Zustand bleibt.

- Consistency: Transaktionen müssen die Datenbank in einen gültigen und konsistenten Zustand bringen. Nach dem Abschluss einer Transaktion sollten die Datenbankregeln und -beschränkungen eingehalten werden.

- Isolation: Transaktionen sollten isoliert voneinander ausgeführt werden, um Interferenzen zu vermeiden. Wenn mehrere Transaktionen gleichzeitig ablaufen, sollten sie sich nicht gegenseitig beeinflussen oder durcheinanderbringen.

- Durability: Sobald eine Transaktion abgeschlossen ist, sollten die darin vorgenommenen Änderungen dauerhaft in der Datenbank gespeichert werden. Selbst nach einem Stromausfall oder einem Neustart der Datenbank sollten die Daten noch vorhanden sein.

## Praxis
### Aufgabe 1 (Leicht)
Angenommen, du entwickelst ein System zur Bestandsverwaltung für ein Warenlager. Implementiere eine Transaktion

, um den Bestand eines Produkts zu aktualisieren und die Bestellinformationen hinzuzufügen. Verwende die folgenden Funktionen: `update_inventory(product_id, quantity)` und `add_order_info(order_id, product_id, quantity)`.

#### Musterlösung:
```python
def process_order(product_id, quantity, order_id):
    try:
        # Start der Transaktion
        start_transaction()
        
        # Bestand aktualisieren
        update_inventory(product_id, quantity)
        
        # Bestellinformationen hinzufügen
        add_order_info(order_id, product_id, quantity)
        
        # Transaktion erfolgreich
        commit_transaction()
        
        print("Bestellung erfolgreich bearbeitet!")
    except Exception as e:
        # Transaktion fehlgeschlagen
        rollback_transaction()
        
        print("Fehler bei der Bestellverarbeitung:", str(e))
```

### Aufgabe 2 (Schwer)
Angenommen, du entwickelst ein Bankensystem und musst eine Transaktion implementieren, um Geld von einem Konto auf ein anderes zu überweisen. Implementiere die Funktion `transfer_funds(from_account, to_account, amount)`, die die Überweisung durchführt. Stelle sicher, dass die Transaktion atomar ist und bei Fehlern rückgängig gemacht wird.

#### Musterlösung:
```python
def transfer_funds(from_account, to_account, amount):
    try:
        # Start der Transaktion
        start_transaction()
        
        # Abhebung vom Konto A
        withdraw(from_account, amount)
        
        # Einzahlung auf Konto B
        deposit(to_account, amount)
        
        # Transaktion erfolgreich
        commit_transaction()
        
        print("Geldüberweisung erfolgreich!")
    except Exception as e:
        # Transaktion fehlgeschlagen
        rollback_transaction()
        
        print("Fehler bei der Geldüberweisung:", str(e))
```

Herzlichen Glückwunsch! Du hast erfolgreich Transaktionen in Python gelernt und bist nun in der Lage, Datenbankoperationen sicher und zuverlässig auszuführen.

Viel Spaß beim Programmieren und Aufpassen auf deine Daten!