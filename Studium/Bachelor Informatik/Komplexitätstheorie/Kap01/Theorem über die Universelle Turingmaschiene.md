---
lecture: "[[Komplexitätstheorie]]"
---
#BScInfo #Informatik #CoTheo
# Satz
Es gibt eine [[Turingmaschiene]] $\mathcal{U}$ sodass für jede $x, \alpha \in \{0, 1\}^*$ gilt:$$\mathcal{U}(x, \alpha) = M_\alpha(x)$$ Hält $M_\alpha$ auf $x$ in $T$ Schritten, so hält $\mathcal{U}(x, \alpha)$ in $O(T \log T)$ Schritten.