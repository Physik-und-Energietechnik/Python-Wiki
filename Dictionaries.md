

# Python Tutorial - Dictionaries

## Einführung
In diesem Abschnitt lernst du, wie du in Python Daten in einem formatierten und organisierten Format speichern und abrufen kannst. Mit Dictionaries kannst du Daten in Form von Schlüssel-Wert-Paaren speichern. Diese Art der Datenstruktur kann besonders nützlich sein, wenn du große Datenmengen verarbeiten musst, da sie effizienten Zugriff auf Einträge bietet. Am Ende dieses Tutorials wirst du in der Lage sein, Dictionaries zu erstellen, auf Einträge zuzugreifen, sie zu bearbeiten und vieles mehr!
## Theorie

### Sortiert/Unsortiert
Im Gegensatz zu Listen, die eine geordnete Struktur haben, sind Dictionaries unsortiert. Das bedeutet, dass es keine feste Reihenfolge gibt, in der die Einträge gespeichert werden. Die Einträge werden stattdessen durch ihre Schlüssel referenziert.

### Keine Duplikate
Dictionaries erlauben keine Duplikate bei den Schlüsseln. Wenn du versuchst, einen Eintrag mit einem Schlüssel zu erstellen, der bereits im Dictionary existiert, wird der vorherige Eintrag durch den neuen ersetzt.

### Erstellen eines Dictionaries
Ein Dictionary kann auf verschiedene Weise erstellt werden, aber die einfachste besteht darin, geschweifte Klammern {} zu verwenden und die Schlüssel-Wert-Paare durch ein Doppelpunkt zu trennen. Die Schlüssel und Werte können verschiedene Datentypen haben. Hier ist ein Beispiel:

```python
my_dict = {"Name": "Max", "Alter": 23, "Hobby": "Schwimmen"}
```

### Der dict() Konstruktor
Du kannst ein Dictionary auch mit dem dict() Konstruktor erstellen. Der Konstruktor kann eine Liste von Schlüssel-Wert-Paaren oder ein anderes Dictionary als Argument entgegennehmen.

```python
# Allgemeines Code-Beispiel
my_dict = dict(Name='Max', Alter=30, Stadt='Berlin')
print(my_dict)   # Output: {'Name': 'Max', 'Alter': 30, 'Stadt': 'Berlin'}
```

### Hinzufügen von Einträgen
Wenn du einen neuen Eintrag zu einem Dictionary hinzufügen möchtest, musst du einfach einen neuen Schlüssel-Wert-Paar definieren und ihn dem Dictionary zuweisen.

```python
# Hinzufügen von Einträgen
person = {'name': 'Max', 'age': 25, 'city': 'Berlin'}
person['job'] = 'Developer'
print(person) # Output: {'name': 'Max', 'age': 25, 'city': 'Berlin', 'job': 'Developer'}
```

### Zugriff auf Einträge
Um auf einen Eintrag in einem Dictionary zuzugreifen, kannst du den Schlüssel in eckigen Klammern angeben. Wenn der Schlüssel nicht existiert, erhältst du einen KeyError.

```python
my_dict = {'Name': 'Max', 'Alter': 30, 'Stadt': 'Berlin'}
print(my_dict['Name'])   # Output: Max
# KeyError, wenn der Schlüssel nicht existiert
# print(my_dict['job'])
```

### Zugriff auf Schlüssel
Du kannst auch auf alle Schlüssel in einem Dictionary mit der keys() Methode zugreifen.

```python
my_dict = {'Name': 'Max', 'Alter': 30, 'Stadt': 'Berlin'}
print(my_dict.keys())   # Output: dict_keys(['Name', 'Alter', 'Stadt'])
```

### Ändern von Einträgen
Wenn du den Wert eines Eintrags in einem Dictionary ändern möchtest, musst du einfach auf den Schlüssel zugreifen und ihm einen neuen Wert zuweisen.

```python
# Ändern von Einträgen
person = {'name': 'Max', 'age': 25, 'city': 'Berlin'}
person['age'] = 26
print(person) # Output: {'name': 'Max', 'age': 26, 'city': 'Berlin'}
```

### Die update() Methode
Die `update()` Methode ermöglicht es, ein Dictionary mit den Schlüssel-Wert-Paaren eines anderen Dictionaries oder einer Liste von Schlüssel-Wert-Paaren zu aktualisieren:

```python
my_dict = {"Name": "Max", "Alter": 23, "Hobby": "Schwimmen"}
new_data = {"Alter": 24, "Wohnort": "Berlin"}
my_dict.update(new_data)
print(my_dict)
```


### Löschen von Einträgen
Wenn du einen Eintrag aus einem Dictionary löschen möchtest, kannst du die del Anweisung verwenden. Du gibst einfach den Schlüssel an, der gelöscht werden soll. Zum Beispiel:

