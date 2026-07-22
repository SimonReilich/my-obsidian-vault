---
lecture: "[[Komplexitätstheorie]]"
---
#BScInfo #Informatik #Comp
# Definition
Ein [[formale Sprache]] $L \subseteq \{0, 1\}^*$ ist in $\textbf{coNP}$, wenn es ein [[Polynom]] $p: \mathbb{N} \to \mathbb{N}$ und eine [[Polynom|polynomielle]] [[Turingmaschiene]] $M$ gibt, sodass für alle $x \in \{0, 1\}^*$ gilt:$$x \in L \iff \forall u \in \{0, 1\}^{p(x)}, M(x, u) = 1$$
# Beispiele für $\textbf{coNP}$-vollständige Probleme
- [[Tautology]] 