---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs  
# Urheber
Von [[Wladimir Kotelnikow]], [[Claude Elwood Shannon]]
Beeinflusst durch [[Harry Nyquist]], [[Edmund Taylor Whittaker]], [[John Macnaghten Whittaker]], [[Karl Küpfmüller]] 

# Theorem
Ein auf $|f | ≤ B$ bandbegrenztes [[Signal]] $s(t)$ ist vollständig durch äquidistante Abtastwerte $s[n]$ beschrieben, sofern diese nicht weiter als $T_a ≤ 1/2B$ auseinander liegen. Die Abtastfrequenz, welche eine vollständige Signalrekonstruktion erlaubt, ist folglich durch $f_a > 2B$ nach unten beschränkt.

# Nyquist Rate
Sei $B$ die Grenzfrequenz eines bandbegrenzten Kanals. Dann ist die Nyquist-Rate $f_N = 2B$
- eine untere [[Schranke]] für die minimale Abtastrate, die eine vollständige Rekonstruktion des [[Signal|Signals]] erlaubt,
- eine obere [[Schranke]] für die Anzahl an [[Symbol|Symbolen]] je Zeiteinheit, die nach der Übertragung über den Kanal unterscheidbar sind.