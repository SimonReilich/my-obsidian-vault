---
title: Ramsey goes visibly pushdow
author:
  - "[[Oliver Friedmann]]"
  - "[[Felix Klaedtke]]"
  - "[[Martin Lange]]"
publisher: "[[International Colloquium on Automata, Languages and Programming]]"
year: "[[2013]]"
file: "[[Friedmann et al - 2013 - Ramsey Goes Visibly Pushdown.pdf]]"
sources:
---
#Artikel #Informatik #AutoTheo #ToDo 
# Grundlagen
- Viele Probleme der Programmverifikation lassen sich als Sprachprobleme beschreiben
- $\text{Menge der Ausführungen} \subseteq \text{Durch Spezifikation zugelassene Ausführungen}$ ?
- Einige Eigenschaften, wie z.B. dead code oder Zugriff auf uninitialisierte Variablen lassen sich durch [[Reguläre Sprache|reguläre Sprachen]] beschreiben, oft sind aber [[Kontextfreie Sprache|kontextfreie Sprachen]] nötig
- Deshalb werden [[sichtbare Kellersprache|sichtbare Kellersprachen]] als Untermenge der deterministischen [[Kontextfreie Sprache|kontextfreien Sprachen]] eingeführt, für sie bleiben viele Eigenschaften entscheidbar
- Das Konzept lässt sich für unendliche Wörter auch auf [[sichtbare omega-Kellersprache|sichtbare omega-Kellersprachen]] erweitern

# Definitionen
- Definition [[Sichtbarer Kellerautomat]]
- [[sichtbare Kellersprache]] sind die [[formale Sprache|Sprachen]], für die es einen [[Sichtbarer Kellerautomat|sichtbaren Kellerautomaten]] gibt
- Dadurch können nicht-reguläre Eigenschaften, wie
	- partielle 