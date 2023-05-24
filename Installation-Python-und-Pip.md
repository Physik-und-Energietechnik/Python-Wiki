# Python Installation

Python ist eine leistungsstarke und beliebte Programmiersprache, die für ihre Einfachheit und Lesbarkeit bekannt ist. In diesem Abschnitt werden wir dir erklären, wie du Python auf deinem System installieren kannst, damit du mit dem Programmieren in Python beginnen kannst.

## 1. Herunterladen der Python-Installationsdatei

Um Python auf deinem Computer zu installieren, musst du zuerst die entsprechende Installationsdatei von der offiziellen Python-Website herunterladen. Folge diesen Schritten:

1. Öffne einen Webbrowser und gehe zur offiziellen Python-Website: https://www.python.org/
2. Klicke auf den Button "Downloads" in der oberen Menüleiste.
3. Du siehst nun verschiedene Python-Versionen zur Auswahl. Wähle die neueste stabile Version aus, die mit deinem Betriebssystem kompatibel ist. Wenn du unsicher bist, welches Betriebssystem du hast, kannst du dies in den Systemeinstellungen oder Systeminformationen nachschauen.
4. Scrolle nach unten auf der Download-Seite und suche nach der Überschrift "Stable Releases". Dort findest du die Installationsdateien für verschiedene Betriebssysteme.
5. Klicke auf den Link, um die Installationsdatei herunterzuladen. Je nach Betriebssystem wird dies eine ausführbare Datei (z.B. .exe für Windows) oder ein Paket (z.B. .pkg für macOS) sein.

## 2. Installation von Python

Sobald du die Installationsdatei heruntergeladen hast, kannst du mit der Installation von Python beginnen. Folge diesen Schritten, um Python auf deinem System zu installieren:

### Windows:

1. Doppelklicke auf die heruntergeladene Installationsdatei (.exe).
2. Aktiviere das Kontrollkästchen "Add Python to PATH" (Python zum Pfad hinzufügen).
3. Klicke auf "Customize Installation" (Installation anpassen), wenn du spezifische Optionen ändern möchtest. Andernfalls kannst du die Standardeinstellungen beibehalten.
4. Klicke auf "Install Now" (Jetzt installieren), um die Installation zu starten.
5. Warte, bis die Installation abgeschlossen ist. Du kannst den Fortschritt auf dem Bildschirm verfolgen.
6. Klicke auf "Close" (Schließen), um den Installationsassistenten zu beenden.

### macOS:

1. Doppelklicke auf die heruntergeladene Installationsdatei (.pkg).
2. Befolge die Anweisungen des Installationsassistenten und klicke auf "Continue" (Fortfahren).
3. Du kannst spezifische Optionen anpassen, indem du auf "Customize Installation" (Installation anpassen) klickst. Andernfalls kannst du die Standardeinstellungen beibehalten.
4. Klicke auf "Install" (Installieren), um die Installation zu starten. Du musst möglicherweise dein Passwort eingeben, um fortzufahren.
5. Warte, bis die Installation abgeschlossen ist. Du kannst den Fortschritt auf dem Bildschirm verfolgen.
6. Klicke auf "Close" (Schließen), um den Installationsassistenten zu beenden.

### Linux:

Die Vorgehensweise zur Installation von Python kann je nach Linux-Distribution variieren. In den meisten Fällen kannst du jedoch die Paketverwaltung deiner Distribution verwenden, um Python zu installieren. Du kannst die folgenden Befehle in einem Terminal ausführen:

```bash
sudo apt-get update
sudo apt-get install python3
```

Diese Befehle aktualisieren zuerst die Paketliste und installieren dann Python 3 auf deinem System. Je nach Distribution und Konfiguration kann es erforderlich sein, `python3` durch `python` zu ersetzen.

## 3. Überprüfe die Installation

Nachdem die Installation abgeschlossen ist, kannst du überprüfen, ob Python erfolgreich installiert wurde, indem du den folgenden Befehl in einem Terminal oder der Eingabeaufforderung ausführst:

```bash
python --version
```

Wenn du die installierte Python-Version angezeigt bekommst (z.B. "Python 3.9.2"), bedeutet dies, dass Python erfolgreich installiert wurde.

Herzlichen Glückwunsch! Du hast Python erfolgreich auf deinem System installiert und bist nun bereit, in Python zu programmieren. Du kannst einen Texteditor oder eine Entwicklungsumgebung öffnen und mit dem Schreiben deines ersten Python-Codes beginnen.

Viel Spaß beim Entdecken der vielfältigen Möglichkeiten von Python und dem Erstellen großartiger Programme!


# Pip Installation

Pip ist ein Paketverwaltungssystem für Python, das dir dabei hilft, zusätzliche Python-Pakete und -Module einfach zu installieren. In diesem Abschnitt werde ich dir erklären, wie du Pip auf deinem System installieren kannst, um von den zahlreichen verfügbaren Python-Paketen zu profitieren.

## 1. Überprüfe, ob Python installiert ist

Bevor du Pip installierst, solltest du sicherstellen, dass Python bereits auf deinem System installiert ist. Du kannst dies überprüfen, indem du den folgenden Befehl in deinem Terminal oder der Eingabeaufforderung ausführst:

```bash
python --version
```

Wenn du eine Python-Version angezeigt bekommst (z. B. "Python 3.9.2"), bedeutet dies, dass Python bereits installiert ist. Wenn die Ausgabe eine Fehlermeldung ist oder du keine Python-Version angezeigt bekommst, musst du Python zuerst installieren, bevor du Pip verwenden kannst.

## 2. Installiere Pip

Die Installation von Pip ist in der Regel recht einfach. Folge den Schritten entsprechend deinem Betriebssystem:

### Windows:

