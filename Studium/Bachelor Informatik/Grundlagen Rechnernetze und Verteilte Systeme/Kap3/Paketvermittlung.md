---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs 
# Definition
Unterschiede zur [[Nachrichtenvermittlung]]:
- Nachrichten werden nicht mehr als Einheit übertragen sondern in kleinere Einheiten, den Datenteilen von Paketen, unterteilt
- Jedes Paket wird mit einem eigenen Header versehen, der alle Informationen zur Weiterleitung und ggf. auch zur Reassemblierung enthält
- Pakete werden unabhängig voneinander vermittelt, d. h. Pakete derselben Nachricht können über unterschiedliche Wege zum Empfänger gelangen.
- Im Allgemeinen müssen die einzelnen Pakete nicht gleich groß sein, es gibt aber [[Anforderungen]] an die maximale Paketgröße einhergehend mit Datenteilen maximaler Länge $p_{max}$

![[Ablauf Paketvermittlung.png]]

Durch die Vermittlung kleiner Pakete statt langer Nachrichten werden Engpässe fairer genutzt, gehen Pakete verloren, müssen nur Teile einer größeren Nachricht wiederholt werden. Flexibles [[Zeitmultiplex]] einzelner Pakete