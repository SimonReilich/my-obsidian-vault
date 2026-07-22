---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs 
# Definition
Leitungscodes (nicht zu verwechseln mit [[Kanalkodierung|Kanalcodes]]) definieren die Abfolge von einer bestimmten Art von [[Symbol|Grundimpulsen]], welche Bits oder Gruppen von Bits repräsentieren. Eine solche Abfolge von [[Symbol|Grundimpulsen]] wird [[Sendeimpuls]] genannt

# Wichtige Eigenschaften
- Anzahl der Signalstufen (binär, ternär, . . . )
- Anzahl kodierter Bits pro [[Symbol]]
- Schrittgeschwindigkeit (Symbolrate / Baudrate), Einheit db

# Optionale Eigenschaften
- [[Taktrückgewinnung]]
- [[Gleichstromfreiheit]]
- Bereitstellung von [[Steuerzeichen]] (siehe u.a. 4B5B-Kodierung → später)

# Beispiele für Leitungscodes
- [[Non-Return-To-Zero]]
- [[Return-To-Zero]]
- [[Manchester-Code]]
- [[Multi-Level-Transmit 3]]

Wie kann der Empfänger erkennen, ob detektierte Symbole überhaupt Daten repräsentieren (Medium könnte „idle“ sein) und wie kann der Beginn bzw. das Ende einer Nachricht erkannt werden?