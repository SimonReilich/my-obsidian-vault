---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs 
# Definition
Modifikationen gegenüber [[Leitungsvermittlung]]:
- Aufbau und Abbau einer dedizierten Verbindung entfallen
- Der gesamten Nachricht der Länge $L$ wird ein Header der Länge $L_H$ vorangestellt
- Der Header beinhaltet insbesondere Adressinformationen, die geeignet sind, Sender und Empfänger auch über mehrere Zwischenstationen hinweg eindeutig zu identifizieren
- Die so entstehende [[PDU]] wird als Ganzes übertragen

Möglichkeit für asynchrone Kommunikation, d. h. Nachrichten können ggf. an Empfänger versendet werden, die zum Zeitpunkt des Sendens nicht empfangsbereit sind und mögliche Zeitersparnis, da die Phasen zum Aufbau und Abbau der Verbindung entfallen

![[Ablauf Nachrichtenvermittlung.png]]

Das Wegfallen fest vorgegebener Pfade ermöglicht die gemeinsame Nutzung von Teilstrecken ([[Zeitmultiplex]]).