---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs #Atomic 
# Definition
Verfahren, um dauerhafte Kollisionen bei [[CSMA CD]] zu verhindern. Beim $k$-ten Sendeversuch einer Nachricht:
- wählt der Sender zufällig $n ∈ \{0, ... , min\{2k −1 − 1,1023\} \}$ aus und
- wartet $n$ Slotzeiten vor einem erneuten Sendeversuch.
Die maximale Wartezeit ergibt sich bei $k = 11$ (also bei $10$ Wiederholungen) und beträgt $1023$ Slotzeiten. Durch die Wartezeiten, die zufällig gewählt und situationsabhängig größer werden, wird die Kollisionswahrscheinlichkeit bei Wiederholungen reduziert.