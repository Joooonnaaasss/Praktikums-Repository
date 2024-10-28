# Wochenbericht Nr. 3
**Zeitraum:** vom [Datum Beginn] bis [Datum Ende]  
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

**Stempel/Unterschrift:**  
