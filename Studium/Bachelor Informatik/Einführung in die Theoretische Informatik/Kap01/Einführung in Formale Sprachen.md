---
lecture: "[[Einführung in die Theoretische Informatik]]"
degree: "[[Bachelor Informatik]]"
---
#BScInfo #Informatik #Theo
# Einführung
- [[1950]]er: Idee, [[Programmiersprache|Programmiersprachen]] zur Kommunikation mit Maschinen zu nutzen
- Linguist [[Noam Chomsky]] forscht an [[Transformationsgrammatik]], eigentlich mit dem Ziel, die Struktur der menschlichen Sprache zu erklären
- Der begriff [[formale Grammatik]] wird [[1960]] von der Informatik übernommen
- [[Syntax]] von [[Programmiersprache|Programmiersprachen]] lässt sich durch [[formale Grammatik]] beschreiben

# Grundbegriffe
- Definition [[Alphabet]], [[Wort]]
- für ein [[Wort]] $w \in \Sigma^*$ wird $|w|$ als die Länge des Wortes bezeichnet
- Das [[leeres Wort|leere Wort]] wird mit dem [[Symbol]] $\epsilon$ bezeichnet
- Konkatenation: $uv$, Wiederholung: $w^0 = \epsilon, w^{n + 1} = ww^n$ 
- $\Sigma^*$ (die [[reflexiv transitive Hülle]]) ist die Menge aller Wörter über $\Sigma$ 
- Definition [[formale Sprache]] 

# Grammatiken
- Definition [[formale Grammatik]]
- Eine [[formale Grammatik]] $G$ induziert eine [[Ableitungsrelation]] $\to_G$
- $G$ erzeugt das Wort $\alpha$ genau dann, wenn $S \to^*_G \alpha$ 
- Die [[formale Sprache]], die von $G$ erzeugt wird, wird mit $L(G)$ bezeichnet
- [[Chomsky-Hierarchie]]
- Definition [[Wortproblem]] 