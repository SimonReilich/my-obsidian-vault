---
lecture: "[[Algorithmen für Programmierwettbewerbe]]"
degree: "[[Bachelor Informatik]]"
---
#BScInfo #Informatik #ConPra 
# Kriterien
- Beispiel: Währungsumtausch
- Problem: Je nach Währungssystem ist der Algorithmus beliebig schlecht
- Allgemeine Version des Problems ist aber [[NP-hard]] 
- Definition: [[Kanonisches Münzsystem]] 
- [[Chicken-McNugget-Theorem]], [[Frobenius-Münz-Problem]] 
- [[Allgemeine Form eines Greedy Algorithmus]] 
- Beispiele für Greedy Algorithmen: [[Kruskals Algorithmus]], [[Prims Algorithmus]] 
- Definition: [[Unabhängiges System]], [[Matroid]], [[Edmondos-Rado Theorem]] 

# Approximation
- Definition: [[k-faktor Approximationsalgorithmus]] 
- Dadurch kann [[NP-hard|NP-hardness]] umgehen werden
- Manchmal sind greedy Algorithmen gute Approximationsalgorithmen

# Knapsack
- Definition: [[Knapsack-Problem]] 
- Einfache Version ist kein Approximationsalgorithmus, [[Fractional Greedy Knapsack]] ist aber optimal, [[Greedy Knapsack]] ist ein [[k-faktor Approximationsalgorithmus|2-faktor Approximationsalgorithmus]]
- Wenn alle Gewichte gleich sind, ist [[Greedy Knapsack]] ein optimaler Algorithmus

# Job Scheduling
- Definition: [[Job-Scheduling-Problem]] 
- Zwei Greedy-Möglichkeiten:
	- Gib nächste Aufgabe an den weniger beschäftigten Prozessor, [[Greedy Scheduling]] ist ein [[k-faktor Approximationsalgorithmus|2-faktor Approximationsalgorithmus]]
	- Gib längste Aufgabe an den weniger beschäftigten Prozessor, [[Ordered Greedy Scheduling]] ist ein [[k-faktor Approximationsalgorithmus|1,5-faktor Approximationsalgorithmus]] 
- Auch hier ist die optimale Lösung [[NP-hard]] 

# Facility Location
- Definition: [[metrisches unbeschränktes Facility-Location-Problem]] 
- genaue Lösung ist [[NP-hard]]
- Es gibt einen [[k-faktor Approximationsalgorithmus|1.488-faktor Approximationsalgorithmus]], ist die Metrik identisch zum zweidimensionalen euklidischen Raum, gibt es beliebig gute Approximationsalgorithmen
- Für nicht-metrische Versionen des Problems gibt es keine Approximationsalgorithmen, außer wenn [[P gleich NP]] 
- Algorithmus: [[Greedy Facility Location]] ist ein [[k-faktor Approximationsalgorithmus|2-faktor Approximationsalgorithmus]] 