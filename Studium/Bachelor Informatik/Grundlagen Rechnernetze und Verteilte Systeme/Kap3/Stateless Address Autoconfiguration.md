---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs #Atomic 
# Definition
Protokoll zur automatischen Konfiguration von [[Internet Protocol Version 6|IPv6]]-Adressen

# Ablauf

![[SLAAC Ablauf.png]]

- Das Präfix ist fe80::/10.
- Der Subnet Identifier (die folgenden 54 bit) werden auf 0 gesetzt
- Die verbleibenden 64 bit stellen den Interface Identifier dar, welcher aus der [[MAC-Adresse]] des jeweiligen Interfaces als modifizierter EUI-64 Identifier generiert wird:
	- Die ersten 24 bit sind der OUI der [[MAC-Adresse]]
	- Die nachfolgenden 16 bit werden mit ff:fe „gestopft“
	- Die restlichen 24 bit werden mit dem Device Identifier der [[MAC-Adresse]] aufgefüllt
- Dabei ist das vorletzte Bit des ersten Oktett des OUI (global/local-Bit) invertiert:
	- Bei [[MAC-Adresse|MAC-Adressen]] bedeutet eine 0 an dieser Bitstelle eine global eindeutige und eine 1 eine lokal administrierte Adresse (siehe [[Sicherungsschicht]])
	- Bei IPv6 ist es genau andersrum: Durch die Invertierung wird erreicht, dass eine manuell konfigurierte IPv6-Adresse wie 2001:db8::1 nicht einen Interface Identfier enthält, der auf eine global eindeutige [[MAC-Adresse]] hinweist
	- Andernfalls müsste man von Hand Adressen wie 2001:db8::200:0:0:1 vergeben . . .

Auch globale Adressen können über SLAAC konfiguriert werden:
- Um eine globale Adresse konfigurieren zu können, muss der Host zunächst wissen, welche IPv6 Präfixe von den lokalen [[Router|Routern]] bedient werden.
- Präfix Informationen können von den [[Router|Routern]] über das [[Neighbor Discovery Protocol]] in Form von [[Router]] Advertisements versendet werden.
- Der Host kann sich über das /64 Präfix und dem modifizierten EUI-64 Identifier selbstständig eine Adresse erzeugen.
- SLAAC heißt stateless, da die Adressen nicht von einem Server vergeben werden
- Globale Adressen können auch über [[Dynamic Host Configuration Protocol|DHCP]]v6 vergeben werden