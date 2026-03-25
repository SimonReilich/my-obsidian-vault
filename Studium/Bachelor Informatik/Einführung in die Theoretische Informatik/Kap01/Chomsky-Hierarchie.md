---
lecture: "[[Einführung in die Theoretische Informatik]]"
---
#Bachelor #Informatik #Theo #Atomic 

# Definition
Die Chomsky-Hierarchie, [[1956]] von [[Noam Chomsky]] eingeführt, ist ein grundlegendes Modell der theoretischen Informatik, das [[formale Sprache|formale Sprachen]] und [[formale Grammatik|Grammatiken]] nach ihrer Mächtigkeit und Komplexität in vier Stufen klassifiziert. Eine [[formale Grammatik]] $G$ lässt sich wie folgt einordnen:
0. Immer.
1. Falls für jede Produktion $\alpha \to \beta$, außer $S \to \epsilon$, $|\alpha| \leq |\beta|$ gilt und, wenn $S \to \epsilon$ eine Produktion ist, $S$ nicht in $\beta$ vorkommt.
2. Falls $G$ vom Typ 1 ist und für jede Produktion $\alpha \to \beta$, $\alpha \in V$ gilt
3. Falls $G$ vom Typ 2 ist und für jede Produktion $\alpha \to \beta$ außer $S \to \epsilon$ gilt $\beta \in \Sigma \cup \Sigma V$ 
Offensichtlich gilt: Typ 3 $\subset$ Typ 2 $\subset$ Typ 1 $\subset$ Typ 0. Selbiges gilt für die [[formale Sprache]], die von einer Grammatik erzeugt wird. Je nach Typ haben Sprache und Grammatik eigene Namen:
- Typ 3: [[Rechtslineare Grammatik]], [[Reguläre Sprache]] 
- Typ 2: [[Kontextfreie Grammatik]], [[Kontextfreie Sprache]] 
- Typ 1: [[Kontextsensitive Grammatik]], [[Kontextsensitive Sprache]] 
- Typ 0: [[Phasenstrukturgrammatik]], [[Rekursiv aufzählbare Sprache]] 