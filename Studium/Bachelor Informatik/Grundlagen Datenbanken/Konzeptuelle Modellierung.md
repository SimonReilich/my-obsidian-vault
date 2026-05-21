---
aliases:
lecture: "[[Grundlagen Datenbanken]]"
degree: "[[Bachelor Informatik]]"
---
#BScInfo #Informatik  #GDB
# Datenbankentwurf:
- 4 Phasen: Anforderungsanalyse, Konzeptueller Entwurf, Implementationsentwurf, Physischer Entwurf
- Anforderungsanalyse:
	1. Identifikation von Organisationseinheiten
	2. Identifikation der zu unterstützenden Aufgaben
	3. Anforderungs-Sammelplan
	4. Anforderungs-Sammlung
	5. Filterung
	6. Satzklassifikationen
	7. Formalisierung
# Entity-Relationship-Modell (ER-Modell):
- Das ER-Modell wird verwendet, um konzeptuelle Schemata zu erstellen. Es ist eine Methode, um die Strukturen und Beziehungen in einem bestimmten Bereich zu beschreiben
- Entity-Typen (z. B. Studenten, Professoren, Vorlesungen) werden in Rechtecken dargestellt, und die Beziehungen zwischen diesen Entitäten werden durch Linien oder andere grafische Symbole dargestellt.
### Vergleich mit UML:
- UML (Unified Modeling Language) ist ähnlich dem ER-Modell, wird aber oft in der Softwareentwicklung verwendet. Das ER-Modell bildet die Basis für UML, wobei UML etwas andere Grafiken und Konzepte verwendet.
### Relationales Modell:
- Das Relationale Modell setzt Entity-Typen und Beziehungen in Relationen (Tabellen) um. Es ist besonders im Kontext von Datenbanksystemen relevant.
- Beispiel: Studenten und Vorlesungen werden in Tabellen mit spezifischen Attributen wie Matrikelnummer, Vorlesungsnummer usw. dargestellt.
### Transformation in andere Modelle:
- Das konzeptuelle Schema kann in verschiedene spezifische Schemata wie Relationales Schema, XML Schema, Netzwerk Schema und Objektorientiertes Schema umgewandelt werden.
- Diese Transformationen sind wichtig, um die Datenstruktur an unterschiedliche Anwendungen und [[Anforderungen]] anzupassen.
# Generalisierung und Spezialisierung:
- In der ER-Modellierung spielt die Generalisierung eine Rolle, um Struktur in die Klassen oder Entity-Typen zu bringen. Diese Konzepte sind jedoch im Relationalen Modell nicht direkt umsetzbar.
# Funktionalitäten
- 1:1 -> Jedes Entity von links hat genau einen Partner von rechts und umgekehrt
- 1:N -> Ein Entity von der linken Seite kann beliebig viele Partner auf der rechten Seite haben, ein Entity auf der rechten Seite hat genau einen oder keinen Partner auf der linken
- N:M -> Jedes Entity kann beliebig viele Partner auf der anderen Seite haben
- Hat ein Entity in einer Beziehung die Funktionalität 1, so ist es durch alle anderen Mitglieder der Beziehung eindeutig bestimmbar
# (min, max)-Notation
- Hat ein Entity in einer Beziehung die Annotation (min, max), so gibt es zwischen min und max viele Beziehungstupel, die das Entity enthalten
# Konsolidierung:
- Erstellung eines Globalen Schemas durch Sichtenintegration
- Ansprüche an ein Globales Schema: Redundanzfreiheit, Widerspruchsfreiheit, Synonymbereinigt, Homonymbereinigt
- Meist über Teilkonsolidierung, dargestellt durch Konsolidierungsbaum