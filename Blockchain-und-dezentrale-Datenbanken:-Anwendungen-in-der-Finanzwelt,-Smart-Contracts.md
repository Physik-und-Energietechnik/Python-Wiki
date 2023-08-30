
# Blockchain und dezentrale Datenbanken: Anwendungen in der Finanzwelt, Smart Contracts

## Einführung

Willkommen zum faszinierenden Abschnitt über Blockchain und dezentrale Datenbanken! In diesem Tutorial tauchen wir in die Welt der Technologien ein, die die Finanzwelt revolutionieren und darüber hinausgehen. Keine Sorge, wenn dir der Begriff "Blockchain" noch fremd ist. Wir werden alles Schritt für Schritt erkunden.

## Was du lernen wirst

In diesem Abschnitt wirst du Folgendes kennenlernen:

- Was Blockchain ist und wie sie funktioniert, ohne in komplizierte technische Details abzudriften.
- Die Anwendungen von Blockchain in der Finanzwelt, von Kryptowährungen bis hin zu sicheren Transaktionen.
- Smart Contracts und wie sie Verträge automatisieren und menschliche Fehler reduzieren.

## Theorie

### Was ist Blockchain?

Stell dir vor, eine Blockchain ist wie ein digitales, öffentliches Notizbuch. Jedes Mal, wenn eine Transaktion stattfindet, wird sie in diesem Notizbuch aufgeschrieben und mit den vorherigen Transaktionen verknüpft. Dadurch entsteht eine Kette von Transaktionen, daher der Name "Blockchain".

Hier ist ein einfaches Python-Beispiel, um dir eine Idee zu geben, wie eine Blockchain funktioniert:

```python
# Annahme: Eine einfache Blockchain-Struktur
blockchain = [
    {'previous_hash': None, 'data': 'Startblock'},
    {'previous_hash': 'hash1', 'data': 'Transaktion 1'},
    {'previous_hash': 'hash2', 'data': 'Transaktion 2'},
    # ...
]

# Neue Transaktion hinzufügen
new_transaction = {'previous_hash': 'hash3', 'data': 'Transaktion 3'}
blockchain.append(new_transaction)
```

### Anwendungen in der Finanzwelt

Blockchain hat die Finanzwelt im Sturm erobert, besonders durch Kryptowährungen wie Bitcoin. Diese digitalen Währungen nutzen die Blockchain-Technologie, um sichere und dezentrale Transaktionen zu ermöglichen, ohne eine zentrale Autorität wie eine Bank.

### Smart Contracts

Smart Contracts sind wie digitale Verträge, die automatisch ausgeführt werden, sobald bestimmte Bedingungen erfüllt sind. Zum Beispiel könnten wir einen Smart Contract erstellen, der eine Zahlung automatisch an den Verkäufer freigibt, sobald das Produkt vom Käufer erhalten wird.

Hier ist ein einfaches Python-Beispiel für einen Smart Contract:

```python
# Annahme: Ein einfacher Smart Contract zur Zahlungsfreigabe
contract = {
    'seller': 'Verkäufer123',
    'buyer': 'Käufer456',
    'product_received': False,
    'payment_released': False
}

# Produkt empfangen, um den Vertrag zu erfüllen
contract['product_received'] = True

# Zahlung freigeben, weil Bedingungen erfüllt sind
if contract['product_received']:
    contract['payment_released'] = True
```

## Praxis

### Leichte Aufgabe

Deine Aufgabe ist es, eine einfache Blockchain in Python zu erstellen, um Transaktionen zu verfolgen.

### Musterlösung

```python
blockchain = [
    {'previous_hash': None, 'data': 'Startblock'},
    # ...
]

def add_transaction(data):
    previous_hash = blockchain[-1]['previous_hash']
    new_transaction = {'previous_hash': previous_hash, 'data': data}
    blockchain.append(new_transaction)

# Neue Transaktionen hinzufügen
add_transaction('Transaktion 1')
add_transaction('Transaktion 2')
```

### Schwierige Aufgabe

Für Fortgeschrittene: Versuche, einen einfachen Smart Contract in Python zu erstellen, der die Freigabe einer Zahlung automatisch basierend auf bestimmten Bedingungen regelt.

### Musterlösung

Die Erstellung komplexer Smart Contracts erfordert tieferes Wissen über Blockchain-Technologie. Hier ist eine vereinfachte Version:

```python
contract = {
    'seller': 'Verkäufer123',
    'buyer': 'Käufer456',
    'product_received': False,
    'payment_released': False
}

# Produkt empfangen, um den Vertrag zu erfüllen
contract['product_received'] = True

# Zahlung freigeben, weil Bedingungen erfüllt sind
if contract['product_received']:
    contract['payment_released'] = True
```

Du hast jetzt einen spannenden Einblick in die Welt der Blockchain und dezentralen Datenbanken erhalten. Viel Spaß beim Erkunden dieser aufstrebenden Technologien!

