## Daly Scrum
- Besprechung für Probleme bei Tickts
- Herrangehnsweisen 
- Was jeder Heute vor hat zu Arbeiten
- Was jeder gestern gemacht hat

## Arbeit im Team-I Büro
- Verstehen der Serverkabel
- Wozu unterschiedliche Längen?
- Wozu unterschiedliche Anschlüsse?
- Switches im Aufbau (Modularität)

### Unterschiedliche Kabel
- SCSI-Kabel: Diese Kabel verbinden Server mit Festplatten oder anderen SCSI-Geräten. Sie sind oft in verschiedenen Varianten wie Parallel SCSI oder Serial Attached SCSI (SAS) erhältlich.

- Fibre Channel-Kabel: Diese Kabel werden für die Verbindung von Servern mit Speichersystemen über Fibre Channel verwendet, ideal für Hochgeschwindigkeits-Datenübertragungen.

- Power-Kabel: Server benötigen spezielle Netzkabel, die je nach Typ des Servers und der Stromversorgung variieren können.

- KVM-Kabel: Diese Kabel werden für KVM-Switches verwendet, um mehrere Server über eine einzige Tastatur, Maus und Monitor zu steuern.
- Multicast/Singlee

### Kabelinfrasturktur
- Türkise Kabel: Diese werden häufig als Cat6a oder Cat7 Kabel verwendet, die für hohe Geschwindigkeiten  (bis zu 10 Gbit/s) und längere Reichweiten (bis zu 100 Meter) ausgelegt sind. Sie sind oft geschirmt, um elektromagnetische Störungen zu minimieren.

- Gelbe Kabel: Diese sind meist Cat5e Kabel, die Geschwindigkeiten von bis zu 1 Gbit/s unterstützen und ebenfalls eine Reichweite von bis zu 100 Metern haben. Sie sind weniger abgeschirmt als Cat6a oder Cat7, was sie anfälliger für Störungen macht.

## Roman bei einer VM Aufgabe unterstützen (DHCP)
Drei Teammitglieder und ich haben Roman bei einer Aufgabe geholfen, die einige Probleme verursacht hat. Wir mussten in VirtualBox zwei Server miteinander verknüpfen und dazu die Netzwerkkonfiguration ändern. Diese musste ein spezielles Format haben und stellte einige Herausforderungen dar.

Die IP-Adressen mussten auf beiden Servern statisch sein, um die Kommunikation zu ermöglichen. Später bemerkten wir, dass Romans Laptop über WLAN verbunden war, während die Server im LAN waren, was zu Problemen führte, da beide im gleichen Netzwerk sein mussten.

Da Linux Ubuntu spezielle Formate und Anordnungen der Dateien verlangt, war es nicht einfach. Zudem standen wir im Kontakt mit einem Mitarbeiter, da wir zu viert teilweise nicht weiterkamen.

Am Ende gelang es uns, die Server mit statischen IPs miteinander kommunizieren zu lassen. Insgesamt bestand die Aufgabe darin, DHCP zu verstehen. Da Roman noch wenig Erfahrung mit DHCP hatte, sollte ich ihm beim Verständnis helfen.