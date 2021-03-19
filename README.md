# pak-exam-prep

### Datum der Prüfung
April 2014
### Benötigte Lernzeit als Empfehlung
1 Woche
### Verwendete Materialien (Bücher, Skripte etc...)
Skripte, RFCs
### \"Atmosphäre\" der Prüfung / Verhalten der Beisitzer
Angenehm, erst Einstiegsfragen, dann später viel am WhiteBoard gearbeitet. Beisitzer hat nichts gesagt
### Prüfungsfragen
- Zuverlässigkeit in Netzwerken - Definition
- Wie in TCP? ACKs/Timeout
- Probleme bei TCP mit long fat pipes, wie wird das gelöst?
Am WhiteBoard
- TCP Westwood / TCP Cubic (selbst ausgesucht durch Frage vorher)
- Router: Switching / Crossbar - Algorithmen islip
- Scheduling: VoIP und Datenleitung - Priorityscheduling, Token Bucket
- Was ist Bufferbloat? Wie behebt man das? (RED/ CoDel) 
### Note (Optional)
1.0
### Fazit (Gute/schlechte Prüfung , angemessene Benotung etc...)
Angenehme Prüfung, Breite Streuung der Fragen.

### Datum der Prüfung
2/18
### Benötigte Lernzeit als Empfehlung
1 Woche
### Verwendete Materialien (Bücher, Skripte etc...)
Skripte, ggf. RFC
### "Atmosphäre" der Prüfung / Verhalten der Beisitzer
Sehr angenehm, Kaffee und Tee wurden angeboten. Gespräch wurde auf der Couch mit Einstiegsfragen
gestartet und später am WhiteBoard fortgesetzt.
### Prüfungsfragen
- SMTP Funktionsweise erklären
- Wie wird dann das Ende einer Nachricht angezeigt? 
- Was sind Alternativen?
- Was sind Nachteile bei jedem?
- Dann weiter zu TCP
- Abbildung mit Zuständen bei öffnen und schließen von Verbindungen erklären
- Angenommen der Server möchte Verbindung schließen? Probleme?
- Angenommen Server wählt Timeout zu klein? Was passiert im schlimmsten Fall? 

-- Von jetzt an der Tafel -- 
- Zeichnung an Tafel
- Ein Sender überträgt mit großer Datenrate über einen Router der nur kleine Datenrate weitersenden kann
- Was kommt beim Empfänger an?
- Wenn ein weiterer Sender hinzukommt welche Effekte sehen wir dann? (UDP (keine Überlastkontrolle), Warteschlangen, hier mehrere Fälle betrachtet)
- TCP Cubic erkennen und erklären

### Note (Optional)
1,3
### Fazit (Gute/schlechte Prüfung , angemessene Benotung etc...)
Sehr angenehme Prüfung, Faire Bewertung, mehr breite als tiefgehende Fragen, bei Problemen
leichter Schubs in die richtige Richtung


Datum der Prüfung
   2/2018

Benötigte Lernzeit als Empfehlung
 5-7 Tage

Verwendete Materialien (Bücher, Skripte etc...)
Skripte und RFCs (für Details)

Atmosphäre" der Prüfung / Verhalten der Beisitzer
Entspannt, Beisitzer hat sich sehr zurück gehalten 

Prüfungsfragen
- CP Verbindungsaufbau und Abbau anhand eines Zustandautomaten erklären (Timewait...)
- uverlässigkeit in TCP: Definition und Umsetzung
- CP Reno und New Reno: Fast Retransmit, Fast Recovery, sowie Unterschiede zw. den beiden Versionen erklären
- GP und Routing im Internet grob erklären, Probleme von BGP umreisen
- CP Cubic anhand von Verlaufsgraphen erkennen
- ehlerbalken zu einer ns3 Simulation erklären (zwei UDP sender vor einem Bottelneck):
    - as für Fehlerbalken sind das?/Was für Fehlerbalken sind hier sinnvoll?
    - as sollte man bei dieser Simulation erwarten? 
    - arum sehen die nicht so aus wie man das eigentlich erwarten würde? 
   (Stichwort: Selbstsynchronisierungseffekte bei Simulation durch fehlenden Zufall)


Note (Optional)
1.0

Fazit (Gute/schlechte Prüfung , angemessene Benotung etc...)
Lief gut, der Prüfer hat immer wieder mal nachgefragt und hat verschiedene Themen die ich angerissen habe aufgegriffen für 
Folgefragen. Fragen waren insgesamt weit gestreut. Die Frage mit der Simulation war ganz am Ende und es hat relativ lange 
gebraucht bis ich die richtige Idee hatte. Wurde aber nie gehetzt.



### Datum der Prüfung
Maerz 2018
### Benötigte Lernzeit als Empfehlung
Je nach Vorwissen, wie viel man aus der Vorlesung mitgenommen hat schwierig zu sagen. Der Umfang des Stoffes ist aber ziemlich hoch.
### Verwendete Materialien (Bücher, Skripte etc...)
Vorlesungsfolien, bei Detailfragen gelegentlich in Paper geblickt
### "Atmosphäre" der Prüfung / Verhalten der Beisitzer
sehr entspannt
### Prüfungsfragen
1. TCP
- Wie kann man Paketverluste feststellen?
    -> TDACK und Timeouts
- Wie muss man die Timeouts wählen?
    -> exponentielle Glättung + Varianz für die RTT Schätzung, Timeout auf Basis von RTT wählen, exponentielle Erhöhen für Sendewiederholungen
- Wie handelt TCP Reno ein TDACK?
    -> Fast Retransmit + Fast Recovery
