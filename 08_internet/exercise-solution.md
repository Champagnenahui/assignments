# 8. WWW und Internet - Übungen (Musterlösung)

## 8.1 C/S-Modell vs. P2P
Vergleichen Sie Client/Server-Modell mit dem Peer-to-Peer-Modell. Geben Sie Beispiele für die beiden Modelle.

*Lösung:*
Bei Client-Server gibt es eine klare Aufgabentrennung: Der Server bietet Dienste an, der Client nutzt sie. Ein Web-Browser und ein Web-Server agieren nach dem Client-Server-Modell.

Bei Peer-to-Peer ist das anders, da hier alle Parteien gleichberechtigt sind und sowohl Dienste anbieten, als auch nutzen. Filesharing-Dienste, wie z.b. BitTorrent, arbeiten nach dem Peer-to-Peer-Modell.

## 8.2 Namensauflösung
Sie finden folgenden Eintrag in der Datei `/etc/hosts` auf Ihrem Rechner (bzw. `C:\Windows\System32` `\Drivers\etc\hosts`, falls Sie Windows verwenden sollten):

```console
127.0.0.1  localhost
127.0.0.1  www.google.de
```

Was passiert, wenn Sie im Browser die URL `http://www.google.de` eingeben (welche Anzeige sehen Sie und warum)?

*Lösung:*

Da der Namen `www.google.de` zur Adresse `127.0.0.1`, also `localhost` aufgelöst wird, kann der Browser den wirklichen Server von Google unter der IP-Adresse `216.58.205.67` nicht erreichen. Falls ein lokaler Webserver läuft, wird dieser genutzt, andernfalls zeigt der Browser einen Fehler. Auf jeden Fall wird aber nicht die Seite von Google angezeigt.

## 8.3 DNS
Wie funktioniert die Auflösung einer Adresse (z.B. `www.google.com`) in die IP-Adresse? Wo kommt das DNS ins Spiel?

Bitte beschreiben Sie den Ablauf Schritt für Schritt.

*Lösung:*
Zuerst wird versucht, die Adresse lokal aufzulösen:

  1. Als erstes wird die Datei `hosts` durchsucht.
  1. Wird dort kein Eintrag gefunden, überprüft der Client, ob der Name in seinem lokalen Cache (Zwischenspeicher) vorhanden ist.
  3. Verläuft diese Anfrage ergebnislos, wird der DNS-Server konsultiert.

Hat die lokale Auflösung nicht funktioniert, wird der Name über das DNS aufgelöst:

  1. Der Nameserver fragt den Root-Server an, wer als Nameserver für `com` zuständig ist
  2. Sobald er diese Adresse hat, fragt er dort an, welcher Nameserver für  `google.com` zuständig ist.
  3. Sobald er diese Adresse hat, fragt er dort an, ob dieser `www.google.com` kennt bzw. falls nicht, wer den der nächste zuständige Nameserver ist.
  4. Dieser Nameserver kann die Anfrage endlich beantworten und die Adresse ist aufgelöst.

## 8.4 Mail-Protokolle
Wieso gibt es für den Umgang mit E-Mails drei Protokoll (SMTP, POP3, IMAP)?

*Lösung:*
Man muss bei E-Mail unterscheiden zwischen den sogenannten MTA (Mail Transport Agents) und den MUA (Mail User Agent). MTAs sind immer über das Netzwerk erreichbar und übetragen die E-Mails untereinander per SMTP. Somit ist das SMT-Protokoll (Simple Mail Transfer Protocol) für die Zustellung von E-Mails zum Zielserver zuständig. Um die Mails vom Mailserver abzuholen, benötigen die Clients (MUA) ein anderes Protokoll, da sie nicht ständig mit dem Internet verbunden sein müssen. Hierzu dienen POP3 (Post Office Protocol 3) und IMAP (Internet Message Access Protocol). Bei POP3 werden die Mails zum Client geholt und auf dem Server gelöscht, bei IMAP verbleiben sie auf dem Server und werden nur auf dem Client gecached.

## 8.5 HTTPS
Was ist der Unterschied zwischen dem Zugriff auf die URL `http://stargazer.universe.org` und `https://stargazer.universe.org`?

*Lösung:*
HTTPS steht für HTTP Secure. Bei HTTPS erfolgt der Zugriff über SSL (bzw. SSL) und die Kommunikation zwischen Client und Server ist verschlüsselt, sodass andere die Daten nicht mitlesen können.

## 8.6 HTML-Struktur
Öffnen Sie eine Webseite und schauen Sie sich den Quelltext der HTML-Datei an. Welche grundlegende Struktur können Sie erkennen?

*Lösung:*
Header, Body, Tags etc. (Keine vollständige Musterlösung)

## 8.7 SSL-Stripping
Beschreiben Sie bitte kurz und knapp, was man unter einem __SSL-Stripping__-Angriff versteht.

*Lösung:*
Wenn man eine Webseite zuerst per HTTP aufruft und die Seite dann erst per Redirect auf HTTPS wechselt, kann ein Angreifer den SSL-Stripping-Angriff durchführen. Dazu verhindert er den Redirect auf HTTPS und ersetzt in allen Links das `https` durch `http`. So kann er die normalerweise verschlüsselte Kommunikation unverschlüsselt mitlesen.

## 8.8 HTML-Seite erstellen
Erstellen Sie eine einfache HTML-Seite, in der Sie Ihren Lieblingsfilm vorstellen. Verwenden Sie auf jeden Fall Bilder, um die Seite ansprechender zu gestalten. Verwenden Sie CSS, um die Seite optisch zu gestalten.

Legen Sie die Seite auf dem Rechner `agent-smith.informatik.hs-mannheim.de` im Verzeichnis `public_html` (falls nicht vorhanden, müssen Sie das Verzeichnis anlegen) unter dem Namen `index.html` ab. Bilder und weitere Dateien müssen Sie ebenfalls in das `public_html`-Verzeichnis legen. Sie können die Seite dann unter `http://agent-smith.informatik.hs-mannheim.de/~NUTZERNAME/` aus dem Netz der Hochschule erreichen, wobei NUTZERNAME Ihr Nutzername auf dem Rechner ist, z.B. `f.meier`.

Sollte es beim Zugriff auf die Seite eine Fehlermeldung im Browser geben ("Permission denied"), überprüfen Sie bitte, ob Ihr Homeverzeichnis für alle die x-Berechtigung hat und das Verzeichnis `public_html` für alle r- und x-Berechtigungen hat. Falls nicht, ändern Sie die Berechtigungen mit `chmod a+x ~` und `chmod a+rx ~/public_html`.

Abgabe: URL der Seite

*Lösung:*
Keine Musterlösung. Seite wird angeschaut.

