---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs 
# Definition
- Diskretisierung eines [[Signal|Signals]] im Wertebereich
- Die Unterscheidung von $M = 2N$ Signalstufen erfordert Codewörter von $N$ bit
- Jeder Signalstufe wird dabei ein bestimmtes Codewort zugeordnet 
- Die Signalstufen werden im Quantisierungsintervall $I_Q = [a,b]$ „sinnvoll“ verteilt
- Was ist „sinnvoll“?

# Zuweisung
- Die Zuweisung von Codewörtern zu Signalstufen ist im Prinzip willkürlich
- Häufig wählt man jedoch einen Code, welcher die Auswirkung einzelner Bitfehler reduziert (z. B. Gray-Code: Benachbarte Codewörter unterscheiden sich nur in jeweils einer binären Ziffer, d. h. die [[Hamming-Distanz]] ist 1)

![[Quantisiertes Signal.png]]