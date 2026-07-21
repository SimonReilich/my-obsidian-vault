---
lecture: "[[Komplexitätstheorie]]"
---
#BScInfo #Informatik #Comp
# Definition
Seien $L, L' \subseteq \{0, 1\}^*$ zwei [[formale Sprache|formale Sprachen]]. Dann ist $L$ polynomzeit-karp-reduzibel auf $L'$ wenn es eine in [[Polynom|polynomieller]] Zeit berechenbare Funktion $f: \{0, 1\}^* \to \{0, 1\}^*$ gibt, sodass für alle $x \in \{0, 1\}^*$ gilt:$$x \in L \iff f(x) \in L'$$Man schreibt $L \leq_p L'$ 