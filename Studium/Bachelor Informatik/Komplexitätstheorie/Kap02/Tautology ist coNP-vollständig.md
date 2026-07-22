---
lecture: "[[Komplexitätstheorie]]"
---
#BScInfo #Informatik #Comp
# Satz
$$\forall L \in \textbf{coNP}, L \leq_p \text{Tautology}$$[[Tautology]] ist [[coNP]]-vollständig.

# Beweis
Sei $L \in \textbf{coNP}$. Dann liegt das Komplement $\overline{L}$ von $L$ in [[NP]], aufgrund des [[Cook-Levin Theorem]] lässt sich $\overline{L}$ also auf [[SAT]] reduzieren. Es gibt also eine Funktion $x \mapsto \varphi_x$, sodass $\varphi_x \in \text{SAT} \iff x \in \overline{L}$. Daraus folgt:$$\neg \varphi_x \in \text{Tautology \iff x \in L}$$