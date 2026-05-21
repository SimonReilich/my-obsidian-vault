---
lecture: "[[Numerisches Programmieren]]"
degree: "[[Bachelor Informatik]]"
---
#BScInfo #Informatik #NumProg 

# Differentialgleichungen

- Siehe [[Differentialgleichungen]] 
- Zwei Arten: [[gewöhnliche Differenzialgleichungen]] und [[partielle Differenzialgleichungen]] 
- Je nach Bedingungen handelt es sich um ein [[Initialwertproblem]] oder ein [[Randwertproblem]] 
- Analytische Lösung: [[Trennung der Variablen]] 
- [[Kondition]] ist abhängig von der [[Differentialgleichungen|Differenzialgleichung]], im schlimmsten Fall verhält sich schon bei kleinen Fehlern das Ergebnis völlig anders als die eigentliche Lösung

# Annäherung mit endlichen Differenzen

- [[Eulers Methode]]
- [[Methode von Heun]] 
- [[Methode von Runge und Kutta]] 
- Definition [[lokaler Diskretisierungsfehler]] und [[globaler Diskretisierungsfehler]] 
- Andere Möglichkeit: Mehrschrittverfahren, z.B. [[Adams-Bashforth Methode zweiter Ordnung]] 

# Steife Probleme

- Konsistenz, [[Konvergenz]] und [[Stabilität]] können sich asymptotisch verhalten
- Global "unwichtige" Teilterme können trotzdem dazu führen, dass eine extrem feine Auflösung benötigt wird
- Definition [[implizite Methoden]]
- Algorithmus: [[Impliziter Euler]]