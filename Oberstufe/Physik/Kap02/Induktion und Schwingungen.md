---
subject: "[[Physik - Schule]]"
---
#Oberstufe #Physik 
# Induktionsphänomene
- [[Hans Christian Oersted]] entdeckt, dass ein elektrischer Strom eine magnetische Wirkung hat
- [[Michael Faraday]] vermutet, dass auch die Umkehrung der Fall ist und denteckt das Phänomen der [[Induktion]] (häufig: [[Wechselstrom]])
- Im gegensatz zum konstanten Stromfluss, der ein [[Magnetisches Feld]] erzeugt, ist für [[Induktion]] jedoch ein zeitlich veränderliches [[Magnetisches Feld]] nötig
- Für die Induktionsspannung in einer [[Spule]] gilt: $U_{ind} = -N * A * \frac{\Delta B}{\Delta V}$ 
- Definition des [[Magnetischer Fluss|magnetischen Fluss]] und verallgemeinerung zum [[Infuktionsgesetz]] 
- [[Energieerhaltung]] bei der [[Induktion]]: [[Regel von Lenz]]

# Selbstinduktion
- Das von einer [[Spule]] erzeugte [[Magnetisches Feld|Magnetfeld]] kann in der [[Spule]] selbst wieder einen Strom induzieren
- Definition der [[Induktivität]] $L$ als Kenngröße einer [[Spule]] 
- Die [[Spule]] "federt" An- und Abschaltvorgänge ab, genau umgekehrt zum [[Kondensator]] 
- Die magnetische Feldenergie in einer stromdurchflossenen Spule beträgt $E_{mag} = \frac{1}{2} LI^2$ 

# Der elektromagnetische Schwingkreis
- Der [[Elektromagnetischer Schwingkreis|elektromagnetische Schwingkreis]] bildet die Grundlage für Funkübertragungen 
- Ablauf einer halben Periode:
	1. [[Kondensator]] ist maximal geladen, die Spannung ist am größten, es fließt kein Strom: $Q_C(0s) = Q_{max}, U_C(0s) = U_{max}, I(0s) = 0A$ 
	2. Die Kondensatorspannung treibt den Strom durch die [[Spule]], in dieser entsteht aber eine entgegengesetzte Induktionsspannung: $\dot{Q}_C(t) = I(t)$ 
	3. Nach einer viertel Periode ist der [[Kondensator]] vollständig entladen. Der Strom durch die [[Spule]] ist maximal, die Induktionsspannung verschwindet: $Q_C(T / 4) = 0C, U_C(T/4 = 0V), I(T/4) = I_{max}$ 
	4. Durch die Selbsinduktion der Spule fließt der Strom weiter in die selbe Richtung, der [[Kondensator]] wird umgekehrt geladen, die zunehmende Kondensatorspannung verringert den Strom: $I(t) = \dot{Q}_C(t)$
	5. Nach einer halben Periode ist der [[Kondensator]] vollständig geladen (umgekehrte Polung zum Zeitpunkt $t = 0s$): $Q_C(T / 2) = -Q_{max}, U_C(T/2) = -U_{max}, I(T / 2) = 0 A$
- Es ergeben sich: $U_C(t) = U_{max} * \cos(\omega t), I(t) = -I_{max} * \sin(\omega t)$ 
- Über die [[Energieerhaltung]]: $E_{ges} = E_{el} + E_{mag} = \frac{1}{2} C U(t) ^2 + \frac{1}{2} LI(t)^2 = \mathrm{konst}$ 
# Erzwungene Schwingung und Resonanz

# Wechselstromkreise