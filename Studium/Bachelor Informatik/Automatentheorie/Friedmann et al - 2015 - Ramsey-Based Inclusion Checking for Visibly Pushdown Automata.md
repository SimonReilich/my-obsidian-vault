---
title: Ramsey-Based Inclusion Checking for Visibly Pushdown Automata
author:
  - "[[Oliver Friedmann]]"
  - "[[Felix Klaedtke]]"
  - "[[Martin Lange]]"
publisher: "[[ACM Transactions on Computational Logic]]"
year: "[[2015]]"
file: "[[Friedmann et al - 2015 - Ramsey-Based Inclusion Checking for Visibly Pushdown Automata.pdf]]"
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
  - "[[Driscoll et al - 2011 - Checking conformance of a producer and a consumer]]"
  - "[[Driscoll et al - 2012 - OpenNWA - A nested-word-automaton library]]"
  - "[[Dziembowski et al - 1997 - How much memory is needed to win infinite games?]]"
  - "[[Emerson und Jutla - 1991 -  Tree automata, μ-calculus and determinacy]]"
  - "[[Fogarty und Vardi - 2009 -  Büchi complementation and size-change termination]]"
  - "[[Fogarty und Vardi - 2010 - Efficient Büchi universality checking]]"
  - "[[Friedmann et al - 2013 - Ramsey goes visibly pushdow]]"
  - "[[Friedmann und Lange - 2012 - Ramsey-based analysis of parity automata]]"
  - "[[Fritz und Wilke - 2005 - Simulation relations for alternating Büchi automata]]"
  - "[[Gerth et al - 1996 - Simple on-the-fly automatic verification of linear temporal logic]]"
  - "[[Heizmann et al - 2010 - Nested interpolants]]"
  - "[[Kähler und Wilke - 2008 - Complementation, disambiguation, and determinization of Büchi automata unified]]"
  - "[[La Torre et al - 2007 - A robust class of context-sensitive languages]]"
  - "[[Lee et al - 2001 -  The size-change principle for program termination]]"
  - "[[Leroy et al - 2011 - The OCaml system (release 3.12) - Documentation and users manual]]"
  - "[[Löding et al - 2004 - Visibly pushdown games]]"
  - "[[Löding und Thomas - 2000 - Alternating automata and logics over infinite words]]"
  - "[[Madhusudan und Parlato - 2011 - The tree width of auxiliary storage]]"
  - "[[Mehlhorn - 1980 - Pebbling mountain ranges and its application to DCFL-recognition]]"
  - "[[Michel - 1988 - Complementation is more difficult with automata on infinite words]]"
  - "[[Muller und Schupp - 1987 - Altenating Automata on Infinite Trees]]"
  - "[[Pitermann - 2007 - From nondeterministic Büchi and Streett automata to deterministic parity automata]]"
  - "[[Rabin und Scott - 1959 - Finite automata and their decision problems.]]"
  - "[[Friedmann et al - 2015 - Ramsey-Based Inclusion Checking for Visibly Pushdown Automata]]"
  - "[[Schewe - 2009 - Tighter bounds for the determinisation of Büchi automata]]"
  - "[[Sistla et al - 1987 - The complementation problem for Büchi automata with applications to temporal logic]]"
  - "[[Tsai et al - 2011 - State of Büchi complementation]]"
  - "[[Vardi - 2007 - The Büchi complementation saga]]"
  - "[[Vardi und Wolper - 1986 - An automata-theoretic approach to automatic program verification]]"
  - "[[Vardi und Wolper - 1994 - Reasoning about infinite computations]]"
---
#Artikel #Informatik #AutoTheo 
# Grundlagen
- Viele Probleme des Model-Checking lassen sich auf die Frage $L(A) \subseteq L(B)$ reduzieren, so auch im Bereich von [[Büchi-Automat|Büchi-Automaten]]
- Solche Inklusionsprobleme sind im Allgemeinen schwer, für [[Büchi-Automat|Büchi-Automaten]] sind sie [[PSPACE]]-vollständig
- Einfach ist hingegen der Schnitt zweier [[omega-reguläre Sprache|omega-regulärer Sprachen]], der [[Büchi-Automat]] ist höchstens quadratisch größer, $L(A) \cap L(B) = \emptyset$ ist [[NLOGSPACE]]-vollständig 
- $L(A) \subseteq L(B)$ ist äquivalent zu $L(A) \cap L(\bar{B}) = \emptyset$, die Komplementbildung eines [[Büchi-Automat|Automaten]] erhält aber nicht notwendigerweise seine deterministische Eigenschaft und ist deswegen schwierig
- Zur Lösung des Universalitätsproblems ($L(A) = \Sigma^\omega$) gibt es ramsey-basierte Algorithmen (Korrektheit folgt aus [[Ramseys Theorem]])
- Dieser Ansatz lässt sich auf das Inklusionsproblem, sowie auf [[omega-Automat|omega-Automaten]] erweitern
- In diesem Paper wird diese Idee weitergeführt und das Ramsey-basierte Verfahren für das Inklusionsproblem auf [[Transparenter Kellerautomat|transparente Kellerautomaten]] ausgedehnt
- Für diese ist das Inklusionsproblem sogar [[EXPTIME]]-vollständig
- Der Schritt zu allgemeinen [[Kellerautomat|Kellerautomaten]] ist nicht möglich, da für diese Universalität unentscheidbar ist

# Universalität
- Sei $\mathcal{A} = (Q, \Gamma, \Sigma, \delta, q_I, \Omega)$ ein [[Transparenter Kellerautomat]]
- Nun soll ein Algorithmus gezeigt werden, der entscheidet ob $L(\mathcal{A}) = NW(\Sigma)$ 
- Drei Arten von atomaren Transitionsprofilen: [[int-Transitionsprofil]], [[call-Transitionsprofil]] und [[ret-Transitionsprofil]]
- Beschreiben das Verhalten von $\mathcal{A}$ wenn ein einzelnes Zeichen gelesen wird
- Komposition der Transitionsprofile kann genutzt werden um das Verhalten von $\mathcal{A}$ auf endlichen Wörtern zu beschreiben
![[Komposition von Transitionsprofilen.png]]
