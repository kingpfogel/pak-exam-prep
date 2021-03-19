# pak-exam-prep

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


### Prüfungsfragen
- TCP Verbindungsaufbau und Abbau anhand eines Zustandautomaten erklären (Timewait...)
- Zuverlässigkeit in TCP: Definition und Umsetzung
- TCP Reno und New Reno: Fast Retransmit, Fast Recovery, sowie Unterschiede zw. den beiden Versionen erklären
- BGP und Routing im Internet grob erklären, Probleme von BGP umreisen
- TCP Cubic anhand von Verlaufsgraphen erkennen
- Fehlerbalken zu einer ns3 Simulation erklären (zwei UDP sender vor einem Bottelneck):
    - Was für Fehlerbalken sind das?/Was für Fehlerbalken sind hier sinnvoll?
    - was sollte man bei dieser Simulation erwarten? 
    - Warum sehen die nicht so aus wie man das eigentlich erwarten würde? 
   (Stichwort: Selbstsynchronisierungseffekte bei Simulation durch fehlenden Zufall)


### Note (Optional)
1.0

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

