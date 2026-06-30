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
- Definition von [[EXP]]
- Beweis von [[NP liegt zwischen P und EXP]] 
- Formale Definition von [[Karp-Reduktion in Polynomialzeit]] 
- Beispiel: [[3-Coloring <= Indset]] 

# NP-schwer und -vollständig
- Eine Sprache $L$ ist [[NP]]-schwer, wenn $\forall L' \in \textbf{NP}: L' \leq_p L$ gilt
- Eine Sprache $L$ ist [[NP]]-vollständig, wenn $L$ [[NP]]-schwer ist und $L \in \textbf{NP}$ 
- [[Cook-Levin Theorem]]: [[SAT]] ist [[NP]]-vollständig
- Reduktionen: [[SAT <= 3SAT]], [[3SAT <= 0-1-ILP]], [[3SAT <= Indset]], [[3SAT <= 3-Coloring]] 