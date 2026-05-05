---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs 
# Verbindungslose Übertragung
- Header eines Transportprotokolls besteht mind. aus Quell- und Zielport sowie einer Längenangabe der Nutzdaten
- Dies ermöglicht es einer Anwendung beim Senden für jedes einzelne Paket den Empfänger ([[IP-Adresse]]) und die empfangende Anwendung (Protokoll und Zielport) anzugeben
- Probleme: Da die Segmente unabhängig voneinander und aus Sicht der Transportschicht zustandslos versendet werden, kann nicht sichergestellt werden, dass
	- Segmente den Empfänger erreichen (Pakete können verloren gehen) und
	- der Empfänger die Segmente in der richtigen Reihenfolge erhält (Pakete werden unabhängig geroutet)
- Häufigstes Protokoll: [[User Datagram Protokoll]] 

# Verbindungsorientierte Übertragung
- Grundlegende Idee: Linear durchnummeriere Segmente mittels Sequenznummern im Protokollheader
- Sequenznummern ermöglichen insbesondere
	- Bestätigung erfolgreich übertragener Segmente,
	- Identifikation fehlender Segmente,
	- erneutes Anfordern fehlender Segmente und
	- Zusammensetzen der Segmente in der richtigen Reihenfolge
- Probleme: Sender und Empfänger müssen sich zunächst synchronisieren (Austausch der initialen Sequenznummern) und Zustand halten (aktuelle Sequenznummer, bereits bestätigte Segmente, . . . )
- Verbindungsphasen:
	1. Verbindungsaufbau (Handshake)
	2. Datenübertragung
	3. Verbindungsabbau (Teardown)
- Da Overhead durch Warten auf Bestätigung sehr groß: [[Sliding-Window-Verfahren]]
- Häufigstes Protokoll: [[Transmission Control Protokoll]] 
- Ziel der Flusskontrolle ist es, Überlastsituationen beim Empfänger zu vermeiden. Dies wird erreicht, indem der Empfänger eine Maximalgröße für das Sendefenster des Senders vorgibt.
- Ziel der Staukontrolle ist es, Überlastsituationen im Netz zu vermeiden. Dazu muss der Sender Engpässe im Netz erkennen und die Größe des Sendefensters entsprechend anpassen.

# Network Address Translation
[[IP-Adresse|IP-Adressen]] müssen nicht eindeutig sein, wenn
- keine Kommunikation mit im Internet befindlichen Hosts möglich sein muss oder
- die nicht eindeutigen privaten [[IP-Adresse|IP-Adressen]] auf geeignete Weise in öffentliche Adressen übersetzt werden
Definition [[Network Address Translation]] 