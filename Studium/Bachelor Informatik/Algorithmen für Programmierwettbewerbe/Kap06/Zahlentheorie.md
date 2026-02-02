---
lecture: "[[Algorithmen für Programmierwettbewerbe]]"
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