---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs 
# Definition
[[Rahmen]] haben auf Schicht 2 eine maximale Größe, z. B. 1514 B für die L2-PDU (ohne CRC-Checksumme) bei IEEE 802.3u (100 Mbit/s [[Ethernet]]). Diese gibt auch die maximale Größe einer L3-PDU vor, welche als Maximum Transmission Unit (MTU) bezeichnet wird. Überschreitet eine L3-PDU diese Größe, muss die L3-SDU fragmentiert und in Form unabhängiger Pakete versendet werden. Der Empfänger muss die einzelnen Fragmente im Anschluss reassemblieren. [[Internet Protocol Version 6]] verfügt zu diesem Zweck über einen eigenen Extension Header, den Fragment Header

# Aufbau

![[Fragment Header.png]]

Next Header: Gibt den nächsten Extension Header oder das verwendete L4 Protokoll an

Reserved
- Hat derzeit beim Fragmentation Header keine Verwendung.
- Bei den meisten anderen Extension Headers gibt dieses Feld die Länge des jeweiligen Extension Headers an

Fragment Offset
- Offset der fragmenierten L3-SDU in Vielfachen von 8 B
- Bei IPv6 erfolgt die Fragmentierung ausschließlich am Sender

More Fragments (MF): Gibt an, ob auf das aktuelle Paket weitere Fragmente folgen oder ob es sich um das letzte Fragment (gemäß des Fragment Offsets) handelt

Identification: 32 bit langer, vom Sender zufällig gewählter Wert, welcher alle Fragmente identifiziert, die zu einer L3-SDU reassembliert werden sollen