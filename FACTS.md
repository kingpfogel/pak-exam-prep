Zuverlässigkeit mit Pipelining: Go-back-n (empfänger kriegt 10 pakete, wenn eins fehlt in der richtigen Sequenzfolge werden alle bis zum letzten korrekt erhaltenen verworfen

Zuverlässigkeit mit Pipelining: Selective Repeat speichert alle empfangenen Pakete zwischen. über timeouts werden nicht geACKte erneut gesendet

Http/3.0 nutzt statt TLS und TCP nun QUIC (mit integriertem TLS) und UDP. Dadurch das TLS in QUIC integriert ist und keinen extra kryptographischen Handshake wodurch eine RTT gespart werden kann


RFC 1925 you cannot increase the speed of light

Separation of concerns ist nicht durchzuhalten zw. den Protokollschichten


Persistenz: 

- Caching: bedingtes get. CLient if-modified-header, Server last modified header
- Caching: ETag Entity Tag - Prüfsumme
- Caching reduziert nicht RTTs aber die Datenübertragung (Menge) wird gespart.
- Webcaches nur große EInsparungen um lange RTTs durch kurze ersetzen
- Webcaches werden heutzutage vermieden wegen Sicherheit, Verschlüsselung
- RTTs verringern/vermeiden -> Kommunikationsdistanzen reduzieren
- Mit lokalem Caching/fast lokales Caching
- CDNs zu nahegelegenen Kopien umleiten
