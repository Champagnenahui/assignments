# 11. Betriebssysteme - Test (Musterlösung) (100 Punkte)

## 11.1 Textdatei sortieren (5 Punkte)
Sie haben im aktuellen Verzeichnis eine Textdatei mit den Titeln Ihrer Lieblingsfilme (`filme.txt`). Geben Sie bitte die nötigen Eingaben in der Linux-Shell an, um die Datei zu sortieren und das Ergebnis in einer neuen Datei (`filme_sorted.txt`) zu speichern.

*Lösung:*

```console
cat filme.txt | sort > filme_sorted.txt
```

## 11.2 Hilfe holen (5 Punkte)
Wie können Sie sich die Hilfeseiten zum Kommando `sort` anzeigen lassen?

*Lösung:*
Mit `man sort`.

## 11.3 Verzeichnisse (10 Punkte)
Wie können Sie das aktuelle Verzeichnis unter Linux (Unix) wechseln? Wie lassen Sie sich anzeigen, in welchem Verzeichnis Sie sich gerade befinden?

*Lösung:*
Mit `cd VERZEICHNIS` kann man das Verzeichnis wechseln, mit `pwd` das aktuelle Verzeichnis ausgeben lassen.

## 11.4 Spezielle Verzeichnisse (15 Punkte)
Welche Daten findet man im Verzeichnis `/dev` unter Linux, welche unter `/etc`?

*Lösung:*
In `/dev` liegen die Gerätedateien, in `/etc` die meisten Konfigurationen.

## 11.5 sudo (15 Punkte)
Aus welchem Grund ist der Gebrauch von `sudo` für viele Benutzer (z.B. für Sie auf `jonathan`) gesperrt? Was bewirkt das Kommando?

*Lösung:*
Das Kommando `sudo` führt das darauf folgende Kommando mit Administratorrechten aus. Könnte jeder einfach `sudo` ausführen, hätte er damit Zugriff auf alle Dateien und Konfigurationen des Rechners.

## 11.6 Berechtigungen (20 Punkte)
Sie sehen in einem Verzeichnis den folgenden Eintrag:

```console
-rw-rw-r--   1 thomas  staff   6,1K 28 Sep  2017 datei.txt
```

Was können Sie über die Berechtigungen dieser Datei sagen?

*Lösung:*
Die Datei gehört dem Benutzer `thomas` und der Gruppe `staff`. Benutzer und Gruppe dürfen die Datei lesen und schreiben, alle anderen dürfen sie lesen. Sie ist nicht ausführbar.

## 11.7 Prozesse (15 Punkte)
Wie können Sie unter Linux (Unix) eine Liste der laufenden Prozesse anzeigen und dann einen davon von der Konsole aus beenden?

*Lösung:*
Mit `ps` oder `top` kann man die Prozessliste sehen und mit `kill` einen Prozess gezielt beenden.

## 11.8 Inhalte finden (15 Punkte)
Mit welchem Kommando können Sie Dateien nach einem bestimmten Inhalt durchsuchen und sich dann die Treffer anzeigen lassen?

*Lösung:*
Mit `grep` kann man die Inhalte von Dateien durchsuchen. Die Datei und die gefundene Zeile wird ausgegeben.

