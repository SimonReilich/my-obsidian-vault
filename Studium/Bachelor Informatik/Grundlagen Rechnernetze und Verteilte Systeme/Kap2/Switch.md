---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs 
# Definition
Ein Switch arbeitet zunächst wie ein [[Hub]] (Learning-Phase). Dabei merkt sich der Switch, über welchen Port ein [[Rahmen]] empfangen wurde. So ordnet er den Ports die [[MAC-Adresse|MAC-Adressen]] der Knoten zu, die an den jeweiligen Port angeschlossen sind. Die Ziel-Adresse eingehender [[Rahmen]] wird mit den Einträgen in der Switching-Table verglichen. Ist ein Eintrag vorhanden, wir der [[Rahmen]] nur an den betreffenden Ziel-Port weitergeleitet, ist kein Eintrag vorhanden, so wird der [[Rahmen]] an alle Ports weitergeleitet. Einträge erhalten einen Zeitstempel (Timestamp) und werden nach einem festen Zeitintervall invalidiert. Ein Switch unterbricht die [[Kollisionsdomäne]].