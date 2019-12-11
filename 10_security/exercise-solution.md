# 10. IT-Sicherheit - Übungen (Musterlösung)

## 10.1 Begriffe der IT-Sicherheit
Erläutern Sie die folgenden Begriffe:

  1. Vertraulichkeit
  2. Integrität
  3. Verfügbarkeit

*Lösung:*
  1. *Vertraulichkeit*: Informationen sind vertraulich, wenn sie vor unbefugter Preisgabe geschützt sind.  Voraussetzung ist, dass geklärt ist, was "unbefugt" heißt (= i.d.R. ein beschränkter, festgelegter Empfängerkreis).
  2. *Integrität*: Informationen sind integer, wenn sie vor unbefugter Veränderung geschützt sind. Voraussetzung ist, dass geklärt ist, was "unbefugt" heißt (= i.d.R. ein beschränkter, festgelegter Erstellerkreis).
  3. *Verfügbarkeit*: Informationen sind verfügbar, wenn sie zu dem gewünschten Zeitpunkt zur Nutzung zur Verfügung stehen. 

## 10.2 Angriffswerkzeuge
Erläutern Sie die folgenden Begriffe: 

  1. Trojaner, Trojanisches Pferd
  2. Malware
  3. Virus 
  4. Rootkit
  5. Exploit
  6. Zero-day Exploit 

*Lösung:*
  1. *Trojaner*:  Computerprogramm , das als nützliche Anwendung getarnt ist, im Hintergrund aber ohne Wissen des Anwenders eine andere Funktion erfüllt.
  2. *Malware*:  Computerprogramme, die entwickelt wurden, um unerwünschte und gegebenenfalls schädliche Funktionen auszuführen.
  3. *Virus*: Computerprogramm, welches sich selbst verbreitet, sich in andere Computerprogramme einschleust und sich damit reproduziert. 
  4. *Rootkit*: Sammlung von Softwarewerkzeugen, welche nach Eindringen in ein Computersystem installiert werden, um zukünftige Anmeldungen zu erleichtern und die Aktivitäten des Eindringlings zu verbergen. 
  5. *Exploit*: Systematische Möglichkeit, Schwachstellen auszunutzen, die bei der Entwicklung eines  Programms entstanden sind
  6. *Zero-day Exploit*: Zero-Day-Exploit nennt man einen Exploit, der eingesetzt wird, bevor es einen Patch als Gegenmaßnahme gibt.

## 10.3 Überwachungsfreiheit
Heutzutage wird man zunehmend von privaten Anbietern überwacht - und weniger von Staaten (oder...?). Wie soll man sich verhalten, wenn man der Überwachung weitestgehend entgehen will? 

*Lösung:*
  - Keine Computer oder Handy kaufen, deren Betriebssystem ständig nach Hause telefoniert. 
  - Sparsam mit Daten umgehen, nur Dienste nutzen, die Datensparsamkeit versprechen (und im Rechtsraum der EU-DSGVO liegen). 
  - Es gibt keine kostenlosen Angebote im Internet - im Zweifel bezahlt man mit seinen Daten. Also: Finger weg, wenn es nichts kostet!
  - Immer von einem frischen Betriebssystem booten, keine Anmeldungen und Passwörter speichern. Daten im Zweifel immer lokal halten. 

Wie realistisch bzw. wie aufwändig das heute ist - bewerten Sie selbst. 

## 10.4 Sicherheit beim Surfen
  1. Was sind Cookies und sind diese gefährlich?
  2. Welche Einstellungen in meinem Browser sollte ich vornehmen? 
  3. Was sollte ich beim Surfen beachten? 

*Lösung:*
  1. Cookies sind kleine Textdateien, die Informationen über den Benutzer beinhalten, und den Webseiten helfen sollen, den Benutzer mit seinen Gewohnheiten wiederzuerkennen. Sie sind an sich nicht gefährlich, da sie keine Angriffe ermöglichen. Aber sie erlauben das Sammeln von Daten über den Benutzer, und damit auch das Profiling. 
  2. JavaScript abschalten macht heute kaum noch einen Sinn, denn dann gehen keine Webseiten mehr. Cookies abschalten kann man, hat aber keinen großen Nutzen. Wichtig ist die sehr selektive Erlaubnis von Client-seitigen Frameworks, wie etwa Web-App-Plugins, Adobe Flash, etc. - sie sollten nur da "an" sein, wo es unbedingt gefordert ist. 
  3. Trotz aller technischer Vorkehrungen sollten Sie keine unbekannten Webseiten mit dubiosen Adressen ansurfen. Bleiben Sie in vertrautem Gewässer - insbesondere wenn Sie wichtige Daten auf Ihrem Endgerät lagern. 

