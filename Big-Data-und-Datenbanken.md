
# Big Data und Datenbanken

## Einführung

Hallo, wagemutige Datenabenteurer! Heute werden wir uns in den wilden Dschungel der Big Data stürzen und dabei unsere treuen Begleiter, die Datenbanken, mitnehmen. 🌍📊

Hast du dich jemals gefragt, wie Unternehmen Millionen von Datenpunkten verarbeiten? Hier kommen Big Data und Datenbanken ins Spiel! Wir werden entdecken, wie Datenbanken in riesigen Datenumgebungen eingesetzt werden, um Ordnung im Datenchaos zu schaffen.

## Theorie

### Big Data - Die Überflutung der Datenwelt

Big Data ist wie ein riesiger Berg aus Informationen, der immer größer wird. Es sind Daten, die so massiv sind, dass sie nicht mehr in herkömmlichen Methoden verarbeitet werden können. Hier kommen spezialisierte Werkzeuge wie Hadoop und Spark ins Spiel!

### Datenbanken im Big-Data-Kosmos

Datenbanken sind wie die Hüter der Weisheit im Land der Daten. In der Welt von Big Data helfen sie, riesige Datenmengen zu speichern, zu organisieren und abzufragen. Sie arbeiten oft Hand in Hand mit Tools wie Hadoop und Spark, um Datenverarbeitung und -analyse auf eine Weise zu bewältigen, die unser kleines Programmiererherz vor Freude hüpfen lässt.

### Code-Beispiel: Datenbanken und Big Data

Hier ist ein einfaches Beispiel, wie Daten aus einer Datenbank mit Spark verarbeitet werden können:

```python
from pyspark.sql import SparkSession

# Spark-Session erstellen
spark = SparkSession.builder.appName("example").getOrCreate()

# Daten aus der Datenbank laden
df = spark.read.jdbc("jdbc:mysql://localhost:3306/database", "table_name", properties={"user": "your_user", "password": "your_password"})

# Daten analysieren
result = df.groupBy("column_name").count()
result.show()
```

## Praxis

### Leichte Aufgabe

Deine Mission, sollte du sie akzeptieren, ist es, eine einfache Datenbank mit ein paar Datensätzen zu erstellen. Verwende dann Spark, um die Durchschnittswerte einer bestimmten Spalte zu berechnen.

Musterlösung:

```python
# Spark-Session erstellen (siehe vorheriges Beispiel)

# Daten aus der Datenbank laden
df = spark.read.jdbc("jdbc:mysql://localhost:3306/database", "table_name", properties={"user": "your_user", "password": "your_password"})

# Durchschnitt einer Spalte berechnen
average = df.selectExpr("AVG(column_name)").collect()[0][0]
print(average)
```

### Schwierige Aufgabe

Bereit für eine größere Herausforderung? Verwende Hadoop, um riesige CSV-Dateien zu analysieren. Lade die Daten, gruppiere sie nach einer Spalte und zähle die Anzahl der Datensätze in jeder Gruppe.

Musterlösung:

```python
from mrjob.job import MRJob

class GroupAndCount(MRJob):
    
    def mapper(self, _, line):
        # Zeilen in Spalten aufteilen
        columns = line.split(",")
        group_key = columns[0]
        yield (group_key, 1)
        
    def reducer(self, key, values):
        yield (key, sum(values))

if __name__ == '__main__':
    GroupAndCount.run()
```

## Fazit

Bravo, du hast den Gipfel der Datenberge erklommen! Mit Python, Datenbanken, Hadoop und Spark kannst du die Magie von Big Data erleben. Jetzt kannst du Datenberge erklimmen, Muster entdecken und Einblicke gewinnen, die vorher verborgen waren. Denke daran, dass du mit großer Macht (und großen Daten) auch große Verantwortung hast. Auf zur nächsten Datenschatzsuche!
