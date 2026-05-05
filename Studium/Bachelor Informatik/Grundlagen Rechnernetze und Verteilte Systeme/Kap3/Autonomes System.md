---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs 
# Definition
Eine Menge von Netzwerken, die unter einheitlicher administrativer Kontrolle stehen, bezeichnet man als Autonomes System (AS). Ein AS wird durch einen 16 bit bzw. 32 bit Identifier, der sog. AS-Nummer identifiziert. Beim Einsatz von Routingprotokollen wird unterschieden:
- Innerhalb eines autonomen Systems werden Interior Gateway Protocols (IGPs) wie [[Routing Information Protokoll]], [[Open Shortest Path First]], [[Enhanced Interior Gateway Protokoll]] oder [[Intermediate System to Intermediate System]] eingesetzt.
- Zum Austausch von Routen zwischen Autonomen Systemen wird ein [[Exterior Gateway Protocol]] verwendet.
Das einzige in der Praxis verwendete [[Exterior Gateway Protocol]] ist das [[Border Gateway Protocol]].

# Das Internet (Schematisch)

![[Provider.png]]

- Autonome Systeme können durch Upstream-Provider oder durch Peering miteinander verbunden sein
- Peering-Verbindungen sind aus Kostengründen gegenüber Customer-Provider Verbindungen zu bevorzugen
- Die Border-[[Router]] eines AS „announcen“ Präfixe, die über dieses AS erreichbar sind