## 10.5 Kryptographische Verschlüsselung
Was ist der Unterschied zwischen symmetrischer und asymmetrischer Verschlüsselung, und wofür werden diese jeweils im Internet eingesetzt? Geben Sie jeweils 2 Beispiele für Verfahren. 

*Lösung:*
  - *Symmetrische* Verschlüsselung: Verschlüsselungsverfahren, die für Ver- und Entschlüsselung den gleichen Schlüssel verwenden. Beispiele: DES (Data Encryption Standard), AES (Advanced Encryption Standard)
  - *Asymmetrische* Verschlüsselung: Verschlüsselungsverfahren, bei denen für Ver- und Entschlüsselung unterschiedliche Schlüssel verwendet werden; vom "öffentlichen" Schlüssel (der für die Verschlüsselung verwendet wird) kann man nicht auf den "privaten" Schlüssel (der für die Entschlüsselung verwendet wird) schließen. Beispiele: RSA (Rivest-Shamir-Adleman) , ECDL (Elliptic Curve Discrete Logarithm)

Während die sehr schnelle symmetrische Verschlüsselung in Internet-Protokollen für die Verschlüsselung des gesamten Inhalts eingesetzt werden, wird die viel langsamere asymmetrische Verschlüsselung dafür genutzt, den Schlüssel der symmetrischen Verschlüsselung sicher zu übertragen. 

## 10.6 Digitale Signatur
Beschreiben Sie drei Einsatzgebiete der Technologie der "Digitalen Signatur" (im kryptographischen Sinn). 

*Lösung:*
  1. Nachweis der Willenserklärung und Authentizität des Unterzeichners bei elektronischen Dokumenten. 
  2. Integrität und Authentizität von Software-Installationspaketen bei der Installation von Software (speziell Apps in App Marketplaces).  
  3. Authentizität von E-Mails. 

## 10.7 Forward Secrecy
Warum ist es wichtig, dass Webseiten-Betreiber ihre Server so konfigurieren, dass bei TLS die sogenannte __Forward Secrecy__ gewährleistet ist?

*Lösung:*
Wenn man keine Forward Secrecy hat, können in der Vergangenheit aufgezeichnete mit TLS verschlüsselte Kommunikationen nachträglich entschlüsselt werden. Forward Secrecy sorgt dafür, dass dies nachträglich nicht möglich ist.


## 10.8 Authentifizierungsverfahren
Benennen Sie drei verschiedene Authentifizierungsverfahren und jeweils deren primäre Schwäche. 

*Lösung:*
  1. *Passwort*-basierte Authentifizierung. Schwäche ist die einfache Kopierbarkeit von Passwörtern. 
  2. *Challenge-Response*-basierte Authentifizierung. Schwäche ist die Erfordernis, den privaten Schlüssel des Anmeldenden sicher zu verwahren. 
  3. *Biometrische* Authentifizierung. Schwäche ist die Nicht-Veränderbarkeit der biometrischen Daten (und das damit verbundene physische Risiko des Anwenders). 

## 10.9 Garagentoröffner
Viele Garagentore können per Funksender geöffnet werden. Warum reicht es nicht, die Kommunikation zwischen dem Sender und Empfänger aufzuzeichnen, um das Tor später noch einmal zu öffnen?

*Lösung:*
Garagentoröffner setzen im Allgemeinen ein Challenge-Response-Verfahren ein, das sicher gegen ein Wiederabspielen der Kommunikation (_Replay-Attacke_) ist.

Im folgenden wird die Authentifizierung von Alice gegenüber Bob mithilfe eines Challenge-Response-Verfahrens dargestellt:

  1. Alice und Bob besitzen ein gemeinsames Geheimnis S
  2. Alice sendet Bob eine Aufforderung zum Senden der Challenge
  3. Bob sendet Alice eine Zufallszahl Z und berechnet ein Ergebnis E mithilfe einer Einwegfunktion E = F(Z, S)
  4. Alice empfängt eine Zufallszahl Z von Bob
  5. Alice berechnet das Ergebnis E der E = Einwegfunktion F(Z, S)
  6. Alice sendet E an Bob
  7. Bob vergleicht das empfangene E mit seinem selbst berechneten E. Stimmen beide überein, ist Alice wirklich Alice und damit authentifiziert

