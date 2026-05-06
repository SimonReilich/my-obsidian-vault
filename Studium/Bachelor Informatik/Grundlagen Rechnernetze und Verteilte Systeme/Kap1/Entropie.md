---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs 

# Definition
Den mittleren [[Informationsgehalt]] einer Quelle $\mathcal{X}$ bezeichnet man als Entropie $H(X)$, wobei $X$ eine [[Zufallsvariablen|Zufallsvariable]] ist, die mit der jeweiligen Emittierungs-Wahrscheinlichkeit den Wert des Zeichens annimmt.
$$H(X) := \sum_{x \in X}p(x)*I(x) = - \sum_{x \in X} p(x) * log_2(p(x))$$

# Bedingte Entropie
Die bedingte Entropie zweier Zufallsvariablen $X$ und $Y$
$$H(X \mid Y) := \sum_{x \in X}p(x)H(Y \mid X = x) = - \sum_{x \in X} p(x) \sum_{y \in Y}p(y \mid x) log_2(p(y \mid x))$$ entspricht der verbleibenden Unsicherheit von $Y$, wenn $X$ bekannt ist.

## Beobachtung
- Sind $X$ und $Y$ voneinander abhängig, dann ist die bedingte Entropie kleiner als im unabhängigen Fall.
- Sind $X$ und $Y$ voneinander unabhängig und ist der Ausgang von $X$ bereits bekannt, so bleibt die Entropie von $Y$ vollständig erhalten.

# Verbundentropie
Sei $p(x, y)$ die [[Verbunddichte]] zweier [[Zufallsvariablen]] $X$  und $Y$, d.h.
$$ p(x, y) = Pr[X = x | Y = y] * Pr[Y = y] $$
Dann ist die Verbundenthropie $H(X, Y)$ definiert als
$$ H(X, Y) := -\sum_{x \in X} \sum_{y \in Y} p(x, y) * \log_2(p(x, y)) $$

## Berechnung der Verbundenthropie und der bedingten Enthropie
Die Verbundentropie $H(X,Y)$ entsteht aus der Addition der Quellenentropie $H(X)$ mit dem von dieser Quelle statistisch unabhängigen Anteil $H(Y |X)$ einer anderen Quelle:
$$H(X,Y ) = H(X) + H(Y |X)$$
Die bedingte Entropie $H(Y |X)$ errechnet sich aus den Auftrittswahrscheinlichkeiten $p(x, y)$ und $p(y)$ :
$$H(Y |X) = − \sum_{x \in X} \sum_{y \in Y} p(X = x,Y = y) * \log_2 (p(Y = y|X = x))$$
