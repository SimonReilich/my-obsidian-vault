---
lecture: "[[Einführung in die Softwaretechnik]]"
---
#Bachelor #Informatik #Softwaretechnik 
# Definition
[[Software-Architektur]], die auf einem verteilten System basiert. Die Anwendung wird in zwei Komponenten, Client (frägt den Service an) und Server (stellt den server zur Verfügung), aufgeteilt, diese kommunizieren über ein [[Netzwerk]] mit einem anfrage-basierten [[Protokoll]].

# Komponenten
Client: Initiale Anfrage an Service oder Ressource
- Verantwortlich für Benutzer-Interface und -Interaktionen
- Beispiele: Browser, Mibile-Apps, Desktop-Anwendungen
Server: Wartet auf, verarbeitet, und stellt Service für Client anfragen zur verfügung
- Verwaltet Resourcen, Daten, und Sicherheit
- Beispiele: Web-Server, Datenbank-Server, Datei-Server
[[Netzwerk]]: Kommunikationskanal zwischen Client und Server
- Lokales [[Netzwerk]] (LAN) oder Wide-Area-[[Netzwerk]] (WAN) wie das Internet
Protokoll: Definiert das Format und die Regeln der Kommunikation
- Beispiele: [[Representational State Transfer]], [[Remote Procedure Call]] 

# Funktionsweise
- Client sendet eine Anfrage an den Server
- Der Server empfängt und interpretiert die Anfrage
- Der Server verarbeitet die Anfrage, dass kann unter anderem beinhalten:
	- Daten aus einer Datenbank oder Dateien lesen
	- Eine Berechnung ausführen
- Der Server sendet eine Antwort an den Client
- Der Client empfängt die Antwort und zeigt die Ergebnisse dem Benutzer an