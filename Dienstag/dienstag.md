# kjsdfhasdfTag 2 des Praktikumsberichts

## Nginx und Image-Konfiguration
Heute haben wir mehr über Nginx gelernt, insbesondere darüber, wie man Images konfiguriert und richtig verwendet.

## Ports
Außerdem haben wir uns mit dem Thema Ports beschäftigt und gelernt, wie diese zugeordnet sind.

## Proxmox und Container
Wir haben Proxmox kennengelernt und mit Hilfe eines Containers eine HTML-Datei auf dem Localserver hochgeladen.

## Arbeiten mit apt
Wir haben gelernt, mit `apt` zu arbeiten (Updates). Die HTML-Datei haben wir dann mit Vim bearbeitet und dabei einige Befehle für Vim kennengelernt.

## Docker Volumes vs. Bind-Mounts
Ein weiterer wichtiger Punkt war der Unterschied zwischen Docker Volumes und Bind-Mounts.

## Ausfallsicherheit von Containern
Wir haben auch gelernt, wie man einen Container ausfallsicher macht und wie man ein separates Volume für bestimmte Speicherorte erstellt.

## Datenverlust vermeiden
Wenn ein Container heruntergefahren wird mit dem Befehl `kill` und ohne Backup auf Volume, gehen alle Dateien und Einstellungen verloren. Hat man einen zweiten Zugriffsort, kann dies verhindert werden, auch bei einer neuen ID.

# Docker-Befehle

Hier sind einige grundlegende Docker-Befehle, die du für das Management von Containern und Images verwenden kannst:

## Container Management

```bash
# Docker-Container starten
docker run [OPTIONS] IMAGE [COMMAND] [ARG...]

# Container stoppen
docker stop CONTAINER_ID

# Container killen (sofortiges Stoppen)
docker kill CONTAINER_ID

# Container entfernen
docker rm CONTAINER_ID

# Aktuelle Container auflisten
docker ps

# Alle Container auflisten (auch gestoppte)
docker ps -a

# Docker-Image auflisten
docker images

# Docker-Image entfernen
docker rmi IMAGE_ID

# Docker-Container klonen (starten)
docker run -d --name NEW_CONTAINER_NAME IMAGE

# Logs eines Containers anzeigen
docker logs CONTAINER_ID

# Mit einem laufenden Container interagieren (Shell)
docker exec -it CONTAINER_ID /bin/bash

# Docker-Volume erstellen
docker volume create VOLUME_NAME

# Ein Volume in einen Container mounten
docker run -v VOLUME_NAME:/path/in/container IMAGE
```

# Weitere Befehle
```bash
# Tasks anzeigen lassen und aktuelle Prozesse verfolgen
Top

# Schritt 1: Verbinde dich mit dem Nginx-Container
# Ersetze <container_name> durch den tatsächlichen Namen oder die ID deines Containers.
docker exec -it <container_name> /bin/bash

# Schritt 2: Finde das Verzeichnis, in dem die Nginx-Standard-HTML-Website-Datei liegt
# Standardmäßig befindet sich die index.html unter:
cd /usr/share/nginx/html

# Schritt 3: Bearbeite die Datei
# Du kannst nano oder vi verwenden. Hier verwenden wir nano:
nano index.html

# (Nimm deine gewünschten Änderungen vor und speichere die Datei)

# Schritt 4: Refresh deinen Browser
# Öffne deinen Browser und lade die Seite neu, um zu prüfen, ob die Änderung sichtbar ist.

# Schritt 5: Verlasse den Container
# Drücke Ctrl + D oder tippe `exit`, um die Bash-Sitzung zu beenden.

# Schritt 6: Beende den Container
# Benutze den kill-Befehl, um den Nginx-Container zu stoppen:
docker kill <container_name>

# Schritt 7: Starte den Container erneut
# Starte den Container wieder mit:
docker start <container_name>

# Schritt 8: Prüfe die Änderungen
# Lade die Seite im Browser erneut. Du wirst feststellen, dass die Änderungen weg sind.

# Schritt 9: Finde heraus, warum das passiert ist
# Die Änderungen sind verloren gegangen, weil der Nginx-Container ein flüchtiges (ephemeral) Dateisystem hat.
# Änderungen im Container werden gelöscht, wenn der Container gestoppt oder gelöscht wird.

# Schritt 10: Wie kannst du das verhindern?
# Um Daten dauerhaft zu speichern, solltest du ein Volume verwenden.
# Erstelle den Nginx-Container mit einem Volume, das das HTML-Verzeichnis speichert:
docker run -d --name <container_name> -v /path/to/your/html:/usr/share/nginx/html nginx

# Ersetze /path/to/your/html mit dem tatsächlichen Pfad auf deinem Host, wo die HTML-Dateien gespeichert werden.
# Änderungen in diesem Verzeichnis bleiben auch nach dem Neustart des Containers erhalten.
```
