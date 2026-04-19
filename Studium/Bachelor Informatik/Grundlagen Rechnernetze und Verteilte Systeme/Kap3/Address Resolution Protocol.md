---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs  
# Definition
Protokoll, um zu einer gegebenen [[IP-Adresse]] die zugehörige [[MAC-Adresse]] zu erhalten

# Ablauf (selbes Netz)

![[ARP lokal.png]]

- Host 1 will eine Nachricht an Host 2 senden
- Die [[IP-Adresse]] von Host 2 (192.168.1.2) sei ihm bereits bekannt
- Host 1 sendet einen ARP-Request: „Who has 192.168.1.2? Tell 192.168.1.1 at c8:2a:14:4f:dc:02“
- Host 2 antwortet mit einem ARP-Reply: „192.168.1.2 is at 04:0c:ce:e2:c8:2e“

![[ARP Request und Reply.png]]

- Der ARP-Request wird an die MAC-[[Broadcast]]-Adresse ff:ff:ff:ff:ff:ff geschickt, weswegen der [[Switch]] S den [[Rahmen]] an alle angeschlossenen Hosts weiterleitet.
- Der ARP-Reply wird als MAC-[[Unicast]] versendet (adressiert an Host1).
- Die Rollen Sender / Target sind zwischen Request und Reply vertauscht (vgl. Inhalte der grünen und roten Felder)

# Ablauf (unterschiedliches Netz)
- Im Prinzip selbes Verfahren, Host 1 erkennt an der [[IP-Adresse]], dass es sich um ein Ziel außerhalb des eigenen Netzwerks handelt
- Jeder Host sollte einen [[Router]] zum Internet, das sog. Default Gateway, kennen, an das er alle Pakete schickt, deren Zieladressen nicht im eigenen Netz liegen, und für die in seiner Routing-Tabelle nicht ein spezifisches Gateway eingetragen ist
- Host schickt Paket an [[MAC-Adresse]] des [[Router|Routers]], dieser kümmert sich selbst um die Weiterleitung an das richtige [[Netzwerk]] (ggf. nochmal [[Address Resolution Protocol|ARP]]-Request)

# Weiteres
Das Ergebnis einer Adressauflösung wird i. d. R. im ARP-Cache eines Hosts zwischengespeichert, um nicht bei jedem zu versendenden Paket erneut eine Adressauflösung durchführen zu müssen. Die Einträge im ARP-Cache altern und werden nach einer vom [[Betriebssystem]] festgelegten Zeit invalidiert (z.B. 5 – 10 Minuten). ARP-Replies können auch als MAC-[[Broadcast]] verschickt werden, so dass alle Hosts innerhalb einer [[Broadcast]]-Domain den Reply erhalten. Abhängig vom [[Betriebssystem]] werden derartige „unaufgeforderten ARP-Replies“ (engl. unsolicited ARP replies) häufig
ebenfalls im ARP-Cache gespeichert.