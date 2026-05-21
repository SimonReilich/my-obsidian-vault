---
lecture: "[[Petrinetze]]"
---
#BScInfo #Informatik #Petri
# Definition
Ein Netz $N = (S, T, F)$ besteht aus
- Der endlichen Menge $S$ von Stellen, dargestellt als Kreise
- Der endlichen Menge $T$ von Transitionen ($S \cap T = \emptyset$), dargestellt als Rechtecke
- Der Menge $F \subseteq (S \times T) \cup (T \times S)$ von Bögen, dargestellt als Pfeile
Stellen und Transitionen werden gemeinsam auch als Knoten oder Elemente bezeichnet
Für ein beliebiges $x \in S \cup T$ sei$$\cdot x = \{y \mid (y, x) \in T\}, x \cdot = \{y \mid (x, y) \in T\}$$ Für eine Menge $X \subseteq S \cup T$ gilt $\cdot X = \cup_{x \in X} \cdot x$ und $X\cdot = \cup_{x \in X} x\cdot$ 

# Beispiel
$$S = \{s_ 1, ..., s_6\}, T = \{t_1, ..., t_4\}$$$$F = {(s_1 , t_1 ), (t_1 , s_2 ), (s_2 , t_2 ), (t_2 , s_1 ),
(s_3 , t_2 ), (t_2 , s_4 ), (s_4 , t_3 ), (t_3 , s_3 ),
(s_5 , t_3 ), (t_3 , s_6 ), (s_6 , t_4 ), (t_4 , s_5 )}$$ ![[Netz Beispiel.png]]
