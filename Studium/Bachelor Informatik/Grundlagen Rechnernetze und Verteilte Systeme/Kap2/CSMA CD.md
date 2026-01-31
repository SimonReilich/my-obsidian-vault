---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs 
# Definition
Variante von [[Carrier Sense Multiple Access]] mit folgender Abwandlung:
- Erkenne Kollisionen und wiederhole die Übertragung, wenn eine Kollision erkannt wird
- Verzichte auf das Senden von Bestätigungen
- Wird keine Kollision erkannt, gilt die Übertragung als erfolgreich
- Problem: Der Sender muss die Kollision erkennen, während er noch überträgt

# Vorraussetzung
Angenommen zwei Stationen $i$ und $j$ kommunizieren über eine Distanz d mittels [[CSMA CD]]. Damit Kollisionen erkannt werden können, müssen Nachrichten folgende Mindestlänge $L_{min}$ aufweisen:
$$ L_{min} = {2d \over νc_0} r $$
(mit $r =$ [[Übertragungsrate]])

![[Vorraussetzung CSMA CD.png]]

Wird 1-persistentes [[Carrier Sense Multiple Access]] mit Kollisionserkennung verwendet, ergibt sich folgendes Problem:
- Die Kollision zerstört die Nachrichten beider in die Kollision verwickelten Stationen.
- Mind. eine der Stationen sendet ein JAM-Signal.
- Nachdem das Medium frei wird, wiederholen beide Stationen die Übertragung
⇒ Es kommt sofort wieder zu einer Kollision, Lösung: [[Binary Exponential Backoff]] 