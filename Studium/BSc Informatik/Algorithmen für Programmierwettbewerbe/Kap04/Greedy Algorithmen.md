---
lecture: "[[Algorithmen für Programmierwettbewerbe]]"
---
#Bachelor #Informatik #ConPra 
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
- Einfache Version ist kein Approximationsalgorithmus, [[Greedy Knapsack Fractional]] ist aber optimal, [[Greedy Knapsack]] ist ein [[k-faktor Approximationsalgorithmus|2-faktor Approximationsalgorithmus]]
- Wenn alle Gewichte gleich sind, ist [[Greedy Knapsack]] ein optimaler Algorithmus

# Job Scheduling
- Definition: [[Job-Scheduling-Problem]] 
- Zwei Greedy-Möglichkeiten:
	- Gib nächste Aufgabe an den weniger beschäftigten Prozessor, [[Scheduling]]
	- Gib längste Aufgabe an den weniger beschäftigten Prozessor