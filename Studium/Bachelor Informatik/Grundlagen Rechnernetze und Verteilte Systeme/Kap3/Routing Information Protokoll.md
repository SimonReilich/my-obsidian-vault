---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs 
# Definition
Bei RIP handelt es sich um ein einfaches [[Distanz-Vektor-Protokolle|Distanz-Vektor-Protokoll]], dass als einzige Metrik den [[Hop]]-Count nutzt. Es gibt ein [[Hop]]-Count Limit von 15, weit entfernte Ziele sind also nicht erreichbar.

# Funktionsweise
- [[Router]] senden in regelmäßigen Abständen (Standardwert 30 s) den Inhalt ihrer [[Routingtabelle]] an die [[Multicast]]-Adresse 224.0.0.9
- Alle Geräte mit dieser [[Multicast]]-Adresse akzeptieren das Update
- Jeder RIP-[[Router]] akzeptiert diese Update-Nachrichten, inkrementiert die Kosten der enthaltenen Routen um 1 und vergleicht die Routen mit bereits vorhandenen Routen aus seiner [[Routingtabelle]]:
	- Enthält das Update eine noch unbekannte Route, wird diese in die eigene [[Routingtabelle]] übernommen
	- Enthält das Update eine Route zu einem bekannten Ziel aber mit niedrigeren Kosten, so wird die vorhandene Route durch das Update ersetzt
	- Andernfalls wird die vorhandene Route beibehalten
- Bleiben fünf aufeinanderfolgende Updates von einem Nachbarn aus, so werden alle Routen über diesen Next [[Hop]] aus der [[Routingtabelle]] entfernt

# Problem
- Bis jeder [[Router]] den besten Next [[Hop]] bestimmen kann, dauert es ggf. mehrere „Runden“
- Eine obere [[Schranke]] für die Anzahl der notwendigen Nachrichten, die jeder [[Router]] senden muss, ist die maximale Entfernung zwischen zwei [[Router|Routern]] in [[Hop|Hops]]
- Die maximale Entfernung beträgt bei RIP 15 [[Hop|Hops]]
- Da Updates nur alle 30 s verschickt werden, ergibt sich eine maximale Verzögerung von 15 · 30 s = 7,5 min
- Lösung Triggered Updates: Sobald ein [[Router]] eine Änderung an seiner [[Routingtabelle]] vornimmt, sendet er sofort ein Update. Dies führt zu einer Welle von Updates durch das [[Netzwerk]], die Konvergenzzeit wird reduziert, aber das [[Netzwerk]] während der Updates ggf. stark belastet

# Anderes Problem: Count to Infinity
- Split Horizon
	- „Sende dem Nachbarn, von dem Du die Route zu X gelernt hast, keine Route zu X.“
	- Split Horizon verbessert die Situation, kann das Problem aber nicht lösen.
- Poison Reverse
	- Anstelle dem Nachbarn, von dem eine Route zu X gelernt wurde, keine Route zu X mehr zu schicken, wird eine Route mit unendlicher Metrik gesendet.
	- Auch Poison Reverse kann das Problem nicht vollständig lösen.
- Path Vector
	- Sende bei Updates nicht nur Ziel und Kosten, sondern auch den vollständigen Pfad, über den das Ziel erreicht wird.
	- Jeder [[Router]] prüft vor Installation der Route, ob er selbst in diesem Pfad bereits vorhanden ist.
	- Falls ja, handelt es sich um eine Schleife und das Update wird verworfen.
	- Path Vector verhindert Routing Loops und damit auch Count to Infinity, vergrößert jedoch die Update-Nachrichten und die Protokollkomplexität