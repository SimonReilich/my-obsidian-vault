---
lecture: "[[Analysis für Informatik]]"
---
#Bachelor #Informatik #AnaInfo #Atomic 
# Beweis
Angenommen, $\mathbb{R}$ wäre abzählbar. Dann wäre auch das [[Intervall]] $[0; 1]$ abzählbar und es gäbe somit eines [[surjektiv|surjektive]] Abbildung $f: \mathbb{N} \to [1; 0]$. Seien
$$ 
\begin{matrix}
	f(1) = 0,d_{1,1} d_{1,2} d_{1,3} ... \\
	f(2) = 0,d_{2,1} d_{2,2} d_{2,3} ... \\
	f(3) = 0,d_{3,1} d_{3,2} d_{3,3} ... \\
	...
\end{matrix}$$ die entsprechenden Dezimaldarstellungen. Deffiniere $x = 0,d_1 d_2 d_3 ... \in [0; 1]$ durch
$$ d_i = \begin{cases} 0 & \text{falls } d_{i, i} = 9 \\ d_{i, i} + 1 & \text{sonst} \end{cases} $$
Dan ist $\forall i: d_i \neq d_{i, i}$ und daher $\nexists i : f(i) = x$. Damit wäre $x$ nicht [[surjektiv]], was einen Wiederspruch ergibt.