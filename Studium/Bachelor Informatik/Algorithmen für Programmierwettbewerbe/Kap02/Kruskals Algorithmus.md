---
lecture: "[[Algorithmen für Programmierwettbewerbe]]"
---
#Bachelor #Informatik #ConPra #Atomic 
# Definition
Kruskals Algorithmus ist ein [[Greedy Algorithmen|greedy]] Algorithmus zur Berechnung eines [[Minimaler Spannbaum|minimalen Spannbaums]] zu einem gegebenen [[Graph|Graphen]]. Dabei wird wie folgt vorgegangen:
1. Initialisiere die Menge der Kanten mit $\{\}$ und eine eine [[Union-Find Referenz|Union-Find-Datenstruktur]] 
2. Arbeite nun die Kanten sortiert nach Kantengewicht (niedrig -> hoch) ab:
	1. Teste mit der [[Union-Find Referenz|Union-Find-DS]], ob sich die Kanten in unterschiedlichen Komponenten befinden
	2. Falls ja, füge die Kante zu $S$ hinzu und aktualisiere die [[Union-Find Referenz|Union-Find-DS]] 
3. $S$ enthält nun alle Kanten des [[Minimaler Spannbaum|minimalen Spannbaums]] 
Sollte der Graph nicht zusammenhängend sein, so gibt der Algorithmus einen minimalen [[Wald|Spannwald]] zurück. Er hat eine asymptotische Laufzeit von $O(|E| \log |E|)$ 