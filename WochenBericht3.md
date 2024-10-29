# Wochenbericht Nr. 3
**Zeitraum:** 21.10.2024
**Firma:** DGI, Köln  
**Abteilung:** Netzwerk und Serveradministration

| Tag      | Ausgeführte Arbeiten | Einzelstunden     | Gesamtstunden |
|----------|-----------------------|-------------------|---------------|
| Montag   | **Daily Meeting**  <br> Teilnahme am täglichen Zoom-Meeting um 11 Uhr zur Besprechung der aktuellen Aufgaben und Herausforderungen | 11:00 - 11:30 | 0,5 Stunden |
|          | **DNS Setup mit Monitoring – Teil 1: BIND9 Basis-Konfiguration**  <br> Vorbereitung einer VM für das DNS-Setup, Installation und Konfiguration von BIND9 zur Annahme von TCP- und UDP-Verbindungen; Überprüfung der Netzwerkschnittstellen mit `ss -tulpn` und `netstat -tulpn` sowie Erarbeitung der Bedeutung der Parameter | 09:00 - 11:00 | 2 Stunden |
|          | **Erklärung der Parameter in `netstat` und `ss`**  <br> Erlernen der Bedeutung der `t`, `u`, `l`, `p`, `n` Parameter und ihrer Anwendung bei der Netzwerkkonfiguration | 11:30 - 12:00 | 0,5 Stunden |
|          | **Log-Verwaltung und Service Neustart**  <br> Lokalisieren der BIND-Logs in `/var/log/syslog`, Beobachtung der Logs mit `tail -f` und Neustart des BIND-Dienstes mit `sudo systemctl restart bind9` | 12:00 - 12:30 | 0,5 Stunden |
|          | **Mittagspause** | 12:30 - 13:00 | 0,5 Stunden |
|          | **Zone "mann.de" konfigurieren**  <br> Anlegen eines A-Records und AAAA-Records für `jonas.mann.de` auf `127.123.123.1` und `::1`; Verifizierung der DNS-Einträge mithilfe des `host`-Befehls | 13:00 - 15:00 | 2 Stunden |
|          | **DNS-Anfragen testen und Analyse**  <br> Durchführung von DNS-Anfragen über TCP und UDP zum Testen der Konfiguration; Untersuchung des Zwecks der Angabe `127.0.0.1` im `host`-Befehl | 15:00 - 16:00 | 1 Stunde |
|          | **Zusammenfassung und Dokumentation**  <br> Dokumentation der DNS-Konfiguration und der verwendeten Befehle für den internen Wissensaustausch | 16:00 - 17:00 | 1 Stunde |

**Gesamtstunden:** 8 Stunden

---

**Zeitraum:** vom 22.10.2024
**Firma:** DGI, Köln  
**Abteilung:** Netzwerk und Serveradministration

| Tag      | Ausgeführte Arbeiten | Einzelstunden     | Gesamtstunden |
|----------|-----------------------|-------------------|---------------|
| Dienstag | **Daily Meeting**  <br> Teilnahme am Daily-Meeting um 11 Uhr zur Besprechung der aktuellen Aufgaben und Rückblick auf die Arbeit vom Montag | 11:00 - 11:30 | 0,5 Stunden |
|          | **Recherche zu DNS und Servertechniken**  <br> Vertiefung des Verständnisses von DNS und Serverarchitekturen durch YouTube-Tutorials zur Vorbereitung auf spätere Aufgaben | 09:00 - 11:00 | 2 Stunden |
|          | **Recherche zu Grafana und Dashboard-Erstellung**  <br> Lernen, wie Oberflächen und Dashboards in Grafana erstellt werden, speziell für die Verwendung mit Prometheus | 11:30 - 12:30 | 1 Stunde |
|          | **Mittagspause** | 12:30 - 13:00 | 0,5 Stunden |
|          | **Teil 2 - Monitoring Setup**  <br> Installation und Konfiguration von Prometheus und Grafana, Einrichtung von `node_exporter` und `bind_exporter` auf beiden Servern zur Datensammlung für das Monitoring | 13:00 - 15:00 | 2 Stunden |
|          | **Integration der Exporter in Prometheus**  <br> Einbindung der `node_exporter` und `bind_exporter` in Prometheus zur Überwachung der Server | 15:00 - 16:00 | 1 Stunde |
|          | **Erstellung von Dashboards in Grafana**  <br> Aufbau von Dashboards in Grafana zur Visualisierung der Daten aus Prometheus für die Serverüberwachung | 16:00 - 17:00 | 1 Stunde |

