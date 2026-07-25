---
lecture: "[[Petrinetze]]"
---
#BScInfo #Informatik #Petri 
# Satz
Seien $M, M'$ und $L$ beliebige [[Markierung|Markierungen]] eines [[Netz|Netzes]]. Dann gilt:
1. Falls $M \overset{\sigma}{\to} M'$ für eine endliche [[Schaltsequenz]] $\sigma$, dann auch $(M + L) \overset{\sigma}{\to} (M' + L)$ 
2. Falls $M \overset{\sigma}{\to}$ für eine unendliche [[Schaltsequenz]] $\sigma$, dann auch $(M + L) \overset{\sigma}{\to}$ 

# Beweis (1)
Wir beweisn die Aussage durch Induktion über die Länge der Schaltsequenz $\sigma$:
Induktionsanfang: Die einzige [[Schaltsequenz]] mit Länge 0 ist die leere [[Folge]]. Diese ist immer schaltbereit, das Lemma gilt.
Induktionsschritt: Sei $\sigma = \tau t$

# Beweis (2)