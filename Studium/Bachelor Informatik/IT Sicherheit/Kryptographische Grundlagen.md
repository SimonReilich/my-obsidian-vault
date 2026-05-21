---
lecture: "[[IT Sicherheit]]"
degree: "[[Bachelor Informatik]]"
---
#BScInfo #Informatik #ITSec 
## Kryptographische Systeme
- Menge der Klartexte $m$, über Alphabet $M$, $m \in M^*$ , z.B. $M= \{0,1\}$.
- Menge der Kryptotexte $c$ über dem Alphabet $C$, $c \in C^*$ z.B. $C=\{0,1\}$.
- $K$ Menge der Schlüssel (engl. key), $e, d \in K$.
- $E = \{E_e | E_e : M^* \to C^* \}$ Familie von Verschlüsselungsverfahren
- $D = \{D_d | D_d : C^* \to M^* \}$ Familie von Entschlüsselungsverfahren.
- $m \in M*$ , $E_e (m) = c$ , $c \in C^*$, dann existiert $d \in K$, so dass $m = D_d (c)$

Zwei Klassen von Verfahren: symmetrisch und asymmetrisch
## Symmetrische Verfahren, Secret-Key Verfahren
- Verfahren in der Regel einfach und schnell zu berechnen.
- e, d sind gleich (symmetrisch) und geheim (Secret Key) 
## Asymmetrische Verfahren, Public-Key Kryptografie
- Verfahren basieren auf Zahlentheorie
- Jede Entität (Person, Gerät,…) besitzt ein eigenes Schlüsselpaar
- $e$ steht für encryption, $d$ steht für decription

Bemerkungen:
- Die privaten Schlüssel müssen vertraulich verwaltet werden, Z.B. Passwort-geschützt auf Festplatte oder auf USB-Stick.
- Asymmetrische Verschlüsselung ist viel aufwändiger als symmetrische. Es werden deshalb in der regel nur kleine Datenvolumen mit asymmetrischen Verfahren verschlüsselt.
- Frage: Was sind mögliche Beispiele für solche Daten? -> Hybride verfahren, Austausch des Symmetrischen Schlüssels über asymmetrische Kryptographie
## Anforderungen an Krypto-Verfahren
- Kerckhoffs-Prinzip: Auguste Kerckhoffs, [[1883]] -> Stärke des Verfahrens sollte nur von der Güte des geheimen Schlüssels abhängen! D.h. Sicherheit darf nicht von Geheimhaltung der Verfahren abhängen, keine Security by Obscurity!
- Konsequenz: Schlüsselraum muss sehr groß sein, um Brute-Force zu verhindern
- Größenordnung für Schlüsselraum:
    - symmetrisch: min 128 Bit, besser 256 Bit
    - assymetrisch, z.B. RSA ≥ 3000 Bit
    - assymetrisch, ECC (Eliptic Curve Cryptography) ≥ 250 Bit
## Blockchiffre
- Klartext m wird in Blöcke 𝑚𝑖 fester Länge, z.B. 128 Bit, aufgeteilt
- Gegeben Klartext $m$, wird aufgeteilt: $m= m_1 || m_2 || … || m_n$
- Blockweises Verschlüsseln mit dem gleichen Schlüssel $k$
- Verschlüsseln: $𝐸_𝑘 (𝑚) = c$, wobei gilt: $c = c_1 || c_2 || … || c_n$ mit $𝑐_𝑖 =𝐸_𝑘 (𝑚_𝑖 )$
- Entschlüsseln: $𝐷_𝑘 (𝑐) = m$, mit $𝑚_𝑖 =𝐷_𝑘 (𝑐_𝑖 )$
- Blockchiffre erfordert Padding, In der Praxis PKCS#7 Padding: Auffüllen mit einer Anzahl von Byte mit jeweils gleichem Wert; Der Wert im Byte entspricht Anzahl der hinzugefügten Bytes
- Designprinzipien für Blockchiffre
	- Diffusion: Jedes Klartext-Bit beeinflusst jedes Ciphertext-Bit; Technik: Bitweise Permutation. z.B. Bitpermutation beim DES-Verfahren
	- Konfusion: Verschleiert Zusammenhang: Schlüssel, Ciphertext; Technik: nicht lineare Substitutionen: $𝑆(𝐴 ⊕ 𝐵) ≠ 𝑆 (𝐴) ⊕ 𝑆(𝐵)$ z.B. S-Box im AES Verfahren  
