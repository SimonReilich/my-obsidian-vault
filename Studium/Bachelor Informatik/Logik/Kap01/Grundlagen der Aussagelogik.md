---
lecture: "[[Logik]]"
---
#Bachelor #Informatik #Logik
# Definitionen
- Definition [[Atomare Formel|atomarer Formeln]] 
- Rekursive Definition von Aussagelogischen Formeln:
	- $\bot$ (falsch) und $\top$ (wahr) sind Formeln
	- jede [[Atomare Formel]] ist eine Formel
	- Ist $F$ eine Formel, so auch $\neg F$ 
	- Sind $F$ und $G$ Formeln, so auch $(F \circ G)$ for all $\circ \in \{\land, \lor, \implies, \iff\}$ ([[Operatoren der Aussagelogik]]) 
- Formeln können als [[Syntaxbaum]] dargestellt werden
- Eine Zuweisung $\mathcal{A}$ ist eine Funktion $\mathrm{Atome} \to \{0, 1\}$, anhand folgender Regeln erweitern wir zu $\hat{\mathcal{A}}: Formeln \to \{0, 1\}$:$$ \hat{\mathcal{A}}(A_i) = \mathcal{A_i} $$$$\hat{\mathcal{A}}(\neg F) = \begin{cases} 0 & \text{if } \hat{\mathcal{A}}(F) = 1 \\ 1 & \text{otherwise}\end{cases}$$$$\hat{\mathcal{A}}(F \land G) = \begin{cases} 1 & \text{if } \hat{\mathcal{A}}(F) = \hat{\mathcal{A}}(G) = 1 \\ 0 & \text{otherwise} \end{cases}$$$$\hat{\mathcal{A}}(F \lor G) = \begin{cases} \end{cases}$$