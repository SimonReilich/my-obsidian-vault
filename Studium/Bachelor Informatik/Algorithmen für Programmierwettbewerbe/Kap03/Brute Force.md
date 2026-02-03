---
lecture: "[[Algorithmen für Programmierwettbewerbe]]"
---
#Bachelor #Informatik #ConPra 
# Definition
- Testen aller Lösungskandidaten, z.B. Durchprobieren bei Zahlenschloss
- Vorteile: Einfach, findet garantiert eine Lösung (falls diese existiert)
- Nachteile: ineffizient, nicht realistisch für große Eingaben

# Verbesserung
- Idee: Beginne mit wahrscheinlichen Lösungen oder verkleinere den Suchraum
- Repräsentation: ggf. Reihenfolge ignorieren
- Algorithmus: [[Enumeration von bedingten Tupeln]] 
- Andernfalls: [[Steinhaus-Johnson-Trotter Algorithmus]] oder [[Gray-Codes]] 
- Wichtig: Iteration statt Speichern

# Größe des Suchraums
- Koeffizienten: [[Fakultät]], [[fallende Fakultät]], [[Binomialkeoffizienten]], [[Stirlingzahlen zweiter Art]], [[Bell Zahlen]], [[Catalan Zahlen]] 
- [[Satz über die Summe von Polynomen]] 
- Meist reicht eine Näherung, der genaue Wert wird nur äußerst selten benötigt
- Näherungen: [[Stirlingformel]]

# Backtracking
- Konstruiere Teillösungen, sind diese invalide, können alle folgenden Möglichkeiten ignoriert werden ([[Backtracking]]).
- Beispiel: [[CNF SAT]] 