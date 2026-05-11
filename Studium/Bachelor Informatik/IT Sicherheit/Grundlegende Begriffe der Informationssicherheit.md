---
lecture: "[[IT Sicherheit]]"
---
#BScInfo #Informatik #ITSec 
## Security und Safty
- Achtung: Im Deutschen: Sicherheit umfasst Security und Safety (Security als Hauptbestandteil der VL)
- Security: Daten und Informations-Sicherheit: ISO 2382-1
	- Verwundbarkeit von zu schützenden Werten systematisch reduzieren!
	- Bewahren eines Systems vor Beeinträchtigung und Missbrauch durch Angriffe!  
- Erforderlich:
	- Klären, was die zu schützenden [[Werte]] sind! z.B. Unternehmensgeheimnisse, Nutzerdaten
	- Klären, was geeignete Schutzmaßnahmen sind! z.B. Verschlüsselung, Authentifizierung
	- Angriffe -> Störung von außen mit dem Ziel der Datenmanipulation, des Informationsmissbrauchs oder der Funktionsstörung
- **Hauptfrage: Wie kann man das verhindern?**
## Wichtige Begriffe und ihre Zusammenhänge  
- Angriff(-svektor) (attack) ‒ nutzt aus ‒> Schwachstelle (vulnerability)
- Angriff(-svektor) (attack) ‒ konkretisiert ‒> Bedrohung (threat)
- Angriff(-svektor) (attack) ‒ gefährdet konkret ‒> Wert (zu schützen) (asset)
- Schwachstelle (vulnerability) ‒ gefährdet potentiell ‒> Wert (zu schützen) (asset)
- Bedrohung (threat) ‒ bedroht potentiell ‒> Wert (zu schützen) (asset)
- Asset = zu schützendes Gut
- Schwachstelle (vulnerability) = ermöglicht das Umgehen von Sicherheitskontrollen des Systems
- Bedrohung (threat) = Potenzial, die Sicherheit von Assets zu beeinträchtigen
- Angriff bzw. Angriffsvektor (attack vector) = Möglicher Angriffsweg, der eine oder mehrere Schwachstellen ausnutzt
## Angriffsklassen
- Ungenügende Eingabe- (und Ausgabe-) Validierung -> Eingabe/Ausgabedaten werden nur unzureichend geprüft bzw. bereinigt z.B. schreiben außerhalb des Speicherbereichs -> Ändern von Daten, unerlaubte Zugriffe
- Code-Injection -> Nicht validierte Daten werden von einem Interpreter als Bestandteil einer Anfrage verarbeitet z.B. um Kommandos (z.B. delete) auszuführen oder die Semantik zu verändern
- Identitätsdiebstahl -> Schwachstellen bei Identitätsprüfung ermöglichen es Angreifern, unter einer fremden Identität (Maskierung, Spoofing) zu agieren z.B. ARP-Spoofing, IP-Address-Spoofing, gespoofte E-Mail-Absenderadressen
- (Distributed) Denial of Service - (D)DoS -> Absichtlich herbeigeführte Überlast z.B. von Servern, Routern
- Social Engineering -> täuschen von Menschen z.B. durch präparierte Web-Seite, Fake-Mail, Fake-Telefonate
- Web-Application Security -> OWASP Top 10: Liste der wichtigsten Sicherheitsprobleme im Web-Application Bereich. https://owasp.org/Top10/ z.B. Platz 1: Broken Access Control: zuviele Zugriffsberechtigungen, Platz 2: Fehlerhafte oder fehlende Nutzung von Krypto, Platz 3: Injection Angriffe, inklusive XSS
## Klassen von Schadcode
vergleiche [[Informationssicherheit]]
- Virus = nicht selbständiges Programm, das sich selbst in noch nicht infizierte Dateien kopiert. Bei Ausführung des Virus wird seine Schadfunktion (malware) ausgeführt z.B. formatiere die Festplatte
- Trojaner = Programm, das neben der spezifizierten nützlichen Funktionalität zusätzlich eine versteckte Funktionalität enthält. Beispiel: Keylogger, Trojaner in der Login-Funktion
- Ransomware = verschlüsselt Daten auf Opfer-Rechner (Angreifer erpressen Opfer: Geld gegen Schlüssel) Beispiel: WannaCry für Windows-Systeme, [[2014]] 
## Schutzziele
vergleiche [[Informationssicherheit]] 
Basis-Schutzziele -> CIA: Confidentiality, Integrity, Availability
- Informationsvertraulichkeit (confidentiality) -> Schutz vor unautorisierter Informationsgewinnung  Beispiele für Angriffe: Abhören, Passwort knacken
- Datenintegrität (integrity) -> Schutz vor unautorisierter und unbemerkter Modifikation Beispiele für Angriffe: Buffer-Overflow, SQL-Injection
- Bem.: Verhindern einer Manipulation ist nicht immer möglich, z.B. Ändern von Daten, die über WLAN übertragen werden, aber es ist das Ziel, dann nicht mit manipulierten Daten zu arbeiten!
- Verfügbarkeit (availability) -> Schutz vor unbefugter Beeinträchtigung der Funktionalität Beispiele für Angriffe: Ransomware, Spam
- Bem.: befugte Beeinträchtigungen gibt es in Systemen häufig, z.B. Scheduling (Reihenfolge der Ausführung von Programmen auf dem Rechner): hier könnten z.B. Systemprozesse Vorrang vor Anwenderprogrammen erhalten, diese werden berechtigt verzögert
- Authentizität (authenticity) -> Nachweis der Echtheit und Glaubwürdigkeit der Identität einer handelnden Entität (natürliche Person, Maschine, Dienst, …) oder eines zu nutzenden Objekts
- Verbindlichkeit, Zurechenbarkeit (accountability) -> Schutz vor unzulässigem Abstreiten durchgeführter Handlungen Beispiele für verbindliche Handlungen: Versandt einer Mail/einer Instant Message, Bezahlvorgang; Beispiel für Angriffe: Identitätsdiebstahl, Mailadresse fälschen; Schutzkonzepte: Digitale/elektronische Signatur, ggf. Blockchain
- Privatheit (privacy) -> Die Fähigkeit einer natürlichen Person, die Weitergabe und Nutzung seiner personenbeziehbaren Daten zu kontrollieren (informationelle Selbstbestimmung). Beispiele für Angriffe: Profilbildung, Analytics  Schutzkonzepte: u.a. Anonymisierung, Pseudomisierung
- Bemerkung: In Systemen werden in der Regel Kombinationen von mehreren Schutzzielen gefordert.
## Security Policy, IT-Sicherheitsrichtlinien
- Festlegen der Schutzziele und der Menge von einzuhaltenden technischen und organisatorischen Regeln und Richtlinien
- Festlegen von Verantwortlichkeiten
- Bemerkung: In Unternehmen werden die Sicherheitsrichtlinien, in der Regel in einem umfangreichen Handbuch (gerne mal > 100 Seiten) textuell festgehalten, der Nachweis, dass alle Vorgaben eingehalten sind (Audit), ist aufwändig, automatische Tools (gegebenenfalls mit KI) noch selten.
- Beispiele:
	- Organisatorische Regel: 4 Augen-Prinzip bei sensitiven Abläufen
	- Compliance: GDPR Konformität: Zweckbindung, Lösch-Vorgaben,
	- Technisch: Passwort-Regeln: Länge, Sonderzeichen etc.
	- Technisch: Personenbezogene Daten nur verschlüsselt übertragen