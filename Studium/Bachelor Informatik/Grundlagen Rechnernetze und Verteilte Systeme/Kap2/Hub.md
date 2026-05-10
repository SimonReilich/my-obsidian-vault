---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs 
# Definition
Ein Hub verbindet die einzelnen Links zu einem gemeinsamen Bus. Es darf folglich zu jedem Zeitpunkt nur ein Knoten senden, andernfalls treten Kollisionen auf. Ein Hub unterbricht also nicht die [[Kollisionsdomäne]].

Man unterscheidet aktive und passive Hubs:
- Aktive Hubs (Repeater) verstärken die Signale auf der [[Physikalische Schicht|physikalischen Schicht]], ohne dabei die in [[Rahmen]] enthaltenen Felder wie Adressen oder Checksummen zu prüfen
- Passive Hubs sind nur Sternverteiler – man könnte genauso gut die einzelnen Adern der Patchkabel verlöten

Man kann Hubs kaskadieren, aber es gilt bei Ethernet mit Baumtopologie (802.3a/i) die [[5-4-3-Regel]]. Es können auch unterschiedliche Medientypen miteinander verbunden werden, wenn auf allen Abschnitten dasselbe Medienzugriffsverfahren genutzt wird (beispielsweise Verbindung [[Ethernet]] über BNC- und Patch-Kabel mit jeweils gleicher Datenrate). Unterschiedliche Zugriffsverfahren können nicht gekoppelt werden.