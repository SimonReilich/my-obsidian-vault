---
title: Visibly Pushdown Languages
author:
  - "[[Rajeev Alur]]"
  - "[[Parthasarathy Madhusudan]]"
publisher: "[[ACM Symposium on Theory of Computing]]"
year: "[[2004]]"
file: "[[Alur und Madhusudan - 2004 - Visibly Pushdown Languages.pdf]]"
sources:
  - "[[Autebert et al  - 1997 - Context-free languages and pushdown automata]]"
  - "[[Alur et al - 2004 - A temporal logic of nested calls and returns]]"
  - "[[Alur et al - 2001 - Analysis of recursive state machines]]"
  - "[[Berstel und Boasson - 2002 - Balanced grammars and their languages]]"
  - "[[Bouajjani et al - 1997 - Reachability Analysis of Pushdown Automata Application to model-checking]]"
  - "[[Ball und Rajamani - 2000 - A symbolic model checker for boolean programs]]"
  - "[[Burkart und Steffen - 1992 - Model checking for context-free processes]]"
  - "[[Bouquet et al - 2003 - Pushdown games with unboundedness and regular conditions]]"
  - "[[Comon et al - 2002 - Tree automata techniques and applications]]"
  - "[[Cachat et al - 2002 - Solving pushdown games with a winning condition]]"
  - "[[Cohen und Gold - 1977 - Theory of omega-Languages - I Characterizations of omega-Context-Free languages]]"
  - "[[Chatterjee et al - 2003 - Stack size analysis for interrupt driven programs]]"
  - "[[Chen und Wagner - 2002 - Mops - an infrastructure for examining security properties of software]]"
  - "[[Esparza et al - 2003 - Model-checking LTL with regular variations for pushdown systems]]"
  - "[[Henzinger et al - 2002 - Temporal-safety proof for systems code]]"
  - "[[Harel et al - 2000 - Dynamic Logic]]"
  - "[[Jensen et al - 1999 - Verification of control flow based security properties]]"
  - "[[Knuth - 1967 - A characterization of parenthesis languages]]"
  - "[[Lautemann et al - 1994 - Logics for context-free Languages]]"
  - "[[McNaughton - 1967 - Parenthesis Grammars]]"
  - "[[Reps et al - 1995 - Precise interprocedural Dataflow Analysis via Graph Reachability]]"
  - "[[Thomas - 1990 - Automata on infinite objects]]"
  - "[[Vardi und Wolper - 1986 - An automata-theoretic approach to automatic program verification]]"
---
#Artikel #Informatik #AutoTheo 
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