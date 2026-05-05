---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs #Atomic 
# QAM
- Man kann [[Sinus- und Cosinusfunktion|Sinus- und Cosinus]]-förmige Trägersignale mischen
- Trennung durch Orthogonalität von [[Sinus- und Cosinusfunktion|Sinus und Cosinus]] möglich
- Der Cosinus wird als Inphase-Anteil, der Sinus als Quadratur-Anteil bezeichnet
- Die Datenrate lässt sich auf diese Weise verdoppeln
$$ s(t) = (\sum_{n = 1}^\infty d_{In} * g_T(t - nT)) * cos(2 \pi f_0 t) - (\sum_{n = 1}^\infty d_{Qn} * g_T(t - nT)) * sin(2 \pi f_0 t) $$ 