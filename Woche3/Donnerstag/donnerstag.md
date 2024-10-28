# Home Office

### Meeting
- 11Uhr Dalay Meeting (was steht an? Was wurde am Montag gemacht?)

### Teil 3 - Bind9 Secondary Setup

* Forwarding auf `8.8.8.8` & `8.8.4.4` konfigurieren
    * **Was bewirkt das?**
      - Das Forwarding auf die Google DNS-Server (`8.8.8.8` und `8.8.4.4`) ermöglicht es deinem DNS-Server, Anfragen für nicht lokal vorhandene Einträge an diese externen DNS-Server weiterzuleiten.

    * Lokales Auflösen von externen Einträgen `host heise.de 127.0.0.1`
    * Von deinem MacBook: wie kannst du den DNS-Server erreichen? 
        * **Stichwort: Netzwerkinterface-Konfiguration in VirtualBox**
          - Du musst sicherstellen, dass die Netzwerkkonfiguration deiner VM in VirtualBox so eingestellt ist, dass sie im gleichen Netzwerk wie dein MacBook ist (z.B. NAT oder Bridged Adapter).

* Setup eines DNS Secondarys
    * Zone Replication mit AXFR einrichten
    * Automatisches Update der Secondary Zone bei Update auf Primary
* Neuen DNS CNAME Record erstellen: `dgi.mann.de` soll auf `jonas.mann.de` zeigen
    * Von deinem MacBook sollte damit `host dgi.mann.de [secondary DNS-Server]` das Richtige zurückgeben
        * **Was ist ein CNAME Record?**
          - Ein CNAME (Canonical Name) Record ist ein DNS-Eintrag, der einen Alias für einen anderen Domainnamen erstellt. Er verweist auf den kanonischen Namen, wodurch die Verwaltung von Domainnamen vereinfacht wird.

        * **Wie unterscheidet dieser sich von einem ALIAS Record?**
          - Ein ALIAS Record ist ähnlich wie ein CNAME Record, hat jedoch den Vorteil, dass er auf die Root-Domain angewendet werden kann. CNAME-Records dürfen nicht auf der Root-Domain verwendet werden, während ALIAS-Records dies ermöglichen.
          
