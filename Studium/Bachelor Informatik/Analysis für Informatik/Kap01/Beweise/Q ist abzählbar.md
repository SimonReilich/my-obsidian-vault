---
lecture: "[[Analysis für Informatik]]"
---
#Bachelor #Informatik #AnaInfo #Atomic 
# Beweis
Man kann eine [[Abzählbarkeit|Abzählung]] $f: \mathbb{N} \to \mathbb{Q}$ mit Hilfe eines Diagonalarguments angeben:
$$ \begin{matrix}  
     & 1 & & 2 & & 3 & & ... \\  
   1 & 1 \over 1 & → & 2 \over 1 & & 3 \over 1 & → \\ 
     & & ↙ & & ↗ & & ↙ \\
   2 & 1 \over 2 & & 2 \over 2 & & 3 \over 2 \\ 
     & ↓ & ↗ & & ↙ & & ↗ \\
   3 & 1 \over 3 & & 2 \over 3 & & 3 \over 3 \\ 
     & & ↙ & & ↗ \\
   ...
\end{matrix} $$
