
## Einführung

Willkommen zu unserem Python-Tutorial über das Einrichten eines HTTP-Servers! In diesem Tutorial werden wir lernen, wie wir mit Python einen einfachen HTTP-Server erstellen können. Keine Sorge, wenn du noch keine Erfahrung mit Python hast, wir werden alles Schritt für Schritt erklären.

Bevor wir jedoch in die Praxis eintauchen, lassen uns etwas Theorie durchgehen, um ein grundlegendes Verständnis von HTTP-Servern zu bekommen.

## Theorie

Ein HTTP-Server ist ein Programm, das Anfragen von Clients über das Hypertext Transfer Protocol (HTTP) empfängt und darauf antwortet. Der Server hört auf bestimmten Netzwerkports und kann verschiedene Anfragen wie GET, POST, PUT und DELETE behandeln.

Hier ist ein allgemeines Beispiel für das Einrichten eines einfachen HTTP-Servers mit Python:

```python
from http.server import BaseHTTPRequestHandler, HTTPServer

class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type', 'text/html')
        self.end_headers()
        self.wfile.write(b'Hello, World!')

def run_server(port):
    server_address = ('', port)
    httpd = HTTPServer(server_address, MyServer)
    print(f'Server läuft auf Port {port}')
    httpd.serve_forever()

port = 8000
run_server(port)
```

## Praxis

Nun ist es an der Zeit, unser Wissen in die Praxis umzusetzen. Deine Aufgabe besteht darin, einen einfachen HTTP-Server zu erstellen, der eine HTML-Seite ausliefert. Hier ist eine Beispiel-Aufgabe:

**Aufgabe:** Erstelle einen HTTP-Server, der die Datei "index.html" ausliefert, wenn ein Client eine GET-Anfrage an die Wurzel-URL sendet.

**Musterlösung:**

```python
from http.server import BaseHTTPRequestHandler, HTTPServer

class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        if self.path == '/':
            self.send_response(200)
            self.send_header('Content-type', 'text/html')
            self.end_headers()
            with open('index.html', 'rb') as file:
                self.wfile.write(file.read())
        else:
            self.send_response(404)
            self.send_header('Content-type', 'text/plain')
            self.end_headers()
            self.wfile.write(b'404 Not Found')

def run_server(port):
    server_address = ('', port)
    httpd = HTTPServer(server_address, MyServer)
    print(f'Server läuft auf Port {port}')
    httpd.serve_forever()

port = 8000
run_server(port)
```

Erstelle eine Datei namens "index.html" im gleichen Verzeichnis wie den Python-Code. Füge den gewünschten HTML-Inhalt in diese Datei ein. Starte den Server und öffne dann deinen Browser, um die Seite auf http://localhost:8000/ zu sehen.

## Fazit

Herzlichen Glückwunsch! Du hast gerade gelernt, wie man einen einfachen HTTP-Server mit Python erstellt. Du kannst jetzt eigene Server erstellen und Anfragen von Clients empfangen und verarbeiten.

HTTP-Server sind die Grundlage für viele Webanwendungen und bieten die Möglichkeit, Inhalte und Daten über das Internet bereitzustellen. Nutze dein Wissen und werde zum Meister der HTTP-Kommunikation!

Jetzt bist du bereit, deine eigenen Server zu erstellen und mit der Welt zu teilen. Viel Spaß beim Codieren und Erforschen der unendlichen Möglichkeiten, die dir ein HTTP-Server bietet!