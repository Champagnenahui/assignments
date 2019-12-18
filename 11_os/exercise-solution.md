# 11. Betriebssysteme - Übungen (Musterlösung)

Für die Ausführung einiger dieser Übungen benötigen Sie ein funktionierendes Linux-System. Hierzu können Sie entweder

  * Ein eigenes Linux in einer virtuellen Maschine installieren (z.B. [VirtualBox](https://www.virtualbox.org) mit [Ubuntu](www.ubuntu.com))
  * Ein Live-Linux auf Ihrem Rechner starten, z.B. [Slax](http://www.slax.org)
  * An der Hochschule in einem der Poolräume eine Linux-VM starten
  * Sich mit Ihrem Fakultätsaccount auf `jonathan.sv.hs-mannheim.de` bzw. `agent-smith.informatik.hs-mannheim.de` anmelden
  * Unter Android die Terminal-Emulation [Termux](https://play.google.com/store/apps/details?id=com.termux) installieren



## 11.1 Betriebssystem
Was versteht man unter einem Betriebssystem, und was sind dessen zentrale Aufgaben? Welche Betriebssysteme kennen Sie?

*Lösung:*
Ein Betriebssystem, auch OS genannt, ist eine Zusammenstellung von Computerprogrammen, die die Systemressourcen eines Computers wie Arbeitsspeicher, Festplatten, Ein- und Ausgabegeräte verwaltet und diese Anwendungsprogrammen zur Verfügung stellt. Das Betriebssystem bildet dadurch die Schnittstelle zwischen den Hardware-Komponenten und der Anwendungssoftware des Benutzers. Betriebssysteme bestehen in der Regel aus einem Kernel (deutsch: Kern), der die Hardware des Computers verwaltet, sowie speziellen Programmen, die beim Start unterschiedliche Aufgaben übernehmen.

Liste von Betriebssystemen...

## 11.2 Betriebssystem auf Ihrem Smartphone
Welches Betriebssystem befindet sich auf Ihrem Smartphone? Von welchem Betriebssystem stammt es ab?



## 11.3 Prozess vs. Programm
Erläutern Sie den Unterschied zwischen einem __Prozess__ und eine __Programm__.

*Lösung:*
Ein Prozess ist ein Programm, das gerade ausgeführt wird - eine Arbeitseinheit. Ein Prozess führt extakt ein Programm aus.

Ein Programm ist eine passive Entität (auf der Festplatte gespeichert) und wird zu einem Prozess, wenn es in den Speicher geladen und gestartet wird. Ein Programm kann in mehreren Prozessen ausgeführt werden.

## 11.4 Betriebssysteme Architektur
Wie nennt man den Teil des Betriebssystems, der im privilegierten Modus läuft?

*Lösung:*


## 11.5 Auf jonathan anmelden
Um auf den Rechner `jonathan.sv.hs-mannheim.de` bzw. `agent-smith.informatik.hs-mannheim.de` zugreifen zu können, benötigen Sie einen ssh-Client

  * Windows: [PuTTY](https://putty.org)
  * Mac: ssh-Client ist eingebaut
  * Linux: ssh-Client ist eingebaut
  * Android: [JuiceSSH](https://play.google.com/store/apps/details?id=com.sonelli.juicessh)

Nachdem Sie den Client installiert haben, loggen Sie sich auf dem Rechner mit Ihrem Fakultätsaccount ein.

Finden Sie heraus, welchen Inhalt die Datei `/etc/exports` (jonathan) bzw. `/etc/mtab` (agent-smith) hat und geben Sie die ersten 10 Zeilen an.

*Lösung:*
Inhalt der Datei `/etc/exports`

```console
### /rest/doris anja.ki.hs-mannheim.de(rw,async,no_root_squash)
### /rest/doris doris.ki.hs-mannheim.de(rw,async,no_root_squash)
### /rest/doris 141.19.146.166(rw,async,no_root_squash)

/usbdisk anja.ki.hs-mannheim.de(rw,async,no_root_squash)
/usbdisk doris.ki.hs-mannheim.de(rw,async,no_root_squash)
/usbdisk slm.sv.hs-mannheim.de(rw,async,no_root_squash)
#/usbdisk/nora nora.sr.hs-mannheim.de(rw,async,no_root_squash)
/localhome/schreibwerkstatt anja.ki.hs-mannheim.de(rw,async,no_root_squash)
```

Inhalt der Datei `/etc/mtab`

```console
sysfs /sys sysfs rw,nosuid,nodev,noexec,relatime 0 0
proc /proc proc rw,nosuid,nodev,noexec,relatime 0 0
udev /dev devtmpfs rw,nosuid,relatime,size=4052996k,nr_inodes=1013249,mode=755 0 0
devpts /dev/pts devpts rw,nosuid,noexec,relatime,gid=5,mode=620,ptmxmode=000 0 0
tmpfs /run tmpfs rw,nosuid,noexec,relatime,size=816884k,mode=755 0 0
/dev/sda2 / ext4 rw,relatime,data=ordered 0 0
securityfs /sys/kernel/security securityfs rw,nosuid,nodev,noexec,relatime 0 0
tmpfs /dev/shm tmpfs rw,nosuid,nodev 0 0
tmpfs /run/lock tmpfs rw,nosuid,nodev,noexec,relatime,size=5120k 0 0
tmpfs /sys/fs/cgroup tmpfs ro,nosuid,nodev,noexec,mode=755 0 0
```

## 11.6 Hilfe holen
Wie können Sie sich die Hilfeseiten zum Kommando `sort` anzeigen lassen?

*Lösung:*
Mit `man sort`.

## 11.7 Verzeichnisse
Öffnen Sie auf einem Rechner mit dem Betriebssystem Linux eine Shell (Terminal).

  1. Was ist Ihr aktuelles Arbeitsverzeichnis?
  2. Wie können Sie das aktuelle Verzeichnis herausfinden?
  3. Wechseln Sie mit der Shell zum Wurzelverzeichnis (`cd`) und zeigen dort alle Dateien und Verzeichnisse an (`ls`).
  4. Wem gehören die Dateien und Verzeichnisse im Wurzelverzeichnis? Wem in Ihrem Arbeitsverzeichnis?

Schauen Sie sich ein wenig auf dem System um. Was fällt Ihnen auf? Welche Verzeichnisse und Dateien sehen Sie? Was fällt Ihnen auf?

*Lösung:*
Keine allgemeine Musterlösung möglich.

## 11.8 Verzeichnisse und Dateien anlegen/löschen
Öffnen Sie auf einem Rechner mit dem Betriebssystem Linux eine Shell (Terminal).

  1. Legen Sie ein Verzeichnis an (`mkdir`)
  2. Wechseln Sie in das Verzeichnis (`cd`)
  3. Erzeugen Sie im Verzeichnis eine Datei mit einem beliebigen Namen (`touch`)
  4. Verlassen Sie das Verzeichnis (`cd`)
  5. Versuchen Sie das Verzeichnis zu löschen (`rmdir`)

Was passiert? Was müssen Sie tun, um das Verzeichnis zu löschen?

*Lösung:*
Das Verzeichnis kann nicht gelöscht werden, weil es nicht leer ist. Man muss entweder erst die Datei löschen (`rm`) und dann das Verzeichnis oder man muss beim `rm` dir Option `-rf` angeben.

## 11.9 Dateien kopieren/verschieben
Öffnen Sie auf einem Rechner mit dem Betriebssystem Linux eine Shell (Terminal).

  1. Legen Sie ein Verzeichnis an (`mkdir`)
  2. Wechseln Sie in das Verzeichnis (`cd`)
  3. Erzeugen Sie im Verzeichnis eine Datei mit einem beliebigen Namen und schreiben Sie einen Text in die Datei (`nano` oder `vi`)
  4. Kopieren Sie die Datei (`cp`)
  5. Editieren Sie die kopierte Datei (`nano` oder `vi`)
  6. Vergleichen Sie beide Dateien miteinander (`diff`)

Was sehen Sie?

  7. Legen Sie ein weiteres Verzeichnis an (`mkdir`)
  8. Verschieben Sie eine der beiden Dateien in das neue Verzeichnis (`mv`)

*Lösung:*
Das `diff`-Kommando sollte die Unterschiede zwischen den Dateien zeilenweise anzeigen.

## 11.10 Weitere Unix-Kommandos
Schauen Sie sich die Hilfeseiten (oder das Buch "The Linux Command Line") zu den folgenden Kommandos an und geben Sie zu jedem kurz (in einem Satz) dessen Aufgabe an.

  1. `file`
  2. `less`
  3. `cat`
  4. `ln`
  5. `which`
  6. `whoami`
  7. `sort`
  8. `uniq`
  9. `grep`
  10. `head`
  11. `tail`
  12. `wc`
  13. `echo`
  14. `clear`
  15. `history`
  16. `sed`
  17. `du`
  18. `df`

*Lösung:*
Zu jedem Kommando eine kurze Beschreibung...

## 11.11 Spezielle Verzeichnisse
Öffnen Sie auf einem Rechner mit dem Betriebssystem Linux eine Shell (Terminal). Schauen Sie sich auf der Festplatte ein wenig um, indem Sie mit `cd` durch die Verzeichnisse gehen und sich deren Inhalt mit `ls` anzeigen lassen.

Wozu dienen die folgenden Verzeichnisse:

  1. `/etc`
  2. `/dev`
  3. `/bin`
  4. `/home`
  5. `/tmp`

*Lösung:*
  1. `/etc`: Konfigurationsdateien
  2. `/dev`: Geräte
  3. `/bin`: Ausführbare Programme
  4. `/home`: Daten der Benutzer
  5. `/tmp`: Temporäre Dateien

## 11.12 Berechtigungen
Sie sehen in einem Verzeichnis den folgenden Eintrag:

```console
-rw-rw-r--   1 thomas  staff   6,1K 28 Sep  2017 datei.txt
```

Was können Sie über die Berechtigungen dieser Datei sagen?

*Lösung:*
Die Datei gehört dem Benutzer `thomas` und der Gruppe `staff`. Benutzer und Gruppe dürfen die Datei lesen und schreiben, alle anderen dürfen sie lesen. Sie ist nicht ausführbar.

## 11.13 Berechtigungen
Öffnen Sie auf einem Rechner mit dem Betriebssystem Linux eine Shell (Terminal). Schauen Sie sich die Hilfeseiten (oder das Buch "The Linux Command Line") zu den folgenden Kommandos an und experimentieren Sie damit ein wenig.

  1. `chmod`
  2. `chown`
  3. `chgrp`
  4. `passwd`
  5. `sudo`
  6. `su`
*Lösung:*


## 11.14 Prozesse
Öffnen Sie auf einem Rechner mit dem Betriebssystem Linux eine Shell (Terminal). Schauen Sie sich die Hilfeseiten (oder das Buch "The Linux Command Line") zu den folgenden Kommandos an und experimentieren Sie damit ein wenig.

  1. `ps`
  2. `top`
  3. `kill`
  4. `killall`
  5. `shutdown`

*Lösung:*


## 11.15 Eingabe- und Ausgabeumlenkung
Öffnen Sie auf einem Rechner mit dem Betriebssystem Linux eine Shell (Terminal). Experimentieren Sie mit der Eingabe-/Ausgabeumlenkung (`>`, `<`) und Pipes (`|`). Siehe hierzu Kapitel 6 in "The Linux Command Line".

Was ist der Unterschied zwischen `>`/`<` und `|`?

*Lösung:*
`>`/`<` verwendet man mit Dateien, `|` mit Programmen.

