---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs 
# Kodierungsvorschrift
- [[Sendeimpuls]] $g(t) = rect (t)$ mit Periodendauer $T$
- Mögliche Zuweisung der Gewichte $d_n = \begin{cases} 1 & b_n = 1 \\ −1 & b_n = 0 \end{cases}$
- Sendesignal ist definiert als $s(t) = \sum^\infty_{n=1} d_n * g(t − nT)$ 

# Eigenschaften
- Binärer Code (lediglich zwei Signalstufen)
- Effizienz 1 [[Symbol]] pro bit
- Keine [[Taktrückgewinnung]]
- Keine [[Gleichstromfreiheit]]
- Relativ breites Spektrum