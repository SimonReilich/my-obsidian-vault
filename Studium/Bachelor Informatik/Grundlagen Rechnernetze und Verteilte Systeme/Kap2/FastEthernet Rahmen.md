---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs #Atomic 
# Definition
Standardaufbau für [[Rahmen]] bei [[Ethernet]].

# Aufbau
([[Rahmen]] vor der [[4B5B]]-Kodierung)

![[FastEthernet Rahmen.png]]

- Präambel und Start Frame Delimiter (SFD) dienen der Taktsynchronisation.
- Ein Byte der Präambel wird durch das J/K-[[Symbol]] des [[4B5B]]-Codes ersetzt (Start Frame Delimiter).
- RA: Reciever-Adress (Empfänger), TA: Transmitter-Adress (Sender)
- Das Typfeld gibt die Art des Frames an (z. B. 0x0800 = IPv4 Payload, 0x0806 = ARP).
- Das Datenfeld muss (vor der Kodierung) mind. 46B lang sein – andernfalls wird es bis zu diesem Wert gepadded
- Nach der Frame Check Sequence (FCS) wird das T/R-[[Symbol]] des [[4B5B]]-Codes eingefügt (End of Frame).
- Zwischen J/K und T/R liegende Daten werden gemäß des [[4B5B]]-Codes kodiert.