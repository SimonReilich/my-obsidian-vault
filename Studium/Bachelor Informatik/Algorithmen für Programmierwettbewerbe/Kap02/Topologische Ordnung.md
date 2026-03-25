---
lecture: "[[Algorithmen für Programmierwettbewerbe]]"
---
#Bachelor #Informatik #ConPra #Atomic 
# Definition
Für einen [[Graph|Graphen]] $G = (V, E)$ ist $o: V \to \mathbb{N}$  genau dann eine topologische Ordnung, genau dann wenn für alle $(u, v) \in E$ gilt: $o(u) < o(c)$ 

# Eigenschaften
- Topologische Ordnung existiert genau dann, wenn der [[Graph]] [[azyklisch]] ist
- Die Topologische Ordnung ist nicht einzigartig
- Algorithmus zum Finden einer topologischen Ordnung: [[Topological Sort]]