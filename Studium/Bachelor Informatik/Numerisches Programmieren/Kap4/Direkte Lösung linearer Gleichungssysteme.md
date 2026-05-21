---
lecture: "[[Numerisches Programmieren]]"
degree: "[[Bachelor Informatik]]"
---
#BScInfo #Informatik #NumProg 

# Lineare Gleichungssysteme

- möglichst schnelles und effizientes lösen von [[Linearen Gleichungssysteme|Linearen Gleichungssystemen]] 
- Aufgabe: finde $x \in \mathbb{R}^n$ für $A * x = b$ mit $A \in \mathbb{R}^{n \times n}, b \in \mathbb{R}^n$ 
- Nötig für viele Bereiche der [[Numerische Programmierung|Numerischen Programmierung]]: [[Interpolation]], [[gewöhnliche Differenzialgleichungen]], [[partielle Differenzialgleichungen]], ...
- Verschiedene Arten der Struktur von Matrizen: [[Dicht besetzte Matrizen|dicht / voll]] oder [[Dünn besetzte Matrizen|dünn]] besetzt
- Zwei verschiedene Lösungsansätze: [[Direkte Löser|direkt]] und [[Indirekte Löser|indirekt]] 
- Häufigster Algorithmus: [[Gausselimination]] 

# Andere Algorithmen

- [[LR-Zerlegung]], [[Cholesky-Faktorisierung]] 
- geeigneter, wenn selbes Gleichungssystem mehrmals für verschiedene $b \in \mathbb{R}^n$ gelöst werden muss

# Pivotisierung

- Bisherige Annahme für die [[Gausselimination]]: keine $0$-Einträge auf der Diagonalen von $A$
- Tauschen der Zeilen einer Matrix ist aber erlaubt => $0$ kann "weggetauscht" werden
- [[Spaltenpivotisierung]] oder [[totale Pivotisierung]]
- Pivotisierung verbessert auch die [[Stabilität]] des Verfahrens