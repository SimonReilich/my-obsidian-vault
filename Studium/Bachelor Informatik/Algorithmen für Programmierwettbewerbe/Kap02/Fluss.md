---
lecture: "[[Algorithmen für Programmierwettbewerbe]]"
---
#Bachelor #Informatik #ConPra #Atomic 
# Definition
Sei $(V, E, c, s, t)$ ein [[Flussnetzwerk]], sei $f: E \to \mathbb{R}_{\geq 0}$. Es sei definiert:
- der Ausfluss von $v \in V$ als $\mathrm{out}_f(v) := \sum_{u \in vE}f(v, u)$
- der Einfluss von $v \in V$ als $\mathrm{in}_f(v) := \sum_{u \in Ev} f(u, v)$ 
Dann heißt $f$ Fluss, falls $\forall(u, v) \in E: 0 \leq f(u, v) \leq c(u, v)$ und $\forall u \in V \\ \{s, t\}: \mathrm{out}_f(o) = \mathrm{in}_f(u)$. Der Flusswert $|f|$ ist definiert als $\mathrm{out}_f(s) - \mathrm{in}_f(s)$ 