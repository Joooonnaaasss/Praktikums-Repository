# Wochenbericht Nr. 3
**Zeitraum:** vom [Datum Beginn] bis [Datum Ende]  
**Firma:** DGI, Köln  
**Abteilung:** Netzwerk und Serveradministration

| Tag         | Ausgeführte Arbeiten | Einzelstunden     | Gesamtstunden |
|-------------|-----------------------|-------------------|---------------|
| Freitag     | **Arbeit vom Vortag abschließen und Wochenbericht weiterführen**  <br> Fortführung und Abschluss der Dokumentation der bisherigen Arbeiten und des wöchentlichen Fortschritts | 09:00 - 10:00 | 1 Stunde |
|             | **Daily Meeting**  <br> Teilnahme am Daily-Meeting um 11 Uhr zur Besprechung der laufenden Woche und Rückblick auf die Arbeiten seit Montag | 10:00 - 10:30 | 0,5 Stunden |
|             | **Teil 3 - Bind9 Secondary Setup**  <br> Konfiguration des Forwarding auf `8.8.8.8` und `8.8.4.4` für Anfragen, die lokal nicht aufgelöst werden können, sowie Test des Zugriffs von MacBook zur VirtualBox-VM | 10:30 - 12:00 | 1,5 Stunden |
|             | **Test der lokalen Auflösung externer Einträge**  <br> Testen der DNS-Anfrage für externe Domains (`host heise.de 127.0.0.1`) und Anpassung der Netzwerkkonfiguration in VirtualBox für MacBook-Zugriff | 12:00 - 12:30 | 0,5 Stunden |
|             | **Mittagspause** | 12:30 - 13:00 | 0,5 Stunden |
|             | **Einrichten eines Secondary DNS Servers**  <br> Zone Replication über AXFR eingerichtet und automatisches Update der Secondary Zone bei Änderungen im Primary Server konfiguriert | 13:00 - 14:30 | 1,5 Stunden |
|             | **Erstellen eines CNAME Records für dgi.mann.de**  <br> Anlegen eines CNAME Records, der `dgi.mann.de` auf `jonas.mann.de` zeigt, sowie Test der Auflösung über den Secondary DNS Server | 14:30 - 15:30 | 1 Stunde |
|             | **Vergleich von CNAME und ALIAS Records**  <br> Verständnis der Unterschiede zwischen CNAME und ALIAS Records; CNAMEs als Aliase für Subdomains und ALIAS für Root-Domains | 15:30 - 16:30 | 1 Stunde |

**Gesamtstunden:** 8 Stunden

---

**Stempel/Unterschrift:** 