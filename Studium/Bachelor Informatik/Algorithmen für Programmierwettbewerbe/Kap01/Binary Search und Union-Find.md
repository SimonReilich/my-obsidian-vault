---
lecture: "[[Algorithmen für Programmierwettbewerbe]]"
slides: "[[Binary Search und Union-Find - Slides.pdf]]"
---
#BScInfo #Informatik #ConPra 
# Binary Search
- [[Binary Search]] ist ein Algorithmus zum suchen von Elementen innerhalb eines Arrays
- Laufzeit: $O(n \log(n))$ 
- Kann auch genutzt werden, um Index $i$ zu finden, an dem $f(a_i) = x$ gilt (falls $i \mapsto f(a_i)$ [[monoton wachsend]] ist)
- Statt in einem explizit gespeicherten Array kann auch in einem beliebigen [[Intervall]] gesucht werden (z.B. Wurzel einer Fließkommazahl)

# Union Find
- Datenstruktur um [[Partition|Partitionen]] einer Menge zu verwalten
- z.B. Repräsentation von [[Äquivalenzrelation|Äquivalenzrelationen]] 
- Amortisierte Laufzeit wird durch das Inverse der [[Ackermann-Funktion]] beschrieben
- [[Union-Find Referenz]] 