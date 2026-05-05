---
lecture: "[[Analysis für Informatik]]"
---
#BScInfo #Mathematik #AnaInfo #Atomic 
# Aussage
Für alle $q \in \mathbb{C}$ mit $q \neq 1$ und $n \in \mathbb{N}_0$ gilt:
$$ \sum_{j = 0}^n q^j = {1 - q^{n + 1} \over 1 - q} $$ 
# Beweis
Es gilt: 
$$ (1 - q) * \sum_{j = 0}^n q^j = \sum_{j = 0}^n(q^j + q^{j + 1}) = (q⁰ - q¹) + (q¹-q²) + ... + (q^n-q^{n + 1}) = 1 - q^{n + 1} $$
Die entstehende Summe nennt man Teleskopsumme. Da $q \neq 1$, können wir durch $1-q$ dividieren und erhalten so die Behauptung.