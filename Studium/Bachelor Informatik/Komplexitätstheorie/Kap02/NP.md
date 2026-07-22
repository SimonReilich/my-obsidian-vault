---
lecture: "[[Komplexitätstheorie]]"
---
#BScInfo #Informatik #Comp
# Definition
Für $\textbf{NP}$ existieren zwei [[Äquivalenz der Definitionen von NP|äquivalente]] Definitionen: 
$$\textbf{NP} = \bigcup_{c \geq 1}\textbf{NTIME}(n^c)$$$\textbf{NP}$ als Menge aller Sprachen, die in polynomieller Zeit von einer [[Nichtdeterministische Turingmaschiene|nichtdeterministischen Turingmaschiene]] berechnet werden können.
Alternativ kann $\textbf{NP}$ auch als Menge aller Sprachen Definiert werden, für die effiziente Zertifikate existieren. Sei $L \in \textbf{NP}$, $p$ ein [[Polynom]], und $M$ eine in polynomieller Zeit laufende, deterministische [[Turingmaschiene]] dann gilt:$$x \in L \iff \exists u \in \{0, 1\}^{p(|x|)} \text{ s.t. } M(x, u) = 1$$ 
# $\textbf{NP}$-vollständige Probleme
- [[Indset]]
- [[3-Coloring]]
- [[3SAT]] 