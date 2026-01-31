---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs 
# Definition
Verfahren um Overhead bei verbindungsorientierter Übertragung durch Warten auf Bestätigung zu minimieren. Idee: Teile dem Sender mit, wie viele Segmente nach dem letzten bestätigten Segment auf einmal übertragen werden dürfen, ohne dass der
Sender auf eine Bestätigung warten muss.

# Vorteile
- Zeit zwischen dem Absenden eines Segments und dem Eintreffen einer Bestätigung kann effizienter genutzt werden
- Durch die Aushandlung dieser Fenstergrößen kann der Empfänger die Datenrate steuern → Flusskontrolle
- Durch algorithmische Anpassung der Fenstergröße kann die Datenrate an die verfügbare Datenrate auf dem Übertragungspfad zwischen Sender und Empfänger angepasst werden → Staukontrolle

# Nachteile
- Sender und Empfänger müssen mehr Zustand halten (Was wurde bereits empfangen? Was wird als nächstes erwartet?)
- Der Sequenznummernraum ist endlich → Wie werden Missverständnisse verhindert

# Segmentverlust
- Zwei Möglichkeiten
- Go-Back-N
	- Akzeptiere stets nur die nächste erwartete Sequenznummer
	- Alle anderen Segmente werden verworfen
- Selective-Repeat
	- Akzeptiere alle Sequenznummern, die in das aktuelle Empfangsfenster fallen
	- Diese müssen gepuffert werden, bis fehlende Segmente erneut übertragen wurden