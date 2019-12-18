# 10. IT-Sicherheit - Test (Musterlösung) (100 Punkte)

## 10.1 Symmetrische und Asymmetrische Verschlüsselung (15 Punkte)
Was ist der Unterschied zwischen symmetrischer und asymmetrischer Verschlüsselung? Geben Sie Beispiele für entsprechende Verfahren/Algorithmen.

*Lösung:*
  - *Symmetrische* Verschlüsselung: Verschlüsselungsverfahren, die für Ver- und Entschlüsselung den gleichen Schlüssel verwenden. Beispiele: DES (Data Encryption Standard), AES (Advanced Encryption Standard)
  - *Asymmetrische* Verschlüsselung: Verschlüsselungsverfahren, bei denen für Ver- und Entschlüsselung unterschiedliche Schlüssel verwendet werden; vom "öffentlichen" Schlüssel (der für die Verschlüsselung verwendet wird) kann man nicht auf den "privaten" Schlüssel (der für die Entschlüsselung verwendet wird) schließen. Beispiele: RSA (Rivest-Shamir-Adleman) , ECDL (Elliptic Curve Discrete Logarithm)

## 10.2 Challenge-Response-Verfahren (20 Punkte)
Erläutern Sie kurz in eigenen Worten, wie ein Challenge-Response-Verfahren funktioniert und geben Sie ein Beispiel für ein solches Verfahren.

*Lösung:*
Im folgenden wird die Authentifizierung von Alice gegenüber Bob mithilfe eines Challenge-Response-Verfahrens dargestellt:

  1. Alice und Bob besitzen ein gemeinsames Geheimnis S
  2. Alice sendet Bob eine Aufforderung zum Senden der Challenge
  3. Bob sendet Alice eine Zufallszahl Z und berechnet ein Ergebnis E mithilfe einer Einwegfunktion E = F(Z, S)
  4. Alice empfängt eine Zufallszahl Z von Bob
  5. Alice berechnet das Ergebnis E der E = Einwegfunktion F(Z, S)
  6. Alice sendet E an Bob
  7. Bob vergleicht das empfangene E mit seinem selbst berechneten E. Stimmen beide überein, ist Alice wirklich Alice und damit authentifiziert

Ein Beispiel für ein solches Verfahren sind Funkschlüssel oder Garagentoröffner.

## 10.3 Digitale Signatur (10 Punkte)
Wofür kann man die Technologie der "Digitalen Signatur" (im kryptographischen Sinn) einsetzen?

  * [X] Nachweis des Authors eines elektronischen Dokumenten
  * [ ] Verschlüsselung von Dokumenten
  * [X] Integrität und Authentizität von Software-Installationspaketen bei der Installation
  * [ ] Sicherer Austausch von Schlüsseln zwischen Kommunikationspartnern
  * [ ] Sicheres Komprimieren von Dokumenten
  * [X] Nachweis, dass ein elektronisches Dokument nicht verändert wurde

## 10.4 Sichere Passwörter (15 Punkte)
Welche der Passwörter sind sicher?

  * [ ] qwertzuiop
  * [ ] 1w%&cv
  * [ ] qaywsxedcrfv
  * [X] BaldDummeFragenSinnloseVorlesungenWeihnachten
  * [ ] mutti123
  * [ ] MickeyMouse
  * [ ] poiuztrewq=)(/&)
  * [ ] passwort
  * [X] gVHJQ2K2k.v9

## 10.5 Begriffe der IT-Sicherheit (10 Punkte)
Erläutern Sie den Begriff _Vertraulichkeit_ (_confidentiality_).

*Lösung:*
*Vertraulichkeit*: Informationen sind vertraulich, wenn sie vor unbefugter Preisgabe geschützt sind.  Voraussetzung ist, dass geklärt ist, was "unbefugt" heißt (= i.d.R. ein beschränkter, festgelegter Empfängerkreis).

## 10.6 Begriffe der IT-Sicherheit (10 Punkte)
Erläutern Sie den Begriff _Integrität_ (_integrity_).

*Lösung:*
*Integrität*: Informationen sind integer, wenn sie vor unbefugter Veränderung geschützt sind. Voraussetzung ist, dass geklärt ist, was "unbefugt" heißt (= i.d.R. ein beschränkter, festgelegter Erstellerkreis).

## 10.7 Begriffe der IT-Sicherheit (10 Punkte)
Erläutern Sie den Begriff _Verfügbarkeit_ (_availability_).

*Lösung:*
*Verfügbarkeit*: Informationen sind verfügbar, wenn sie zu dem gewünschten Zeitpunkt zur Nutzung zur Verfügung stehen.

## 10.8 Angriffswerkzeuge (10 Punkte)
Warum heißt ein Computervirus *Virus*?

*Lösung:*
Ein *Virus* ist ein Computerprogramm, welches sich selbst verbreitet, sich in andere Computerprogramme einschleust und sich damit reproduziert; es kann auch nur dort "leben". Es funktioniert in dieser Weise genauso wie ein echter, biologischer Virus. 

