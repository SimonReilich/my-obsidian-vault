---
lecture: "[[Analysis für Informatik]]"
---
#Bachelor #Informatik #AnaInfo #Atomic 
# Archimedisch
$\mathbb{R}$ ist archimedisch, dass heißt, für alle $a \in \mathbb{R}$ existiert ein $n \in \mathbb{N}$ mit $a < n$. Insbesondere gibt es keine unendlich großen Zahlen in $\mathbb{R}$.

# Beweis
Angenommen, es gilt nicht $\forall a \in \mathbb{R} : \exists n \in \mathbb{N}$ mit $a < n$, dann gilt die Negation $\exists a \in \mathbb{R} : \forall n \in \mathbb{N} : a \geq n$, $\mathbb{N}$ wäre also in $\mathbb{R}$ nach oben beschränkt. Sei $s$ das [[Supremum]] von $\mathbb{N}$. Da $s$ die kleinste obere Schranke ist, ist $s - 1$ keine obere [[Schranke]] von $\mathbb{N}$, dass heißt: 
$$ \exists n \in \mathbb{N} : s - 1 \leq n \implies s \leq n + 1 \text{ wobei } n \in \mathbb{N} $$
Somit ist $s$ keine obere [[Schranke]] von $\mathbb{N}$, was ein Wiederspruch ist.

# Folgerung
Sei $a > 0$. Dann ist $1 \over a > 0$. Da $\mathbb{R}$ archimedisch ist, existiert $n \in \mathbb{N}$ mit
$$ {1 \over a} < n \implies {1 \over n} < a $$
Somit gibt es keine unendlich kleinen oder großen Zahlen in $\mathbb{R}$.