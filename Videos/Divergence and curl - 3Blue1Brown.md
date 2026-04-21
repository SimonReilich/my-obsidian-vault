---
title: Divergence and curl
description: The language of Maxwell's equations, fluid flow, and more
year: "[[2018]]"
links:
  - https://www.youtube.com/watch?v=rB83DpBJQsE
channel: "[[3Blue1Brown]]"
thumbnail: "[[Divergence and curl - 3Blue1Brown.png]]"
---
#Video #Physik 
# Vektorfelder
- Definition von [[Vektorfeld|Vektorfeldern]]
- Zum Beispiel für [[Gravitation]], [[Elektrisches Feld]] oder [[Magnetisches Feld]]
- [[Vektorfeld|Vektorfelder]] sind in der Physik häufig zeitlich variabel, hier beschränken wir unss aber auf statische 2-dimensionale [[Vektorfeld|Vektorfelder]] 

# Was ist Divergenz?
- Analogie zu Flüssigkeiten: Es gibt Quellen und Abflüsse
- Divergenz gibt an, wie sehr ein Ort im Feld einer Quelle ($\mathrm{div}F(x, y) > 0$) bzw. einem Abfluss ($\mathrm{div}F(x, y) < 0$) entspricht
- Für reale Flüssigkeiten muss logischerweise überall $\mathrm{div}F(x, y) = 0$ gelten

# Was ist Rotation?
- $\mathrm{curl}F(x, y)$ gibt an, wie sehr die imaginäre Flüssigkeit um den Ort "rotiert"
- $\mathrm{curl}F(x, y) < 0$ für "Drehung" im und $\mathrm{curl}F(x, y) > 0$ gegen den Uhrzeigersinn

# Die Maxwell-Gleichungen
- Die [[Maxwell-Gleichungen]] lassen sich mit $\mathrm{div}$ und $\mathrm{curl}$ umschreiben:$$\mathrm{div} E = \frac{\rho}{\epsilon_0}, \space \mathrm{curl} E = -\frac{\partial B}{\partial t}$$$$\mathrm{div} B = 0, \space \mathrm{curl} B = \mu_0\left(J + \epsilon_0\frac{\partial E}{\partial t}\right)$$

# Dynamische Systeme