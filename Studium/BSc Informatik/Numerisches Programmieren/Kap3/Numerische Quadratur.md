---
lecture: "[[Numerisches Programmieren]]"
---
#Bachelor #Informatik #NumProg 

# Numerische Integration

- Numerische Quadratur: Berechnung eines definitiven [[Integral|Integrals]] $I(f) := \int_{\Omega} f(x) \space dx$ mit der Funktion $f: \mathbb{R}^d \supseteq \Omega \to \mathbb{R}$ (integrand) und der Integrationsdomäne $\Omega$ 
- Im folgenden: univariante Quadratur ($d = 1$)
- Häufige Form für regeln: $I(f) \approx Q(f) := \sum_{i = 0}^n g_if(x_i) = \sum_{i = 0}^n g_iy_i$
- Idee: Exakte Integration von Interpoliertem Polynom: [[Integration mit Lagrange Polynomen]] 
- [[Kondition]]: Gut, wenn nur positive Gewichte genutzt werden

# Einfache und Zusammengesetzte Regeln

- Einfache Regeln: [[Rechteckregel]], [[Trapezregel]], [[Keplers Regel]], [[Newton-Cotes Formels]] und [[Clenshwa-Crutis Formeln]] 
- Zusammengesetzte Regeln: [[Trapezsumme]] und [[Simpson Summe]] 

# Extrapolation


- Kombiniert man Schätzungen niedrigerer Ordnung, erhält man eine Schätzung höherer Ordnung
- Diese Idee wird von der [[Romberg-Quadratur]] genutzt

# Andere Verfahren

- [[Monte-Carlo Quadratur]], [[Gauss Quadratur]], [[Archimedes Quadratur]] 