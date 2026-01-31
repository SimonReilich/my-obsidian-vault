---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs 
# Definition
[[WLAN]] Access Points sind im wesentlichen [[Bridge|Bridges]] zwischen Twisted Pair und Funkübertragung:
- Ein RJ45-Interface in Richtung des kabelgebundenen Netzwerks
- Ein Wireless Transceiver in Richtung des Funknetzwerks
Wichtig: Im Gegensatz zum [[Switch]] wird der Access Point explizit adressiert. Innerhalb eines kabellosen Netzes ist ein AP daher nicht transparent.

Der Begriff „WLAN [[Router]]“ ist technisch falsch:
- Hersteller verkaufen hier Geräte, welche gleichzeitig
	- DSL- oder Kabel-[[Modem]],
	- [[Ethernet]] [[Switch]],
	- [[Router]] ([[Ethernet]] ↔ DSL/Cable/etc.) und
	- [[WLAN]] Access Point sind.
- Tatsächlich sind [[WLAN]] Access Points nicht mehr als [[Switch|Switches]] mit integrierten Medienkonvertern, wobei meistens gleich noch ein [[Router]] integriert wird.
- Routing (siehe [[Vermittlungsschicht]]) findet innerhalb kabelloser Netzwerke im Infrastructure Mode nicht statt