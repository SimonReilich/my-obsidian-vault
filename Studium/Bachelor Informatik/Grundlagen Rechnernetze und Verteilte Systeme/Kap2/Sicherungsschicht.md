---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs 
# Aufgaben
- Fokus: sogenannte [[Direktverbindungsnetz|Direktverbindungsnetze]] 
- Aufgaben der Schicht 2: Steuerung des Medienzugriffs, Prüfung der Nachrichten auf Fehler und Adressierung innerhalb des Direktnetzwerks
- Typischerweise: Darstellung von [[Netzwerk|Netzwerken]] als [[Graph|Graphen]] 

# Verbindungen
- Definition [[Übertragungsrate]] und [[Serialisierungszeit]]
- [[Ausbreitungsverzögerung]] und [[Übertragungszeit]]
- Durch Ausbreitungverzögerung besitzt ein Kanal eine "Speicherkapazität", das [[Bandbreitenverzögerungsprodukt]]
- Für Mehrfachzugriff: Verschiedene [[Multiplexing]]-Verfahren
- Medienzugriffsverfahren: [[ALOHA]], [[Slotted ALOHA]] und [[Carrier Sense Multiple Access]]

![[Medienzugriffsverfahren Vergleich.png]]

- Weiteres Verfahren: [[CSMA CD]], [[CSMA CA]] und [[Token-Passing]] 

# Rahmenbildung, Adressierung und Fehlererkennung
- Im Kontext der Sicherungsschicht bezeichnen wir Nachrichten fortan als [[Rahmen]] 
- Wie kann der Empfänger [[Rahmen]] erkennen?
	- Längenangabe der Nutzdaten
	- [[Steuerzeichen]] (Start / Ende)
	- Begrenzungsfelder und „Bit-Stopfen“
	- Coderegelverletzung
- Adressen auf Schicht 2 bezeichnet man allgemein als [[MAC-Adresse|MAC-Adressen]] 
- Im Gegensatz zur [[Kanalkodierung]] (fehlerkorrigierende Codes) auf der [[Physikalische Schicht|physikalischen Schicht]] dient die Prüfsumme eines Schicht-2-Protokolls üblicherweise nicht der Fehlerkorrektur sondern lediglich der Fehlererkennung
- Übliches Verfahren: [[Cyclic Redundancy Check]] 

# Verbindungen zwischen Schicht 1 & 2
- [[Hub|Hubs]], [[Switch|Switches]] und [[Bridge|Bridges]] 
- Definition [[Kollisionsdomäne]] 
- Als Brücke zwischen Twisted-Pair und Funkübertragung: [[WLAN Access Points]] 