1. Öffne den Webbrowser und gehe zur offiziellen Pip-Website: https://pip.pypa.io/en/stable/installing/
2. Lade das Skript "get-pip.py" herunter, indem du auf den Link "get-pip.py" klickst.
3. Navigiere im Datei-Explorer zu dem Ordner, in dem du "get-pip.py" heruntergeladen hast.
4. Halte die Umschalttaste gedrückt, klicke mit der rechten Maustaste in den Ordner und wähle "Eingabeaufforderung hier öffnen" aus dem Kontextmenü.
5. Gib den folgenden Befehl in der Eingabeaufforderung ein und drücke die Eingabetaste:

```bash
python get-pip.py
```

### macOS und Linux:

1. Öffne das Terminal.
2. Führe den folgenden Befehl aus, um das Pip-Installationsskript herunterzuladen:

```bash
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
```

3. Führe den folgenden Befehl aus, um Pip zu installieren:

```bash
python3 get-pip.py
```

## 3. Überprüfe die Installation

Nachdem die Installation abgeschlossen ist, kannst du überprüfen, ob Pip ordnungsgemäß installiert wurde, indem du den folgenden Befehl ausführst:

```bash
pip --version
```

Wenn du die Pip-Version angezeigt bekommst (z. B. "pip 21.0.1"), bedeutet dies, dass Pip erfolgreich installiert wurde.

Herzlichen Glückwunsch! Du hast Pip erfolgreich auf deinem System installiert. Du bist jetzt bereit, zusätzliche Python-Pakete zu installieren, um deine Python-Erfahrung zu erweitern.

Viel Spaß beim Entdecken und Verwenden der vielfältigen Python-Pakete, die über Pip verfügbar sind!

# Python dem PATH hinzufügen

Der PATH ist eine Umgebungsvariable, die eine Liste von Verzeichnissen auf deinem Computer enthält. Wenn du im Terminal oder der Eingabeaufforderung einen Befehl ausführst, sucht dein Betriebssystem nach diesem Befehl in den Verzeichnissen, die im PATH aufgeführt sind. Wenn der Befehl gefunden wird, kann er ausgeführt werden.

Warum muss Python dem PATH hinzugefügt werden?

Wenn Python nicht zum PATH hinzugefügt wird, bedeutet dies, dass der Befehl `python` oder `python3` nicht erkannt wird, wenn du ihn im Terminal oder der Eingabeaufforderung eingibst. In diesem Fall müsstest du den vollständigen Pfad zum Python-Interpreter angeben, um Python-Befehle oder -Skripte auszuführen.

Das Hinzufügen von Python zum PATH erleichtert dir das Arbeiten mit Python erheblich. Du kannst einfach `python` oder `python3` eingeben, egal in welchem Verzeichnis du dich befindest, und der Computer findet automatisch den richtigen Python-Interpreter und führt den Befehl aus.

Durch das Hinzufügen von Python zum PATH kannst du Python-Befehle und -Skripte bequem von überall ausführen, ohne den vollständigen Pfad zum Python-Interpreter angeben zu müssen.

Es ist wichtig zu beachten, dass das Hinzufügen von Python zum PATH optional ist. Du kannst auch Python ohne das Hinzufügen zum PATH verwenden, indem du den vollständigen Pfad zum Python-Interpreter verwendest. Das Hinzufügen von Python zum PATH ist jedoch eine gängige Praxis, um das Arbeiten mit Python einfacher zu machen.

1. Öffne den Datei-Explorer (Windows) oder den Finder (macOS).

2. Navigiere zu dem Ordner, in dem Python installiert ist. Standardmäßig wird Python in folgenden Ordnern installiert:

   - Windows: `C:\PythonXX` (wobei "XX" für die installierte Python-Version steht, z. B. "Python37" für Python 3.7)
   - macOS: `/Library/Frameworks/Python.framework/Versions/XX/bin` (wobei "XX" für die installierte Python-Version steht, z. B. "3.9" für Python 3.9)

3. Kopiere den vollständigen Pfad zum Python-Ordner.

4. Öffne den Systemdialog für die Umgebungsvariablen:

   - Windows: Klicke mit der rechten Maustaste auf "Computer" oder "Dieser PC" und wähle "Eigenschaften" aus dem Kontextmenü. Klicke dann auf "Erweiterte Systemeinstellungen" und wähle den Reiter "Erweitert" aus. Klicke auf "Umgebungsvariablen".
   - macOS: Öffne das Terminal und gib den Befehl `nano ~/.bash_profile` ein.

5. Füge den Python-Pfad zur Umgebungsvariable PATH hinzu:

   - Windows: Finde die Variable "Path" in der Tabelle "Systemvariablen" und klicke auf "Bearbeiten". Füge den kopierten Pfad am Ende der Variable hinzu, trenne ihn jedoch mit einem Semikolon (`;`) von den anderen Pfaden.
   - macOS: Füge den folgenden Code am Ende der `.bash_profile`-Datei hinzu:
     ```bash
     export PATH="/Library/Frameworks/Python.framework/Versions/XX/bin:$PATH"
     ```
     Ersetze dabei "XX" durch die installierte Python-Version.

6. Speichere die Änderungen.

7. Schließe das Terminal (macOS) und öffne es erneut, um die Änderungen zu übernehmen.

Jetzt solltest du Python zu deinem PATH hinzugefügt haben. Du kannst dies überprüfen, indem du im Terminal den Befehl `python --version` (Windows) oder `python3 --version` (macOS) ausführst. Wenn die installierte Python-Version angezeigt wird, wurde Python erfolgreich zum PATH hinzugefügt.

Jetzt kannst du Python-Befehle und -Skripte von überall auf deinem System ausführen, ohne den vollständigen Pfad zum Python-Interpreter angeben zu müssen. 