---
lecture: "[[Komplexitätstheorie]]"
---
#Bachelor #Informatik #CoTheo
# Definition
Eine $k$-Band [[Turingmaschiene]] ist ein Tripel $(\Gamma, Q, \delta)$ mit
- dem [[Alphabet]] $\Gamma$ bestehend aus $0$, $1$, $\square$ (leere Zelle) und $\rhd$ (Startsymbol)
- der Zustandsmenge $Q$, die die Zustände $q_{Start}$ und $q_{Halt}$ beinhaltet
- der Transitionsfunktion $\delta: Q \times \Gamma^k \to Q \times \Gamma^{k - 1} \times \{l, n, r\}^k$ mit $\delta(q_{Halt}, \vec)$