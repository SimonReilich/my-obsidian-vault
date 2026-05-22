---
lecture: "[[Komplexitätstheorie]]"
---
#BScInfo #Informatik #Comp
# Definition
Sein $T: \mathbb{N} \to \mathbb{N}$ eine [[zeitkonstruierbare Funktion]]. Eine [[formale Sprache]] $L \subseteq \{0, 1\}^*$ ist Element von $\textbf{DTIME}(T)$ wenn es eine [[Turingmaschiene]] gibt, die $L$ in der [[Laufzeit einer Turingmaschiene|Zeit]] $T' \in O(T)$ entscheidet.