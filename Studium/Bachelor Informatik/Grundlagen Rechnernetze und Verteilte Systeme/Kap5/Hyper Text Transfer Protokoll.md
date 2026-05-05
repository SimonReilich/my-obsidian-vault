---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs #Atomic 
# Definition
HTTP ist in seiner ursprünglichen Form zunächst zustandslos, zwischen unterschiedlichen Anfragen und Antworten besteht daher zunächst kein Zusammenhang. [[Cookies]] ermöglichen es, dass eine Sitzung über mehrere Anfragen und Antworten, Interaktionen und [[Transmission Control Protokoll|TCP]]-Verbindungen hinweg bestehen bleibt. HTTP wird üblicherweise der Anwendungsschicht (Schicht 7) zugeordnet, beinhaltet aber auch Funktionen der Darstellungs- und Sitzungsschicht (Schichten 6/5).

# Methoden
- GET – Anfrage zur Übertragung eines bestimmten Objekts vom Server
- HEAD – Anfrage zur Übertragung des Headers eines bestimmten Objekts (z. B. bestehen Webseiten aus mehreren Sektionen, wovon eine als Header bezeichnet wird)
- PUT – Übertragung eines Objekts vom Client zum Server, welches ggf. ein bereits existierendes Objekt überschreibt
- POST – Übertragung eines Objekts vom Client zum Server, welches ggf. an ein bereits existierendes Objekt angehängt wird (z. B. Anhängen von Text)
- DELETE – Löschen eines Objekts vom Server

# Status-Codes
- 200 – OK
- 3xx – Redirection
- 400 – Bad Request
- 401 – Unauthorized
- 403 – Forbidden
- 404 – Not Found
- 418 – I’m a teapot (RFC 2324)
- 5xx – Server Error
- etc