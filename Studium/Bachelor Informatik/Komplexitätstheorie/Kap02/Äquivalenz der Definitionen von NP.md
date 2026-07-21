---
lecture: "[[Komplexitätstheorie]]"
---
#BScInfo #Informatik #Comp
# Satz
Die folgenden Definitionen der Komplexitätsklasse [[NP]] sind äquivalent:
- $\textbf{NP} = \{L \mid x \in L \iff \exists u \in \{0, 1\}^{p(|x|)} \text{ s.t. } M(x, u) = 1\}$ 
- $\textbf{NP} = \bigcup_{c \geq 1}\textbf{NTIME}(n^c)$

# Beweis
- (2 => 1): $L \in \textbf{NP}$ heißt, dass $L \in \textbf{NTIME}(n^c)$ für ein bestimmtes $c$ gilt. Die Folge der Wahlen der Transitionsfunktion in der [[Nichtdeterministische Turingmaschiene|nichtdeterministischen Turingmaschiene]] ist somit ein [[Polynom|polynomielles]] Zertifikat
- (1 => 2): Es gibt eine deterministische [[Turingmaschiene]] $M$, so dass $x \in L \iff M(x, u) = 1$ für ein Zertifikat $u \in \{0, 1\}^{p(|x|)}$. Eine [[Nichtdeterministische Turingmaschiene]] kann nun das Zertifikat in [[Polynom|polynomieller]] Zeit "raten"