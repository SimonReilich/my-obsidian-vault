---
lecture: "[[Komplexitätstheorie]]"
---
#BScInfo #Informatik #Comp
# Definition
Bis auf folgende zwei Ausnahmen ist die Definition äquivalent zur [[Turingmaschiene|deterministischen k-band-Turingmaschiene]]:
- $Q$ enthält den Zustand $q_{Accept}$ 
- $\delta$ ist ein Paar $(\delta_0, \delta_1)$ von Transitionsfunktionen
In jedem Schritt wird nichtdeterministisch eine deer beiden Transitionsfunktionen gewählt. Die Eingabe wird akzeptiert, wenn es eine folge von Entscheidungen gibt, sodass $q_{Accept}$ erreicht wird. Sie wird nicht akzeptiert, falls es keine solche Folge gibt.