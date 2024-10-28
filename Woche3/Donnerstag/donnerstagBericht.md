# Wochenbericht Nr. 3
**Zeitraum:** vom [Datum Beginn] bis [Datum Ende]  
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
|             | **Verständnis der Unterschiede zwischen CNAME und ALIAS Records**  <br> Erarbeitung der Unterschiede: CNAMEs als Alias für Subdomains, ALIAS für Root-Domains verwendbar | 15:30 - 16:30 | 1 Stunde |

**Gesamtstunden:** 8 Stunden

---

**Stempel/Unterschrift:**  
