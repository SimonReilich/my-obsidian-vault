---
lecture: "[[Analysis für Informatik]]"
---
#BScInfo #Mathematik #AnaInfo #Atomic 
# Aussage
Für die drei [[Konvergenz|konvergenten]] [[Folge|Folgen]] $(a_n)_{n \in \mathbb{N}}, (b_n)_{n \in \mathbb{N}}, (c_n)_{n \in \mathbb{N}}$ gelte $\exists n_0 \in \mathbb{N} : \forall n \geq n_0 : a_n \leq b_n \leq c_n$. Falls ein $\alpha \in \mathbb{R}$ existiert mit $\lim_{n \to \infty} a_n = \alpha = \lim_{n \to \infty} c_n$, dann gilt auch $\lim_{n \to \infty} b_n = \alpha$.

# Beweis
Sei $\epsilon > 0$. Nach Voraussetzung gilt:
$$ ∃n_1 ∈ \mathbb{N} : ∀n ≥ n_1 |a_n − α| < ε/
3 $$
$$ ∃n_2 ∈ \mathbb{N} : ∀n ≥ n_2 : |c_n − α| < ε
/3 $$
Sei $n_0 = \max\{n_1, n_2\}$ und $n \geq n_0$. Dann gilt:
$$ |b_n − α| ≤ |b_n − a_n | + |a_n − α| < |b_n − a_n | + ε/3 $$
Weiter gilt:
$$ |b_n − a_n | = b_n − a_n ≤ c_n − a_n = |c_n − a_n | ≤ |c_n − α| + |α − a_n | < ε
/3 + ε
/3 $$
Einsetzen für alle $n \geq n_0$ liefert $|b_n - \alpha| < \epsilon / 3$ 