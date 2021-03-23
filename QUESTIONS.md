## Flusskontrolle
- Wieviele darf der Sender senden, wieviel kann der Empfänger verarbeiten?
- Was garantiert Flusskontrolle?
- Wie funktioniert der Sliding Window Algorithmus?
- Wie funktionieren Sende- und Empfängerpuffer? Wie erfährt der Sender wieviel noch gesendet werden kann? rwin + last acked segment 
- Volle Empfangspuffer also wenn der Sender ein rwin=0 erhält, würden den Sender für immer davon abhalten neue Pakete zu senden, wie kann man dieses Problem lösen?
- Wichtigste Formel des Semesters Datenrate <= Fenstergröße/RTT
- Die wichtigste Formel ist eine obere Schranke für die Datenrate die das Protokoll erreichen kann.
- Wie löst die Senderseite das rwin=0 Problem?
- Wie hilft die Empfängerseite das rwin=0 Problem zu lösen?
- Was ist der Persist-Timer?
- Wann wird der Persist Timer aktiv?
- Was ist der Window Update Mechanismus? Empfänger sendet ein erneutes ACK mit größerem rwin
- Wann darf ein Probe Packet (1Byte) gesendet werden?
- Was ist das Silly Window Syndrome?
- Das Silly Window Syndrome, tritt auf der Empfängerseite, was ist ein ähnliches Problem auf der Senderseite, dass durch den Nagle Algorithmus gelöst werden konnte?
## Warteschlangen
- Zu kleine Fenstergröße => Stop and Wait Effekt, zu große Fenstergröße reguliert (self clocking) sich selbst, ist aber trotzdem nicht gut
- Warum bleibt die Formel Datarate R=W/RTT erhalten, selbst wenn die Fenstergröße größer als das BDP gewählt wird? 
- Man muss unterscheiden zwischen R und Rb(b=bottleneck link) und kann dann dementsprechend die Formel anpassen und die RTT für den Rb und W ausrechnen. Diese RTT ist dann die im ausgelasteten Netz und RTT0 ist die am Anfang. BDP0 = Rb*RTT0
- Warteschlangentheorie???
- Lambda Datenrate bzw: der Wert, der uns die Information liefert wie groß die durchschnittlichen Zeiten zwischen 2 Paketen sind
- In der normalen Netzwerktheorie würde ein gerade abfließendes Paket nicht mitgezählt werden, in der Wartenschlangentheorie hingegen schon. Warum ist das so?
## MSS und MTU
- Was bedeuten die beiden abgekürzten Bottlenecks?
- 576 kleinste Byte Menge per Definition = (TCP-Datenmenge)+20(Ip-Header)+20(TCP-Header) kleinste Byte Menge per TCP Definition glaub ich
- Warum ist die minimale Segment Größe von TCP 536 und die minimale Transmission Unit ist aber durch den Wert 576 beschränkt?
- Wie kann der Sender vom Empfänger erfahren wie groß ein Segment maximal sein darf?
- Woher stammt die Größe der MTU? Sicherungsschicht gibt das normalerweise vor? Schicht 2 gibt vor, eigentlich ist es eine Eigenschaft des Pfades und somit ein Konzept der Netzwerkschicht und beachtet muss sie in der Transportschicht werden 
- Path MTU Discovery Paper screenen?
- Was ist MSS Clamping und warum ist es ein "Hack"?
- Welche Schicht pfuscht beim MSS Clamping in einer anderen herum und mit welchem Ziel?
- MSS Clamping widerspricht dem Konzept: separation of concerns? 
- MSS in TCPsprech (ugs.) meint minimum aus MSS und MTU
- Wie geht man mit nichtvollen Segmenten um, also mit Segmenten, dessen Datenmenge < MSS ist?
- Was ist das Tinygram Problem?
- Wie bietet die Funktionsweise des Nagle-Algorithmus eine Lösung auf das Tinygram Problem?
- Rewatch 5-28
- Wie nennt man Netzwerke mit hoher RTT und hoher Bandbreite?
- Das rwin Feld ist nur 16-bit (64kBit) groß weshalb wir keine Datenpakete die größer als 64kByte sind akündigen können. Das ist viel zu klein für heutige Maßstäbe. Wie löst man das Problem?
- Wie funktioniert der Window Scaling Algorithmus? Optionsheader Optionstyp 3
- Rewatch 5-31
- Sequenznummern-Überprüfung? 32 Jahre später Bug gefunden? Fin war, Syn war? Zeitgleicher Zero-Window Zustand Probe-Packe-Versand (war :D)
- Sequenznummern-Überprüfungskriterien? Segmentlänge > 0? Fenstergröße > 0 -> gültig gdw es min. teilweise in das Fenster fällt
- Sequenznummern-Überprüfungskriterien? Segmentlänge > 0? Fenstergröße = 0 -> ungültig
- Sequenznummern-Überprüfungskriterien? Segmentlänge = 0? Fenstergröße > 0 -> gültig gdw Seq.Nr. ins Fenster fällt
- Sequenznummern-Überprüfungskriterien? Segmentlänge = 0? Fenstergröße = 0 -> gültig gdw die Seq.Nr genau das erste fehlende Byte hinter dem Fenster ist
## Timeout berechnen (im Zusammenhang mit Zuverlässigkeit)
- TCP Timeout: Wie kann man den RTO heutzutage in TCP berechnen? EstimatedRTT + 4 * DevRtt
- Exponentiell gleitendes Mittel
- DevRtt_new = (1-beta)DevRTT_old + beta *  | SampleRTT-EstimatedRTT |
- Warum ist 2*EstimatedRTT kein gutes Maß für das RTO?
- Woraus setzt sich das EstimatedRTT zusammen?
- Was sieht die Modifikation durch den Karn-Algorithmus vor? Man darf kein ACK als RTT Messung heranziehen, wenn das Paket bereits mehr als 1 mal übertragen wurde
- Timestamp Option noch besser als Karn.
- Wie funktioniert die Timestamp Option?
- Was ist muss in ein TCP Segment gebastelt werden damit die Timestamp Option funktioniert?
- Was ist ein TDACK und wie sieht es in einem Sequenzdiagramm aus?
- Was ist der Fast Retransmit Mechanismus?
- Inwiefern weicht der Fast Retransmit Mechanismus der in TCP Tahoe angewandt wird vom Standard Go-Back-n ab?
- Selective Acknowledgements (SACKs) Option 4 in TCP Optionen wenn man das beherrscht und 5 beinhaltet Segmente
- Warum kann die SACK-Option nicht endlos lang werden?
- DACK Delayed ACK / Jedes 2. mit begrenzung von 500ms
- Was ist die funktionsweise des DACK-Mechanismus?
- Welchen Mechanismus soll das DACK effizienter gestalten?

