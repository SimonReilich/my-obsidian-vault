---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs 
# Definition

Ziel der Kanalkodierung ist es, den zu übertragenden Daten gezielt Redundanz hinzuzufügen, so dass eine möglichst große Anzahl an
- Bitfehlern erkannt und
- korrigiert werden kann.

# Blockcodes
unterteilen den Datenstrom
- in Blöcke der Länge $k$ und
- übersetzen diese in Kanalwörter der Länge $n > k$ wobei
- die zusätzlichen $n − k$ bit für Fehlererkennung und Rekonstruktion verwendet werden
Das Verhältnis $R = {k \over n}$ wird als Coderate bezeichnet.