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
	- [[Dijkstras Algorithmus]] (Generalisierung von BFS)

# Topologische Sortierung
- Definition [[Topologische Ordnung]] 
- Algorithmus: [[Topological Sort]] 

# Minimale Spannbäume
- Definition: [[Spannbaum]], [[Minimaler Spannbaum]] 
- Ansätze: [[Kruskals Algorithmus]] und [[Prims Algorithmus]] 

# Kürzeste Pfade
- Klassifizierung: [[Single-Pair-Shortest-Path]], [[Single-Source-Shortest-Path]] oder [[Any-Pairs-Shortest-Path]] 
- Algorithmen: [[Dijkstras Algorithmus]], [[Bellman-Ford-Algorithmus]] 
- Naiver Ansatz für [[Any-Pairs-Shortest-Path]]: Führe [[Dijkstras Algorithmus]] $|V|$-mal aus, Laufzeit von $O(|V|*|E| + |V|^2 \log |V|)$
- Besser: [[Floyd-Warshall-Algorithmus]] 
- Längster Pfad: [[Floyd-Warshall-Algorithmus]] mit negierten Gewichten, oder nutze [[Topological Sort]] 

# Längste Pfade
- Problem ist auf allgemeinen Graphen [[NP-hard]]
- Für gerichtete azyklische Graphen gibt es allerdings Algorithmen in [[P]] 
- Möglichkeit 1: negiere Kantengewichte, wende [[Bellman-Ford-Algorithmus]] an, Laufzeit von $O(|V| * |E|)$
- Möglichkeit 2: berechne [[Topologische Ordnung]] und arbeite Vertecies in dieser Reihenfolge ab, Laufzeit von $O(|V| + |E|)$ 

# Maximaler Fluss
- Definition [[Flussnetzwerk]], [[Fluss]]
- Einfacher Algorithmus: [[Ford-Fulkerson-Algorithmus]] 
- Noch besser: [[Dinics Algorithmus]], [[Push]]