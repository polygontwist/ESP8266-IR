# ESP8266-IR
IR Signale empfangen und senden. Codes für Denon RC-1016 für DENON AVR-2106 ermittelt.


## Quellen
* https://github.com/markszabo/IRremoteESP8266


## Hardwaresetup
<img src="https://github.com/polygontwist/ESP8266-IR/blob/master/fritzing/schaltung.png" width="386" alt="Schaltplan ESP8266 IR">

Verwendung auf eigene Gefahr!

## Funktionen
* Schalten per WLAN-Verbindung
* definieren von Timern (Schaltuhrfunktion)
* Uhr wird per NTP (Network Time Protocol) aktuell gehalten, Server ist 0.europe.pool.ntp.org (siehe myNTP.h)
* automatische Umschaltung Sommer-/Winterzeit
* update per OTA möglich (Arduino)
* Oberfläche per Javascript und CSS gestaltbar


