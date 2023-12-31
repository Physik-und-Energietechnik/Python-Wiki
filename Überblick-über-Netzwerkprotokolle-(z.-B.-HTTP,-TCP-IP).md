
## Einführung
Willkommen zu diesem aufregenden Abschnitt des Tutorials! Heute begeben wir uns auf eine Reise in die Welt der Netzwerkprotokolle. Aber Moment mal, was sind Netzwerkprotokolle überhaupt? Keine Sorge, ich werde es dir auf eine Weise erklären, dass selbst ein Tintenfisch es verstehen würde!

Stell dir vor, du schreibst einen Brief an deinen besten Freund. Du steckst den Brief in einen Umschlag und schreibst die Adresse darauf. Dann gibst du den Umschlag der Post, die ihn zum Empfänger bringt. Der Umschlag und die Art und Weise, wie du den Brief verpackst und die Adresse schreibst, sind wie Netzwerkprotokolle. Sie stellen sicher, dass die Informationen auf dem Weg zwischen Absender und Empfänger korrekt übertragen werden.

In diesem Tutorial werden wir einen Überblick über zwei wichtige Netzwerkprotokolle erhalten: HTTP und TCP/IP. Wir werden lernen, wie sie funktionieren und wie Python uns dabei helfen kann, mit ihnen zu interagieren. Also, schnall dich an und lass uns in die wundervolle Welt der Netzwerkprotokolle eintauchen!

## Theorie
### HTTP - Das HyperText Transfer Protocol
HTTP ist wie ein Kommunikationsmittel zwischen einem Client (z. B. deinem Webbrowser) und einem Server (z. B. einer Webseite). Es ermöglicht den Austausch von Informationen in Form von Hypertext-Dokumenten. Hier ist ein allgemeines Beispiel, wie eine HTTP-Anfrage und eine HTTP-Antwort aussehen könnten:

```python
# HTTP-Anfrage
GET /index.html HTTP/1.1
Host: www.example.com

# HTTP-Antwort
HTTP/1.1 200 OK
Content-Type: text/html
Content-Length: 1274

<html>
<head>
  <title>Willkommen auf meiner Webseite</title>
</head>
<body>
  <h1>Hallo, Welt!</h1>
</body>
</html>
```

### TCP/IP - Das Transmission Control Protocol/Internet Protocol
TCP/IP ist wie das Rückgrat des Internets. Es ist ein Protokollstapel, der aus verschiedenen Schichten besteht und sicherstellt, dass Datenpakete zwischen verschiedenen Computern im Internet korrekt übertragen werden. TCP kümmert sich um die Zuverlässigkeit und die Reihenfolge der Übertragung, während IP für die Adressierung und das Routing der Datenpakete zuständig ist.

### Python und Netzwerkprotokolle
Jetzt kommt der aufregende Teil! Python bietet uns eine Vielzahl von Modulen und Bibliotheken, um mit Netzwerkprotokollen zu interagieren. Hier ist ein Beispiel, wie wir mit dem `requests`-Modul eine HTTP-Anfrage senden und die Antwort erhalten können:

```python
import requests

response = requests.get("https://www.example.com")
print(response.text)
```

In diesem Beispiel verwenden wir das `requests`-Modul, um eine HTTP-GET-Anfrage an `www.example.com` zu senden. Die Antwort speichern wir in der Variable `response` und geben den Inhalt der Antwort mit `response.text` aus.

## Praxis
Jetzt ist es an der Zeit, dein erlangtes Wissen zu überprüfen! Hier ist eine leichte Aufgabe für dich: Schreibe einen

 Python-Code, der eine HTTP-Anfrage an eine beliebige Webseite sendet und den Statuscode der Antwort ausgibt. Hier ist ein Beispiel für die Lösung:

```python
import requests

response = requests.get("https://www.example.com")
print("Statuscode:", response.status_code)
```

Mit diesem Code senden wir eine HTTP-GET-Anfrage an `www.example.com` und geben den Statuscode der Antwort aus.

## Fazit
Herzlichen Glückwunsch! Du hast erfolgreich einen Überblick über Netzwerkprotokolle wie HTTP und TCP/IP erhalten. Du hast gelernt, dass HTTP das Protokoll ist, das den Austausch von Informationen zwischen einem Client und einem Server ermöglicht. TCP/IP ist das Rückgrat des Internets und sorgt dafür, dass Datenpakete zuverlässig übertragen werden.

Außerdem hast du gesehen, wie Python uns dabei helfen kann, mit Netzwerkprotokollen zu interagieren. Mit dem `requests`-Modul können wir HTTP-Anfragen senden und die Antworten erhalten. Du bist nun bereit, die Welt der Netzwerkprotokolle mit Python zu erkunden und erstaunliche Dinge zu tun!

Mach weiter so und lass deine Python-Kenntnisse wachsen!