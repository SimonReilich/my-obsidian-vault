---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs #Atomic 
# Definition
In der Routing-Tabelle speichert ein [[Router]] (oder Host)
- die Netzadresse eines Ziels,
- die Länge des Präfixes,
- den zugehörigen Next-[[Hop]] (auch Gateway genannt),
- das Interface, über welches dieser Next-[[Hop]] erreichbar ist, und
- die Kosten bis zum Ziel
Intern nutzt die Routing Tabelle den [[Longest Matching Prefix]] Algorithmus um zu bestimmen, an welchen [[Hop]] das Paket als nächstes weitergeleitet wird.

# Beispielhafte Tabelle

![[Routing Tabelle Beispiel.png]]