- Fast Recovery genauer erklären: Wie funktioniert Window Inflation, warum funktioniert das, Unterschiede zwischen Reno und new Reno erklären.
- Kummulatives Diagramm über die Häufigkeit von Paketgrößen gegeben, erklären was man sieht, warum man es sieht und umwandeln.
2. Router
- Wie findet ein Router den richtigen Ausgangsport für ein Paket?
    -> Matching und Longest Prefix matching erklären, vor allem im Hinblick auf Effizienz
- Wie können Router aufgebaut werden um Pakete weiterleiten zu können?
    -> Switching Fabric und Crossbar Switches erklären und einmal durch die gesamten Algorithmen durchturnen + Beispiele für Worst Case Szenarien
3. TCP (Nochmal)
- Wie sieht der Verlauf von der Fenstergröße aus über der Zeit aus (Sägezähne)? Einmal mit RTT auf der x-achse, einmal mit der Echtzeit
- Wie verändern sich die Sägezähne wenn die RTT sich auf einmal verdoppelt?

### Note (Optional)
### Fazit (Gute/schlechte Prüfung , angemessene Benotung etc...)
Insgesamt eine sehr angenehme Prüfung. Der Prüfer hat schwierige Fragen gestellt aber war auch zufrieden wenn man etwas braucht um auf die Lösung zu kommen. Am Ende war er mit meiner Prüfungsleistung zufriedener als ich.



### Datum der Prüfung
4/2018
### Benötigte Lernzeit als Empfehlung
1 Woche bei Anwesenheit in der vl
### Verwendete Materialien (Bücher, Skripte etc...)

### "Atmosphäre" der Prüfung / Verhalten der Beisitzer
Entspannt, die erste Hälfte der Prüfung ist auf dem Sofa, der zweite am Whiteboard. Der Beisitzer war still.
### Prüfungsfragen
1. TCP-Zustandsdiagramm:
1.1 Wie verhält sich ein Http-Server, welche Zustände durchläuft er?
1.2 Was passiert wenn der timeout beim timewait zu kurz ist?(ack beim client kommt nicht an->fin resend ->server antowrtet mit rst->verbindung geschlossen, ABER: mit FIN gesendete Daten vom Client sind nicht bestätigt, client weiß nicht ob angekommen oder nicht!
2.: Laserverbindung zw. Mars und Erde, mehrere Gbit/s Datenrate, RTT im Minutenbereich ->Warum ist das für ein Transportprotokoll problematisch? 
2.1 Warum ist das für tcp blöd?(stichwort long fat pipes)
3. Wie funktioniert Routing (im Internet)?(link-state-routing, dinstance vector,BGP erklären)
3.1 Wie sehen bgp-routen aus? (ip-präfix,as-liste,next-hop)
3.2 warum muss die as-liste vollständig sein?(ev. Kreisrouting)
4: Verbindung mit 2 Routern: A-10Mbits, 10ms->(R)- 2Mbits, 30ms->(R)- 1Gbit/s, 10ms->(B)
4.1 Zeichne Graph und erkläre: R(W) und RTT(W) bei einem sliding-window
4.2 Wo entstehen queues und wie groß sollte man die buffer bei tcp tahoe/reno wählen, um das bottleneck auszunutzen?
4.3 Gibt es TCP-Varianten bei denen der A. Nonym nicht gefüllt wird?
4.4 Wenn der A. Nonym vor dem Bottleneck nur halb so groß ist, reicht das noch bei tcp cubic? (ja, qmax muss nur 1/4 von bdp0 sein)
4.5 Angenommen bei dem Link zw. R und B tritt ein zufälliger Paketverlust bei 10 hoch -7 der Pakete auf. Ist das Schlimm für TCP?
(R###sqrt(3/2p)mss/rtt-formel benutzen)
### Note (Optional)
1,3
### Fazit (Gute/schlechte Prüfung , angemessene Benotung etc...)
Sehr Fair, ich hätte mich eher bei 2,x gesehen



### Datum der Prüfung
April 2018
### Benötigte Lernzeit als Empfehlung
~10 Tage
### Verwendete Materialien (Bücher, Skripte etc...)
Skript, Übungsaufgaben, vereinzelt Paper und RFCs
### "Atmosphäre" der Prüfung / Verhalten der Beisitzer
sehr angenehm, Beisitzer sagt nichts
### Prüfungsfragen
- Was bedeutet Zuverlässigkeit im Kontext von TCP? Wie wird diese umgesetzt?
- Wie routet man innerhalb des Internets, welche Routing-Prinzipien kennen wir
  und wie funktionieren diese?
- Angenommen wir müssen eine Marsstation mit Daten versorgen, wie setzen wir das
  um? Ist ein Schiebefenster hier überhaupt notwendig?
- An der Tafel war ein Netzwerk mit mehreren Routern aufgemalt: Verlauf von
  Datenrate/RTT bei wachsender Sendedatenrate/Fenstergröße
- Dazu: wie können wir mit Hilfe der Warteschlangentheorie Vorhersagen über u.a.
  Paketverlustraten anstellen?
- Wie ist die durchschnittliche Datenrate im angemalten Szenario bei Verwendung
  von TCP Reno? Wie ist die Paketverlustwahrscheinlichkeit?
### Note (Optional)
ganz ok
### Fazit (Gute/schlechte Prüfung, angemessene Benotung etc...)
gute Prüfung, hätte eine schlechtere Note erwartet. Es empfiehlt sich, während
der Prüfung seine Gedankengänge laut auszusprechen um Rückmeldung vom Prüfer zu
erhalten. Formeln werden, sofern notwendig, durch den Prüfer aufgeschrieben; das
Auswendiglernen war (zumindest bei mir) nicht nötig
