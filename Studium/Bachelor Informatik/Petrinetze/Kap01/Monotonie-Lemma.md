---
lecture: "[[Petrinetze]]"
---
#BScInfo #Informatik #Petri 
# Satz
Seien $M, M'$ und $L$ beliebige [[Markierung|Markierungen]] eines [[Netz|Netzes]]. Dann gilt: Falls $M \overset{\sigma}{\to} M'$ für eine endliche [[Schaltsequenz]] $\sigma$, dann auch $(M + L) \overset{\sigma}{\to} (M' + L)$.

# Beweis
Wir beweisn die Aussage durch Induktion über die Länge der Schaltsequenz $\sigma$:
Induktionsanfang: Die einzige [[Schaltsequenz]] mit Länge 0 ist die leere [[Folge]]. Diese ist immer schaltbereit, das Lemma gilt.
Induktionsschritt: Sei $\sigma = \tau t$, so dass $M \overset{\tau}{\to} M'' \overset{t}{\to} M'$. Nach Induktionshypothese gilt das Monotonie-Lemma für die Sequenz $\tau$: $(M + L) \overset{\tau}{\to} (M''+L)$. Durch die Definition des Schaltvorgangs und $M'' \overset{t}{\to} M'$ erhalten wir $(M'' + L) \overset{t}{\to} (M' + L)$ und damit auch $(M + L) \overset{\tau t}{\to} (M' + L)$.