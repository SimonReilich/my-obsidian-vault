---
lecture: "[[Algorithmen für Programmierwettbewerbe]]"
---
#Bachelor #Informatik #ConPra 
# Algorithmus
Finde [[Topologische Ordnung]] eines [[Graph|Graphen]]
- Speichere für jeden Knoten die Anzahl der Vorgänger
- Solange es noch Knoten gibt, wähle den mit $0$ Vorgängern aus und entferne ihn
- Die Reihenfolge, in der die Knoten entfernt wurden, ist eine [[Topologische Ordnung]]