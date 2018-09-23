# ESP8266-IR
IR Signale empfangen und senden. 

Ich habe die Codes vom Denon RC-1016 für DENON AVR-2106 ermittelt, siehe codes.txt.

Das Grundsetup habe ich von https://github.com/polygontwist/ESP_sonoff_Schaltuhr abgeleitet (TA, Timersteuerung,...).

# Quellen und Inspirationen
folgende Bibliothecken wurden verwendet:
* JeVe_EasyOTA (Version 2.2.0) https://github.com/jeroenvermeulen/JeVe_EasyOTA/
* ESP8266WiFi
* WiFiClient
* ESP8266WebServer
* time
* FS (SPIFFS)
* https://github.com/markszabo/IRremoteESP8266

* https://daniel-ziegler.com/arduino/esp/mikrocontroller/2017/07/28/arduino-universalfernbedienung/

# Installation mit Arduino IDE 1.8.5
* zuerst müssen die Zeilen #define WIFI_SSID und #define WIFI_PASSWORD aus kommentiert und befüllt werden
* die Zeile #include "wifisetup.h" ist auszukommentieren (ich habe dort meine Wifi-Einstellungen abgelegt)
* Einstellung: Generic ESP8266 Modul, 80 MHZ, 40MHz, DOUT, 115200, 1M (64k SPIFFS)
* Um den ESP im Netzwerk zu finden, sollte ARDUINO_HOSTNAME definiert werden

Bei upload auf den ESP muß der Flash-Button gedrück werden und dann Reset gedrückt werden - damit geht der ESP8266 in den Programiermodus.

Nach dem Übertragen startet der ESP8266 neu und meldet sich im angegeben Netzwerk an. Mit der Seriellen Konsole kann der Bootvorgang beobachtet werden. Wenn alles klappt kann man updates per OTA einspielen.


## Hardwaresetup
* IR-Diode: ld 274-3
* Empfänger: TSOP31240

<img src="https://github.com/polygontwist/ESP8266-IR/blob/master/fritzing/schaltung.png" width="365" alt="Schaltplan ESP8266 IR">

Verwendung auf eigene Gefahr!


## Funktionen
* Schalten per WLAN-Verbindung
* definieren von Timern (Schaltuhrfunktion)
* Uhr wird per NTP (Network Time Protocol) aktuell gehalten, Server ist 0.europe.pool.ntp.org (siehe myNTP.h)
* automatische Umschaltung Sommer-/Winterzeit
* update per OTA möglich (Arduino)
* Oberfläche per Javascript und CSS gestaltbar

## Webview
<img src="https://github.com/polygontwist/ESP8266-IR/blob/master/fritzing/webview.png" width="248" alt="Webview">
