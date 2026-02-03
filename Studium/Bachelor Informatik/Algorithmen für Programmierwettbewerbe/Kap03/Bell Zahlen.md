---
lecture: "[[Algorithmen für Programmierwettbewerbe]]"
---
#Bachelor #Informatik #ConPra 
# Definition
Die Bell-Zahlen $B_n$ bezeichnen die Anzahl möglicher Partitionen von $[n]$. Sie Lassen sich mithilfe der [[Stirlingzahlen zweiter Art]] berechnen: $\sum_{k = 0}^n S_{n, k} = B_n$ 

# Approximation
$$ B_n ~ \textasciitilde ~ {1 \over \sqrt{n}} ({n \over W(n)})^{n + 0,5} e^{{n \over W(n)}-n-1} $$ Wobei $W(n)$ die sogenannte [[Lambert-W-Funktion]] ist.