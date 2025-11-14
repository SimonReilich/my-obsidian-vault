---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs 

# Kodierungsvorschrift

- [[Sendeimpuls]] $g(t) = rect (2t + {T \over 2}) - rect(2t - {T \over 2})$ mit Periodendauer $T$
- Gewichte $d_n = \sin( {\pi \over 2} \sum_{k = 1}^n b_k )$ (abhängig von Anzahl der bisher beobachteten 1er bits)
- Sendesignal ist definiert als $s(t) = \sum^\infty_{n=1} d_n * g(t − nT)$ 

# Eigenschaften

- Ternärer Code (lediglich zwei Signalstufen)
- Effizienz 1 [[Symbol]] pro bit
- keine [[Taktrückgewinnung]] möglich
- keine [[Gleichstromfreiheit]] 
- Schmales Spektrum, da die Grundperiode durch den periodischen Signalverlauf reduziert wird