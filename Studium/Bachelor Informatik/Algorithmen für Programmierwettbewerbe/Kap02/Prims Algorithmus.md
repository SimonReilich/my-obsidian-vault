---
lecture: "[[Algorithmen für Programmierwettbewerbe]]"
---
#BScInfo #Informatik #ConPra #Atomic 
# Definition
Prims Algorithmus ist ein Algorithmus zur Berechnung eines [[Minimaler Spannbaum|minimalen Spannbaums]] zu einem gegebenen [[Graph|Graphen]]. Dabei wird wie folgt vorgegangen:
1. Es werden 3 "Farben" für Vertecies verwendet: schwarz (bereits Teil des MSP), grau (Nachbar eines schwarzen Vertex) und weiß (unentdeckt)
2. Starte mit einzelnem schwarzen Vertex, speichere entdeckte Vertecies
3. Wähle den grauen Vertex, der zum schwarzen die geringste Distanz hat und färbe ihn schwarz, färbe seine Nachbarn grau
4. Wiederhohle das, bis es keine grauen Vertecies mehr gibt
Der Algorithmus hat eine asymptotische Laufzeit von $O(|E| + |V| \log |V|)$ unter Verwendung eines [[Fibonacci-Heap|Fibonacci-Heaps]] 