## Random
- Was bedeuten kumulative ACKs?



## CDN Ziele und Ideen um RTTs zu verkürzen
- Was sind Content Distribution Networks?
- Was ist das Ziel von Content Distribution Networks? RTTs verkürzen - Servernähe zu Client/Browsernähe

- Was ist ANycast beim Routing?
- Was ist der naheliegene Gedanke für CDNs um zu rekonstruieren wo man eine Anfrage hin routen sollte?
- Request Routing auf Transportschicht? Dreieck? A->B->C->A

## Http Stuff
- Wann entsteht ist Head-of-Line Blocking (Http/1)?
- Wann entsteht ist Head-of-Line Blocking (Http/2)? verloren gegangenes Segment

- Warum wird in modernen Browsern Pipelining vermieden?
- Was ist Pipelining?
- Was sind Probleme bei mehreren parallelen TCP Verbindungen im Zsmhg. von Http?
- Was ist eine kritische Variable bei Http die im wesentlichen versucht wird zu reduzieren?
- Probleme mit dem Content-Length Header bei Http?
- Warum ist es nicht so gutes Design, dass bei HTTP die Serverseite das Schließen von TCP Verbindugnen anstößt?
- Warum sind Latenzen oftmals wichtiger als Datenraten? - Fact 2
- Warum ist es nicht egal wer zuerst redet? kostet Rtt
- Warum ist es nicht egal wer das letzte Wort hat? Entscheidet wer Verbindungen in Tabelle mit TIME_WAIT halten muss

## From exam protocols
- Was sind long fat pipes?
- Was ist ein Router?
- Was ist Router switching?
- Was ist der islip Algorithmus?
- Was ist ein Bufferbloat?
- Wie behebt man einen Bufferbloat? Was ist RED/CoDel?
- Was sind die n Eigenschaften von TCP?
- Wie funktioniert SMTP?
- Wie sieht das Ende einer SMTP Nachricht aus?
- Was sind die Vor-/Nachteile an der Art wie eine SMTP Nachricht beendet wird?
- Was sind die bekanntesten TCP Modelle, die in der VL vorkamen?
- Zustandsdiagramme von TCP Algorithmen?
- Was sind mögliche Probleme, wenn der Server seine Verbindung schließen möchte?
- Und was passiert im schlimmsten Fall, wenn der Server sein Timeout zu klein wählt?

- Ein Sender überträgt mit großer Datenrate über einen Ruter der nur kleine Datenraten weitersenden kann?

## Sachen die in Fragen verpackt werden müssen, wenn notwendig
- Fehlerbalken
- Bottleneck
- TCP Cubic
- TCP Reno
- TCP New Reno
- Fast Retransmit
- Fast Recovery
- Unterschiede: TCP Reno und TCP New Reno

- BGP und Routing

- Selbstsynchronisierungseffekte
- Was ist ein TDACK?
- Wie kann man Paketverluste feststellen?
- Wie handelt TCP Reno ein TDACK? -> Fast Retransmit + Fast Recovery
- Fast Recovery genauer erklären: Wie funktioniert Window Inflation, warum funktioniert das, Unterschiede zwischen Reno und new Reno erklären.
- Welche Routing Prinzipien kennen sie?
- Wie funktioniert der Sliding Window Algorithmus?
