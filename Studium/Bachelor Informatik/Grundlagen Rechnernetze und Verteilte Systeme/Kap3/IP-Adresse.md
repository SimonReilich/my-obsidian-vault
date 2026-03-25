---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs #Atomic 
# Definition
IP-Adressen dienen der End-zu-End-Adressierung zwischen mehreren [[Direktverbindungsnetz|Direktverbindungsnetze]] und werden beim Forwarding durch einen [[Router]] nicht verändert. Jedem Host ist eine IP-Adresse zugewiesen. Jede IPv4-Adresse ist in vier Gruppen zu je einem Byte, durch Punkte getrennt, dargestellt (Dotted Decimal Notation), IPv6-Adressen werden in 8 Gruppen zu je 16 bit getrennt durch Doppelpunkte (colon-separated) in hexadezimaler Schreibweise dargestellt, wobei führende Nullen in den Blöcken weggelassen werden können. Höchstens eine Gruppe konsekutiver Blöcke, die nur aus Nullen bestehen, darf ausgelassen und mit "::" ersetzt werden. Jedes Paket muss mit einer Absender- und Ziel-IP-Adresse (im IP-Header) versehen werden:

![[IPv4-Header.png]]

Dabei gibt zwei unterschiedliche Standards: [[Internet Protocol Version 4]] und [[Internet Protocol Version 6]].

Historisch ist der IP-Adresseraum in folgende fünf Klassen unterteilt:

![[IPv4 Klassen.png]]

Als IPv4 [[1981]] eingeführt wurde, konnte man sich nicht vorstellen, dass $∼ 2^{32}$ Adressen aufgeteilt in die Klassen A, B und C nicht ausreichend würden. Es wurden große Adresseblöcke an Firmen, Behörden und Bildungseinrichungen vergeben, z. B. ganze Klasse-A Netze an [[HP]], [[IBM]], [[AT&T]], [[Apple]], [[MIT]], [[Generel Electric]], US Army, . . .
Folge:
- Ineffiziente Aufteilung und Nutzung des Adressraums
- Große Netze mit internen [[Router|Routern]] ⇒ weitere Unterteilung in [[Subnetzmaske|Subnetze]] notwendig
Vergabe des letzten IPv4 Adressblocks am 3.2.[[2011]] durch die IANA an eine der fünf Regional Internet Registries (RIRs), das APNIC. IPv4-Adressraum praktisch aufgebraucht.