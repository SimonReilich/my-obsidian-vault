---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs 
# Definition
Bei CRC handelt es sich um eine Familie fehlererkennender Codes. Mit ihrem Einsatz werden folgende Ziele verfolgt:
- Eine große Anzahl von Fehlern (Einbit-, Mehrbit-, Burstfehler) sollen erkannt werden.
- Die zugefügte Redundanz soll gering sein.
- Fehler sollen lediglich erkannt aber nicht korrigiert werden können.

# Grundlagen
Ein Datenwort der Länge n bit lässt sich darstellen als [[Polynom]]
$$ a(x) = \sum_{i = 0}^{n - 1} a_i x^i \text{ mit } a_i \in \mathbb{F}_2 \text{ mit } \mathbb{F}_2 = \{0, 1\} $$
Alle Datenworte der Länge genau n bit bilden die Menge
$$ F_q[x] = \{ a \mid a(x) = \sum_{i = 0}^{n - 1} a_i x^i, a_i \in \mathbb{F}_2 \} $$
Zusammen mit passend definierter [[Addition]] und [[Multiplikation]] entsteht ein sog. endlicher [[Körper]] (finite extension field) $⟨Fq[x], + ,·⟩$ mit $q = 2n$ Elementen, auf dem die üblichen Regeln zur [[Addition]] und [[Multiplikation]] gelten.

Was heißt "passend deffiniert"?
- [[Summe]]: Für die [[Summe]] zweier beliebiger $a,b ∈ Fq [x]$ erhalten wir$$c(x) = a(x) + b(x) = \sum_{i = 0}^{n - 1} ( a_i + b_i ) x^i$$wobei für die [[Summe]] der Koeffizienten die [[Addition]] des $GF(2)$ gilt, d. h. die [[Summe]] zweier Datenwörter entspricht einer bitweisen [[XOR]]-Verknüpfung
- Produkt: Das Produkt ist komplizierter, da für $d(x) = a(x) · b(x)$ der Grad von $d(x)$ im Allgemeinen größer als $n − 1$ ist und damit $d(x) \notin Fq [x]$. Daher wählt man ein Reduktionspolynom $r(x)$ mit $grad(r(x)) = n$ und definiert das Produkt von $a,b ∈ Fq [x]$ als$$d(x) = (a(x) · b(x)) mod r(x)$$Dies entspricht einer normalen Polynommultiplikation (wobei die Addition einer [[XOR]]-Verknüpfung entspricht) mit anschließender [[Modulo]]-Operation über $r(x)$. Die [[Modulo]]-Operation entspricht einer [[Polynomdivision]] mit dem Divisionsrest als Ergebnis. Dies sorgt dafür, dass $grad(d(x)) < n$ ist.

Anmerkungen:
- Wählt man für $r(x)$ ein irreduzibles [[Polynom]], d. h. heißt $r(x)$ kann nicht als Produkt zweier $a,b ∈ F_q [x]$ dargestellt werden, so erhält man einen endlichen [[Körper]] mit $q = 2n$ Elementen
- Für CRC wählt man häufig $r(x) = p(x)(x + 1)$ mit $p ∈ F_q [x]$ als Reduktionspolynom von Grad $n$:
	- Sowohl $p(x)$ als auch $x + 1$ sind Elemente von $F_q [x]$ und $r(x)$ ist als Produkt zweier solcher Elemente offensichtlich nicht irreduzibel.
	- Mit dieser Wahl von $r(x)$ ist $⟨Fq [x], + ,·⟩$ kein endlicher [[Körper]].
	- Diese Wahl von $r(x)$ ermöglicht es jedoch, alle ungeradzahligen Fehler zu erkennen.
	- Die Wahl von $r(x)$ bestimmt also nicht nur die Länge der Prüfsumme, sondern auch maßgeblich die Fehlererkennungseigenschaften

# Funktionsweise
- CRC berechnet zu einem gegebenen Datenblock (z. B. L2-PDU) eine Checksumme fester Länge.
- Codewörter sind [[Polynom|Polynome]] $a ∈ F_q [x]$.
- Der Grad $n$ des Reduktionspolynoms $r(x)$ bestimmt den maximalen Grad $n − 1$ aller möglichen Codewörter $a ∈ F_q [x]$ sowie welche Arten von Bitfehlern (Einbit-, Mehrbit-, Burstfehler) erkannt werden können.
- Ethernet verwendet CRC-32 mit dem Reduktionspolynom$$r(x) = x^{32} + x^{26} + x^{23} + x^{22} + x^{16} + x^{12} + x^{11} + x^{10} + x^8 + x^7 + x^5 + x^4 + x^2 + x + 1$$
- Angenommen wir haben ein Reduktionspolynom $r(x)$ des Grads $n$ und eine Nachricht $m(x)$ des Grads $k$ (d. h. die Nachricht besteht aus $k + 1$ bit), die mittels CRC gesichert werden soll:
	1. Hänge $n$ Nullen an $m(x)$ an: $m'(x) = m(x) · x^n$
	2. Bestimme den Divisionsrest $c(x) = m'(x) \mod r(x)$, welcher der Prüfsumme entspricht
	3. Die zu sendende Nachricht besteht aus der [[Summe]] $s(x) = m'(x) + c(x)$
- Der Empfänger prüft die eingehende Nachricht $s'(x) = s(x) + e(x)$, welche möglicherweise einen Übertragungsfehler $e(x) \neq 0$ enthält:
	1. Er bestimmt den Divisionsrest $c'(x) = s'(x) \mod r(x) = (s(x) + e(x)) \mod r(x)$
	2. Ist $c'(x) = 0$, so ist mit hoher Wahrscheinlichkeit kein Übertragungsfehler aufgetreten. Ist $c'(x) \neq 0$, so ist sicher ein Fehler aufgetreten.