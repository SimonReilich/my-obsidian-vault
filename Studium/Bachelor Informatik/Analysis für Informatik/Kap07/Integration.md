---
lecture: "[[Analysis für Informatik]]"
---
#Bachelor #Informatik #AnaInfo 
# Das Integral
- Problem: Bestimmung des Flächeninhalts unter einer Kurve
- Idee: Zerlegung $Z$ in kleine Rechtecke $[x_i, x_{i + 1}]$ 
- Feinheit $|Z| = \max_{1 \leq i \leq n}|x_i - x_{i - 1}|$ 
- Definition [[Riemann-Summe]]
- Wählt man [[Folge]] $Z_n, n \in \mathbb{N}$, sodass $|Z_n| \to_{n \to \infty} 0$, erhält man durch den Grenzwert der [[Riemann-Summe]] den Flächeninhalt (bei den meisten Funktionen), die Funktion heißt dann [[Riemann-integrierbar]] 

# Eigenschaften des Integrals
- [[Eigenschaften des Integrals für allgemeine Integranden]]
- Jede stetige Funktion ist [[Riemann-integrierbar]]
- [[Mittelwertsatz der Integralrechnung]] 

# Stammfunktionen
- [[Hauptsatz der Differential- und Integralrechnung]] definiert Integration als Umkehr der Differentiation
- Nützlicher Trick: [[Partialbruchzerlegung]], [[Partielle Integration]]
- [[Substitutionsregel]], [[Skalierungsregel]] 

# Parameterabhängige Integrale
- Definition der [[partielle Ableitung|partiellen Ableitung]] 
- Es gilt der [[Satz von Fubin]], Differentiation und Integration dürfen vertauscht werden
- Gibt es eine konvergente [[Majoranten- und Minorantenkriterium|Majorante]] $a_k$ für $f_k$, so gilt $\int_a^b \sum_{k = 1}^\infty f_k(x) dx = \sum_{k = 1}^\infty \int_a^b f_k(x) dx$ 
- Nützlich für Funktionen, die als [[Potenzreihe]] dargestellt werden
- [[Integralkriterium für die Konvergenz von Reihen]]