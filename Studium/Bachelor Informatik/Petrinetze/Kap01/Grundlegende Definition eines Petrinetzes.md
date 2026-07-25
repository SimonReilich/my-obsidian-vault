---
lecture: "[[Petrinetze]]"
degree: "[[Bachelor Informatik]]"
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
- Wenn eine Transition $t$ für eine [[Markierung]] $M$ schaltbereit ist und schaltet, führt das zu einer neuen [[Markierung]] $$M' = \begin{cases} M(s) - 1 & \text{wenn } s \in \cdot t \setminus t \cdot \\ M(s) + 1 & \text{wenn } s \in t\cdot \setminus \cdot t \\ M(s) & \text{sonst} \end{cases}$$
- Definition einer [[Schaltsequenz]] 
- Man schreibt $M \overset{t}{\rightarrow} M'$, $[M\textrangle$ ist die Menge aller von $M$ aus erreichbaren [[Markierung|Markierungen]]
- Eine [[Markierung]] ist tot, wenn keine Transition schaltbereit ist
- [[Monotonie-Lemma]]: Durch hinzufügen von Tokens werden Transitionen nicht deaktiviert
- Ein [[Petrinetz]] ist ein [[Tupel]] aus einem [[Netz]] und einer initialen [[Markierung]] 
- [[Erreichbarkeitsgraph-Algorithmus]] 
- Interessante Eigenschaften: [[Deadlock-Freiheit]], [[Lebendigkeit]], [[Beschränktheit (Petrinetze)|Beschränktheit]] 

# Varianten des Modells
- [[Petrinetz mit Kapazitäten]], [[Petrinetz mit gewichteten Bögen]], [[Vektor-Additions-Systeme]] (mit Zuständen): gleiche Mächtigkeit
- [[Populationsprotokoll]]: weniger Mächtig
- [[Petrinetz mit Sperr-Bögen]], [[Petrinetz mit Reset-Bögen]]: höhere Mächtigkeit
- Anwendungen: biologische Systeme, Prozessabläufe, etc