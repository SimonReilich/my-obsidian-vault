---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
degree: "[[Bachelor Informatik]]"
---
#BScInfo #Informatik #GRnVs 

# Information, Enthropie und Signale

- Definition: [[Signal]] und [[Symbol]]
- von [[Claude Elwood Shannon]]: [[Entropie]]  
- Beispiele:
	- Deterministische, diskrete Quelle, welche stets das Zeichen $'A'$ emittiert $\implies I(A) = -log_2(1) = 0bit; H(\mathcal{X}) = 0bit$ 
	- Binäre Quelle, welche mit selber Wahrscheinlichkeit die Zeichen $'0'$ und $'1'$ emittiert $\implies I(0) = I(1) = -log_2(0,5) = 1bit; H(X) = 0,5 * 1bit + 0,5 * 1bit = 1bit$ 
- Informationstheoretisches Modell eines [[Gedächtnisloser Kanal|gedächtnislosen Kanals]] 
- Bedeutung eines [[Signal|Signals]]: Ein [[Signal]] transportiert [[Informationsgehalt|Information]]. Erst durch eine Interpretationsvorschrift erhält diese Information eine Bedeutung, d. h. es muss eine [[Abbildung]] zwischen [[Symbol|Symbolen]] (Signalwerten bzw. Wertebereichen) und Daten geben.

# Signaldarstellung

- Definition: [[Forierreihe]]
- Bislang haben wir nur periodische Signale betrachtet. Was ist mit nicht-periodischen Signalen?
- Keine Entwicklung als [[Forierreihe]] möglich
- Kontinuierliches (anstatt diskretes) Spektrum
- => [[Foriertransformation]] 

# Abtastung, Rekonstruktion und Quantisierung

- Natürlich vorkommende Signale sind zeitkontinuierlich und wertkontinuierlich, d. h. sie nehmen zu unendlich vielen Zeitpunkten beliebige reelle Werte an.
- Problem für Computer: Endlicher Speicher, Endliche Rechengenauigkeit
- Lösung: [[Abtastung]] und [[Quantisierung]]
- Ein zeit- und wertdiskretes [[Signal]] ist digital und wird in [[Wörtern]] fester Länge gespeichert

# Übertragungskanal

- Wegen der für Kanäle typischen Tiefpasscharakteristik kann man von einer Kanalbandbreite $B$ sprechen
- Niedrige Frequenzen passieren ungehindert ([[Tiefpass]])
- Hohe Frequenzen werden gedämpft
- Ab einer bestimmten Frequenz ist die Dämpfung so stark, dass die betreffenden Signalanteile vernachlässigt werden können
- Vereinfacht nehmen wir eine scharfe Grenze für $B$ an:
	- Frequenzanteile $|f | < B$ passieren
	- Frequenzanteile |$f | ≥ B$ werden gesperrt
- Dies führt zu einer neuen Interpretation der Frequenz $f = 2B$, welche auch als [[Nyquist-Rate]] bezeichnet wird
- [[Hartleys Gesetz]] 
- Maß für Stärke des Rauschens: [[Signal to Noise Ratio]] 
- [[Shannon-Hartley-Theorem]] 
- Die Kanalkapazität $C$ ist durch zwei Faktoren beschränkt:
	- Die Anzahl M der unterscheidbaren Symbole, selbst ein rauschfreier Kanal hilft nichts, wenn wir nur zwei Symbole nutzen (können).
	- [[Signal]]-to-Noise Ratio (SNR), ist das [[Signal]]-zu-Rausch-Verhältnis SNR zu gering, muss ggf. der Abstand $∆$ zwischen den Signalstufen erhöht und damit die Anzahl unterscheidbarer Symbole verringert werden, um eine zuverlässige Unterscheidung gewährleisten zu können.
- Für die tatsächliche Kanalkapazität $C$ gilt also folgende obere [[Schranke]]: $C < \min{C_H, C_S}$ 

# Nachrichtenübertragung

![[Nachrichtenübertragung.png]]
- Definitionen: [[Quellenkodierung]], [[Kanalkodierung]], [[Leitungskodierung]], [[Modulation]] 

# Übertragungsmedien
- Unterscheidungen: leitungsgebunden oder nicht-leitungsgebunden bzw. akustisch oder [[Elektromagnetische Wellen|elektromagnetisch]] 
- Leitungen: [[Koaxialleiter]], [[Twisted-Pair-Kabel]], [[optische Leiter]]