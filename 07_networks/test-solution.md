# 7. Netzwerke - Test (Musterlösung) (100 Punkte)

## 7.1 MAC-Adresse (10 Punkte)
Wozu wird die MAC-Adresse benötigt?

*Lösung:*
Die MAC-Adresse dient der Identifikation einer Netzwerkkarte im lokalen Netz (LAN) und ist spezifisch für das Ethernet-Protokoll.

## 7.2 Bitbreite von IPv4- und IPv6-Adressen (10 Punkte)
Wie breit (in Bit) ist eine IPv4- bzw. eine IPv6-Adresse?

*Lösung:*
IPv4-Adressen haben 32, IPv6-Adressen 128 Bit.

## 7.3 NAT (10 Punkte)
Was versteht man unter NAT?

*Lösung:*
Bei NAT (Network Address Translation) werden mehrere Rechner in einem Netz hinter einer einzigen IP-Adresse verborgen.

## 7.4 ARP (10 Punkte)
Welchem Zweck dient ARP?

*Lösung:*
Um ein IP-Paket zustellen zu können, muss der Router die IP-Adresse zu der MAC-Adresse des Ziel-Hosts auflösen. Hierzu wird das *Address Resolution Protocol (ARP)* verwendet.

## 7.5 Anhängsel an URL (10 Punkte)
Warum muss man manchmal an eine URL noch eine Zahl mit Doppelpunkt anhängen, z.B. `http://joe.cs.hs-mannheim.de:8080`?

*Lösung:*
Manchmal läuft ein Dienst nicht auf dem Standard-Port. In diesem Fall, muss der Port zusätzlich mit angegeben werden. D.h. bei der angehängten Zahl handelt es sich um den Port des Webservers.

## 7.6 Netzmaske berchnen (15 Punkte)
Gegeben sei ein IPv4-Netz mit einer /16-Netzmaske. Bestimmen Sie bitte für die IP-Adresse `8.8.19.240` die Netz-Adresse.

*Lösung:*
Das die Netzmaske auf einer Byte-Grenze liegt, lässt sich die Netz-Adresse einfach als `8.8.0.0` bestimmen.

## 7.7 TCP vs. UDP (15 Punkte)
Welche Unterschiede gibt es zwischen TCP und UDP?

*Lösung:*
TCP ist verbindungsorientiert und zuverlässig, UDP hingegen paketorientiert und unzuverlässig. Zuverlässig bzw. unzuverlässig bedeutet, dass die Fehlerkorrektur bei UDP Sache des Programmierers, bei TCP hingegen des Protokolls ist.

## 7.8 Multicast (10 Punkte)
Was versteht man im Rahmen von Netzwerken unter *Multicast*? Geben Sie bitte auch ein Beispiel.

*Lösung:*
*Multicast* (Einer-an-Viele) - Ein Sender sendet an eine ausgewählte Menge von Empfänger, z.B. Telefonkonferenz, Video on demand.

## 7.9 Hidden-Station-Problem (10 Punkte)
Was ist das Hidden-Station-Problem, auch Hidden-Node-Problem genannt?

  * [ ] Eine Station ist vor allen Teilnehmern und dem Access-Point (AP) verborgen
  * [X] Der Access-Point (AP) sieht eine Station, andere Teilnehmer im Netz können sie nicht sehen
  * [ ] Eine Station versteckt sich absichtlich vor anderen
  * [ ] Eine Station sieht weder die anderen Teilnehmer, noch den Access-Point (AP)

