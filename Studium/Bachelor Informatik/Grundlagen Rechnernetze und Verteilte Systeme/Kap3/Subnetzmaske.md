---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs 
# Definition
Um das Problem der schwindenden Anzahl an freien [[IP-Adresse|IP-Adressen]] zu bekämpfen, wurde bereits [[1993]] mit CIDR5 ein Verfahren zur Unterteilung von IP-Netzen eingeführt:
- Zusätzlich zur [[IP-Adresse]] erhält ein Interface eine ebenfalls 32 bit lange Subnetzmaske
- Die Subnetzmaske unterteilt die [[IP-Adresse]] in einen Netzanteil und einen Hostanteil
- Eine logische 1 in der Subnetzmaske bedeutet Netzanteil, eine logische 0 Hostanteil
- [[AND]]-Verknüpfung von [[IP-Adresse]] und Subnetzmaske ergibt die Netzadresse
- Die übliche Klassenzugehörigkeit hat damit nur noch im Sprachgebrauch eine Bedeutung

# Beispiel

![[Subnetzmaske Beispiel.png]]

- 23 bit Netzanteil, 9 bit Hostanteil ⇒ $2⁹ = 512$ Adressen, 510 nutzbare Adressen für Hosts.
- Anstelle die Subnetzmaske auszuschreiben, wird häufig nur die Länge des Netzanteils (Anzahl führender Einsen in der Subnetzmaske) angegeben, z. B. 192.168.0.0/23
- Gegebenenfalls können Netze so zusammengefasst werden (z.B. 192.168.0.0/24 und 192.168.1.0/24 zu 192.168.0.0/23)