---
lecture: "[[Komplexitätstheorie]]"
---
#Bachelor #Informatik #CoTheo
# Turingmaschienen
- Viele verschiedene Modelle für Berechnungen:
	- [[Turingmaschiene]]
	- [[Random-Access-Machine]]
	- [[mu-rekursive Funktionen]], [[Lambda-Kalkül]]
	- [[Programmiersprache]]
	- ...
- [[Church-Turing-These]]: Jedes physikalisch umsetzbare Modell kann von einer [[Turingmaschiene]] simuliert werden
- [[Starke Church-Turing-These]]: Das ist mit ledeglich [[Polynom|polynomiellem]] Overhead möglich
- Hier betrachten wir folgende Variation: [[k-Band Turingmaschine]] 
- Definition der [[Laufzeit einer Turingmaschiene]] $T(n)$ (muss eine [[zeitkonstruierbare Funktion]] sein)

# Variationen
- Größe des [[Alphabet|Alphabets]] 
- Anzahl der Arbeitsbänder (eines reicht bereits aus)
- Dimension des bandes (unbidirektional, bidirektional, zweidimensional, ...)
- Random Access
- [[vergessliche Turingmaschiene]] 
- All diese Variationen sind gleich mächtig und können sich mit [[Polynom|polynomiellem]] Overhead gegenseitig simulieren.

# Die Universelle Turingmaschiene
- [[Turingmaschiene|Turingmaschienen]] können als [[Wort]] über dem [[Alphabet]] $\{0, 1\}$ kodiert werden
- Jedes [[Wort]] $\alpha \in \{0, 1\}^*$ repräsentiert eine [[Turingmaschiene]] $M_\alpha$ 
- [[Theorem über die Universelle Turingmaschiene]] 

# Entscheidbarkeit und das Halteproblem

# Die Klassen DTIME und P