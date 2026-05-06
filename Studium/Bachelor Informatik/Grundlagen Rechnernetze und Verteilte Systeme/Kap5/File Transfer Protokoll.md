---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs 
# Definition
Das File Transfer Protocol (FTP) ist ein weiteres Protokoll zum Transfer von Daten (Text wie Binärdaten). Unterschiede zu [[Hyper Text Transfer Protokoll|HTTP]]:
- FTP nutzt zwei getrennte TCP-Verbindungen:
	1. Kontrollkanal zur Übermittlung von Befehlen und Statuscodes zwischen Client und Server.
	2. Datenkanal zur Übertragung der eigentlichen Daten.
- Der Kontrollkanal bleibt über mehrere Datentransfers hinweg bestehen, d. h. FTP ist stateful.
- FTP erfordert grundsätzlich eine Art von Authentifizierung (anonymer Zugang mittels Benutzername anonymous und beliebigem Passwort sofern konfiguriert).

FTP arbeitet entweder im active oder passive mode:
- In beiden Fällen baut der Client den Kontrollkanal zum Server auf [[Transmission Control Protokoll|TCP]] 21 auf.
- Im active mode teilt der Client mittels des PORT-Kommandos dem Server eine zufällige Portnummer mit, auf der der Server vom Quellport TCP 20 eine neue [[Transmission Control Protokoll|TCP]]-Verbindung zum Client aufbaut, die als Datenkanal verwendet wird.
- Im passive mode sendet der Client das Kommando PASV über den Kontrollkanal und erhält vom Server [[IP-Adresse]] und Portnummer, zu der der Client eine zweite [[Transmission Control Protokoll|TCP]]-Verbindung aufbauen soll, die wiederum als Datenkanal verwendet wird

Achtung: active Mode funktioniert standartmäßig nicht mit [[Network Address Translation]], dafür muss die NAT-Implementierung erweitert werden. oder der passive Mode genutzt werden.