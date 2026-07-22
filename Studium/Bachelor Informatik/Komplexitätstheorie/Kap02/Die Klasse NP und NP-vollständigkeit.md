---
lecture: "[[Komplexitätstheorie]]"
degree: "[[Bachelor Informatik]]"
---
#BScInfo #Informatik #Comp 
# Nichtdeterminismus
- Definition einer [[Nichtdeterministische Turingmaschiene|nichtdeterministischen Turingmaschiene]] 
- Menge der [[Berechenbarkeit|berechenbaren]] Funktionen verändert sich nicht gegenüber deterministischer [[Turingmaschiene]]
- Definition der Klassen [[NTIME]] und [[NP]] als nichtdeterministische Varianten von [[DTIME]] und [[P]]
- Alternative Definition von [[NP]]: Menge der Sprachen mit effizient prüfbaren Zertifikaten
- Beweis [[Äquivalenz der Definitionen von NP]] 

# Verhältnis von NP zu anderen Klassen
- Definition von [[EXP]] und [[NEXP]] 
- Beweis von [[NP liegt zwischen P und EXP]] 
- Formale Definition von [[Karp-Reduktion in Polynomialzeit]] 
- Beispiel: [[Reduktion von 3-Coloring auf Indset]] 

# NP-schwer und -vollständig
- Eine Sprache $L$ ist [[NP]]-schwer, wenn $\forall L' \in \textbf{NP}: L' \leq_p L$ gilt
- Eine Sprache $L$ ist [[NP]]-vollständig, wenn $L$ [[NP]]-schwer ist und $L \in \textbf{NP}$ 
- [[Cook-Levin Theorem]]: [[SAT]] ist [[NP]]-vollständig
- Reduktionen: [[Reduktion von SAT auf 3SAT]], [[Reduktion von 3SAT auf 0-1-ILP]], [[Reduktion von 3SAT auf 3-Coloring]] 

# Komplemente von Komplexitätsklassen
- Definition der [[Komplementklasse]] und damit [[coNP]] 
- Offensichtlicherweise gilt $\textbf{P} = \textbf{coP}$, unbekannt ist aber $\textbf{NP} \overset{?}{=} \textbf{coNP}$ 
- Beweise [[Tautology ist coNP-vollständig]] 

# Unbekanntes
- Die meisten bekannten Probleme in [[NP]] sind [[NP]]-vollständig
- Unbekannt sind aber z.B. [[Iso]] oder [[Faktor]]
- Heutzutage lassen sich Probleme aus [[NP]] mit [[SAT Solver|SAT Solvern]] effizient lösen
- [[Ladners Theorem]]: Falls $\textbf{P} \neq \textbf{NP}$, dann existieren Sprachen in [[NP]], die nicht [[NP]]-vollständig sind