---
lecture: "[[Algorithmen für Programmierwettbewerbe]]"
---
#BScInfo #Informatik #ConPra #Atomic 
# Definition
Sei $S \subseteq [n]^k$ eine Menge von Tupeln
- Ein Tupel $(x_1, ..., x_I)$ mit $i \leq k$ ist ein valides Präfix in $S$, falls es $x_{I + 1}, ..., x_k$ gibt, sodass $(x_1, ..., x_i, x_{I + 1}, ..., x_k) \in S$ ist.
- Sei $x = (x_1, ..., x_k) \in S$. Wir sagen, dass $x$ an der Stelle $i \in [k]$ zu $v \in [n]$ inkrementiert werden kann, wenn $x_i < v$ und $(x_1, ..., x_{i - 1}, v)$ ein valides Präfix in $S$ ist.

# Algorithmus
- Wähle zuerst das lexikographisch kleinste Element in $S$, genannt $x$
- Solange $x$ inkrementierbar ist: 
	- Wähle das größt mögliche $i$ und das kleinst mögliche $v$ und setze $x' = (x_1, ..., x_{i - 1}, v)$
	- Wähle das lexikographisch kleinste Suffix $s$, sodass $(x', s) \in S$ und setze $x = (x', s)$
