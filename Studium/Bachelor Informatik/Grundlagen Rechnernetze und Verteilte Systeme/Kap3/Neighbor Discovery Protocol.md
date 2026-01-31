---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs 
# Definition
Bestandteil von [[Internet Control Message Protocol v4|ICMP]]v6 mit unter anderem folgenden Funktionen:
- Adressauflösung, Duplicate Address Detection und Neighbor Unreachability Detection: Neighbor Solicitations und Advertisements.
- Automatisches Auffinden von [[Router|Routern]] innerhalb des lokalen Netzsegments, Adress-Präfixen und Parameter Konfiguration: [[Router]] Discovery und [[Router]] Advertisements.
- Umleitung zu anderen Gateways: Redirects

# Neighbor Solicitation (Request)

![[Neighbor Solicitation (Request).png]]

ICMPv6 Header: Type und Code (0x87 und 0x00 für eine Neighbor Solicitation Nachricht) sowie die ICMPv6 Checksumme

Neighbor Discovery Body
- Die ersten 32 bit sind reserviert, so dass die Nachricht insgesamt wieder ein Vielfaches von 8 B lang wird
- Im Anschluss folgt die Ziel-IPv6-Adresse, zu der die entsprechende [[MAC-Adresse]] gesucht wird

Neighbor Discovery Options
- Neighbor Discovery Pakete können selbst wiederum Optionen enthalten
- Type und Length geben den Typ (1 für Source Link Layer Address) und Gesamtlänge der Option in Vielfachen von 8 B an
- Im Fall eines Neighbor Solicitation Pakets folgt L2-Adresse des anfragenden Knotens (Source Link Address)
- Je nach Typ des NDP-Pakets können weitere Optionen folgen, wobei Empfänger unbekannte Optionen ignorieren müssen.

# Neighbor Advertisement (Reply)

![[Neighbor Advertisement (Reply).png]]

ICMPv6 Header: Type und Code (0x88 und 0x00 für ein Neighbor Advertisement) sowie die ICMPv6 Checksumme.

Neighbor Discovery Body
- Die drei höchstwertigen Bit des erste Oktetts haben folgende Bedeutungen:
	- [[Router]]-Flag R wird gesetzt, wenn der antwortende Knoten ein [[Router]] ist
	- Solicited Flag S gibt an, ob das Advertisement infolge einer Solicitation geschickt wird
	- Override Flag O wird gesetzt, wenn das Advertisement eine möglicherweise gecached Link-Layer Adresse beim Empfänger aktualisieren soll

Neighbor Discovery Options
- Type und Length geben den Typ (2 für Target Link Layer Address) und Gesamtlänge der Option in Vielfachen von 8 B an
- Im Fall eines Neighbor Advertisements folgt die L2-Adresse des angefragten Knotens (Target Link Address)
- Je nach Typ des NDP-Pakets können weitere Optionen folgen, wobei Empfänger unbekannte Optionen ignorieren müssen