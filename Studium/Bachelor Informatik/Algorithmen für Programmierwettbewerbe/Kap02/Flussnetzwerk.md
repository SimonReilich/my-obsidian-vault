---
lecture: "[[Algorithmen für Programmierwettbewerbe]]"
---
#BScInfo #Informatik #ConPra #Atomic 
# Definition
Ein Flussnetzwerk ist ein 5-Tupel $(V , E , c, s, t)$, wobei
- $(V, E)$ ein gerichteter [[Graph]] ist
- $c: E \to \mathbb{R}_{\geq 0}$ ist die Kapazitätsfunktion
- $s \in V$ ist die Quelle
- $t \in V$ ist der Abfluss
Ohne Beschränkung der Allgemeinheit betrachten wir nur [[Graph|Graphen]] ohne antiparalelle Kanten, also $(u, v) \in E \implies (v, u) \notin E$.