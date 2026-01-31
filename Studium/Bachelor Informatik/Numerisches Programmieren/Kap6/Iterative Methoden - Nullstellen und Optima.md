---
lecture: "[[Numerisches Programmieren]]"
---
#Bachelor #Informatik #NumProg 

# Große, dünne LGSs

- Oft müssen wir Gleichungssysteme mit sehr großen, aber dünn besetzten Matrizen lösen, dann ist eine Laufzeit von $O(n³)$ aber nicht mehr hinnehmbar
- [[Gausselimination]] zerstört Struktur (tridiagonal, Bandstruktur, Blockstruktur, ...) der Matrix => Speicherplatzbedarf steigt
- Für diesen Fall gibt es bessere [[Indirekte Löser|Iterative Methoden]] 
- zwei Familien von Algorithmen: [[Methoden der Lockerung]] und [[Konjugierte Gradientenmethoden]] 

# Nicht-lineare Gleichungssysteme

- mit den bisherigen Methoden ist nur das Lösen von [[Linearen Gleichungssysteme|linearen Gleichungssystemen]] möglich
- Idee: zu jeder Gleichung können wir eine Funktion formulieren, deren Nullstellen genau den Lösungen des [[Linearen Gleichungssysteme|linearen Gleichungssystems]] entsprechen
- Finde alle Nullstellen $\overline{x} \in ]a, b[$  einer Funktion $f: \mathbb{R} \to \mathbb{R}$ 
- Einfache Methoden: [[Bisektionsmethode]], [[Regula falsi]] und [[Skeantenmethode]] 
- Noch besser: [[Newtonmethode]] bzw. [[Varianten der Newtonmethode|Varianten]] 

# Multigrid

- Sowohl bei [[Methoden der Lockerung]] als auch [[Konjugierte Gradientenmethoden]] gilt: Je höher die Auflösung, desto mehr Schritte sind nötig
- => [[Multigrid Methode]] 