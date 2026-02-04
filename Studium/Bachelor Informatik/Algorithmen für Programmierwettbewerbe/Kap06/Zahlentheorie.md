---
lecture: "[[Algorithmen für Programmierwettbewerbe]]"
slides:
  - "[[Zahlentheorie - Slides.pdf]]"
---
#Bachelor #Informatik #ConPra 
# Große Integer
- definiere Ziffern zur Basis $b$: $\Sigma_b = \{0, 1, ..., b - 1\}$ 
- Zahl kann dann als Liste von Ziffern dargestellt werden: $x = x_n x_{n-1} ... x_0$
- Wert: $(x)_b = \Sigma_{i = 0}^n x_i * b^i$ 
- Sind führende $0$-en verboten, führt das zu einer eindeutigen Darstellung positiver Zahlen
- Üblicherweise: wähle $b =$ `size(long)`/`size(int)`/...

# Rationale Zahlen
- Häufige Probleme von [[normalisierte t-Stellen Gleitkommazahl zur Basis B|Gleitkommazahlen]]: Rundungsfehler
- Speichere [[Rationale Zahlen]] als Bruch

# Multiplikation
- Gegeben sind $x = x_n...x_0$ und $y = y_m...y_0$, wir wollen $x * y$ effizient berechnen
- Naiver Ansatz: $x * y = \sum_{i = 0}^n \sum_{j = 0}^m x_i * y_j * b^{i + j}$, Laufzeit: $O(n^2)$
- Bessere Verfahren: [[Karatsuba-Algorithmus]], [[Toom-Cook-Algorithmus]]
- Logarithmische Laufzeit: [[FFT]]-basierte Verfahren: [[Algorithmus von Schönhage-Strassen]], [[Fürers Algorithmus]], [[Algorithmus von Harvey und van der Hoeven]] 

# Potenzen
- Klassischer Ansatz sehr langsam ($n$-mal multiplizieren)
- Zerlege Exponenten stattdessen in $2$er-Potenzen, können instantan als Bitshift ausgeführt werden