---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs 
# Header

![[Augbau IPv4-Header.png]]

Version
- Gibt die verwendete IP-Version an
- Gültige Werte sind 4 ([[Internet Protocol Version 4|IPv4]]) und 6 ([[Internet Protocol Version 6|IPv6]])

IHL (Internet Header Length)
- Gibt die Länge des IP Headers inkl. Optionen in Vielfachen von 32 bit an
- Wichtig, da der IPv4-Header durch Optionsfelder variable Länge hat

TOS (Type of Service)
- Dient der Klassifizierung und Priorisierung von IP-Paketen (z. B. Hinweis auf zeitsensitive Daten wie Sprachübertragungen)
- Möglichkeit zur Staukontrolle (Explicit Congestion Notification) auf der [[Vermittlungsschicht]] (optional)

Total Length
- Gibt die Gesamtlänge des IP-Pakets (Header + Daten) in Bytes an
- Die Maximallänge eines IP-Pakets beträgt damit 65 535 B
- Der Sender passt die Größe ggf. an, um Fragmentierung zu vermeiden
- Die maximale Paketlänge, so dass keine Fragmentierung notwendig ist, bezeichnet man als Maximum Transmission Unit (MTU)
- Diese ist abhängig von der [[Physikalische Schicht|physikalischen Schicht]] bzw. der [[Sicherungsschicht]] und beträgt bei [[FastEthernet Rahmen|FastEthernet]] 1500 B

Identification
- Für jedes IP-Paket (zufällig) gewählter 16 bit langer Wert
- Dient der Identifikation zusammengehörender Fragmente ([[IP-Fragmentierung]])

Flags
- Bit 16: Reserviert und wird auf 0 gesetzt
- Bit 17: Don’t Fragment (DF). Ist dieses Bit 1, so darf das IP-Paket nicht [[IP-Fragmentierung|fragmentiert]] werden
- Bit 18: More Fragments (MF). Gibt an, ob weitere Fragmente folgen (1) oder dieses Paket das letzte Fragment ist (0). Wurde das Paket nicht fragmentiert, wird es ebenfalls auf 0 gesetzt

Fragment Offset
- Gibt die absolute Position der Daten in diesem Fragment bezogen auf das unfragmentierte Paket in ganzzahligen Vielfachen von 8 B an
- Ermöglicht zusammen mit dem Identifier und MF-Bit die Reassemblierung fragmentierter Pakete in der richtigen Reihenfolge

TTL (Time to Live)
- Leitet ein [[Router]] ein IP-Paket weiter, so dekrementiert er das TTL-Feld um 1
- Erreicht das TTL-Feld den Wert 0, so verwirft ein [[Router]] das Paket und sendet eine Benachrichtigung an den Absender (ICMP Time Exceeded)
- Dieser Mechanismus beschränkt die Pfadlänge im Internet und verhindert endlos kreisende Pakete infolge von Routing Loops

Protocol
- Identifiziert das Protokoll auf der [[Transportschicht]], welches in der Payload (Datenteil) des IP-Pakets enthalten ist
- Relevant u. a. für das [[Betriebssystem|Betriebssystem]], um Pakete dem richtigen Prozess zuordnen zu können
- Gültige Werte sind beispielsweise 0x06 ([[Transmission Control Protokoll]]) und 0x11 ([[User Datagram Protokoll]])

Header Checksum
- Einfache, auf Geschwindigkeit optimierte Prüfsumme, welche nur den IP-Header (ohne Daten) schützt
- Die Prüfsumme ist so ausgelegt, dass die Dekrementierung des TTL-Felds einer Inkrementierung der Prüfsumme entspricht
- Es ist also keine komplette Neuberechnung der Prüfsumme bei der Weiterleitung von Paketen notwendig, lediglich eine Inkrementierung +1
- Es ist lediglich Fehlererkennung aber keine Korrektur möglich

Source Address: [[IP-Adresse]] des Absenders

Destination Address: [[IP-Adresse]] des Empfängers

Options / Padding
- IP unterstützt eine Reihe von Optionen (z. B. Route Recording, Zeitstempel, . . . ), welche als optionale Felder an den IP-Header angefügt werden können.
- Nicht alle diese Optionen sind 4 B lang. Da die Länge des IP-Headers jedoch ein Vielfaches von 4 B betragen muss, werden kürzere Optionen ggf. durch [[Padding]] auf ein Vielfaches von 4 B ergänzt

# Sonstiges
- für Fehlerbehandlung: [[Internet Control Message Protocol v4]] 
- Wie bekommen Hosts IP-Adressen? 
	- Statische Konfiguration von Hand, oder
	- dynamisch von einem [[Dynamic Host Configuration Protocol|DHCP]]-Server

# Besondere Adressbereiche
1. 0.0.0.0 / 8: Hosts in diesem [[Netzwerk]]
	- Verwendung z.B. als Quelladresse bei [[Dynamic Host Configuration Protocol]], wenn ein Client noch keine [[IP-Adresse]] besitzt.
	- [[Client-Server Architektur|Serveranwendungen]] erwarten eingehende Verbindungen auf der Adresse 0.0.0.0, was soviel bedeutet wie „jede Adresse, die verfügbar ist“.
	- Andere Adressen innerhalb dieses Bereichs dürfen als Zieladresse für bestimmte Hosts innerhalb des lokalen Netzes verwendet werden.
	- Adressen aus diesem Bereich werden grundsätzlich nicht geroutet.
2. 127.0.0.0 / 8: „Loopback-Adressen“
	- Adressen in diesem Bereich identifizieren den lokalen Rechner (Localhost), z. B. 127.0.0.1.
	- Diese Adressen werden grundsätzlich nicht geroutet.
	- Pakete mit dieser Zieladresse würden niemals gesendet sondern vor dem Sendevorgang „geloopt“.
3. 10.0.0.0 / 8, 172.16.0.0 / 12, 192.168.0.0 / 16: Private Adressbereiche
	- Dürfen innerhalb lokaler Netzwerke ohne Registrierung durch die IANA verwendet werden.
	- Adressen innerhalb dieser Bereiche dürfen zwischen privaten Netzen geroutet werden.
	- Mehrfache Vergabe in unterschiedlichen privaten Netzen möglich.
	- Dürfen nicht in öffentliche Netze geroutet werden.
4. 169.254.0.0 / 16: Automatic Private IP Adressing (APIPA)
	- Block zur automatischen Adressvergabe (APIPA).
	- Routing wie bei den privaten Adressbereichen.
5. 255.255.255.255 / 32: Global [[Broadcast]]
	- Identifiziert im Prinzip alle Hosts.
	- Wird niemals geroutet.