---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#BScInfo #Informatik #GRnVs 
# Definition
Uniform Resource Locator (URL) sind Adressangaben der Form
```
<protocol>://[<username>[:<password>]@]<fqdn>[:<port>][/<path>][?<query>][#<fragment>]
```
- protocol gibt das Anwendungsprotokoll an, z. B. HTTP(S), FTP, SMTP, etc.
- username und password ermöglicht die optionale Angabe eines Benutzernamens und Kennworts
- fqdn ist der vollqualifizierte Domain Name , der das Ziel auf Schicht 3 identifiziert.
- port ermöglicht die optionale Angabe einer vom jeweiligen well-known Port abweichenden Portnummer für das Transportprotokoll.
- fragment ermöglicht es einzelne Fragmente bzw. Abschnitte in einem Dokument zu referenzieren
- /<path> ermöglicht die Angabe eines Pfads auf dem Ziel relativ zur Wurzel </> der Verzeichnisstruktur.
• ?<query>path ermöglicht die Angabe eines Pfads auf dem Ziel relativ zur Wurzel der Verzeichnisstruktur 
- query ermöglicht die Übergabe von Variablen in der Form <variable>=<value>. Variablen können mittels & konkateniert werden.