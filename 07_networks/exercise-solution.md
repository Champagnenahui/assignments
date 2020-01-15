# 7. Netzwerke - Übungen (Musterlösung)

## 7.1 Datentransferrate
Wie lange braucht man, um einen Roman mit 300 Seiten, codiert in Unicode (UCS2) bei einer Datentransferrate von 54 Mbit/s zu übertragen?

*Lösung:*
Bei einem Buch sind 30 Zeilen mit jeweils 60 Zeichen üblich. Bei einer Kodierung mit UCS2 benötigt jedes Zeichen 2 Byte. Damit ergibt sich für das Buch eine Größe von 30 * 60 * 2 * 300 = 1.080.000 Byte = 1,03 MB. Bei einer Datenrate von 54 MBit/s können theoretisch maximal 6,75 MByte/s übertragen werden. Das Buch wäre also nach 0,15s oder 150 msec übertragen.

## 7.2 MAC-Adresse
Wieso hat die Netzwerkkarte in Ihrem Rechner zusätzlich zur IP-Adresse auch noch eine MAC-Adresse? Wie hängen die beiden zusammen? 

*Lösung:*
Die MAC-Adresse dient der Identifikation einer Netzwerkkarte im lokalen Netz (LAN) und ist spezifisch für das Ethernet-Protokoll. Die IP-Adresse dient der Identifikation im Internet und ist nicht an ein physikalisches Medium gebunden. MAC- und IP-Adresse liegen auf unterschiedlichen Ebenen des OSI-Referenzmodells. Die MAC-Adresse ist dem Data Link Layer zuzuordnen, die IP-Adresse dem Network-Layer.

## 7.3 MAC statt IP
Angenommen, es hätte das Ethernet-Protokoll schon zu der Zeit gegeben, als das Internet entwickelt wurde: Hätte es nicht gereicht, einfach die MAC-Adresse zu verwenden und ganz auf die IP zu verzichten?

*Lösung:*
Nein, die MAC-Adresse hätte nicht gereicht, weil sie nicht hierarchisch aufgebaut ist, d.h. sie erlaubt es nicht, ein Routing anhand von Teilen der Adresse durchzuführen. Damit wären die Router komplett überfordert, weil die Routing-Tabellen jede einzelne MAC-Adresse aufführen müssten.

## 7.4 NAT
Wieso hat die Einführung von *NAT* die Knappheit bei den IPv4-Adressen etwas gemildert?

*Lösung:*
Bei NAT (Network Address Translation) werden mehrere Rechner in einem Netz hinter einer einzigen IP-Adresse verborgen. Die Rechner innerhalb des Netzes bekommen eine IP-Adresse aus den privaten Adressbereich und benötigen daher keine der knappen IPv4-Adressen. Nur für den Router, der das NAT durchführt ist eine öffentliche IP-Adresse nötig.

## 7.5 Spezielle Adressen
Was ist das Besondere an den IP-Adressen `192.168.*.*`, `10.*.*.*`, `127.0.0.1`?

*Lösung:*
Bei den Adressen `192.168.*.*`, `10.*.*.*` handelt es sich um sogenannte private Adressen, die im Internet nicht geroutet werden. Diese Adressen darf jeder in seinem eigenen Netz frei verwenden. Die Adresse `127.0.0.1` ist ebenfalls reserviert, bezieht sich aber immer auf den eigenen Rechner.

## 7.6 Hidden-Station-Problem
Was ist das Hidden-Station-Problem, auch Hidden-Node-Problem genannt?

*Lösung:*
Das Hidden-Station-Problem liegt vor, wenn eine Station zwar vom Access-Point (AP) aus gesehen wird aber die anderen Teilnehmer im Netz sie nicht sehen können. Damit einher gehen Schwierigkeiten bei der Erkennung von Kollisionen.

## 7.7 CSMA/CD im WLAN
Warum kann man das CSMA/CD-Protokoll nicht in einem WLAN verwenden?

*Lösung:*
Im WLAN wird das CSMA/CA-Protokoll verwendet. Beim CSMA/CD müssen die Teilnehmer eine Kollision erkennen, was aber bei einem WLAN wegen des Hidden-Station-Problems schwierig ist. Die Knoten können nicht erkennen, dass sie eine Kollision mit einer Hidden-Station vorliegt und so käme es zu Problemen. Beim CSMA/CA-Protokoll senden die Knoten nur, wenn sie keine Kommunikation auf dem Medium entdecken können.

## 7.8 IPv6 Adressraum
IPv4 benutzt 32-Bit-Adressen, die inzwischen nicht mehr ausreichen, um alle Geräte im Internet zu adressieren. IPv6 setzt 128-Bit-Adressen ein. Ist dies diesmal ausreichend oder wird es in der Zukunft wieder zu Knappheit der Adressen kommen? Begründen Sie Ihre Antwort.

