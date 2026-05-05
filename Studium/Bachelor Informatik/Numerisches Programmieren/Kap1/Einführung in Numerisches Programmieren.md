---
lecture: "[[Numerisches Programmieren]]"
---
#BScInfo #Informatik #NumProg
# Was ist Numerik?

- Unterscheidung: [[Numerische Mathematik]], [[Numerische Programmierung]] und [[Numerische Simulation]]
- Mögliche Anwendungen von numerischen Methoden: [[Geometrische Modellierung]], [[Computergrafik]], [[Bildverarbeitung]], [[HPC]], [[Spielentwicklung]] und [[Maschinelles Lernen]] 
- Zentrales Prinzip: [[Diskretisierung]] 

# Gleitkommazahlen und Rundung

- Um Zahlen in einem Computer darstellen zu können ist nicht nur [[Diskretisierung]], sondern auch Begrenzung wichtig, es können nicht beliebig große Zahlenwerte dargestellt werden.
- Definition [[Fixpunktarithmetik]] und [[Gleitkommaarithmetik]]
- Definition der [[normalisierte t-Stellen Gleitkommazahl zur Basis B|normalisierten t-Stellen Gleitkommazahlen zur Basis B]] und der davon abgeleiteten [[Maschinenzahlen]]
- [[Maschinenzahlen]] sind sowohl diskret als auch endlich => von Computern darstellbar
- In heutigen Systemen wird der IEEE 754 Standard [[binary32]] am häufigsten verwendet
- Definition [[Rundung]] und [[Relativer Rundungsfehler]] 
- Definition [[Ideale Arithmetik]] und [[Maschinengenauigkeit]] 
- Probleme: [[Assoziativität]] geht verloren, [[Auslöschung]]

# Analyse von Rundungsfehlern

- Mögliche Taktiken: [[Vorwärtsanalyse]] und [[Rückwärtsanalyse]]
- Beispiel: [[Horner Schema]] 
- Definition [[Kondition]] und [[Stabilität]] 