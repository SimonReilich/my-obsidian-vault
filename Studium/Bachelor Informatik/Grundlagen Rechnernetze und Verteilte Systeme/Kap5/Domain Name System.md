---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs #Atomic 
# Definition
Das Domain Name System (DNS) besteht aus drei wesentlichen Komponenten:
- Der Domain Namespace ist ein hierarchisch aufgebauter Namensraum, und hat eine baumartige Struktur.
- Der Nameserver speichern Informationen über den Namensraum, jeder Server kennt nur kleine Ausschnitte des Namensraums.
- Resolver sind Programme, die durch Anfragen an Nameserver Informationen aus dem Namespace extrahieren, und anfragenden Clients bzw. Anwendungen zur Verfügung stellen

Gleichzeitig abstrahiert DNS von [[IP-Adresse|IP-Adressen]], d. h. anstelle die [[IP-Adresse]] eines Servers z. B. im Emailprogramm konfigurieren zu müssen, kann sein Name angegeben werden. Die [[IP-Adresse]] kann sich damit sogar ändern, ohne dass die Konfiguration des Mailprogramms geändert werden muss.