---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs 
# Definition
Algorithmus, um zu entscheiden, an welchen Next-[[Hop]] ein Paket weitergeleitet werden soll. Die [[Routingtabelle]] wird von längeren Präfixen (spezifischeren Routen) hin zu kürzeren Präfixen (weniger spezifische Routen) durchsucht. Der erste passende Eintrag liefert das Gateway (Next-Hop) eines Pakets. Diesen Prozess bezeichnet man als Longest Prefix Matching.

# Algorithmus
1. Der [[Router]] berechnet das logische [[AND]] aus der Zieladresse des Pakets und den Subnetzmasken (welche aus der Präfixlänge hervorgehen) in seiner [[Routingtabelle]], in absteigender Präfixlänge.
2. Das Ergebnis wird mit dem Eintrag in der Spalte „Destination“ verglichen.
3. Stimmt das Ergebnis damit überein, werden Gateway und zugehöriges Interface bestimmt.
4. Nachdem die [[MAC-Adresse]] des Gateways ggf. via [[Address Resolution Protocol]] aufgelöst wurde, wird das Paket mit einem neuen [[Ethernet]]-Header versehen und weitergeleitet.