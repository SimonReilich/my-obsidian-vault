---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs #Atomic 
# Kodierungsvorschrift
- [[Sendeimpuls]] $g(t) = rect (2t + {T \over 2}) - rect(2t - {T \over 2})$ mit Periodendauer $T$
- Mögliche Zuweisung der Gewichte $d_n = \begin{cases} 1 & b_n = 1 \\ −1 & b_n = 0 \end{cases}$
- Sendesignal ist definiert als $s(t) = \sum^\infty_{n=1} d_n * g(t − nT)$ 

# Eigenschaften
- Binärer Code (lediglich zwei Signalstufen)
- Effizienz 2 [[Symbol]] pro bit
- [[Taktrückgewinnung]] durch erzwungenen Pegelwechsel einfach
- [[Gleichstromfreiheit]] gewährleistet, da jeder Grundimpuls gleichstromfrei ist
- sehr breites und langsam abklingendes Spektrum