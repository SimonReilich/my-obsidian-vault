---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs 
# Definition
Eine einfache Verbesserung von [[Slotted ALOHA]]: „Listen Before Talk“ Höre das Medium ab und beginne erst dann zu senden, wenn das Medium frei ist.

# Varianten:
- $1$-persistentes CSMA:
	1. Wenn Medium frei, beginne Übertragung
	2. Wenn Medium belegt, warte bis frei und beginne dann Übertragung
- $p$-persistentes CSMA:
	1. Wenn Medium frei, übertrage mit Wahrscheinlichkeit $p$ oder verzögere mit Wahrscheinlichkeit $1 − p$ um eine feste Zeit dann 1.
	2. Wenn Medium belegt, warte bis frei, dann 1.
- nicht-persistentes CSMA:
	1. Wenn Medium frei, beginne Übertragung
	2. Wenn belegt, warte eine zufällig gewählte Zeitspanne dann 1.