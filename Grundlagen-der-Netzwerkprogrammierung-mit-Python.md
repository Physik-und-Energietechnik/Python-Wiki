# 2. Grundlagen der Netzwerkprogrammierung mit Python

## 2.1 Überblick über Netzwerkprotokolle (z. B. HTTP, TCP/IP)

Netzwerkprotokolle sind die grundlegenden Regeln und Verfahren, die es ermöglichen, dass Computer miteinander kommunizieren können. Einige der gängigen Netzwerkprotokolle umfassen HTTP (Hypertext Transfer Protocol), TCP (Transmission Control Protocol) und IP (Internet Protocol).

### Beispielcode (allgemeines Code-Beispiel):
```python
# TCP/IP Socket erstellen
import socket

# Host und Port festlegen
host = 'www.example.com'
port = 80

# Socket erstellen
sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

# Verbindung zum Server herstellen
sock.connect((host, port))

# Daten senden
message = 'GET / HTTP/1.1\r\nHost: {}\r\n\r\n'.format(host)
sock.sendall(message.encode())

# Daten empfangen
response = sock.recv(4096)

# Verbindung schließen
sock.close()

print(response.decode())
```

## 2.2 Verwendung von Python-Sockets für die Netzwerkkommunikation

Python bietet das `socket`-Modul, das die Netzwerkprogrammierung erleichtert. Mit `socket` können wir Verbindungen zu Servern herstellen, Daten senden und empfangen.

### Beispielcode (allgemeines Code-Beispiel):
```python
# TCP/IP Socket erstellen
import socket

# Host und Port festlegen
host = 'www.example.com'
port = 80

# Socket erstellen
sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

# Verbindung zum Server herstellen
sock.connect((host, port))

# Daten senden
message = 'Hello, server!'
sock.sendall(message.encode())

# Daten empfangen
response = sock.recv(4096)

# Verbindung schließen
sock.close()

print(response.decode())
```

## 2.3 HTTP-Anfragen und -Antworten verstehen

HTTP (Hypertext Transfer Protocol) ist ein weit verbreitetes Protokoll für die Übertragung von Daten über das Internet. Es wird verwendet, um Webseiten, Bilder, Videos und andere Ressourcen abzurufen.

Eine HTTP-Anfrage besteht aus einer Methode (z. B. GET oder POST), einem Pfad zur Ressource und optionalen Header-Informationen. Die HTTP-Antwort enthält den Statuscode, Header-Informationen und den Inhalt der angeforderten Ressource.

### Beispielcode (allgemeines Code-Beispiel):
```python
import requests

# HTTP-GET-Anfrage senden
response = requests.get('https://www.example.com')

# Antwortstatuscode abrufen
status_code = response.status_code

# Antwortinhalt abrufen
content = response.content

print(status_code)
print(content)
```

### Beispielcode (explizites Code-Beispiel in Python):
```python
import http.client

# HTTP-Verbindung herstellen
conn = http.client.HTTPSConnection("www.example.com")

# GET-Anfrage senden
conn.request("GET", "/")

# Antwort erhalten
response = conn.getresponse()

# Antwortstatuscode abrufen
status_code = response.status

# Antwortinhalt abrufen
content = response.read()

# Verbindung schließen
conn.close()

print(status_code)
print(content.decode())
```

## 3. Praxis

### Leichte Aufgabe

Schreibe ein Python

-Programm, das eine HTTP-GET-Anfrage an eine beliebige URL sendet und den Inhalt der Antwort auf der Konsole ausgibt.

#### Musterlösung

```python
import requests

# URL festlegen
url = 'https://www.example.com'

# HTTP-GET-Anfrage senden
response = requests.get(url)

# Antwortinhalt abrufen und ausgeben
print(response.content)
```

### Schwere Aufgabe

Schreibe ein Python-Programm, das einen einfachen HTTP-Server erstellt und eine HTTP-POST-Anfrage mit JSON-Daten empfangen kann. Das empfangene JSON soll auf der Konsole ausgegeben werden.

#### Musterlösung

```python
from http.server import BaseHTTPRequestHandler, HTTPServer
import json

# Server-Klasse erstellen
class RequestHandler(BaseHTTPRequestHandler):
    # POST-Anfragen verarbeiten
    def do_POST(self):
        # Header setzen
        self.send_response(200)
        self.send_header('Content-type', 'text/plain')
        self.end_headers()

        # POST-Daten empfangen und dekodieren
        content_length = int(self.headers['Content-Length'])
        post_data = self.rfile.read(content_length).decode('utf-8')

        # JSON-Daten parsen und ausgeben
        json_data = json.loads(post_data)
        print(json_data)

        # Antwort senden
        self.wfile.write(b'Success')

# Server erstellen und starten
server_address = ('', 8000)
httpd = HTTPServer(server_address, RequestHandler)
print('Server läuft auf http://localhost:8000')
httpd.serve_forever()
```

Das waren die Grundlagen der Netzwerkprogrammierung mit Python. Mit diesem Wissen kannst du Netzwerkprotokolle verstehen, Python-Sockets verwenden und HTTP-Anfragen und -Antworten manipulieren. Viel Spaß beim Programmieren!