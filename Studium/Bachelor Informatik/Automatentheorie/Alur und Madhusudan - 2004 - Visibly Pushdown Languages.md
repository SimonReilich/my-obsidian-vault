---
title: Visibly Pushdown Languages
author:
  - "[[Rajeev Alur]]"
  - "[[Parthasarathy Madhusudan]]"
publisher: "[[ACM Symposium on Theory of Computing]]"
year: "[[2004]]"
file: "[[Alur und Madhusudan - 2004 - Visibly Pushdown Languages.pdf]]"
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
- Definition von [[Transparenter omega-Kellerautomat|transparenten omega-Kellerautomaten]] als Erweiterung für unendliche Wörter

# Ergebnisse
- [[Geschachtelte Sprache|Transparente Kellersprachen]] sind unter [[Vereinigung]], [[Schnitt]], [[Konkatenation]], [[Komplementbildung]], [[Kleene-Stern]] und Umbenennung abgeschlossen
- Jeder [[Transparenter Kellerautomat|transparente Kellerautomat]] hat einen äquivalenten deterministischen [[Transparenter Kellerautomat|transparenten Kellerautomat]] mit $O(2^{n^2})$ Zustanden und einem Keller-Alphabet der Größe $O(2^{n^2} * |\Sigma_c|)$ 
- Leerheit einer [[Geschachtelte Sprache|transparenten Kellersprache]] ist in [[PTIME]]
- Universalität und Inklusion sind für [[Geschachtelte Sprache|transparente Kellersprachen]] [[EXPTIME]]-vollständig
- Für [[Transparenter omega-Kellerautomat|transparente omega-Kellersprachen]] gelten die selben Abgeschlossenheits-eigenschaften
- [[Transparenter omega-Kellerautomat|Transparente omega-Kellerautomaten]] sind allerdings nicht determinisierbar