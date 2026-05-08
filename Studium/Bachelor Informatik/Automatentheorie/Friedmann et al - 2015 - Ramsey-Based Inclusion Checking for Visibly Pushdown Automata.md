---
title: Ramsey-Based Inclusion Checking for Visibly Pushdown Automata
author:
  - "[[Oliver Friedmann]]"
  - "[[Felix Klaedtke]]"
  - "[[Martin Lange]]"
publisher: "[[ACM Transactions on Computational Logic]]"
year: "[[2015]]"
file: "[[Olivier Friedmann, Felix Klaedtke, Martin Lange - 2015 - Ramsey-Based Inclusion Checking for Visibly Pushdown Automata.pdf]]"
sources:
  - "[[Abdulla et al - 2011 - Advanced Ramsey-based Büchi automata inclusion testing]]"
  - "[[Abdulla et al - 2010 - When simulation meets antichains]]"
  - "[[Alur et al - 2005 - Analysis of recursive state machines]]"
  - "[[Alur und Madhusudan - 2009 - Adding nesting structure to words.]]"
  - "[[Ball und Rajamani - 2000 - Boolean programs: A model and process for software analysis]]"
  - "[[Breuers et al - 2012 - Improved Ramsey-based Büchi complementation]]"
  - "[[Bruyere et al - 2013 - Visibly pushdown automata - Universality and inclusion via antichains]]"
  - "[[Büchi - 1960 - On a decision method in restricted second-order arithmetic]]"
  - "[[Choueka - 1974 - Theories of automata on omega-tapes - a simplified approach]]"
  - "[[Dax et al - 2006 -  A proof system for the linear time μ-calculus]]"
  - "[[De Wulf et al - 2006 - Antichains - A new algorithm for checking universality of finite automata]]"
  - "[[Doyen und Raskin - 2009 - Antichains for the automata-based approach to model-checking]]"
---
#Literatur #Informatik 
# Grundlagen
- Viele Probleme des Model-Checking lassen sich auf die Frage $L(A) \subseteq L(B)$ reduzieren, so auch im Bereich von [[Büchi-Automat|Büchi-Automaten]]
- Solche Inklusionsprobleme sind im Allgemeinen schwer, für [[Büchi-Automat|Büchi-Automaten]] sind sie [[PSPACE]]-vollständig
- Einfach ist hingegen der Schnitt zweier [[omega-reguläre Sprache|omega-regulärer Sprachen]], der [[Büchi-Automat]] ist höchstens quadratisch größer, $L(A) \cap L(B) = \emptyset$ ist [[NLOGSPACE]]-vollständig 
- $L(A) \subseteq L(B)$ ist äquivalent zu $L(A) \cap L(\bar{B}) = \emptyset$, die Komplementbildung eines [[Büchi-Automat|Automaten]] erhält aber nicht notwendigerweise seine deterministische Eigenschaft und ist deswegen schwierig
- Zur Lösung des Universalitätsproblems ($L(A) = \Sigma^\omega$) gibt es ramsey-basierte Algorithmen (Korrektheit folgt aus [[Ramseys Theorem]])
- Dieser Ansatz lässt sich auf das Inklusionsproblem, sowie auf [[omega-Automat|omega-Automaten]] erweitern
- In diesem Paper wird diese Idee weitergeführt und das Ramsey-basierte Verfahren für das Inklusionsproblem auf [[Sichtbarer Kellerautomat|sichtbare Kellerautomaten]] ausgedehnt
- Für diese ist das Inklusionsproblem sogar [[EXPTIME]]-vollständig
- Der Schritt zu allgemeinen [[Kellerautomat|Kellerautomaten]] ist nicht möglich, da für diese Universalität unentscheidbar ist