```python
person = {"name": "Max", "alter": 30, "stadt": "Berlin"}
del person["stadt"]
print(person)  # {"name": "Max", "alter": 30}
```

In diesem Beispiel wird der Schlüssel `"stadt"` aus dem `person`-Dictionary gelöscht.

### Die pop() Methode
Die `pop()` Methode entfernt den Eintrag mit dem angegebenen Schlüssel aus dem Dictionary und gibt dessen Wert zurück. Wenn der Schlüssel nicht im Dictionary vorhanden ist, wird ein KeyError ausgelöst.

Hier ist ein Beispiel, wie du `pop()` verwendest:

```python
mein_dict = {"Name": "Max", "Alter": 25, "Stadt": "Berlin"}

alter = mein_dict.pop("Alter")

print(mein_dict) # {"Name": "Max", "Stadt": "Berlin"}
print(alter)     # 25
```

In diesem Beispiel wird der Eintrag mit dem Schlüssel "Alter" aus dem Dictionary `mein_dict` entfernt und sein Wert in der Variable `alter` gespeichert. Das verbleibende Dictionary wird dann ausgegeben.

### Die popitem() Methode
Die `popitem()` Methode entfernt das letzte Schlüssel-Wert-Paar aus dem Dictionary und gibt es als Tupel zurück. Wenn das Dictionary leer ist, wird ein KeyError ausgelöst.

Hier ist ein Beispiel, wie du `popitem()` verwendest:

```python
mein_dict = {"Name": "Max", "Alter": 25, "Stadt": "Berlin"}

letztes = mein_dict.popitem()

print(mein_dict) # {"Name": "Max", "Alter": 25}
print(letztes)   # ("Stadt", "Berlin")
```

In diesem Beispiel wird das letzte Schlüssel-Wert-Paar des Dictionaries `mein_dict` entfernt und als Tupel in der Variable `letztes` gespeichert. Das verbleibende Dictionary wird dann ausgegeben.

Wenn du alle Einträge aus einem Dictionary entfernen möchtest, kannst du die `clear()` Methode verwenden:

```python
person.clear()
print(person)  # {}
```

### Durch ein Dictionary Schleifen

Es gibt verschiedene Möglichkeiten, durch ein Dictionary zu iterieren und auf dessen Elemente zuzugreifen. Eine Möglichkeit besteht darin, die `items()` Methode zu verwenden, die eine Liste von Tupeln zurückgibt, wobei jedes Tupel einen Schlüssel und den dazugehörigen Wert enthält. Zum Beispiel:

```python
person = {"name": "Max", "alter": 30, "stadt": "Berlin"}

for key, value in person.items():
    print(key + ":", value)
```

Dies würde folgende Ausgabe erzeugen:

```
name: Max
alter: 30
stadt: Berlin
```

Eine andere Möglichkeit besteht darin, nur über die Schlüssel oder nur über die Werte zu iterieren. Dazu kannst du die Methoden `keys()` und `values()` verwenden. Zum Beispiel:

```python
for key in person.keys():
    print(key)

for value in person.values():
    print(value)
```

### Kopieren von Dictionaries

Manchmal musst du ein Dictionary kopieren, um eine unabhängige Kopie des ursprünglichen Dictionarys zu erstellen. Dazu gibt es zwei Möglichkeiten: die `copy()` Methode und den `dict()` Konstruktor.

```python
person = {"name": "Max", "alter": 30, "stadt": "Berlin"}

# Mit der copy() Methode
person_copy = person.copy()

# Mit dem dict() Konstruktor
person_copy2 = dict(person)

# Überprüfung der Kopien
print(person == person_copy == person_copy2)  # True
```

### Verschachtelte Dictionaries

Es ist möglich, ein Dictionary innerhalb eines anderen Dictionarys zu erstellen. Das kann nützlich sein, wenn du zum Beispiel eine Datenstruktur benötigst, die aus mehreren Ebenen besteht. Hier ist ein Beispiel:

```python
person = {"name": "Max", "alter": 30, "adressen": {"privat": "Hauptstraße 1", "arbeit": "Nebenstraße 2"}}
print(person["adressen"]["privat"])  # Hauptstraße 1
```

In diesem Beispiel ist das Dictionary `"adressen"` ein Dictionary, das innerhalb des `person`-Dictionarys verschachtelt ist. Du kannst auf die Werte innerhalb des verschachtelten Dictionarys zugreifen, indem du den Schlüssel des äußeren Dictionarys gefolgt von dem Schlüssel des inneren Dictionarys angibst.

### Länge eines Dictionaries
Die Länge eines Dictionaries gibt die Anzahl der Einträge im Dictionary zurück. Du kannst die Länge eines Dictionaries mit der len() Funktion ermitteln.

```python
my_dict = {'Name': 'Max', 'Alter': 30, 'Stadt': 'Berlin'}
print(len(my_dict))   # Output: 3
```

## Zusammenfassung
