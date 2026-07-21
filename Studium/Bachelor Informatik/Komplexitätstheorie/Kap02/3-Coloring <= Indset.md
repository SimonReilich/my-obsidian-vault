---
lecture: "[[Komplexitätstheorie]]"
---
#BScInfo #Informatik #Comp
# Satz
$$\text{3-Coloring} \leq_p \text{Indset}$$

# Beweis
Wir wollen zeigen, dass sich [[3-Coloring]] auf [[Indset]] [[Karp-Reduktion in Polynomialzeit|reduzieren]] lässt:
- Reduktionsfunktion: Verdreifache den ursprünglichen [[Graph]] $G = (V, E)$ zu $G' = (V \times \{1, 2, 3\}, E')$ mit $E' = \{((v, i), (w, i)) \mid (v, w) \in E, i \in \{1, 2, 3\}\} \cup$ $\{((v, i), (v, j)) \mid v \in V, i \neq j \in \{1, 2, 3\}\}$ 
- Verifikation: $(V, E)$ ist 3-färbbar gdw. $(V \times{1, 2, 3}, E')$ ein [[stabile Menge]] der größe $|V|$ besitzt