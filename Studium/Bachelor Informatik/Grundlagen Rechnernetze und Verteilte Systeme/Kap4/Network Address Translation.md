---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs #Atomic 
# Definition
Als Network Address Translation (NAT) bezeichnet man allgemein Techniken zur Übersetzung von N ≥ 1 auf M ≥ 1 andere [[IP-Adresse|IP-Adressen]]. Bei [[Internet Protocol Version 4|IPv4]] ist der weitaus häufigste Anwendungsfall die Abbildung von N privaten (nicht öffentlichen) auf M öffentliche (global eindeutige) [[IP-Adresse|IP-Adressen]]:
- N ≤ M: Die Übersetzung geschieht statisch oder dynamisch indem jeder privaten [[IP-Adresse]] mind. eine öffentliche [[IP-Adresse]] zugeordnet wird.
- N > M: In diesem Fall wird eine öffentliche [[IP-Adresse]] von mehreren Computer gleichzeitig genutzt. Eine eindeutige Unterscheidung kann mittels Port-[[Multiplexing]] erreicht werden. Der häufigste Fall ist M = 1, z. B. bei einem privaten DSL-Anschluss

# Private [[IP-Adresse|IP-Adressen]] 
Private IP-Adressen sind spezielle Adressbereiche, welche
- zur privaten Nutzung ohne vorherige Registrierung freigegeben sind,
- deswegen in unterschiedlichen Netzen vorkommen können,
- aus diesem Grund weder eindeutig noch zur Ende-zu-Ende-Adressierung zwischen öffentlich erreichbaren Netzen geeignet sind und
- daher IP-Pakete mit privaten Empfänger-Adressen von Routern im Internet nicht weitergeleitet werden (oder werden sollten)

Die privaten Adressbereiche bei [[Internet Protocol Version 4|IPv4]] sind: 10.0.0.0 / 8, 172.16.0.0 / 12, 169.254.0.0 / 16 und 192.168.0.0 / 16

Der Bereich 169.254.0.0 / 16 wird zur automatischen Adressvergabe (Automatic Private IP Adressing) genutzt:
- Startet ein Computer ohne statisch vergebene Adresse, versucht dieser, einen DHCP-Server zu erreichen
- Kann kein DHCP-Server gefunden werden, vergibt das [[Betriebssystem]] eine zufällig gewählte Adresse aus diesem Adressblock
- Schlägt anschließend die [[Address Resolution Protocol|ARP]]-Auflösung zu dieser Adresse fehl, wird angenommen, dass diese Adresse im lokalen Subnetz noch nicht verwendet wird. Andernfalls wird eine andere Adresse gewählt und der Vorgang wiederholt

# Funktionsweise
- Üblicherweise übernehmen [[Router]] die Netzwerkadressübersetzung
- Dieser ordnet in NAT-Tabelle Privaten [[IP-Adresse|IP-Adressen]] jeweils einen privaten und einen öffentlichen Port zu
- Die Kommunikation zwischen privatem und öffentlichem [[Netzwerk]] läuft dann über diese Ports des [[Router|Routers]] 
- Da z.B. [[Internet Control Message Protocol v4|ICMP]] keine Portnummern hat, können auch andere Kennzeichen wie die ICMP-ID verwendet werden.