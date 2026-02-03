---
lecture: "[[Algorithmen für Programmierwettbewerbe]]"
---
#Bachelor #Informatik #ConPra 
# Definition
Der Floyd-Warshall-Algorithmus ist ein Algorithmus, der das [[Any-Pairs-Shortest-Path]]-Problem für beliebige Graphen löst. Die [[Adjazenzmatrix]] des Graphen wird genutzt, um iterativ immer kürzere Pfade zu finden:
$$A_{i, j} = \min\{A_{i, j}, A_{i, k} + A_{k, j}\}$$ 