- Bemerkung: Diffusion u. Konfusion erzeugen Avalanche Effekt (Lawine) -> Kleine Änderung in der Eingabe (z.B. 1 Bit) haben große Auswirkungen auf die Ausgabe (z.B. jedes Bit ändert sich mit 50% Wahrscheinlichkeit)  
## Stromchiffre
- Ziel: Verschlüsselung eines Klartext-Stroms: z.B. Sprache, Verschlüsselung muss schnell sein: in der Praxis mit xor ($⊕$)
- Problem: xor ist keine starke Chiffre!
- Lösung: One-Time Pad, Vernam-Chiffre
- Für jeden Klartext-Strom wird eine individuelle Schlüsselfolge $KS$ als pseudozufällige [[Folge]] von Bits erzeugt.
- Verschlüsselung eines Stroms $m$: $m ⊕ KS$ (bitweise xor) Die Schlüsselfolge $KS$ hat die gleiche Länge wie der Klartext $m$
- Deterministische Generierung von KS, abhängig von Länge und initialem Seed-Wert $k$
- Problem: unterschiedliche Klartexte $m_1, m_2$ erfordern unterschiedliche Schlüsselfolgen! -> k muss sich bei jeder Nachricht ändern, z.B. durch Hochzählen
## Betriebsmodi von Blockchiffren
1. ECB Electronic Code Block Modus
	- Vorteile: Parallelisierung, kleine Fehlerausbreitung
	- Nachteile: Gleiche Klartextblöcke mit gleichem k ergeben gleichen Chiphertext
	- Konsequenz: Muster im Ciphertext -> Kryptoanalyse
2. CBC Cipher Block chaining Modus
	- Vorteile: Ciphertext hängt auch vom Vorgänger ab -> keine Muster
	- (Nachteile: keine Parallelisierung, große Fehlerausbreitung)
	- Aber: Fehler breitet sich über max. 2 Blöcke aus
3. CTR Counter Modus
	- Initialisierung eines Zählers ctr mit Zufallszahl Nonce
	- Zählerstand pro Block $m_i : ctr(i) = ctr(i-1) + 1$
	- Verschlüsselung des i-ten Blockes: $c_i = m_i ⊕ E_k ( \text{Nonce}||ctr(i))$
	- Entschlüsselung des i-ten Blockes: $m_i = c_i ⊕ E_k (\text{Nonce}||ctr(i))$
4. GCM Galois/Counter Modus
	- Verschlüsseln von Blöcken $m_i$, Blocklänge 128 Bit
	- Verschlüsseln durch Blockchiffre im CTR Modus
	- Authentisieren der verschlüsselten Daten durch Multiplikation im Galoiskörper $GF(2128)$ Urhebernachweis
	- Eingaben:
		- Klartext $m$, Schlüssel $k$, $IV$,
		- ggf. zusätzlich noch assoziierte Daten (AD), z.B. Header-Daten GCM liefert auch Authentizität der assoziierten Daten AD  
	- GCM Modus implementiert→die AEAD-Eigenschaft
	- AEAD (Authenticated Encryption with Associated Data) Modus
		- Authentizität des Ciphertextes (AE) und
		- Authentizität assoziierter Daten (AD)
