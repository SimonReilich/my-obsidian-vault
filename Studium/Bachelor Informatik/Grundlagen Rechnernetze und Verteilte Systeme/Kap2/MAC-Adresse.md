---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs #Atomic 
# Definition
Als MAC-Adressen (Media Access Control) werden Adressen auf der [[Sicherungsschicht]] (Schicht 2) bezeichnet. Sie gewährleisten eine eindeutige Identifizierung der Knoten innerhalb des [[Direktverbindungsnetz|Direktverbindungsnetzes]]. Zumeist existiert eine [[Broadcast]]-Adresse, welche alle Knoten im [[Direktverbindungsnetz]] anspricht. Zusätzlich kann es [[Multicast]]-Adressen geben, die bestimmte Gruppen von Knoten ansprechen. MAC-Adressen dienen zur Adressierung innerhalb eines [[Direktverbindungsnetz]] und werden beim Forwarding durch einen [[Router]] verändert.

# Aufbau

![[MAC Aufbau.png]]

- Netzwerkkarten besitzen eine ab Werk im ROM (Read Only Memory) hinterlegte MAC-Adresse
- Auftrennung in OUI (Organizationally Unique Identifier) und Device ID ermöglicht es den Herstellern von Netzwerkkarten, eindeutige MAC-Adressen zu vergeben
- Der Hersteller einer Netzwerkkarte kann folglich anhand deren MAC-Adresse identifiziert werden (z. B. 7c:6d:62 = [[Apple]])
- Als [[Broadcast]]-Adresse ist ff:ff:ff:ff:ff:ff („all ones“) definiert
- Ob es sich bei einer Adresse um eine [[Unicast]]- oder [[Multicast]]-Adresse handelt, bestimmt das lowest order Bit des ersten Oktetts

Anmerkung: Für bestimmte Anwendungen ist es sinnvoll, auf die herstellerübergreifende Eindeutigkeit zu verzichten, z. B. bei virtualisierten Netzwerkadaptern. Hierfür sind die sog. lokal-administrierten Adressen (zweites Bit des ersten Oktetts) vorgesehen.