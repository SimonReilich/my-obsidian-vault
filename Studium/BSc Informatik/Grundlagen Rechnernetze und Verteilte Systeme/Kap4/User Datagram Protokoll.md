---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs 
# Definition
Das User Datagram Protcol (UDP) ist eines der beiden am häufigsten verwendeten Transportprotokolle im Internet. Es bietet ungesicherte und nachrichtenorientierte Übertragung bei geringem Overhead.

# Header

![[UDP Header.png]]

- „Length“ gibt die Länge von Header und Daten in Vielfachen von Byte an.
- Die Prüfsumme erstreckt sich über Header und Daten.
	- Die Verwendung der UDP-Prüfsumme ist bei [[Internet Protocol Version 4|IPv4]] optional, wird für [[Internet Protocol Version 6|IPv6]] jedoch vorausgesetzt.
	- Wird sie nicht verwendet, wird das Feld auf 0 gesetzt.
	- Wird sie verwendet, wird zur Berechnung ein Pseudo-Header genutzt (eine Art „Default-IP-Header“ der nur zur Berechnung der Prüfsumme dient). Er beinhaltet folgende Felder des IP-Headers: Quell- und Ziel-[[IP-Adresse]], ein 8 bit langes Feld mit Nullen, Protocol-ID und Länge des UDP-Datagramms.

# Vorteile
- Geringer Overhead
- Keine Verzögerung durch Verbindungsaufbau oder Retransmits und Reordering von Segmenten
- Gut geeignet für Echtzeitanwendungen (Voice over IP, Online-Spiele) sofern gelegentlicher Paketverlust in Kauf genommen werden kann
- Keine Beeinflussung der Datenrate durch Fluss- und Staukontrollmechanismen

# Nachteile
- Keine Zusicherung irgendeiner Form von Dienstqualität (beliebig hohe Fehlerrate)
- Datagramme können out-of-order ausgeliefert werden (beispielsweise bei Verwendung mehrerer Pfade zu einem Ziel)
- Keine Flusskontrolle (schneller Sender kann langsamen Empfänger überfordern)
- Keine Staukontrollmechanismen (Überlast im Netz führt zu hohen Verlustraten)

# Einsatzbereiche
- Wo gelegentlicher Verlust von Datagrammen tolerierbar ist bzw. durch höhere Schichten wieder ausgeglichen wird oder
- ein zeitaufwendiger Verbindungsaufbau, wie er bei anderen Transportprotokollen benötigt wird, nicht tolerierbar ist.
- Namesauflösung mittels [[Domain Name System]]
- Datenverkehr mit Echtzeitanforderungen
- Google’s QUIC