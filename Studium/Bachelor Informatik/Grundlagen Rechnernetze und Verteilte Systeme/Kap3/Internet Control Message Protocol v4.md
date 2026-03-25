---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs #Atomic 
# Definition
Das [[Internet Protocol Version 4]] unterstützt das Senden von Paketen an Ziel-Hosts. Dabei kann es zu Fehlern kommen, z. B. ein Paket gerät in eine Routing-Schleife, ein [[Router]] kennt keinen Weg zum Zielnetz, der letzte [[Router]] zum Ziel kann die [[MAC-Adresse]] des Empfängers nicht auflösen . . . Das Internet Control Message Protocol (ICMP) dient dazu, in derartigen Fällen den Absender über das Problem zu benachrichtigen und stellt zusätzlich Möglichkeiten bereit, um z. B. die Erreichbarkeit von Hosts zu prüfen („Ping“) oder Pakete umzuleiten (Redirect).

# Aufbau

![[ICMP Allgemein.png]]

![[ICMP Request & Reply.png]]

Wozu dient der Identifier?
- Der IP-Header besitzt ein TTL-Feld, welches bei der Weiterleitung eines Pakets durch den jeweiligen [[Router]] um 1 dekrementiert wird
- Erreicht es den Wert 0, so wird das betreffende Paket verworfen
- Der [[Router]] generiert ein ICMP Time Exceeded und schickt es an den Absender des verworfenen Pakets zurück