---
aliases:
lecture: "[[Grundlagen Datenbanken]]"
---
#Bachelor #Informatik #GDB
# Grundlagen des Relationalen Modells:
- Domänen $D_1, D_2, ..., D_n$ (Wertebereiche)
- Relationen: $R \subseteq D_1 \times D_2 \times ... \times D_n$ (Teilmenge des Kreuzprodukts über Domänen)
- Tupel $t \in R$
- Schema legt die Struktur der gespeicherten Daten fest 
- Relationenname: {\[Attributname: Datentyp]} (Primärschlüssel wird unterstrichen)
- Ausprägung: Der aktuelle Zustand der Datenbasis
- Schlüssel: minimale Menge von Attributen, deren Werte ein Tupel eindeutig identifizieren
# Verfeinerung des Schemas:
- Regel: Relationen mit gleichem Schlüssel kann man zusammenfassen 
- Aber nur diese und keine anderen!
# Relationale Algebra:
- $\sigma_{\theta}$ Selektion
- $\pi_{D_1, ..., D_n}$ Projektion
- $\bowtie_{\theta}$ (Theta) Join
- $\rho_{B <- A}$ Umbenennung
- $\div$ Mengendivision
- ⋉ / ⋊ Semi-Join (linkes / rechtes Argument wird gefiltert)
- ⟗ äußerer Join
- $\rhd$/$\lhd$ Anti-Join (linkes/rechtes Argument wird gefiltert)
- $\gamma_{\text{Gruppe; Attribute}}$ Gruppierung und Aggregation
# Das Relationenkalkül / Tupelkalkül
- Eine Anfrage im Relationenkalkül hat die Form $\{t \mid P(t)\}$ mit $P(t)$ Formel.
- Beispiel C4-Professoren: $\{p \mid p \in \text{Professoren} \land \text{p.Rang} = \text{'C4'}\}$
- In der Formel ist Logik erster und zweiter Ordnung erlaubt
# Das Domänenkalkül
- Ein Ausdruck des Domänenkalküls hat die Form $\{[v_1, v_2 , ..., v_n]\mid P (v_1 ,..., v_n)\}$ mit $v_1 ,..., v_n$ Domänenvariablen und $P$ Formel.
- Beispiel MatrNr und Namen der Prüflinge von Curie: $\{[m, n] \mid \exists ([m, n, s] \in \text{Studenten} \land \exists v, p, g ([m, v, p, g] \in \text{prüfen} \land \exists a, r, b ([p, a, r, b] \in \text{Professoren} \land a = \text{'Curie'}))]\}$