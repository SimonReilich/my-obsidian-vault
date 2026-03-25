---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs #Atomic 
# Definition
Variante von [[Carrier Sense Multiple Access]], bei der Kollisionen nicht nur erkannt werden (wie bei [[CSMA CD]]), sondern verhindert werden (Colission Avoidacen). Achtung: In Funknetzwerken funktioniert CSMA/CD nicht, da der Sender einer Nachricht eine Kollision auch bei ausreichender Nachrichtenlänge nicht immer detektieren kann.

![[Hidden Station.png]]

# Umsetzung (IEEE 802.11 DCF)
- Festes Zeitintervall zwischen [[Rahmen]]: DIFS (DCF Interframe Spacing).
- Wenn Medium mind. für DIFS unbelegt ist, dann wähle unabhängig und gleichverteilt eine Anzahl von Backoff-Slots aus dem [[Intervall]] $\{0,1,2, ... , \min \{2^{c+k −1} − 1255\}\}$.
- c ist abhängig vom PHY (z. B. c = 4), k ist die Anzahl der Sendeversuche (siehe [[Binary Exponential Backoff]]).

![[IEEE 820.11 DCF.png]]

- Medienzugriff hat durch festes $c > 0$ stets ein Contention Window.
- Ein [[Rahmen]] gilt in IEEE 802.11 als erfolgreich übertragen, wenn
	- im Fall von Unicasts der Empfänger eine Bestätigung schickt (Link-Layer Acknowledgements) oder
	- im Fall von Broadcasts die Übertragung eines Frames störungsfrei abgeschlossen wird.
- Da i. d. R. nicht gleichzeitig gesendet und das Medium geprüft werden kann (anders bei [[Ethernet]]), ist die zweite Bedingung praktisch bereits erfüllt, wenn ein Knoten zu senden beginnt.

# Erweiterung RTS/CTS
- Request to Send / Clear To Send
- Übertragungen werden i. d. R. von einer Basisstation gesteuert
- Bevor ein Knoten eine Nachricht überträgt, wird ein RTS an die Basisstation geschickt
- Nur wenn die Basisstation mit einem CTS antwortet, darf die Übertragung beginnen