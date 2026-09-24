---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs 
# Definition
Ein periodisches [[Signal]] s(t) lässt sich als Summe gewichteter [[Sinus]]- und [[Cosinus]]-Schwingungen darstellen. Die so entstehende Reihenentwicklung von s(t) bezeichnet man als Fourierreihe:
$$ s(t) = {a_0 \over 2} + \sum_{k = 1}^\infty (a_k * \cos(k \omega t) + b_k * \sin(k \omega t)) $$
Das $k$-te Summenglied bezeichnet man auch als $k$-te Harmonische. Das konstante Glied $a_0 /2$ repräsentiert eine Verschiebung der Signalamplitude bezüglich der Ordinate ($4$-Achse) und damit den konstanten Anteil der Funktion. Die Kreisfrequenz $ω = 2π/T$ stellt lediglich eine Normierung bezüglich der Periodendauer $T$ des Signals dar.

# Berechnung
Die Koeffizienten (Gewichte) $a_k$ und $b_k$ lassen sich wie folgt bestimmen:
$$ a_k = {2 \over T} \int_0^T s(t) * cos(k \omega t) \space dt $$
$$ b_k = {2 \over T} \int_0^T s(t) * sin(k \omega t) \space dt $$

# Einfache Signaleigenschaften
- [[Punktsymmetrie]] zu $(T/2, 0)$ => $a_0 = 0$, kein Gleichanteil
- $s(t)$ ist genau in Phase mit Cosinus => Sinus-Anteile ($b_k$) sind null
- $s(t)$ ist genau in Phase mit Sinus => Cosinus-Anteile ($a_k$) sind null

Für nicht kontinuierliche Signale: [[Foriertransformation]] 