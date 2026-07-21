---
lecture: "[[Komplexitätstheorie]]"
---
#BScInfo #Informatik #Comp
# Definition
Eine $k$-Band-Turingmaschine ist formal definiert als ein Tripel $(\Gamma, Q, \delta)$ mit den folgenden Komponenten:
- $\Gamma$ ([[Alphabet|Bandalphabet]]): Eine endliche Menge von Band-Symbolen. Es enthält mindestens $\{0, 1, \square, \triangleright\}$, wobei $\square$ für eine leere Zelle (blank) und $\triangleright$ für das Startsymbol steht.
- $Q$ (Zustandsmenge): Eine endliche Menge von Zuständen zur Steuerung, welche unter anderem die ausgezeichneten Zustände $q_{\text{start}}$ (Startzustand) und $q_{\text{halt}}$ (Haltezustand) enthält.
- $\delta$ (Transitionsfunktion): Eine Funktion, welche die Zustandsübergänge und Schreib-/Leseaktionen regelt:$$\delta: Q \times \Gamma^k \rightarrow Q \times \Gamma^{k-1} \times \{l, s, r\}^k$$
# Funktionsweise der Transitionsfunktion $\delta$
Die Übergangsfunktion liest den aktuellen Zustand sowie die Symbole unter den $k$ Lese-/Schreibköpfen ($\Gamma^k$). Sie liefert als Ergebnis:
1. Den folgenden Zustand aus $Q$.
2. Die neu zu schreibenden Symbole auf den $k-1$ verbleibenden Bändern ($\Gamma^{k-1}$). (Das erste Band ist das schreibgeschützte Eingabeband und wird nicht überschrieben.)
3. Die Bewegungsrichtungen $\{l, s, r\}^k$ für jeden der $k$ Köpfe, wobei:
    - $l$ = links
    - $s$ = stehen bleiben
    - $r$ = rechts

# Haltebedingung
Für den Haltezustand $q_{\text{halt}}$ gilt per Definition, dass keine weiteren Inhaltsänderungen auf den Bändern vorgenommen werden und die Köpfe in ihrer Position verharren:
$$\delta(q_{\text{halt}}, \vec{\sigma}) = (q_{\text{halt}}, \vec{\sigma}_{2..k}, \vec{s})$$
wobei $\vec{\sigma}_{2..k} = (\sigma_2, \dots, \sigma_k)$ die gelesenen Symbole auf den Bändern $2$ bis $k$ bezeichnet und $\vec{s} = (s, \dots, s)$ bedeutet, dass alle Köpfe auf ihrer Position stehen bleiben.