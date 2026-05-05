---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs #Atomic 
# Definition
Standardaufbau für [[Rahmen]] bei [[WLAN]].

# Aufbau

![[WLAN Rahmen.png]]

Physical Layer Convergence Procedure (PLCP)
- Header der [[Physikalische Schicht|physikalischen Schicht]] 
- Dient der Synchronisation sowie der Mitteilung von Übertragungsparametern (Datenrate, [[Modulation]], Coderate, etc.)
- Nicht Bestandteil des L2-Headers

Frame Control (FC)
- Gibt den Typ des Rahmens an (Data, Management oder Control)
- Definiert, wie die im [[Rahmen]] enthaltenen Adressen zu interpretieren sind (ToDS / FromDS Bits)
- Verschiedene weitere Parameter:
	- Folgen weitere Fragmente, die zum selben [[Rahmen]] gehören?
	- Handelt es sich um einen Retransmit (Wiederholung)?
	- Liegen am Sender noch weitere [[Rahmen]] vor?
	- . . .

[[MAC-Adresse|MAC-Adressen]] (variable Anzahl, nachfolgend typische Nutzung der Felder)
- Address 1 gibt den direkten Empfänger (Receiver Address, RA) an
- Address 2 gibt die Adresse der übertragenden Station (Transmitter Address, TA) an
- Address 3 gibt den Sender (Source Address, SA) bzw. das Ziel (Destination Address, DA) an

Sequence Control
- Sequenznummer des Rahmens
- Dient der Erkennung von fehlenden [[Rahmen]] und der Sortierung empfangener [[Rahmen]]

Subnetwork Access Protocol (SNAP)
- Header variabler Länge zur Angabe des Typs der L3-PDU
- Entfernt vergleichbar mit dem Ethertype (aber um vieles flexibler)

Daten (L3-PDU)
- Daten variabler Länge
- Die maximale Rahmengröße in IEEE 802.11-Netzen ist um ein Vielfaches größer als bei [[Ethernet]]
	- Der Medienzugriff benötigt hier sehr viel Zeit
	- Je kleiner die einzelnen [[Rahmen]], desto mehr Zeit geht durch den Medienzugriff verloren
	- ⇒ Tendenz zu größeren [[Rahmen]] trotz höherer Bitfehlerwahrscheinlichkeit

Frame Check Sequence (FCS)
- 32-bit CRC-Prüfsumme über den gesamten L2-[[Rahmen]] (alles außer PLCP und die FCS selbst)
- Bis auf Implementierungsdetails identisch zu [[Ethernet]]
- FCS wird mit anderem [[Polynom]] als bei [[Ethernet]] berechnet