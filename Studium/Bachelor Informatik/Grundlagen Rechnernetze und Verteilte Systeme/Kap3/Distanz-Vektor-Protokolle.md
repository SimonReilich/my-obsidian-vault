---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs #Atomic 
# Definition
Familie von Routingprotokollen mit folgenden Eigenschaften:
- [[Router]] kennen nur Richtung (Next-[[Hop]]) und Entfernung (Kosten) zu einem Ziel (vgl. Straßenschild mit Richtungs- und Entfernungsangabe)
- [[Router]] haben keine Information über die Netzwerktopologie
- [[Router]] tauschen untereinander lediglich kumulierte Kosten aus (z. B. den Inhalt Ihrer [[Routingtabelle]])
- Funktionsprinzip basiert auf dem [[Algorithmus von Bellman-Ford]], der kürzeste Wege ausgehend von einem Startknoten ermittelt und sich leicht verteilt implementieren lässt.
Beispiele: [[Routing Information Protokoll]], [[Interior Gateway Routing Protokoll]], [[Enhanced Interior Gateway Protokoll]] oder [[Ad hoc On-Demand Distance Vector]] 