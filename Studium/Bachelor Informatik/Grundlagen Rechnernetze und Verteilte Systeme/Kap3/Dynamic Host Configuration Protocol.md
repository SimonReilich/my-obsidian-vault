---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs #Atomic 
# Definition
Protokoll auf der [[Vermittlungsschicht]], um Hosts [[IP-Adresse|IP-Adressen]] zuzuweisen.

# Ablauf
1. Client sendet DHCP-Discover (Layer 2 [[Broadcast]])
2. DHCP-Server antwortet mit DHCP-Offer, wodurch er dem Client eine [[IP-Adresse]] anbietet
3. Client antwortet mit DHCP-Request, wodurch er die angebotene Adresse anfordert
4. DHCP-Server antwortet mit DHCP-ACK, wodurch er die angeforderte Adresse zur Nutzung freigibt, oder mit DHCP-NACK, wodurch er die Nutzung der Adresse untersagt

# Anmerkungen
- Die vom DHCP-Server zugewiesene Adresse wird auch als Lease bezeichnet und ist in ihrer Gültigkeit zeitlich begrenzt
- Clients erneuern ihr Lease in regelmäßigen Abständen beim DHCP-Server.
- Gerade in kleineren (privaten) Netzwerken übernimmt häufig ein [[Router]] die Rolle des DHCP-Servers
- Ein versehentlich ins [[Netzwerk]] eingebrachter DHCP-Server (z. B. durch einen achtlos angeschlossenen [[Router]] oder [[WLAN Access Points]]) kann beträchtliche Auswirkungen auf das [[Netzwerk]] haben und ist häufig schwer zu finden