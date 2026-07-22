---
lecture: "[[Analysis für Informatik]]"
---
#BScInfo #Mathematik #AnaInfo 
# Definition
Eine komplexe [[Folge]] $(a_n)_{n \in \mathbb{N}_0}$ konvergiert gegen $a \in \mathbb{C}$, falls für jede Genauigkeit $\epsilon > 0$ ein $n_0 \in \mathbb{N}$ existiert, sodass für alle $n > n_0$ gilt:
$$ |a_n - a| < \epsilon $$
Man schreibt $\lim_{n \to \infty} a_n = a$. Gibt es für eine [[Folge]] keinen Grenzwert, heißt sie divergent.

# Rechenregeln
Falls $\lim_{n \to \infty} a_n = a \in \mathbb{R}$ und $\lim_{n \to \infty} b_n = b \in \mathbb{R}$, so gilt auch:
1. $\lim_{n \to \infty} (a_n + b_n) = a + b$
2. $\lim_{n \to \infty}ca_n = ca$ für alle $c \in \mathbb{R}$
3. $\lim_{n \to \infty}a_n b_n = ab$
4. $\lim_{n \to \infty} {a_n \over b_n} = {a \over b}$, falls $b \neq 0$ 