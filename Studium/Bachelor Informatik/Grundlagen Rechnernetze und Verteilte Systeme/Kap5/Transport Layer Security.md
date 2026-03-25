---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs #Atomic 
# Definition
TLS ist ein Protokoll zur sicheren Übertragung von Daten über einen verbindungsorientierten Transportdienst. Es ist die Grundlage u.a. für [[HTTPS]]. Es bietet unter anderem:
- [[Authentifizierung]]
- [[Integrität]]
- [[Vertraulichkeit]]
Es gibt unzählige kryptographische Verfahren, viele sind unsicher. [[Client-Server Architektur|Client]] und [[Client-Server Architektur|Server]] müssen sich auf die bestmöglichen Parameter einigen, die beide implementieren (Kompatibilität vs. Sicherheit). Sitzungen können mit Hilfe von [[Session]]-IDs über mehrere [[Transmission Control Protokoll|TCP]]-Verbindungen hinweg erhalten bleiben. Während die Funktionen zur Sitzungsverwaltung und -wiederaufnahme eher der Sitzungsschicht zugeordnet werden, gehören die Verschlüsselungsfunktionen zur Darstellungsschicht.