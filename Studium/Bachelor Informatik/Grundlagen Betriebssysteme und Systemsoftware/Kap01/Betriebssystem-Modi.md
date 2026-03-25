---
lecture: "[[Grundlagen Betriebssysteme und Systemsoftware]]"
---
#Bachelor #Informatik #GBS #Atomic 
# Definition
Ziel der [[Betriebssystem]]-Modi: Schutz des [[Betriebssystem|Betriebssystems]] vor Programmierfehlern und Angriffen. Der Lösungsansatz dabei ist, nach Arbeitsmodi unterschiedliche Berechtigungen zu vergeben. (zunächst) Zwei Modi:
- Benutzermodus (User Mode / Space)
	- Hardwarezugriff nur über das [[Betriebssystem]]
	- Keine privilegierten Befehle wie Ein-/Ausgabe
	- Kein oder nur lesender Zugriff auf Systemcode und -daten
	- Zugriff nur auf [[virtuelle Adressen]]
	- => Anwendungen
- Systemmodus (Kernel Mode / Space)
	- alle ausführbaren [[Maschienenbefehle]]
	- direkter Hardwarezugriff
	- Exklusiver Zugriff auf Systemcode und -daten
	- => Betriebssystemkern
Wenn trotzdem aus dem User-Space privilegierte Befehle durchgeführt werden sollen: [[Systemcalls]]