*Lösung:*
128 Bit-Adressen werden mehr als ausreichen. Damit lassen sich 2^128 einzelne Hosts adressieren, das entspricht ungefähr 10^38. Diese Zahl ist ausreichend, um jedem Atom in der Erdkruste eine eigene IPv6-Adresse zu geben oder jedem Quadratmillimeter der Erdoberfläche (Erdoberfläche ca. 510.000.00 km^2) 6.6*10^24 Adressen zuzuweisen. Somit ist es höchst unwahrscheinlich, dass die Adressen nicht reichen könnten.

## 7.9 Bridge vs. Router vs. Switch
Erläutern Sie bitte kurz die Unterschiede zwischen einer Bridge, einem Router und einem Switch.

*Lösung:*
Eine Bridge verbindet zwei Netzwerksegmente und arbeitet auf OSI-Level 2, der Sicherungsschicht. Ein Router verbindet verschiedene Subnetze miteinander. Er hat in jedem Subnetz ein Interface mit MAC- und IP-Adresse. Er arbeitet auf OSI-Layer 3 (Vermittlungsschicht). Ein Switch arbeitet in einem einzigen Netzwerksegment und verteilt die Ethernet-Pakete an die einzelnen Hosts.

## 7.10 Hub oder Switch
Wenn Sie die Wahl hätten, einen Hub oder einen Switch einzusetzen, welche Komponente würden Sie (unter der Annahme gleicher Kosten) einsetzen? Begründen Sie Ihre Antwort kurz.

*Lösung:*
Man sollte einen Switch einsetzen, weil bei einem Switch die Datenpakete nur an die Ports gesendet werden, an denen die Adressaten angeschlossen sind. Ein Hub sendet die Pakete immer an alle Ports. Damit vermeidet ein Switch zum einen Netzwerkkollisionen und ist zum anderen sicherer.

## 7.11 Fehlerkorrektur in UDP
Mit welchem Verfahren behandelt UDP das Auftreten eines Fehlers, z.B. ein verlorenes oder ein doppelt empfangenes Paket? Was ist der Unterschied zwischen UDP und TCP?

*Lösung:*
Das UPD-Protokoll kennt keine Fehlerkorrektur. Es ist der Anwendung überlassen, auftretende Fehler zu korrigieren.

TCP ist verbindungsorientiert und zuverlässig, UDP hingegen paketorientiert und unzuverlässig. Zuverlässig bzw. unzuverlässig bedeutet, dass die Fehlerkorrektur bei UDP Sache des Programmierers, bei TCP hingegen des Protokolls ist.

## 7.12 ARP
Um ein IP-Paket zustellen zu können, muss der Router die IP-Adresse zu der MAC-Adresse des Ziel-Hosts auflösen. Hierzu wird das *Address Resolution Protocol (ARP)* verwendet. Beschreiben Sie bitte grob, wie eine solche Auflösung abläuft.

*Lösung:*
  * Broadcast im LAN an ff:ff:ff:ff:ff:ff fragt nach Rechner mit passender IP-Adresse
  * Rechner mit der IP-Adresse antwortet mit seiner MAC-Adresse 
  * Router speichert die Zuordnung (cache) für eine gewisse Zeit
  * Router kann dann das Paket dorthin ausliefern

## 7.13 Unicast / Multicast / Braodcast
Man unterscheidet im Rahmen von Netzwerken zwischen *Unicast*, *Broadcast* und *Multicast*. Bitte erläutern Sie was diese Begriffe bezeichnen und worin die Unterschiede bestehen. Geben Sie jeweils ein Beispiel.

*Lösung:*
  * *Unicast* (Punkt-zu-Punkt-Übertragung) - Genau zwei Teilnehmer kommunizieren direkt miteinander, z.B. Telefon.
  * *Broadcast* (Einer-an-Alle) - Ein Sender sendet Daten an alle Empfänger innerhalb eines Netzwerkes, z.B. Radio, Fernsehen.
  * *Multicast* (Einer-an-Viele) - Ein Sender sendet an eine ausgewählte Menge von Empfänger, z.B. Telefonkonferenz, Video on demand.

## 7.14 Netzmaske
Im Rahmen des Internet Protocols Version 4 (IPv4) taucht immer wieder die sogenannte __Netzmaske__ auf. Beschreiben Sie bitten welchem Zweck die Netzmaske dient, wie sie aufgebaut ist und wie man sie notieren kann.

