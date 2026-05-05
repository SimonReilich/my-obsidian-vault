---
lecture: "[[Algorithmen für Programmierwettbewerbe]]"
---
#BScInfo #Informatik #ConPra #Atomic 
# Definition
Topological Sort ist ein Algorithmus, der zu einem gegebenen [[Graph]] eine [[Topologische Ordnung]] berechnet (falls eine solche existiert).Dabei wird nach folgendem erfahren vorgegangen:
1. Ordne die Vertecies nach der Anzahl der eingehenden Kanten
2. Wähle einen Vertex mit $0$ eingehenden Kanten und entferne ihn aus dem Graphen (falls es keinen solchen gibt, existiert keine [[Topologische Ordnung]], der Graph ist [[Zyklus|zyklisch]])
3. Wiederhohle Schritt 2 solange, bis alle Vertecies entfernt wurden
4. Die Reihenfolge, in der Vertecies entfernt wurden, ist eine [[Topologische Ordnung]]
Topological Sort hat damit eine asymptotische Laufzeit von $O(|V| + |K|)$ (falls die Anzahl an eingehenden Kanten in linearer Zeit bestimmt werden kann)