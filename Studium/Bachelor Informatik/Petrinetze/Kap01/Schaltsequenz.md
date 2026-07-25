---
lecture: "[[Petrinetze]]"
---
#BScInfo #Informatik #Petri
# Definition 
Sei $N = (S, T, F)$ ein [[Netz]] und sei $M$ eine [[Markierung]] von $N$. Eine endliche [[Folge]] $\sigma = t_1 ... t_n$ ist schaltbereit, wenn es [[Markierung|Markierungen]] $M_1, ..., M_{n + 1}$ gibt, sodass $M_1 \overset{t_1}{\to} ... \overset{t_n}{\to} M_{n+1}$, wir schreiben $M_1 \overset{\sigma}{\to} M_{n + 1}$. Die leere Schaltsequenz $\epsilon$ ist immer schaltbereit. Eine unendliche [[Folge]] $\sigma = t_1, t_2 ...$ ist schaltbereit, wenn es [[Markierung|Markierungen]] $M_1, M_2, ...$ gibt, sodass $M \overset{t_1}{\to} M_2 \overset{t_2}{\to} ...$. Die leere Schaltsequenz $\epsilon$ ist immer schaltbereit. 