---
lecture: "[[Petrinetze]]"
---
#BScInfo #Informatik #Petri
# Syntax
- Definition eines [[Netz|Netzes]] 
- $N'=(S', T', F')$ ist ein Teilnetz von $N = (S, T, F)$ genau dann wenn
	- $S' \subseteq S$
	- $T' \subseteq T$
	- $F' = F \cap ((S' \times T') \cup (T' \times S'))$ 
- [[Pfad]], [[Zyklus]] und (stark) [[Zusammenhängend]] sind für [[Netz|Netze]] analog zu [[Graph|Graphen]] definiert

# Semantik
- Definition einer [[Markierung]]
- Eine Transition $t$ ist für eine gegebene [[Markierung]] $M$ schaltbereit, wenn für jede Stelle $s \in \cdot t$ $M(s) \geq 1$ 
- Wenn eine Transition $t$ für eine [[Markierung]] $M$ schaltbereit ist und schaltet, führt das zu einer neuen [[Markierung]] $$M' = \begin{cases} M(s) - 1 & \text{wenn } s \in \cdot t \end{cases}$$