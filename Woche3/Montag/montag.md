# Montag

## Daily

* Täglich um 11 Uhr
* Zoom-Meeting

## Aufgabe: DNS Setup mit Monitoring

### Teil 1 - Bind9 Basis Config

* VM Setup (bestehende verwenden)
* BIND9 Installieren (z.B. [Anleitung auf ubuntuusers.de](https://wiki.ubuntuusers.de/DNS-Server_Bind/))
* BIND9 konfigurieren, dass auf TCP und UDP gelauscht wird
    * Überprüfen: `ss -tulpn` oder `netstat -tulpn`
    * Du hast zwar `bind9` installiert, der Prozess heißt aber `named`!
    * Für was stehen die einzelnen Buchstaben in `tulpn`? (`man netstat`, `man ss`)

    ### Erklärung
    Die Buchstaben in der Ausgabe von `netstat` und `ss` beziehen sich auf verschiedene Arten von Verbindungen und deren Status. Hier ist eine Übersicht, was jeder Buchstabe in `tulpn` bedeutet:
    
    - **t**: TCP – Zeigt TCP-Verbindungen an.
    - **u**: UDP – Zeigt UDP-Verbindungen an.
    - **l**: Listening – Zeigt nur die Ports an, die im "Listening"-Zustand sind (d.h. Ports, auf denen Anwendungen auf Verbindungen warten).
    - **n**: Numerisch – Zeigt IP-Adressen und Portnummern in numerischer Form an, anstatt sie in Namen (z. B. Hostnamen) aufzulösen.

    Zusammengefasst zeigt der Befehl `netstat -tuln` oder `ss -tuln` alle aktiven TCP- und UDP-Verbindungen an, die auf eingehende Verbindungen warten, und listet die IP-Adressen und Ports numerisch auf.

    * **Wo finden sich die Logs von BIND? Wie kannst du dir diese ansehen?**
      - Die Logs von BIND befinden sich in der Regel in `/var/log/syslog` oder `/var/log/named/`. Du kannst die Logs mit einem Befehl wie `tail -f /var/log/syslog` einsehen, um die neuesten Einträge live zu beobachten.

    * **Wie kannst du den Service neu starten?**
      - Du kannst den BIND-Dienst mit dem Befehl `sudo systemctl restart bind9` neu starten.

* Zone "mann.de." konfigurieren
    * A-Record: `jonas.mann.de` auf `127.123.123.1` anlegen
    * AAAA-Record: `jonas.mann.de` auf `::1` anlegen
* Einträge verifizieren
    * Vom Server: `host jonas.mann.de 127.0.0.1` sollte folgendes zurückgeben:
      ```
      jonas.mann.de has address 127.123.123.1
      jonas.mann.de has IPv6 address ::1
      ```
    * **Warum steht an dem `host`-Befehl als zweites Argument `127.0.0.1`?**
      - Das zweite Argument `127.0.0.1` gibt an, dass die DNS-Anfrage an den lokal laufenden DNS-Server gesendet wird, sodass du die Konfiguration des eigenen Servers testen kannst.

    * **Wie kannst du mit `host` explizit eine Anfrage über TCP oder UDP absetzen?**
      - Um eine DNS-Anfrage über TCP abzusenden, kannst du den `-t` Parameter verwenden, z.B. `host -t A jonas.mann.de 127.0.0.1`. Um UDP zu verwenden, kannst du einfach den Befehl ohne den `-t` Parameter verwenden, da die Standard-DNS-Anfrage über UDP erfolgt.