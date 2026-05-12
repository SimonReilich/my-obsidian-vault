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
- Deshalb werden [[Geschachtelte Sprache|transparente Kellersprachen]] als Untermenge der deterministischen [[Kontextfreie Sprache|kontextfreien Sprachen]] eingeführt, für sie bleiben viele Eigenschaften entscheidbar
- Das Konzept lässt sich für unendliche Wörter auch auf [[Geschachtelte omega-Sprache|transparente omega-Kellersprachen]] erweitern

# Definitionen
- Definition [[Transparenter Kellerautomat]]
- [[Geschachtelte Sprache|Transparente Kellersprachen]] sind die [[formale Sprache|Sprachen]], für die es einen [[Transparenter Kellerautomat|transparenten Kellerautomat]] gibt
- Dadurch können nicht-reguläre Eigenschaften, wie partielle und totale Korrektheit,  lokale Eigenschaften oder Zugriffskontrolle verifiziert werden
- Definition von [[Transparenter omega-Kellerautomat|transparent omega-Kellerautomaten]] als Erweiterung für unendliche Wörter

# Ergebnisse
- [[Geschachtelte Sprache|sichtbare Kellersprachen]] sind unter [[Vereinigung]], [[Schnitt]], [[Konkatenation]], [[Komplementbildung]], [[Kleene-Stern]] und Umbenennung abgeschlossen
- Jeder [[Transparenter Kellerautomat|sichtbare Kellerautomat]] hat einen äquivalenten deterministischen [[Transparenter Kellerautomat|sichtbaren Kellerautomat]] mit $O(2^{n^2})$ Zustanden und einem Keller-Alphabet der Größe $O(2^{n^2} * |\Sigma_c|)$ 
- Leerheit einer [[Geschachtelte Sprache|sichtbaren Kellersprache]] ist in [[PTIME]]
- Universalität und Inklusion sind für [[Geschachtelte Sprache|sichtbare Kellersprachen]] [[EXPTIME]]-vollständig
- Für [[Transparenter omega-Kellerautomat|sichtbare omega-Kellersprachen]] gelten die selben Abgeschlossenheits-eigenschaften
- [[Transparenter omega-Kellerautomat|Sichtbare omega-Kellerautomaten]] sind allerdings nicht determinisierbar