---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs #Atomic 
# Definition
Nachfolger von [[Internet Protocol Version 4]]. Die wesentlichen Änderungen gegenüber [[Internet Protocol Version 4]] umfassen:
- Vergrößerung des Adressraums von $2^32$ auf $2^{128}$
- Vereinfachung des Headerformats (effizientere Verarbeitung auf Routern).
- Änderungen bei der IP-Fragmentierung.
- Flexibilität durch sog. Extension Header bei gleichzeitiger Vereinfachung des Headerformats.
- [[Stateless Address Autoconfiguration]] ([[Stateless Address Autoconfiguration]]) mittels ICMPv6.
- Möglichkeit für Stateful Autoconfiguration durch DHCPv6.
- Nativer Einsatz von [[Multicast]], beispielsweise um alle [[Router]] in einem Segment zu adressieren

# Header

![[IPv6-Header.png]]

Version
- Gibt die verwendete IP-Version an
- Gültige Werte sind 4 (IPv4) und 6 (IPv6)

Traffic Class
- Äquivalent zum TOS-Feld des [[Internet Protocol Version 4|IPv4]]-Headers
- Wird zur Verkehrspriorisierung / Quality of Service (QoS) verwendet

Flow Label
- Ursprünglich vorgesehen für Echtzeitanwendungen
- Wird heute in erster Linie von [[Router|Routern]] verwendet, um zusammengehörende Pakete (Flows) auf der [[Vermittlungsschicht]] zu erkennen
- Pakete, die zum selben Flow gehören sollen ggf. gleich behandelt werden, z. B. im Fall mehrerer möglicher Pfade zum Ziel alle über denselben Pfad geroutet werden

Payload Length
- Gibt die Länge der auf den IPv6-Header folgenden Daten an
- Angabe in Vielfachen von 1 B
- Der IPv6-Header inkl. seiner Extension Header muss immer ein Vielfaches von 8 B sein

Next Header
- Gibt den Typ des nächsten Headers an, der am Ende des IPv6-Headers folgt
- Dies kann entweder ein L4-Header (z. B. [[Transmission Control Protokoll]] oder [[User Datagram Protokoll]]), ein [[Internet Control Message Protocol v4|ICMP]]v6-Header oder ein sog. IPv6 Extension Header sein

Hop Limit
- Entspricht dem TTL-Feld des IPv4-Headers
- Wird beim Weiterleiten eines Pakets durch einen [[Router]] um jeweils 1 dekrementiert
- Erreicht der Wert 0, wird das Paket verworfen und ein ICMPv6 Time Exceeded an den ursprünglichen Sender des Pakets zurückgeschickt

Source Address: 128 bit lange IPv6-Quelladresse

Destination Address: 128 bit lange IPv6-Zieladresse

# Extension Header
- Extension Header erlauben es zusätzliche Layer 3 Informationen in einem IPv6 Paket anzufügen
- Das jeweilige Next Header Feld gibt den jeweils nächsten Extension Header oder das L4 Protokoll an
- Die Next Header Felder des IPv6 Pakets bzw. der Extension Header bilden hierbei eine Kette, z. B.
	- IPv6 Header, Next Header: Routing
	- [[Routing Header]], Next Header: Fragment
	- [[Fragment Header]], Next Header: [[Transmission Control Protokoll]]
	- [[Transmission Control Protokoll]] Payload
- Das Format hängt vom jeweiligen Header ab
- Mit Ausnahme des [[Hop-by-Hop Options Header]] und des [[Routing Header]] werden Extension Header nur vom Empfänger ausgewertet

# Besondere Adressbereiche
1. ::1 / 128 – Loopback-Adresse
	- Adressiert den Localhost, d.h. Pakete mit dieser Zieladresse verlassen den lokalen Rechner gar nicht erst, sondern werden über das sog. Loopback-Interface sofort wieder zugestellt (vgl. 127.0.0.1 bei [[Internet Protocol Version 4]])
	- Werden nicht geroutet
2. :: / 128 – nicht-spezifizierte Adresse
	- Analogon zu 0.0.0.0 bei [[Internet Protocol Version 4]]
	- Wird nicht geroutet
3. fe80:: / 10 – Link-Local Adressen
	- Jedes IPv6 Interface benötigt eine Link-Local-Adresse
	- Die Link-Local-Adresse wird aus dem Interface-Identifier generiert
	- Hat nur innerhalb des lokalen Links Gültigkeit und wird daher nicht geroutet
4. fc00:: / 7 – Unique-Local [[Unicast]]-Adressen
	- Adressen, die nur für lokale Kommunikation (z. B. innerhalb eines Firmennetzes) vorgesehen sind
	- Dürfen wie private [[Internet Protocol Version 4|IPv4]]-Adressen lokal aber nicht im Internet geroutet werden
5. ff00:: / 8 – [[Multicast]]-Adressen
	- Adressen, die eine bestimmte Gruppe von Hosts adressieren
	- Werden geroutet
6. (fast) der ganze Rest – Globale Adressen
	- Global eindeutige Adressen, die für den Einsatz in öffentlichen Netzen vorgesehen sind
	- Werden geroutet

# Multicast Adressen
1. ff02::1 – All Nodes: Adressiert alle Knoten auf dem lokalen Link
2. ff02::2 – All Routers: Adressiert alle [[Router]] auf dem lokalen Link
3. ff02::1:2 – All DHCP-Agents: Adressiert alle DHCP-Server auf dem lokalen Link
4. ff02::1:ff00:0/104 – Solicited-Node Address
	- Die Solicited-Node Adresse wird im [[Neighbor Discovery Protocol]] verwendet, welches u. a. zur Adressauflösung dient
	- Die Solicited-Node Adresse zu einer IPv6 Adresse wird aus dem ff02::1:ff00:0/104 und den letzten 24 bit der ursprünglichen IPv6 Adresse generiert
	- Die Solicited-Node Adresse für 2001:0db8:1ee7:2ea2:0921:2e11:d2c6:938b ist somit ff02::1:ffc6:938b
	- IPv6-Multicasts werden auch auf Schicht 2 mittels [[Multicast]]-Adressen versendet
		- [[Switch|Switches]] müssen [[Multicast]]-[[Rahmen]] nur an die Ports weiterleiten, an denen ein Mitglied der entsprechenden [[Multicast]]-Gruppe angeschlossen ist
		- In großen L2-Netzen können so unnötige Broadcasts vermieden werden
		- Knoten, für die eine Nachricht nicht von Interesse ist, bekommen diese somit erst gar nicht

# Mapping zu [[MAC-Adresse|MAC-Adressen]] 
- IPv6-Pakete mit einer Zieladresse aus dem Präfix ff00::/8 werden mit der zugehörigen [[Multicast]]-Adresse auf Schicht 2 ([[Ethernet]]) versendet.
- Um Multicasts auf Schicht 3 auch auf Schicht 2 abbilden zu können, muss es einen Zusammenhang zwischen den verwendeten Adressen beider Schichten geben.
- Die ersten 2 Oktette der [[MAC-Adresse]] werden auf 33:33 gesetzt.
- letztes Bit des ersten Oktetts ist gesetzt → [[Multicast]]
- vorletztes Bit des ersten Oktetts ist gesetzt → locally administered
- siehe [[Sicherungsschicht]]
- Die letzten 4 Oktette der Ethernetadresse werden die letzten 4 Oktette der IPv6 Multicastadresse