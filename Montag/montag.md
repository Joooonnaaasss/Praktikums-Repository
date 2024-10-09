# Tag 1 des Praktikumsberichts

## Einrichtung der MacBooks
- Grundlegende Einstellungen vornehmen (Sprache, Benutzerkonto, Internetverbindung).
- Software-Updates installieren.
- Wichtige Anwendungen (z.B. Browser, Office) installieren.

## Einrichtung von Mattermost
- Registrierung und Login-Prozess.
- Einladung in Teams und Kanäle.
- Benutzerprofile anpassen.

## Fehlerbehebung in Mattermost
- Lizenz wechseln: Schritte zur Änderung der Lizenzdokumentation.
- Unterstützung bei häufigen Fehlern (z.B. Anmeldeprobleme).

## Grundbefehle des Mac Terminals
- `ls`: Auflisten von Dateien und Verzeichnissen.
- `cd`: Verzeichnis wechseln.
- `mkdir`: Neues Verzeichnis erstellen.
- `rm`: Dateien oder Verzeichnisse löschen.

## Docker kennenlernen
- Grundlagen von Containern und Images verstehen.
- Docker-Installation und grundlegende Befehle (z.B. `docker run`, `docker ps`).

## Webseite mit Docker-Container (Debian) erstellen
- Docker-Image für Debian erstellen.
- Webserver (z.B. Apache oder Nginx) einrichten.
- Testen der Webseite im Container.

## Live Meeting (Retrospektive)
- Reflexion über vergangene Projekte.
- Erfolge und Herausforderungen diskutieren.
- Verbesserungsvorschläge sammeln.

## Lernen des Ticketsystems
- Vorteile des Ticketsystems: 
  - Übersichtlichkeit
  - Arbeitsteilung
  - Nachverfolgbarkeit von Aufgaben
- Nutzung des Systems zur Priorisierung und Planung.


```Bash 
# Schritt 1: Finde mehr über den Container heraus
# Zeige die IP-Adresse des Containers an.
# Ersetze <container_name> durch den tatsächlichen Namen oder die ID deines Containers.
docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' <container_name>

# Schritt 2: Zeige die Logs des Containers an
# Um die Logs eines Containers anzuzeigen, benutze den folgenden Befehl:
docker logs <container_name>

# Schritt 3: Zeige die Portweiterleitungen des Containers an
# Um die Portweiterleitungen anzuzeigen, kannst du ebenfalls `docker inspect` verwenden:
docker inspect -f '{{.HostConfig.PortBindings}}' <container_name>

# Schritt 4: Starte den Nginx-Container detached mit einer Portweiterleitung
# Hier ist ein Beispiel, wie du den Nginx-Container auf Port 8080 (oder einem anderen freien Port) starten kannst:
docker run -d --name <container_name> -p 8080:80 nginx

# Schritt 5: Öffne die Nginx-Standard-Website im Browser
# Jetzt kannst du deinen Browser öffnen und zu folgendem Link navigieren:
# Ersetze <PORT> mit dem von dir gewählten Port (hier 8080):
# http://localhost:8080

# Schritt 6: Prüfe die Nginx-Standard-Website
# Du solltest die Standard-Nginx-Website sehen, die anzeigt, dass der Server erfolgreich läuft.
```