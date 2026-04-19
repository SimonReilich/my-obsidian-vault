---
subject: "[[Physik - Schule]]"
---
#Oberstufe #Physik 
# Induktionsphänomene
- [[Hans Christian Oersted]] entdeckt, dass ein elektrischer Strom eine magnetische Wirkung hat
- [[Michael Faraday]] vermutet, dass auch die Umkehrung der Fall ist und denteckt das Phänomen der [[Induktion]] (häufig: [[Wechselstrom]])
- Im gegensatz zum konstanten Stromfluss, der ein [[Magnetisches Feld]] erzeugt, ist für [[Induktion]] jedoch ein zeitlich veränderliches [[Magnetisches Feld]] nötig
- Für die Induktionsspannung in einer [[Spule]] gilt: $U_{ind} = -N * A * \frac{\Delta B}{\Delta t}$ 
- Definition des [[Magnetischer Fluss|magnetischen Fluss]] und verallgemeinerung zum [[Induktionsgesetz]] 
- [[Energieerhaltung]] bei der [[Induktion]]: [[Regel von Lenz]]

# Selbstinduktion
- Das von einer [[Spule]] erzeugte [[Magnetisches Feld|Magnetfeld]] kann in der [[Spule]] selbst wieder einen Strom induzieren
- Definition der [[Induktivität]] $L$ als Kenngröße einer [[Spule]] 
- Die [[Spule]] "federt" An- und Abschaltvorgänge ab, genau umgekehrt zum [[Kondensator]] 
- Die magnetische Feldenergie in einer stromdurchflossenen Spule beträgt $E_{mag} = \frac{1}{2} LI^2$ 

# Der elektromagnetische Schwingkreis
- Der [[Elektromagnetischer Schwingkreis|elektromagnetische Schwingkreis]] bildet die Grundlage für Funkübertragungen 
- Für die Periodendauer gilt die [[Thomsonsche Schwingungsgleichung]] 
- In der Realität geht aber [[Energie]] verloren, es kommt zu einer gedämpften Schwingung
- Problem lässt sich über [[Differentialgleichungen]] lösen, man unterscheidet 3 Fälle:
	- schwache Dämpfung: Schwingung mit exponentiell abnehmender Amplitude
	- Kriechfall: Dämpfung ist so stark, dass das System nie zur anderen Seite ausschwingt
	- aperiodischer Grenzfall: "Grenzwert" des Kriechfalls
- Definition der [[Erzwungene Schwingung|erzwungenen Schwingung]], anregung des Schwingkreis über [[Induktive Kopplung]].

# Wechselstromkreise
- Zur Visualisierung von Phasenverschiebung im [[Wechselstrom|Wechselstromkreis]] werden [[Zeigerdiagramm|Zeigerdiagramme]] genutzt
- Bei einer [[Spule]] läuft die [[Elektrische Stromstärke]] der [[Spannung]] hinterher. $I(t)$ ist gegenüber $U_L(t)$ um den Winkel $\Delta \phi = - 90°$ phasenverschoben
- Bei einem [[Kondensator]] verhält es sich genau andersherum: $I(t)$ ist um $\Delta \phi = 90°$ gegenüber $U_C(t)$ phasenverschoben
- Bei einem [[Ohmscher Widerstand|Ohmschen Widerstand]] findet keine Phasenverschiebung statt
- Im [[Wechselstrom|Wechselstromkreis]] wird meist mit Effektiv- statt mit Maximalwerten gerechnet:$$U_{eff} = \frac{U_{max}}{\sqrt{2}}, \space I_{eff} = \frac{I_{max}}{\sqrt{2}}$$
- Im [[Wechselstrom|Wechselstromkreis]] können neben [[Ohmscher Widerstand|ohmschen Widerständen]] auch [[Spule|Spulen]] und [[Kondensator|Kondensatoren]] einen Widerstand haben, man spricht vom [[Wechselstromwiderstand]] $X$ 
- technische Anwendungen: [[Hochpass]], [[Tiefpass]] oder [[Bandpass]] 