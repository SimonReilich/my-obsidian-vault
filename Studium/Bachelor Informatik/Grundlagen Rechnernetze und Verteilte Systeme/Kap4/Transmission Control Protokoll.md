---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs 
# Definition
TCP ist das dominierende Transportprotokoll im Internet (rund 90 % des Datenverkehrs im Internet). Es bietet gesicherte / stromorientierte Übertragung mittels Sliding-Window und Selective Repeat sowie Mechanismen zur Fluss- und Staukontrolle.

# Header

![[TCP Header.png]]

- Quell- und Zielport werden analog zu [[User Datagram Protokoll]] verwendet.
- Sequenz- und Bestätigungsnummer dienen der gesicherten Übertragung. Es werden bei TCP nicht ganze Segmente sondern einzelne Bytes bestätigt (stromorientierte Übertragung)

(Data) Offset
- Gibt die Länge des TCP-Headers in Vielfachen von 4 B an
- Der TCP-Header hat variable Länge (Optionen, vgl. [[Internet Protocol Version 4|IPv4]]-Header)

Reserved: Hat in bisherigen TCP-Versionen keine Verwendung. Muss auf 0 gesetzt werden, so dass zukünftige TCP-Versionen bei Bedarf das Feld nutzen können

Flag URG („urgent“) (selten verwendet): Ist das Flag gesetzt, werden die Daten im aktuellen TCP-Segment beginnend mit dem ersten Byte bis zu der Stelle, an die das Feld
Urgent Pointer zeigt, sofort an höhere Schichten weitergeleitet

Flag ACK („acknowledgement“)
- Ist das Flag gesetzt, handelt es sich um eine Empfangsbestätigung
- Bestätigungen können bei TCP auch „huckepack“ (engl. piggy backing) übertragen werden, d. h. es werden gleichzeitig Nutzdaten von A nach B übertragen und ein zuvor von B nach A gesendetes Segment bestätigt
- Die Acknowledgement-Number gibt bei TCP stets das nächste erwartete Byte an

Flag PSH („push“)
- Ist das Flag gesetzt, werden sende- und empfangsseitige Puffer des TCP-Stacks umgangen.
- Sinnvoll für interaktive Anwendungen (z. B. Telnet-Verbindungen)

Flag RST („reset“): Dient dem Abbruch einer TCP-Verbindung ohne ordnungsgemäßen Verbindungsabbau

Flag SYN („synchronization“)
- Ist das Flag gesetzt, handelt es sich um ein Segment, welches zum Verbindungsaufbau gehört (initialer Austausch von Sequenznummern)
- Ein gesetztes SYN-Flag inkrementiert Sequenz- und Bestätigungsnummern um 1 obwohl keine Nutzdaten transportiert werden

Flag FIN („finish“)
- Ist das Flag gesetzt, handelt es sich um ein Segment, welches zum Verbindungsabbau gehört
- Ein gesetztes FIN-Flag inkrementiert Sequenz- und Bestätigungsnummern um 1 obwohl keine Nutzdaten transportiert werden

Receive Window
- Größe des aktuellen Empfangsfensters $W_r$ in Byte
- Ermöglicht es dem Empfänger, die Datenrate des Senders zu drosseln

Checksum
- Prüfsumme über Header und Daten
- Wie bei [[User Datagram Protokoll|UDP]] wird zur Berechnung ein Pseudo-Header verwendet

Urgent Pointer (selten verwendet): Gibt das Ende der „Urgent-Daten“ an, welche unmittelbar nach dem Header beginnen und bei gesetztem URG-Flag sofort an höhere
Schichten weitergereicht werden sollen

Options: Zusätzliche Optionen, z. B. Window Scaling (s. Übung), selektive Bestätigungen oder Angabe der Maximum Segment Size (MSS)

# Staukontrolle
Zwei Phasen:
1. Slow-Start
	- Für jedes bestätigte Segment wird Wc um eine MSS vergrößert.
	- Dies führt zu exponentiellem Wachstum des Staukontrollfensters bis ein Schwellwert (engl. Congestion Threshold) erreicht ist.
	- Danach wird mit der Congestion-Avoidance-Phase fortgefahren
2. Congestion Avoidance
	- Für jedes bestätige Segment wird Wc lediglich um (1/wc ) MSS vergrößert, d. h. nach Bestätigung eines vollständigen Staukontrollfensters um genau eine MSS.
	- Ein vollständiges Fenster kann frühestens nach 1 RTT bestätigt sein.
	- Dies führt zu linearem Wachstum des Staukontrollfensters in der RTT

TCP interpretiert den Verlust von Segmenten (Daten und Bestätigungen) stets als eine Folge einer Überlastsituation im [[Netzwerk]] (und nicht als Folge von Bitfehlern einer unzuverlässigen Übertragung).
- In der Folge reduziert TCP die Datenrate.
- Handelt es sich bei den Paketverlusten jedoch um die Folge von Bitfehlern, so wird die Datenrate unnötiger Weise gedrosselt.
- Durch die ständige Halbierung der Datenrate bzw. neue Slow-Starts kann das Sendefenster nicht mehr auf sinnvolle Größen anwachsen.
- In der Praxis ist TCP bereits mit 1 % Paketverlust, der nicht auf Überlast zurückzuführen ist, überfordert.