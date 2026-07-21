---
lecture: "[[Komplexitätstheorie]]"
---
#BScInfo #Informatik #Comp
# Definition ($k$-Band Turingmaschiene)
Eine $k$-Band-Turingmaschine verfügt über insgesamt $k$ unendlich lange, in einzelne Zellen unterteilte Arbeitsbänder. Unter diesen $k$ Bändern befindet sich ein schreibgeschütztes Eingabeband (read-only), ein Ausgabeband sowie eine Reihe von Arbeitsbändern. Für jedes dieser Bänder existiert ein eigener Schreib-/Lesekopf, der sich auf einer individuellen Zelle befindet und Symbole lesen sowie schreiben kann.
Gesteuert wird das System durch ein Register mit einer endlichen Menge von Zuständen, das ein endliches Regelwerk vorgibt, sowie durch ein festgelegtes Vokabular beziehungsweise Alphabet von Symbolen, die auf die Bänder geschrieben werden können.
Die Aktionen der Maschine umfassen das Bewegen der Köpfe (nach links, nach rechts oder Stoppen) sowie das Schreiben von Symbolen in die aktuellen Zellen. Welche konkrete Aktion ausgeführt wird, hängt jeweils vom aktuellen Steuerungszustand der Maschine und den Zeichen ab, die sich genau unter den $k$ Lese-/Schreibköpfen befinden.