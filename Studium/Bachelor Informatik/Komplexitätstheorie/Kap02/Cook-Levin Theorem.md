---
lecture: "[[Komplexitätstheorie]]"
---
#BScInfo #Informatik #Comp
# Satz
Die Probleme [[SAT]] und [[3SAT]] sind beide [[NP]]-vollständig.

# Beweis für [[SAT]]
Offensichtlicherweise gilt $\text{SAT} \in \textbf{NP}$, die Zuweisung der Atome ist ein polynomielles Zertifikat. Es bleibt noch zu zeigen, dass [[SAT]] [[NP]]-schwer ist, bzw. dass$$\forall L \in \textbf{NP}, L \leq_p \text{SAT}$$Da $L \in \textbf{NP}$ gibt es eine [[Turingmaschiene]] $M$ die in [[Laufzeit einer Turingmaschiene|Zeit]] $T(\cdot)$ läuft und ein [[Polynom]] $p$ sodass$$\forall x \in L, \exists u \in \{0, 1\}^{p(x)}, M(x, u) = 1 \iff x \in L$$Wir benötogen nun eine Funktion $x \mapsto \varphi_x$ sodass $x \in L \iff \varphi_x \in \text{SAT}$. Sei $M$ eine [[vergessliche Turingmaschiene]] (kann beliebige [[Turingmaschiene]] mit [[Polynom|polynomiellem]] Overhead simulieren) mit zwei Bändern. Führe $M$ nun für $T(n + p(n))$ Schritte auf $\left< 0^n, 0^{p(n)}\right>$ aus und speichere für jedes $i = 1, 2, ..., T(n + p(n))$ folgendes:
- $\mathrm{inputpos}(i)$: Position des Kopfes des Eingabebands nach $i$ Schritten
- $\mathrm{prev}(i)$: Vorheriger Schrit