---
lecture: "[[Algorithmen für Programmierwettbewerbe]]"
---
#Bachelor #Informatik #ConPra 
# Definition
Sei $S \subseteq [n]^k$ eine Menge von Tupeln
- Ein Tupel $(x_1, ..., x_I)$ mit $i \leq k$ ist ein valides Präfix in $S$, falls es $x_{I + 1}, ..., x_k$ gibt, sodass $(x_1, ..., x_i, x_{I + 1}, ..., x_k) \in S$ ist.
- Sei $x = (x_1, ..., x_k) \in S$. Wir sagen, dass $$