## 10.10 Probleme von Keyless-Entry-Systemen
Man hört und [sieht](https://youtu.be/odG2GX4_cUQ) häufiger, dass Autos mit Keyless-Entry-Systemen gestohlen werden. Die Schlüssel setzen allerdings ein Challenge-Response-Verfahren ein, das als sicher gilt. Wie gelingt des den Tätern trotzdem das Fahrzeug zu stehlen und welche Schwachstelle nutzen sie aus?

*Lösung:*
Die Schwachstelle der Keyless-Entry-Systeme ist, dass der Start der Authentifizierung nicht vom Schlüssel, sondern vom Fahrzeug ausgeht. Berührt man den Türgriff oder kommt auch nur in seine Nähe, schickt das Auto einen Challenge an den Schlüssel. Ist dieser in der Nähe - oder wird das Signal von den Dieben verstärkt, sodass der Schlüssel in der Nähe scheint - antwortet er mit der korrekten Response. Das Fahrzeug öffnet sich. Die Diebe müssen also nur dafür Sorgen, dass das Fahrzeug irgendwie mit dem Schlüssel kommunizieren kann und schon können sie es öffnen. Sie brauchen _keinen_ physischen Zugriff auf den Schlüssel. Bei klassischen Funkschlüsseln funktioniert dies nicht, weil man hier physischen Zugriff auf den Schlüssel braucht, um den Knopf zu drücken.

## 10.11 Sichere Passwörter
Angenommen ein Passwort besteht aus acht Zeichen aus dem Alphabet A-Z (26 Zeichen) und die Überprüfung des Passwortes dauert eine Millisekunde.

  1. Wie lange dauert es, alle möglichen Passwörter durchzuprobieren?
  2. Erweitern Sie die möglichen Zeichen (bei gleicher Passwortlänge) noch um die Zahlen 0-9: Wie lange dauert es jetzt?
  3. Erweitern Sie die Passwortlänge um eins (ohne die Zahlen 0-9): wie lange dauert es jetzt?
  4. Was ist besser? Mehr unterschiedliche Zeichen, oder längere Passwörter?
  5. Wie lange brauchen moderne Prozessoren, um ein Passwort zu testen?

*Lösung:*
  1. Alle Passwörter überprüfen: 8 Zeichen mit 26 Möglichkeiten --> 26^8 = 2,1 * 10^11 Millisekunden = 6,6 Jahre
  2. Alle Passwörter überprüfen: 8 Zeichen mit 36 Möglichkeiten --> 36^8 = 2,8 * 10^12 Millisekunden = 89,5 Jahre
  3. Alle Passwörter überprüfen: 9 Zeichen mit 26 Möglichkeiten --> 26^9 = 5,4 * 10^12 Millisekunden = 172 Jahre
  4. Den Exponenten erhöhen vergrößert die Zahl schneller als die Basis --> Längere Passwörter sind viel besser!
  5. Laut [automationrhapsody.com](https://automationrhapsody.com/md5-sha-1-sha-256-sha-512-speed-performance/) vom 03.05.2018 kann SHA-256 (ein heute übliches und sicheres Hashverfahren für Passwörter) 1.000.000 Tests in ca. 738 ms durchführen. D.h. ein Passwort-Test dauert ca. 0,738 MICROsekunden!

## 10.12 Speicherung von Passwörtern
Grundsätzlich sollte man als Programmierer keine Sicherheitsfunktionen selbst implementieren, sondern immer vorhandene und gut getestete Bibliotheken verwenden.

Trotzdem angenommen, Sie wollten ein Passwort sicher speichern und verarbeiten, wie gehen Sie vor?

Ihre Antwort sollte die Folgenden Begriffe berücksichtigen:

  1. Rainbow Table
  2. Salt
  3. Brute-Force-Angriff
  4. Round (Runden)
  5. Hash-Algorithmen
  6. Klartext-Passwort

*Lösung:*
Eine Anwendung sollte niemals ein _Klartext-Passwort_ speichern, sondern immer nur dessen Hash-Wert, der über einen enstprechenden _Hash-Algorithmus_ bestimmt wird. Ein Hash-Wert lässt sich aus dem Passwort berechnen, aber aus dem Hash-Wert kann man das Passwort nicht wieder konstruieren (Einweg-Funktion). Bei der Anmeldung wird zu dem Passwort erneut der Hash-Wert berechnet und dieser mit dem gespeicherten Wert verglichen. Stimmen beide überein, wird dem Nutzer Zugang gewährt.

Das Passwort wird vor der Berechnung des Hash-Wertes mit einem weiteren Zufalls-Wert, dem _Salt_ angereichert und dieses wird zusammen mit dem Hash-Wert gespeichert. Dieses verhindert einen Angriff per _Rainbow Table_: In einem solchen sind die Hash-Werte für alle gängigen Passwörter und Buchstabenkombinationen gespeichert. Durch das Salt wird es unmöglich, einen Rainbow Table für alle Passwörter und alle möglichen Salts zu berechnen (Speicherplatz und Rechenzeit).

Trotz Salt ist das Passwort immer noch anfällig für einen _Brute-Force-Angriff_, bei dem einfach alle Passwörter durchprobiert werden. Diesen kann man durch einen entsprechend langsamen Hash-Algorithmus und die Verwendung von _Runden_ vereiteln: Hierbei wird der Hash-Wert wiederholt noch einmal durch den Hash-Algorithmus geschickt. Mit jeder Runde erhöht sich der Zeitaufwand für einen Brute-Force-Angriff entsprechend.


## 10.13 Hashen von Telefonnummern
In einem Softwareprojekt soll das Verhalten von deutschen Telefonkunden _anonym_ ausgewertet werden. Der Projektleiter schlägt vor, dass die Telefonnummern als Hashwert (MD5) gespeichert werden soll und behauptet, dass so keinerlei Rückschluss auf die ursprüngliche Nummer möglich ist. Wie bewerten Sie diese Aussage? Begründen Sie Ihre Antwort ausführlich!

*Lösung:*
Es gibt in Deutschland ca. 5200 Vorwahlen und in jedem Vorwahlbereich Telefonnummern mit bis zu 9 Ziffern, wobei die Regel ist, dass die Vorwahl (Ortsnetzkennziffer  ONKz) und Nummer zusammen nicht länger als 11 Ziffern sein dürfen. Die führende 0 bei der Vorwahl zählt nicht mit. Somit können in Berlin (Vorwahl 30) bis zu 9 weitere Ziffern vorkommen, in Seilershof (Vorwahl 33085) nur noch 6 weitere Ziffern.

Folgende Verteilung bei der Länge der Vorwahlen ist gegeben und daraus ergibt sich als maximale Länge der Teilnehmernummer:

| Länge ONKz | Anzahl | max. Länge |
|------------|--------|------------|
|          2 |      4 |          9 |
|          3 |     85 |          8 |
|          4 |   3882 |          7 |
|          5 |   1231 |          6 |

Damit ergibt sich die Anzahl der maximal zu testenden Nummern als:

| Länge ONKz | Anzahl | Anzahl zu testen |
|------------|--------|------------------|
|          2 |      4 |    1.000.000.000 |
|          3 |     85 |      100.000.000 |
|          4 |   3882 |       10.000.000 |
|          5 |   1231 |        1.000.000 |

Der Einfachheit halber wird hier ignoriert, dass keine Telefonnummer mit einer 0 beginnen kann.

In Summe müsste man also `4 * 1.000.000.000 + 85 * 100.000.000` `+ 3882 * 10.000.000` `+ 1231 * 1.000.000 = 52.551.000.000` Nummern hashen, um eine passende Rainbow-Table aufzubauen bzw. eine entsprechende Anzahl von Hashes berechnen, um eine Nummer zu finden.

Auf einer NVIDIA GTX1080 kann man ca. 24.000.000.000 MD5-Hashes pro Sekunde berechnen ([Quelle](https://gist.github.com/epixoip/6ee29d5d626bd8dfe671a2d8f188b77b)). Auf einer normalen Intel-CPU kann man immer noch ca. 20.000.000 Hashes pro Sekunde berechnen. Damit wären alle Telefonnummern in 43 Minuten entschlüsselt, d.h. eine vollständige Rückberechnung der Nummern ist vollkommen realistisch.

Das Hashen der Telefonnummern bietet also keine hinreichende Anonymisierung und sollte nicht verwendet werden.

