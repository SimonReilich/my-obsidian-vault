---
lecture: "[[Komplexitätstheorie]]"
---
#BScInfo #Informatik #Comp
# Satz
Die Probleme [[SAT]] ist [[NP]]-vollständig.

# Beweis
Offensichtlicherweise gilt $\text{SAT} \in \textbf{NP}$, die Zuweisung der Atome ist ein polynomielles Zertifikat. Es bleibt noch zu zeigen, dass [[SAT]] [[NP]]-schwer ist, bzw. dass$$\forall L \in \textbf{NP}, L \leq_p \text{SAT}$$Da $L \in \textbf{NP}$ gibt es eine [[Turingmaschiene]] $M$ die in [[Laufzeit einer Turingmaschiene|Zeit]] $T(\cdot)$ läuft und ein [[Polynom]] $p$ sodass$$\forall x \in L, \exists u \in \{0, 1\}^{p(x)}, M(x, u) = 1 \iff x \in L$$Wir benötogen nun eine Funktion $x \mapsto \varphi_x$ sodass $x \in L \iff \varphi_x \in \text{SAT}$. Sei $M$ eine [[vergessliche Turingmaschiene]] (kann beliebige [[Turingmaschiene]] mit [[Polynom|polynomiellem]] Overhead simulieren) mit zwei Bändern. Führe $M$ nun für $T(n + p(n))$ Schritte auf $\left< 0^n, 0^{p(n)}\right>$ aus und speichere für jedes $i = 1, 2, ..., T(n + p(n))$ folgendes:
- $\mathrm{inputpos}(i)$: Position des Kopfes des Eingabebands nach $i$ Schritten
- $\mathrm{prev}(i)$: Vorheriger Schritt $j$ an dem sich der Kopf an der selben Position befunden hat (default $1$)
Da $M$ eine [[vergessliche Turingmaschiene]] ist, ist dies identisch für jede Eingabe $x, u$. Wir können nun Snapshots von $M$ im $i$-ten Schritt erstellen:$$z_i = \left<\text{state }q_i, \text{symbol at }\mathrm{inputpos}(i), \text{symbol in work head}\right>$$$$z_{i+1} = F(z_i, \text{input at }\mathrm{inputpos}(i+1), z_{\mathrm{prev}(i+1)})$$Mit deren Hilfe können wir nun wiefolgt eine Formel $\varphi_x = \varphi_1 \land \varphi_2 \land \varphi_3 \land \varphi_4$ erstellen:
- $\varphi_1$ kodiert die Eingabe $x$ (ohne Zertifikat $u$)
- $\varphi_2$ kodiert den ersten Spanshot $z_1 = \left<q_{Start}, \triangleright, \triangleright\right>$ 
- $\varphi_3 = \land \varphi_{3, i}$ stehen jeweils für den Snapshot $z_{i} = F(z_{i-1}, \text{input at }\mathrm{inputpos}(i), z_{\mathrm{prev}(i)})$ 
- $\varphi_4$ steht für den letzten Snapshot $z_{T(n+p(n))}$ mit Zustand $q_{halt}$ und der Ausgabe $1$
Die Länge von $\varphi$ ist [[Polynom|polynomiell]] in $n$, somit erhalten wir $L \leq_p \text{SAT}$ für beliebige $L \in \textbf{NP}$, somit ist [[SAT]] [[NP]]-vollständig.