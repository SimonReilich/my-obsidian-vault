---
lecture: "[[Algorithmen für Programmierwettbewerbe]]"
---
#Bachelor #Informatik #ConPra
# Graphen
- Definition [[Graph]], [[Zyklus]], [[Zusammenhängend]], [[Baum]], [[Wald]]
- Interface: `make`, `get_vertecies`, `get_edges`, `test_edge`, `get_succ`
- Repräsentation: [[Adjazenzmatrix|Adjazenzmatrizen]] oder [[Adjazenzliste|Adjazenzlisten]] (meist besser)
- [[Graph]] wird als dicht bezeichnet, wenn $|E| = O(|V|^2)$ 

# Traversion
- Besuche alle Knoten im Graph in einer bestimmten Reihnfolge
- Zwei Ansätze: [[Depth-First-Search]] und [[Breadth-First-Search]] 
- Anwendungen:
	- [[Dijkstra Algorithmus]] (Generalisierung von BFS)

# Topologische Sortierung
- Definition [[Topologische Ordnung]] 
- Algorithmus: [[Topological Sort]] 

# Minimale Spannbäume
- Definition: [[Spannbaum]], [[Minimaler Spannbaum]] 
- Ansätze: [[Kruskals Algorithmus]] und [[Prims Algorithmus]] 

# Kürzeste Pfade
- Klassifizierung: [[Single-Pair-Shortest-Path]], [[Single-Source-Shortest-Path]] oder [[Any-Pairs-Shortest-Path]] 
- Algorithmen: [[Dijkstras Algorithmus]], [[Bellman-Ford-Algorithmus]] 
- Variante: [[Bellman-Ford-Algorithmus mit negativer Zyklendetektierung]] 
- [[Floyd-Warshall-Algorithmus]] 
- Längster Pfad: [[Floyd-Warshall-Algorithmus]] mit negierten Gewichten, oder nutze [[Topological Sort]] 