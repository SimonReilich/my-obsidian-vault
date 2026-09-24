---
lecture: "[[Numerisches Programmieren]]"
degree: "[[Bachelor Informatik]]"
---
#BScInfo #Informatik #NumProg 

# Das Annäherungsproblem

- Definition [[Annäherung]] und [[Approximant]] 
- Variante: [[Interpolation]] und [[Interpolant]] 

# Interpolation mit Polynomen

- Nutzt ein [[Polynom]] zur Interpolation von Funktionswerten
- Vorteil: für $n$ Wertepaare gibt es genau ein [[Polynom]] von minimalem Grad $<n$ das durch alle Punkte verläuft
- Problem: Bei vielen Stützpunkten benötigt man schnell [[Polynom|Polynome]] hohen Grades
- Definition [[Interpolationsfehler]]
- Methoden zur Polynominterpolation: [[Lagrange Polynome]], [[Schema von Aitken und Neville]] und [[Schema von Newton]] (liefern alle selbes Ergebnis)
- Probleme: Bei äquidistanten Stützpunkten wird die [[Kondition]] des Problems schon ab $7$ Punkten sehr schlecht, [[Runge-Effekt]]
- Ansatz: [[Chebyshev Punkte]], funktioniert aber nur, wenn x-Koordinaten frei gewählt werden können

# Splines

- Anstatt eines [[Polynom|Polynoms]] durch alle Stützpunkte zu legen, kann man auch mehrere Polynome 'zusammenkleben' => [[Splines]] 

# Ausgleichsgeraden

- Messpunkte selbst können Fehlerbehaftet sein
- Oft wollen wir auch keine Funktion, die genau die Messpunkte trift, sondern nur ungefähre Trends erkennen
- Definition [[Methode der kleinsten Quadrate]] 

# Trigonometrische Interpolation

- Polynominterpolation eignet sich nicht für periodische Funktionen, wir wollen unsere Funktion als Summe von [[Sinus]]- und [[Cosinus|Cosinusfunktionen]] darstellen
- Definition [[DFT]] und [[IDFT]]
- Haben beide hohe Laufzeitkomplexität, deshalb [[FFT]] 