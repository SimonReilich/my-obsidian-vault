---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs 

# Definition

Der Informationsgehalt eines [[Symbol|Symbols]] drückt aus, wieviel Information durch das [[Symbol]] übertragen wird.

# Eigenschaften

- Je seltener ein Zeichen auftritt, desto höher ist sein Informationsgehalt.
- Der Informationsgehalt einer Zeichenkette ist die Summe der Informationsgehalte der einzelnen Zeichen
- Der Informationsgehalt eines vorhersagbaren Zeichens ist 0
Die [[Logarithmus]]-Funktion ist die einfachste Funktion zur Definition eines Informationsgehalts mit diesen Eigenschaften.

# Information

Der Informationsgehalt eines Zeichens $x ∈ \mathcal{X}$ aus einem Alphabet $\mathcal{X}$ hängt von der Wahrscheinlichkeit $p(x)$ ab, dass das informationstragende [[Signal]] zum Beobachtungszeitpunkt den diesem Zeichen zugeordneten Wert bzw. Wertebereich annimmt. Der Informationsgehalt $I$ des Zeichens $x$ mit der Auftrittswahrscheinlichkeit $p(x)$ ist definiert als:
$$l(x) = -log_2p(x) \text{ mit } [I] = bit$$
