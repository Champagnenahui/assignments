# 9. Künstliche Intelligenz - Test (Musterlösung) (100 Punkte)

## 9.1 Typologie künstlicher Intelligenz (15 Punkte)
Man unterscheidet häufig _vier Typen_ (oder Stufen) von künstlicher Intelligenz. Bitte erläutern Sie diese kurz.

*Lösung:*
  * Type I: Rein reaktiv
  * Type II: System mit begrenztem Gedächtnis
  * Type III: System mit eigenem Bewusstsein
  * Type IV: Sich "seiner selbst" bewusstes System

## 9.2 Neuron (15 Punkte)
Ein künstliches Neuronales Netz besteht aus sogenannten _künstlichen Neuronen_. Welche der folgenden Aussagen über ein solches Neuron sind korrekt?

  * [X] es gewichtet seine Eingaben
  * [X] es hat einen Schwellwert
  * [ ] es bestimmt seine Ausgabe durch eine Übertragungsfunktion
  * [ ] es hat genau einen Eingang
  * [X] es hat mehrere Eingänge
  * [X] es verwendet einen Übertragungsfunktion, um die gewichteten Eingaben zusammenzufassen
  * [ ] es verwendet einen Aktivierungsfunktion, um die gewichteten Eingaben zusammenzufassen
  * [X] es bestimmt seine Ausgabe durch eine Aktivierungsfunktion
  * [ ] es hat mehrere Ausgänge
  * [X] es hat genau einen Ausgang
  * [X] es basiert auf dem Modell einer biologischen Nervenzelle

## 9.3 Künstliche Intelligenz? (10 Punkte)
Bei welchen der folgenden Dinge handelt es sich um künstliche Intelligenz?

  * [ ] Tabellenkalkulation, die eine Summen und andere Funktionen für die gegebenen Daten ausrechnet
  * [ ] Den Aktienmarkt durch das Anpassen einer Kurve an vergangene Aktienpreise vorhersagen
  * [ ] Bildbearbeitung, z.B. die Anpassung von Helligkeit und Kontrast in Photoshop
  * [X] Musikempfehlungen (z.B. bei Spotify) basierend auf dem Hörverhalten
  * [ ] Big-Data-Lösungen, die große Mengen von Daten speichern, verarbeiten und an viele Nutzer gleichzeitig verteilen können
  * [X] Filter zur Übertragung von Kunststilen (Impressionismus, Kubismus, etc.) auf beliebige Fotos
  * [ ] Die schnellste Route in einem GPS-Navigationssystem suchen

## 9.4 Deep Learning (15 Punkte)
Welche der folgenden Aussagen _trifft_ auf _Deep Learning_ zu?

  * [X] wird bei neuronalen Netzen mit vielen Zwischenlagen angewendet
  * [ ] ist der Oberbegriff für Maschinelles Lernen
  * [X] ist eine Optimierungsmethode für künstliche neuronale Netze
  * [X] ist eine Teilmenge des Maschinellen Lernens
  * [ ] ist ein biologischer Vorgang bei dem Neuronen sich tief vernetzen
  * [X] ermöglichen auch bei neuronalen Netzen mit zahlreichen Zwischenlagen einen stabilen Lernerfolg
  * [ ] wird häufig zusammen mit klassischer Konditionierung eingesetzt

## 9.5 Backpropagation (15 Punkte)
Welche der folgenden Aussagen über _Backpropagation_ treffen zu?

  * [ ] funktioniert auch bei unbekannten Zielwerten
  * [X] die Zielwerte müssen bekannt sein
  * [ ] gehört zu den Verfahren des unsupervised learning
  * [ ] dient dazu, die letzte Schicht (Backplane) in einem künstlichen neuronalen Netz zu strukturieren
  * [X] gehört zu den Verfahren des supervised learning
  * [X] dient dem Einlernen von künstliche neuronalen Netzen

## 9.6 Möglichkeiten und Grenzen der KI (15 Punkte)
Welche der folgenden Aussagen über Künstliche Intelligenz treffen zu?

  * [ ] KIs bestehen den Turing-Test zuverlässig
  * [X] KIs können Autos autonom fahren lassen
  * [X] KIs schlagen Profispieler bei Go
  * [X] KIs können selbständig Retro-Spiele wie Super Mario lernen und spielen
  * [ ] KIs erreichen ähnliche intellektuelle Fähigkeiten wie Menschen
  * [X] KIs schlagen Profispieler bei Schach
  * [X] KIs können Flugzeuge autonom steuern

## 9.7 Berechnungen an einem Neuron (15 Punkte)
Gegeben sei ein künstliches Neuron mit drei Eingängen (x1, x2 und x3) (und einem Ausgang a). Die Gewichte für die drei Eingänge sind:

`(w1, w2, w3) = (0.3, 0.5, 0.2)`

Als Aktivierungsfunktion wird die Sigmoid-Funktion verwendet, wobei vorher noch ein Bias addiert wird. Der Bias beträgt konstant -1.0. Den Verlauf der Sigmoid-Funktion `f` für das Neuron können Sie aus folgender Grafik ableiten (`f(x) = 1 / (1 + exp(-x))`):

<img src="img/sigmoid.png" width="500">

Berechnen Sie für folgende Werte die Ausgabe des Neurons:

`(x1, x2, x3) = (0.0, 2.0, 0.0)`

*Lösung:*


  * Gewichtete Summe der Eingabewerte: `0.3 * 0.0 + 0.5 * 2.0 + 0.2 * 0.0 = 1.0`
  * Plus Bias: `1.0 + (-1.0) = 0.0`
  * Die Ausgabe a ergibt sich aus der Sigmoid-Funktion: `a = 0.5`