**Gesamtstunden:** 8 Stunden

---

**Zeitraum:** vom 23.10.2024 
**Firma:** DGI, Köln  
**Abteilung:** Netzwerk und Serveradministration

| Tag      | Ausgeführte Arbeiten | Einzelstunden     | Gesamtstunden |
|----------|-----------------------|-------------------|---------------|
| Mittwoch | **Daily Meeting**  <br> Teilnahme am Daily-Meeting um 11 Uhr zur Besprechung der anstehenden Aufgaben und Rückblick auf die Arbeit vom Montag | 09:00 - 09:30 | 0,5 Stunden |
|          | **Team-Call um 11 Uhr**  <br> Austausch im Team über Fortschritte und Fragen zu aktuellen Projekten, insbesondere zum Monitoring | 09:30 - 10:00 | 0,5 Stunden |
|          | **Teil 2 - Monitoring Setup**  <br> Installation und Konfiguration von Prometheus und Grafana, sowie Einrichtung von `node_exporter` und `bind_exporter` auf beiden Servern zur Datensammlung | 10:00 - 12:00 | 2 Stunden |
|          | **Mittagspause** | 12:00 - 12:30 | 0,5 Stunden |
|          | **Integration der Exporter in Prometheus**  <br> Einbindung der `node_exporter` und `bind_exporter` in Prometheus zur Serverüberwachung | 12:30 - 13:30 | 1 Stunde |
|          | **Erstellung von Dashboards in Grafana**  <br> Aufbau von Grafana-Dashboards zur Visualisierung der gesammelten Monitoring-Daten | 13:30 - 14:30 | 1 Stunde |
|          | **Weiterbildung Raspberry Pi und Nextcloud**  <br> Vertiefung in die Themen Raspberry Pi und Nextcloud, speziell zur Domain-Verwaltung | 14:30 - 15:30 | 1 Stunde |
|          | **Thema CPU-Bau und Binärcodes**  <br> Grundlagen zur CPU-Architektur, Hexadezimal- und Binärcode-Addition, als Vorbereitung für die Arbeit mit Taschenrechnern und Rechenoperationen auf niedrigem Level | 15:30 - 17:00 | 1,5 Stunden |

**Gesamtstunden:** 8 Stunden

---

**Zeitraum:** vom 24.10.2024 
**Firma:** DGI, Köln  
**Abteilung:** Netzwerk und Serveradministration

| Tag         | Ausgeführte Arbeiten | Einzelstunden     | Gesamtstunden |
|-------------|-----------------------|-------------------|---------------|
| Donnerstag  | **Daily Meeting**  <br> Teilnahme am täglichen Zoom-Meeting um 11 Uhr zur Besprechung der Aufgaben und des Fortschritts seit Montag | 11:00 - 11:30 | 0,5 Stunden |
|             | **Teil 3 - Bind9 Secondary Setup**  <br> Konfiguration von Forwarding auf die Google DNS-Server `8.8.8.8` und `8.8.4.4` zur Weiterleitung von Anfragen nicht lokaler Einträge | 09:00 - 11:00 | 2 Stunden |
|             | **Test der DNS-Auflösung**  <br> Überprüfung der lokalen Auflösung externer Einträge, z.B. `host heise.de 127.0.0.1`, und Konfiguration des Netzwerkinterfaces in VirtualBox für Zugriff vom MacBook | 11:30 - 12:30 | 1 Stunde |
|             | **Mittagspause** | 12:30 - 13:00 | 0,5 Stunden |
|             | **Setup eines DNS Secondary Servers**  <br> Einrichtung von Zone-Replication mit AXFR sowie automatisches Update der Secondary Zone bei Änderungen im Primary | 13:00 - 14:30 | 1,5 Stunden |
|             | **Erstellung eines DNS CNAME Records**  <br> Anlegen eines CNAME Records `dgi.mann.de`, der auf `jonas.mann.de` verweist; Test der DNS-Auflösung über den Secondary DNS-Server | 14:30 - 15:30 | 1 Stunde |
|             | **Verständnis der Unterschiede zwischen CNAME und ALIAS Records**  <br> Erarbeitung der Unterschiede: CNAMEs als Alias