*Lösung:*
Beim CIDR wird der Netzwerk und Host-Teil der IP-Adresse durch eine Netzmaske festgelegt und nicht mehr aus der Klasse des Netzes abgeleitet. So kann die Aufteilung zwischen Netz und Host variable erfolgen. Die Netzmaske gibt an, welche Bits der IP-Adresse zum Netz-Teil gehören. Hierzu kann man sie entweder wie eine IP-Adresse als 4 Byte schreiben (z.B. `255.255.255.0`) oder man gibt einfach die Anzahl der Bits in der Form `/ANZAHL` (z.B. `/8`) an.

## 7.15 Netzmaske berechnen
Gegeben sei ein IPv4-Netz mit einer /12-Netzmaske. Bestimmen Sie bitte für die IP-Adresse `192.168.64.86` die Netzadresse.

*Lösung:*
```console
Adresse       11000000.10101000.01000000.01010110
Netzmaske &   11111111.11110000.00000000.00000000
------------------------------------------------
Netzadresse   11000000.10100000.00000000.00000000
```

Damit ist die Netzadresse 192.160.0.0

## 7.16 Netzmaske berechnen
Gegeben sei ein IPv4-Netz mit einer /16-Netzmaske. Bestimmen Sie bitte für die IP-Adresse `192.168.64.240` die Netz-Adresse.

*Lösung:*
Das die Netzmaske auf einer Byte-Grenze liegt, lässt sich die Netz-Adresse einfach als `192.168.0.0` bestimmen.

## 7.17 Routing
Eine wichtige Eigenschaft des Internets ist das sogenannte __Routing__. Erläutern Sie bitte kurz, was sich hinter dem Begriff Routing verbirgt.

*Lösung:*
Beim Routing handelt es sich darum, dass die Pakete im Internet anhand der IP-Adresse in unterschiedliche Richtungen weitergeleitet werden. D.h. ein Router liest die IP-Adresse, schaut in einer Routing-Tabelle nach, wohin Pakete mit bestimmten IP-Adress-Bereichen geleitet werden sollen und übergibt das Paket dann an einen der Router mit denen er verbunden ist.

## 7.18 Dynamisches Routing
Erläutern Sie bitte kurz, warum ein paktvermitteltes Netz eine Grundvoraussetzung für das dynamische Routing von Daten im Netzwerk ist.

*Lösung:*
Wenn die Daten nicht als einzelne Pakete übertragen werden, besteht auch keine Möglichkeit, einzelne Teile (Pakete) andere Wege nehmen zu lassen. Somit ist dynamisches Routing nur in einem paketvermittelten Netz möglich.

## 7.19 Ports
Sowohl TCP als auch UDP verwenden sogenannte __Ports__. Erläutern Sie bitte, welchem Zweck die Ports bei TCP und UDP dienen. Geben Sie Ihnen bekannte Ports an.

*Lösung:*
Ein Host ist im Internet eindeutig über seine IP-Adresse ansprechbar. Da aber auf einem Host mehrere Dienste angeboten werden können, muss es eine Information geben, welcher Dienst gemeint ist. Deshalb gibt es zusätzlich zur IP-Adresse noch den Port. Das Tupel IP:Port beschreibt dann einen Dienst im Internet eindeutig. Unter welchem Port ein Dienst angesprochen wird ist für die Ports < 1024 standardisiert: HTTP 80, SSH 22, SMTP 25 etc.

## 7.20 Verbindung in TCP
Das __Transmission Control Protocol (TCP)__ ist verbindungsorientiert und zuverlässig. Erläutern Sie bitte, wie es TCP gelingt eine Verbindung und die Zuverlässigkeit der Kommunikation auf Grundlage des paketvermittelten IP-Protokolls zu realisieren.

*Lösung:*
Die Verbindung wird durch den Austausch bestimmter Nachrichten aufgebaut und beleibt solange bestehen, bis sie explizit geschlossen wird oder durch eine Timeout ausläuft. Die Zuverlässigkeit wird dadurch erreicht, dass jedes Datenpaket bestätigt (acknowledgement) wird. Geht für ein Paket keine Bestätigung ein, wird es erneut gesendet. Es gibt Prüfsummen für die TCP-Header und die Daten, sodass korrupte Pakete erkannt werden. Jedes Datenpaket hat eine Sequenznummer, damit der Empfänger die Daten sortieren und doppelte Pakete löschen kann. 

## 7.21 DHCP
Ein wichtiges Protokoll im Rahmen des Internet ist *DHCP*. Beschreiben Sie bitte kurz, um was es sich bei DHCP handelt und wie das Protokoll funktioniert.

*Lösung:*
DHCP (Dynamic Host Configuration Protocol) ist ein Protokoll, um Hosts in einem Netz dynamisch eine IP-Adresse zuzuordnen. Hierzu gibt es einen (DHCP-) Server, der die Adressen verwaltet und sie den Clients zuweist.

