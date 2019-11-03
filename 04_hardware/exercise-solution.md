# 4. Hardware - Übungen (Musterlösung)

## 4.1 PC konfigurieren
Stellen Sie zwei PCs zusammen, einmal einen mit maximaler Leistung für Computer-Spiele und einmal einen einfachen Rechner für das Surfen im Internet. Verwenden Sie keinen komplett PC, sondern stellen Sie die Geräte aus einzelnen Komponenten zusammen, die Sie im Internet bei einem Hardware-Versand (z.B. [Alternate](https://www.alternate.de)) finden.

Stellen Sie eine Stückliste, inklusive Preisen zusammen. Was kosten die beiden Rechner?

*Lösung:*
Keine Musterlösung möglich... Wenn zwei Rechner halbwegs vernünftig konfiguriert wurden, ist die Aufgabe gelöst.

## 4.2 Vergleich Harvard- mit von Neumann-Architektur
Vergleichen Sie kurz die Harvard mit der von Neumann-Architektur:

  * Welche Eigenschaften zeichnen die jeweilige Architektur aus?
  * Welche Vor- und Nachteile haben sie jeweils?

*Lösung:*
Die Harvard-Architektur bezeichnet in der Informatik ein Schaltungskonzept, bei dem der Befehlsspeicher logisch und physisch vom Datenspeicher getrennt ist. Die logische Trennung ergibt sich aus verschiedenen Adressräumen und verschiedenen Maschinenbefehlen zum Zugriff auf Befehl- und Datenspeicher. Die physische Trennung ist mit zwei getrennten Speichern realisiert, auf die der Zugriff über je einen eigenen Bus erfolgt. [Quelle: Wikipedia](https://de.wikipedia.org/wiki/Harvard-Architektur)

Die Harvard-Architektur findet sich hauptsächlich in Single-Chip-Microcontrollern, z.B. von AVR.

Die Von-Neumann-Architektur (VNA) ist ein Referenzmodell für Computer, wonach ein gemeinsamer Speicher sowohl Computerprogrammbefehle als auch Daten hält.

Sie besteht im Kern aus:

  * Prozessor (= Steuerwerk + Rechenwerk)
  * Speicher
  * Eingabewerk
  * Ausgabewerk

Vorteile der Harvard-Architektur

  * Schutz von Programmen vor Veränderung
  * Höhere Durchsatz, da zwei getrennte Busse für Daten/Programme parallel arbeiten

Vorteile der von Neumann-Architektur

  * Speicher kann besser genutzt werden (keine Fragmentierung)
  * Programme werden streng sequentiell abgearbeitet

## 4.3 RISC vs. CISC
Stellen Sie kurz die Unterschiede zwischen einer CISC- und einer RISC-Architektur bei Prozessoren zusammen. Nennen Sie jeweils ein Beispiel für einen Prozessor mit RISC- bzw. CISC-Architektur. Haben moderne Intel-Prozessoren, z.B. der i7, eine RISC- oder CISC-Architektur? Wie verhält es sich mit dem Prozessor in heutigen Smartphones?

*Lösung:*
Die Bezeichnung __CISC (Complex Instruction Set Computer)__ wurde in den 1970er Jahren von IBM gewählt, um klassische Befehlssätze von einer neuartigen Form abzugrenzen, dem __Reduced Instruction Set Computer (RISC)__. Ein CISC-Befehlssatz zeichnet sich durch viele, verhältnismäßig mächtige Einzelbefehle aus, wohingegen RISC zugunsten einer hohen Ausführungsgeschwindigkeit und eines niedrigeren Decodieraufwands weitgehend auf komplexe Befehle verzichtet.

Moderne Intel-Prozessoren werden zwar mit CISC-Befehlen programmiert, diese werden aber von einer speziellen Einheit im Prozessor in RISC-Befehle übersetzt und dann auf einer RISC-Einheit ausgeführt. Genau genommen sind es also intern RISC-Prozessoren.

In den meisten Smartphones kommt ein ARM-Prozessor zum Einsatz, der ein reinrassiger RISC-Prozessor ist -- der Name ARM steht für __Advanced RISC Machines__.

## 4.4 Prozessor
Aus welchen Einheiten besteht ein Prozessor und welche Funktion haben diese jeweils?

*Lösung:*
  * ALU (Rechenwerk) - Führt die eigentlichen Berechnungen durch
  * Register - Speichert Daten zwischen, die vom Rechenwerk verwendet werden bzw. vom Speicher geladen und in diesen geschrieben werden
  * I/O - Kümmert sich um die Kommunikation mit der Außenwelt über Adress- und Datenbus
  * Steuerwerk - Holt die Befehle über die I/O-Einheit und führt sie aus

## 4.5 Register des Prozessors
Jeder Prozessor hat neben den "normalen" Registern einen Program Counter (PC) und ein Instruction Register (IR).

  1. Wie läuft die Ausführung von Befehlen ab?
  2. Wie werden Sprünge im Programm realisiert?

*Lösung:*
Der Program Counter enthält die Adresse des aktuellen Befehls, das Instruction Register den Befehl selbst.

Ablauf der Befehlsausführung

  1. _fetch_: Nächste Instruktion aus dem Speicher in das Instruction Register laden
  2. _decode_: Instruktion im Register dekodieren
  3. _increment PC_: Programm Counter um eins erhöhen
  4. _fetch operands_: Operanden aus dem Speicher laden
  5. _execute_: Instruktion ausführen
  6. _write_: Ergebnisse zurück schreiben
  7. Zurück zu Schritt 1

Realisierung von Sprüngen

Sprünge werden realisiert indem der Program Counter auf die Adresse des Sprungziels gesetzt wird.

## 4.6 Adressraum
Wie viel Speicher (in Kilo- bzw. Megabyte) kann ein Computer mit 16 Bit-Adressen ansprechen? Wie viel Speicher kann man entsprechend mit 32 Bit-Adressen verwenden?

*Lösung:*
Mit 16 Bit lassen sich 2^16 Adressen verwalten, d.h. 65536 Byte oder 64 kB. Mit 32 Bit kann man 2^32 = 4 GB an Speicher verwalten.

## 4.7 64 Bit im Smartphone
Warum ist es für Smartphone-Nutzer wichtig, dass die Prozessoren im Smartphone in Zukunft auch 64 Bit-Architekturen sind?

*Lösung:*
Smartphone-Prozessoren mit 32 Bit können nur 4 GB an Hauptspeicher verwalten. Aktuelle Smartphones haben bereits 4 GB RAM (Galaxy S9) oder sogar schon mehr (Galaxy S9+ mit 6 GB). Um in Zukunft mehr RAM im Smartphone verbauen zu können, ist es daher wichtig, dass die Prozessoren eine 64 Bit-Architektur haben.

## 4.8 GPU vs. CPU
Worin unterscheiden sich Grafikprozessoren (GPU) von "normalen" Prozessoren (CPU)? Beschreiben Sie die Unterschiede kurz.

*Lösung:*
GPUs sind für die Berechnungen speziell im Umfeld von Grafikanwendungen und Spielen konzipiert. Sie besitzen sehr viele parallele Recheneinheiten (Shader), die gleichzeitig verschiedene Teile eines Bildes berechnen können. Jede einzelne Einheit ist nicht besonders schnell, das machen sie durch ihre große Anzahl wett. CPUs sind Allzweckprozessoren und können beliebige Berechnungen durchführen. Jede einzelne Berechnung kann sehr schnell ausgeführt werden, dafür kann nur eine begrenzte Anzahl von Berechnungen parallel ablaufen.

## 4.9 SSDs - Vorteile und Nachteile
Solid State Disks (SSDs) sind deutlich schneller als Festplatten (HDDs). Welche Gründe sprechen für und welche gegen eine SSD? Welche Anschlussmöglichkeiten gibt es für SSDs an den Rechner?

*Lösung:*
SSDs haben konstruktionsbedingt _weniger Speicherkapazität_ als Festplatten, da jedes einzelne Bit in einer Flash-Zelle gespeichert werden muss. Außerdem unterliegen SSDs, genauso wie Festplatten, einem _Verschleiß_, da jede einzelne Flash-Zelle nur eine sehr begrenzte Zahl von Malen geschrieben werden kann. Dafür ist die _Schreib- und Lesegeschwindigkeit_ bei einer SSD deutlich höher als bei einer Festplatte, da keine mechanischen Teile eingesetzt werden. Außerdem ist sie _resistent gegen Erschütterungen_, die für Festplatten problematisch sind und bis zum Datenverlust führen können.

Für SSDs gibt es primär folgende Anschlussmöglichkeiten

  * SATA - SSD wird wie eine normale Festplatte an den Serial ATA-Port angeschlossen
  * M2 - Spezielle Schnittstelle für SSDs, die vor allem in Notebooks zum Einsatz kommt
  * PCIe - SSD wird direkt über den PCI-Express-Bus mit dem Rechner verbunden

## 4.10 Rotationsgeschwindigkeit
Was gewinnt man, wenn man die Rotationsgeschwindigkeit einer Festplatte oder DVD erhöht?

*Lösung:*
Die Datenrate einer Festplatte oder eines optischen Mediums hängt davon ab, wie schnell die Daten am Lesekopf vorbeikommen. Je schneller sich das Medium dreht, desto mehr Daten kommen pro Zeiteinheit am Kopf vorbei.

## 4.11 Größe einer Textdatei
Manchmal verändert sich die Größe auf der Festplatte einer Textdatei beim Hinzufügen eines einzelnen Zeichens überhaupt nicht, ein anders Mal direkt um einige Hundert Bytes. Woran liegt das?

*Lösung:*
Auf der Festplatte werden die Daten in Blöcken fester Größe gespeichert. Ein Block (oder Cluster) kann nicht zwischen mehreren Dateien geteilt werden, d.h. er gehört immer exklusiv zu einer Datei. Ein einzelnes Zeichen belegt normalerweise ein Byte. Ist noch Platz im Block, nimmt die Größe auf dem Datenträger überhaupt nicht zu. Ist der Block voll, muss ein ganzer neuer Block belegt werden.

## 4.12 Leistung von USB-Ports
HD-Video hat eine Auflösung von 1920x1080 Pixel bei 30 Frames pro Sekunde mit 24 Bit pro Pixel. Kann man einen unkomprimierten HD-Video-Strom live über einen

  * USB 1.1-Port (12 MBit/s)
  * USB 2.0-Port (480 MBit/s)
  * USB 3.0-Port (5 GBit/s)

senden?

*Lösung:*
Eine Auflösung von 1920x1080 hat 2.073.600 Pixel, die bei 24 Bit pro Pixel 6.220.800 Byte pro Bild benötigen. Bei 30 Frames pro Sekunde fallen somit 1920x1080x3x30=186.624.000 Byte pro Sekunde an (178 MByte/s). Ignoriert man alle Fehlerkorrektur-Informationen benötigt man dafür eine Bandbreite von 1.492.992.000 Bit/s = 1,4 GBit/s. Ein solches Video kann man also nur über USB 3.0 übertragen.

## 4.13 Datenrate einer Tastatur
Wie viele Bits pro Sekunde muss eine Tastatur übertragen, um mit einem Nutzer mitzuhalten, der 40 Worte pro Minute tippt?

*Lösung:*
Die durchschnittliche Wortlänge im Deutschen beträgt ca. 7 Zeichen dazu kommen noch die Leerzeichen zwischen den Wörtern, sodass jedes Wort ca. 8 Zeichen auf der Tastatur erfordert. Damit ergeben sich pro Minute 320 Zeichen und pro Sekunde 5 1/3 Zeichen/s. Wird jedes Zeichen mit 8 Bit codiert, sind dies ca. 43 Bit/s.

