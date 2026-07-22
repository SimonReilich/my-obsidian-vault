---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs 
# Definition
Während einer verbindungsorientierten Übertragung können drei Phasen unterschieden werden:
1. Verbindungsaufbau
	- Austausch von Signalisierungsnachrichten zum Aufbau einer dedizierten Verbindung zwischen Sender und Empfänger.
	- Dieser Schritt beinhaltet die Wegwahl, welche vor Beginn der Datenübertragung durchgeführt wird.
2. Datenaustausch
	- Kanal steht den Kommunikationspartnern zur exklusiven Nutzung bereit.
	- Auf die Adressierung des Kommunikationspartners kann während der Übertragung weitgehend verzichtet werden (Punkt-zu-Punkt-Verbindung).
3. Verbindungsabbau
	- Austausch von Signalisierungsnachrichten zum Abbau der Verbindung.
	- Die durch die Verbindung belegten [[Ressourcen]] werden für nachfolgende Verbindungen freigegeben.

![[Ablauf Leitungsvermittlung.png]]

Vorteile:
- Gleichbleibende Güte der dedizierten Verbindung nach dem Verbindungsaufbau
- Schnelle Datenübertragung ohne Notwendigkeit, weitere Vermittlungsentscheidungen treffen zu müssen

Nachteile:
- Ressourcenverschwendung sofern Leitung nicht dauerhaft ausgelastet wird, da Leitung zur exklusiven Nutzung reserviert wird
- Verbindungsaufbau kann komplex sein und benötigt u. U. weit mehr Zeit, als die [[Ausbreitungsverzögerung|Ausbreitungsverzögerungen]] vermuten lassen (z. B. Einwahl ins Internet mittels [[Modem]])
- Hoher Aufwand beim Schalten physikalischer Verbindungen
