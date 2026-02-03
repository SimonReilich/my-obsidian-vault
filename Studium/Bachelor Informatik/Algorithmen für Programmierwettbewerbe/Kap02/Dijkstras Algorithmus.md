---
lecture: "[[Algorithmen für Programmierwettbewerbe]]"
---
#Bachelor #Informatik #ConPra 
# Definition
Dijkstras Algorithmus ist ein Algorithmus zum finden kürzester Pfade in einem [[Graph|Graphen]] mit nicht-negativen Kantengewichten (er löst also das [[Single-Source-Shortest-Path]]-Problem). Er wurde von [[Edsger W. Dijkstra]] im Jahr [[1959]] publiziert. Der [[Graph]] wird ähnlich wie bei [[Breadth-First-Search|BFS]] / [[Depth-First-Search|DFS]] traversiert, anstatt eines [[Stack|Stacks]] bzw. einer [[Queue]] wird allerdings eine [[Priority-Queue]] (sortiert nach der Distanz zum Startknoten) verwendet. Zusätzlich speichert man zu jedem Vertex seinen Vorgänger, damit lassen sich dann die kürzesten Pfade konstruieren. Insgesamt hat der Algorithmus eine asymptotische Laufzeit von $O(|E| + |V| \log |V|)$.