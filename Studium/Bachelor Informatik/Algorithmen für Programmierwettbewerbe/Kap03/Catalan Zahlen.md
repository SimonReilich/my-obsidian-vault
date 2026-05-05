---
lecture: "[[Algorithmen für Programmierwettbewerbe]]"
---
#BScInfo #Informatik #ConPra #Atomic 
# Definition
Die Catalan Zahlen lassen sich wie folgt berechnen: $C_n = {1 \over n + 1} (\begin{smallmatrix}2n \\ n\end{smallmatrix})$. Sie haben verschiedene Anwendungsbereiche, explizit seien genannt:
- Anzahl der wohlgeklammerten Wörter in $\{(, )\}^{2n}$ 
- Anzahl der verschiedenen Möglichkeiten, ein Produkt von $n + 1$ Zahlen durch Anwendung des [[Assioziativgesetz|Assoziativgesetzes]] zu berechnen
- Anzahl der Möglichkeiten, ein [[Konvex|konvexes]] [[Polygon]] mit $n + 2$ Vertecies ohne kreuzende Linien zu triangulieren

# Approximation
$$ C_n ~ \textasciitilde ~ {4^n \over \sqrt{\pi} * n^{3 / 2}} $$ 