## Asymmetrische Kryptographie
- Anforderung an asymmetrische Verfahren: Für $(𝑒, 𝑑)$ gilt
- $D_d (E_e (m)) = m$, für alle Klartexte $m$.
- $d$ ist der private Schlüssel und muss geheim bleiben.
- $d$ kann aus $e$ nicht effizient berechnet werden.
## RSA
- Berechnung eines RSA Schlüsselpaares $(e,d)$
	1. Wähle 2 große, geheime Primzahlen $p$, $q$ (> 1024 bit)
	2. Berechne RSA-Modul $n = pq$, $n$ ist öffentlich. $p, q$ sind geheim
	3. Berechne $\phi(n) = (p -1)(q -1)$, $\phi(n)$ effizient zu berechnen, da $p,q$ Primzahlen
	4. Wähle $e \in {1, 2, …, \phi(n)-1}$ so, dass gilt $ggT(\phi(n), e) = 1$, $(e, n)$ ist der öffentliche Schlüssel
	5. Berechne den privaten Schlüssel $d$ zu $e$, so dass gilt: $ed = 1 \mod \phi(n)$. $p$ und $q$ sind Trapdoor-Informationen: denn mit $p,q$ kann man $\phi(n)$ berechnen.
- RSA Verschlüsselung→$RSA_e (x) = x^e \mod n = y,\text{ mit }x,y \in ℤ_n$
- RSA Entschlüsselung→$x = RSA_d (y) = y^d \mod n$
## Elliptische Kurven Kryptographie (ECC)
- Elliptische-Kurve (EC)→EC ist eine Punktmenge, die eine Polynomial-Gleichung erfüllt.
- Die Menge der Punkte $\{(𝑥, 𝑦) \mid 𝑥, 𝑦 ∈ \mathbb{Z}_p \}$, für die gilt: $y^2 = x^3 + ax + b \mod p$, so dass $4a^3+27b^2 ≠ 0$. Parameter $a,b$ definieren die Form der jeweiligen Kurve
- Voraussetzungen ECC:
	- Gegeben sei eine Elliptische Kurve $E$ über dem [[Körper]] $\mathbb{Z}_p$.
	- Der [[Körper]] $\mathbb{Z}_p$ ist ein Primzahlkörper.
	- Gegeben sei ein Generator-Element $G$ auf der Kurve $E$  
- ECC - Generieren eines asymmetrischen Schlüsselpaars $(T, d)$:
	- Wähle $d$ und berechne $dG = T$, $d$ geheim ($d$ ist Integer-Wert)
	- $T$ ist ein Punkt auf der Kurve, öffentlicher Schlüssel
- ECC - Verschlüsselung über ECDL-Problem (EC Discrete Log):
	- Finde den Integer-Wert $d$, $1 ≤ d ≤ | E |$, so dass $d = \log_G T$
	- $T = d * G = G + G + ... + G$ ($d$-mal)
## Sicherheitsniveau eines kryptographischen Verfahrens
- symmetrisches kryptographisches Verfahren erreicht ein Sicherheitsniveau von $n$ Bit -> erfolgreiche Angriffe erfordern Aufwand, der der Ausführung von $2^n$ Verschlüsselungen effizienter Blockchiffre entspricht
- asymmetrisches kryptographisches Verfahren erreicht ein Sicherheitsniveau von $n$ Bit -> Der Schlüsselraum ist mindestens $2^n$ Schlüssel groß
# Post Quantum Kryptographie
- Bedrohungen:
	- Symmetrische Verfahren:
		- Mit dem Grover-Algorithmus kann der QC die Berechnungszeit bei der Suche nach dem Schlüssel erheblich beschleunigen
		- Konsequenz: Der Aufwand für Brute-Force wird um die Hälfte reduziert, Schlüssellänge von > 256 Bit nötig.
	- Assymetrische Verfahren:
		- Der Shore-Algorithmus ermöglicht QC sowohl das Faktorisierungs- als auch das Diskreter-Logarithmus-Problem in polynomieller Zeit zu lösenErforderlich für RSA 4096: QC mit mindestens 1 Millionen QBits
- Alle gängigen Verfahren sind unsicher
- Neue Verschlüsselungsverfahren, PQC, sind erforderlich!
- Bemerkung: Store now, Decrypt later -> Sichere Verfahren sind schon jetzt notwendig