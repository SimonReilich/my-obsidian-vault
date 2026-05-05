---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs #Atomic 
# Definition
- Kollisionsfreie Übertragung durch Weitergabe eines Tokens
- Stationen werden zu einem logischen Ring zusammen geschaltet
- Ein Token zirkuliert im Ring
- Will eine Station senden, nimmt sie das Token vom Ring und darf danach als einzige Station im Ring übertragen
- Nachdem alle Nachrichten gesendet wurden (oder nach einer definierten Zeitspanne) wird das Token wieder auf den Ring gelegt

# Empfang von Nachrichten
- Die Nachricht zirkuliert wie das Token durch den Ring
- Der Empfänger markiert die Nachricht als gelesen und schickt sie weiter
- Trifft sie wieder beim Sender ein, so nimmt dieser sie vom Netz
- Was ist, wenn das Token „verloren geht“?
	- Es gibt eine Monitor-Station, z. B. die Station, die das erste Token erzeugt hat
	- Diese Monitor-Station erzeugt bei Bedarf neue Tokens, entfernt endlos kreisende Pakete und entfernt doppelte Token
	- Fällt die Monitor-Station aus, wird von den verbleibenden Stationen eine Neue gewählt