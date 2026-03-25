---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs #Atomic 
# Definition
Wenn mehrere [[Signal|Signale]] gleichzeitig gesendet werden sollen, steht nur ein begrenztes Spektrum zur Verfügung. Dazu wird das Basisbandsignal [[Tiefpass|tiefpass-gefiltert]] (Begrenzung des Spektrums) und auf ein Trägersignal moduliert (Verschiebung des Spektrums).

# Ablauf
- Die Sendeimpulse g(t) werden mittels Tiefpassfilterung auf eine maximale Frequenz $f_{max}$ beschränkt. Die so gefilterten Impulse bezeichnen wir als $g_T (t)$.
- Das ebenfalls bandbegrenzte Sendesignal $s_T (t)$ wird auf ein Trägersignal der Frequenz $f_0$ aufmoduliert:
$$s(t) = s_T(t) * cos(2 \pi f_0 t) = (\sum_{n =1}^{\infty}d_n * g_T(t-nT)) * cos(2 \pi f_0 t)$$ ![[Modulation.png]]

# Modulationsverfahren
- [[Amplitude Shift Keying]]
- [[Quadratur-Amplituden-Modulation]] 