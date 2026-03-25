---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs #Atomic 
# Definition
- Diskretisierung eines [[Signal|Signals]] im Zeitbereich.

# Rekonstruktion
- Mittels der Abtastwerte $s[n]$ ist es möglich, das ursprüngliche [[Signal]] $s(t)$ zu rekonstruieren:
$$ s(t) \approx \sum_{n = - \infty}^\infty s[t] * sinc({t - nT_a \over T_a}) $$
- ($sinc(x) = {\sin(\pi x) \over \pi x}$; $T_a$ ist das Abtastintervall)
- Wann ist verlustfreie Rekonstruktion möglich? => [[Abtasttheorem von Shannon und Nyquist]]
- Wählt man $f_a < 2B$, so überlappen sich die periodischen Wiederholungen des Spektrums
- Diesen Effekt bezeichnet man als Aliasing
- Eine verlustfreie Rekonstruktion ist in diesem Fall nicht möglich

![[Abgetastetes Signal.png]]