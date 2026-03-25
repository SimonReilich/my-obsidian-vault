---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs 

![[Kanal Modell.png]]

# Definition
- Für die [[Entropie]] auf der Empfangsseite (Empfangsentropie) erhalten wir $H(Y ) = H(X) − H(X|Y ) + H(Y |X)$ (Sendeentropie abzüglich eines Informationsverlusts durch den Kanal zuzüglich der Fehlinformation).
- Die transportierte [[Informationsgehalt|Information]] (Transinformation) entspricht der Sendeentropie abzüglich des Informationsverlusts bzw. der Empfangsentropie abzüglich der Fehlinformation.

# Transformation

Die von Sender zu Empfänger über einen gedächtnislosen Kanal transportierte Information bezeichnet man als Transinformation (engl. Mutual Information)
$$ I(X; Y) := H(X) - H(X | Y) = H(Y) - H(Y | X) $$
