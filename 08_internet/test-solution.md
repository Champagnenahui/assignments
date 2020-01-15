# 8. WWW und Internet - Test (Musterlösung) (100 Punkte)

## 8.1 Mail-Server (15 Punkte)
Welche Protokolle kommen primär im Zusammenhang von E-Mails zum Einsatz? Nennen Sie zu jedem Protokoll kurz den Zweck zu dem es im Rahmen von E-Mail-Übertragungen eingesetzt wird.

*Lösung:*

  - SMTP (Simple Mail Transfer Protocol): Versand der E-Mail und Zustellung zwischen den Mail-Servern
  - POP3 (Post Office Protocol 3): Abholen der E-Mails vom Client
  - IMAP: Verwalten und lesen von E-Mails auf dem Server durch den Client

## 8.2 DNS (15 Punkte)
Welchen Zweck hat das Domain Name System (DNS) und wie ist es technisch aufgebaut?

*Lösung:*

Das DNS löst Namen zu IP-Adressen auf. Ist hierarchisch aufgebaut und löst die Namen ausgehend von den sog. Root-Serven von hinten nach vorne auf.

## 8.3 HTML vs. CSS (10 Punkte)
Welche Aufgabe hat HTML, welche CSS bei einer modernen Webseite?

*Lösung:*

In modernen Webseiten trennt man den Inhalt von der Darstellung. HTML beschreibt die Inhalte, CSS, wie diese angezeigt werden sollen.

## 8.4 HTTPS (15 Punkte)
Welche Aussagen über HTTPS sind korrekt?

  * [ ] es basiert auf SSH
  * [X] der Server identifiziert sich gegenüber dem Browser
  * [X] der Browser kann sich gegenüber dem Server identifizieren
  * [ ] die Speicherung der Daten erfolgt verschlüsselt
  * [ ] es verschlüsselt die Daten asymmetrisch
  * [X] es verwendet Zertifikate
  * [ ] es verwendet PGP-Keys
  * [X] die Kommunikation erfolgt verschlüsselt
  * [X] es basiert auf SSL/TLS

## 8.5 HTTPS (10 Punkte)
Sie rufen mit Ihrem Browser eine Seite auf und sehen die folgende Ausgabe:

<img src="img/ssl-error.png" width="400">

Was kann die Ursache für diese Anzeige sein?

*Lösung:*
Das SSL-Zertifikat passt nicht zu dem Namen der Webseite, die aufgerufen wurde. Die Ursache kann zum einen Schlampigkeit sein, d.h. das Zertifikat wurde nicht für alle möglichen Namen ausgestellt, unter denen die Seite verfügbar ist. Zum anderen kann es daran liegen, dass ein Angreifer versucht, sich in die Kommunikation als _Man-in-the-Middle_ einzuhängen.

## 8.6 Aufbau einer HTML-Seite (20 Punkte)
Geben Sie den ungefähren Aufbau einer HTML-Seite mit den entsprechenden Bereichen (Header, Titel, Meta-Daten, Body, etc.) an. Formulieren Sie Ihre Antwort mit den entsprechenden HTML-Tags.

*Lösung:*

```html
<!DOCTYPE html>
<html>
  <head>
    <meta name="keywords" content="HTML, JavaScript, PHP">
    <title>Meine Webseite</title>
  </head>
  <body>
    
  </body>
</html>
```

## 8.7 Hypertext (15 Punkte)
HTML steht für _HyperText Markup Language_. Welche Aussagen zu _Hypertext_ sind korrekt?

  * [X] Dokumente enthalten Verweise auf andere Stellen im selben Dokument
  * [X] Dokumente werden miteinander verknüpft
  * [X] Dokumente enthalten Verweise auf andere Dokumente
  * [ ] In HTML ist das `<link>` Tag entscheidend für die Verlinkung der Dokumente
  * [ ] Dokumente enthalten nicht nur Text, sondern auch Bilder und andere Medien
  * [ ] Dokumente enthalten andere Dokumente
  * [X] In HTML ist das `<a>` Tag entscheidend für die Verlinkung der Dokumente
  * [X] Dokumente bauen eine netzartige Struktur auf
  * [ ] Dokumente bilden einen Hyperkubus

