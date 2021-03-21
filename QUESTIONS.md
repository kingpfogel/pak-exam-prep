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
