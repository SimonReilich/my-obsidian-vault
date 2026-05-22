---
lecture: "[[Komplexitätstheorie]]"
---
#BScInfo #Informatik #Comp
# Definition
Eine $k$-Band [[Turingmaschiene]] ist ein Tripel $(\Gamma, Q, \delta)$ mit
- dem [[Alphabet]] $\Gamma$ bestehend aus $0$, $1$, $\square$ (leere Zelle) und $\rhd$ (Startsymbol)
- der Zustandsmenge $Q$, die die Zustände $q_{Start}$ und $q_{Halt}$ beinhaltet
- der Transitionsfunktion $\delta: Q \times \Gamma^k \to Q \times \Gamma^{k - 1} \times \{l, n, r\}^k$ mit $\delta(q_{Halt}, \vec{\sigma}) = (q_{Halt}, \vec{\sigma}_{2...k}, \vec{n})$ 
Sei $x \in (\Gamma \setminus \{\square, \rhd\})^*$  die Eingabe der [[Turingmaschiene]] $M$ und $f: \{0, 1\}^* \to \{0, 1\}^*$ eine Funktion. Die Startkonfiguration von $M$ ist $\rhd x \square^\omega$ auf dem Eingabeband und $\rhd \square^\omega$ auf allen anderen $k - 1$ Bändern. Alle Köpfe befinden sich auf $\rhd$, $M$ befindet sich im Zustand $q_{Start}$. Befindet sich $M$ im Zustand $q$, die Symbole $(\sigma_1, ..., \sigma_k)$ werden gelesen und $\delta(q, \vec{sigma}) = (q', \vec{\sigma}'_{2..k}, \vec{d})$, so geht $M$ in den Zustand $q'$ über, ersetzt $\sigma_{2..k}$ mit $\sigma'_{2..k}$ und bewegt den Kopf auf dem $k$-ten Band entsprechend dem Wert von $\vec{d}_k$. Die [[Turingmaschiene]] hält, sobald sie den Zustand $q_{Halt}$ erreicht hat. Sie berechnet die Funktion $f$, wenn sie auf jeder Eingabe $x$ hält und $f(x)$ auf dem Ausgabeband steht.