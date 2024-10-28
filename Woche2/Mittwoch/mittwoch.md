# Tagesbereicht 

Ich habe einen Resberry Pi 4 ausgeliehen bekommen und habe einige sachen ausprobiert.
Ich habe die Nextcloud installiert und somit meinen ersten eigenen mini Server ohne Backup erstellt.

Ich habe Roman bei einem Problem mit Prometheus und Grafana geholfen, da die Oberfläche von Grafana im localhost nicht angezeigt wurde. Wir konnten es beheben, weil der Port 3000 bereits von einer VM belegt war, die jedoch nicht aktiv war. Mit der Deaktivierung wurde das Problem behoben.
### Kenngelernter Befehlt
sudo arp-scan -N -I en9 10.255.100.0/24
### Erkärung
- Er scannt das Subnetz 10.255.100.0/24 über das Netzwerkinterface en9, um alle aktiven Hosts im Netzwerk zu finden.

- Die DNS-Namensauflösung wird dabei deaktiviert, sodass nur die IP- und MAC-Adressen zurückgegeben werden.

- Da der Befehl mit sudo ausgeführt wird, hat er die notwendigen Berechtigungen, um die ARP-Pakete zu senden und zu empfangen.

## Nextcloud install Befehle
1. sudo apt update
2. sudo apt upgrade

