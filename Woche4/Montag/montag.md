### Tagesbericht

**Projekt:** Einrichtung und Konfiguration von Traefik und Redlib im Docker-Umfeld

---

#### Aufgaben und Tätigkeiten

**1. Analyse und Implementierung von Traefik:**

Zu Beginn des Tages habe ich mich intensiv mit Traefik als Reverse-Proxy beschäftigt und dafür das bereitgestellte Beispiel aus der offiziellen Traefik-Dokumentation als Grundlage genutzt ([Link zur Dokumentation](https://doc.traefik.io/traefik/user-guides/docker-compose/basic-example/)). Ziel war es, eine Lösung zu erarbeiten, die es ermöglicht, mehrere Services hinter der gleichen IP-Adresse über die Ports 80 und 443 anzusprechen.

- **Aufsetzen der Traefik-Konfiguration:**  
  Hierbei habe ich eine `docker-compose.yml`-Datei erstellt, die Traefik als zentralen Reverse-Proxy im Netzwerk verwendet. Die Konfiguration enthält spezifische Einträge, um das Dashboard und den HTTP-Zugriff bereitzustellen:
  - Aktivierung des `insecure API` Modus für das Dashboard zur Überwachung.
  - Einbindung des Docker-Sockets, um Container automatisch erkennen zu lassen.
  - Bereitstellung eines HTTP-Einstiegspunkts auf Port 80 für Traefik.

- **Testen des Setups:**  
  Nach dem Starten der Docker-Container wurde das Traefik-Dashboard unter `localhost:8081` erfolgreich aufgerufen, um die aktive Verbindung und Konfiguration zu prüfen.

**2. Einrichtung und Integration von Redlib:**

Parallel zur Traefik-Konfiguration wurde Redlib als zusätzlicher Service im Docker-Umfeld integriert. Dazu erstellte ich ein Docker-Image für Redlib basierend auf einer `Dockerfile`, die ich wie folgt konfiguriert habe:

- **Dockerfile für Redlib:**  
  ```dockerfile
  FROM alpine:latest
  COPY redlib /Users/jmann/Desktop/redlib-docker/redlib
  RUN chmod +x /Users/jmann/Desktop/redlib-docker/redlib
  ENTRYPOINT ["/Users/jmann/Desktop/redlib-docker/redlib"]
