---
title: Ramsey-Based Inclusion Checking for Visibly Pushdown Automata
author:
  - "[[Oliver Friedmann]]"
  - "[[Felix Klaedtke]]"
  - "[[Martin Lange]]"
publisher: "[[ACM]]"
year: "[[2015]]"
source: "[[Olivier Friedmann, Felix Klaedtke, Martin Lange - 2015 - Ramsey-Based Inclusion Checking for Visibly Pushdown Automata.pdf]]"
---
#Literatur #Informatik 
# Grundlagen
- Viele Probleme des Model-Checking lassen sich auf die Frage $L(A) \subseteq L(B)$ reduzieren, so auch im Bereich von [[Büchi-Automat|Büchi-Automaten]]
- Solche Inklusionsprobleme sind im Allgemeinen schwer, für [[Büchi-Automat|Büchi-Automaten]] sind sie [[PSPACE]]-vollständig
- Einfach ist hingegen der Schnitt zweier [[omega-reguläre Sprache|omega-regulärer Sprachen]], der [[Büchi-Automat]] ist höchstens quadratisch größer, $L(A) \cap L(B) = \emptyset$ ist [[NLOGSPACE]]-vollständig 
- $L(A) \subseteq L(B)$ ist äquivalent zu $L(A) \cap L(\bar{B}) = \emptyset$, die Komplementbildung eines [[Büchi-Automat|Automaten]] erhält aber nicht notwendigerweise seine deterministische Eigenschaft und ist deswegen schwieri