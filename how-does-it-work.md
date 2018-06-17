# Wie funktioniert es?

OpenPlotter kann Daten der Schnittstellen NMEA 0183, NMEA 2000 und Signal K verarbeiten.

Alle Daten im NMEA 0183- und NMEA 2000-Format werden in das Signal K-Format konvertiert. Einige Sensoren verwenden direkt das Signal K-Format.

Wenn die Daten einmal in Signal K übersetzt sind, kannst Du sie in unterschiedlichen Apps darstellen oder wieder zurück nach NMEA 0183 oder NMEA 2000 konvertieren, um sie dann weiter an andere Apps oder Geräte zu leiten. 

## Datenfluß

![](.gitbook/assets/nav_data3.png)

## NMEA 0183

OpenPlotter kann NMEA 0183-Daten von seriellen Geräten \(USB, UART...\) ebenso lesen wie aus dem Netzwerk über UDP oder TCP.

Serielle Geräte werden über den Reiter "Serial" definiert, Netzwerkverbindungen über den Reiter "Kplax":

{% page-ref page="serial/" %}

{% page-ref page="kplex.md" %}

Der Signal K-Server liest NMEA 0183-Daten, konvertiert alle NMEA 0183 Sequenzen, die er verstehen kann, in das Signal k-Format und gibt die NMEA 0183-Rohdaten weiter an den TCP-Port 10110.

Wenn Du Geräte hast, die NMEA 2000- oder Signal K-Daten senden und Du möchtest diese in ein NMEA 0183-Format übersetzen und zusätzlich an den TCP-Port 10110 senden, musst Du die NMEA 0183-Sequenzen aktivieren, die im Plugin "_Convert Signal K to NMEA 0183_" benötigt werden.

{% page-ref page="signal-k-server/signal-k-to-nmea-0183.md" %}

## NMEA 2000

Um NMEA 2000-Daten zu senden und zu empfangen, muss ein serieller Konverter wie der USB-CAN Stick angeschlossen werden. Der Activesense NGT-1 wird ebenfalls unterstützt.

{% page-ref page="can/can-usb-stick.md" %}

Das Gerät muss im Reiter "_Serial_" definiert und im Reiter "_CAN_" konfiguriert werden.

Wenn Du Geräte verwendest, die NMEA 0183- oder Dignal k-Daten versenden und diese sollen in NMEA 2000 konvertiert und an NMEA 2000-Geräte versendet werden, muss der Empfang der PGN's in den Geräten erlaubt werden und definiert werden, welche Singal K-Daten versendet werden sollen:

{% page-ref page="can/" %}

## SIGNAL K

Daten von NMEA 0183 und NMEA 2000 Geräten werden automatisch in Signal -Daten übersetzt.

Rohdaten aus  IMU - GPIO - I2C - 1W - SPI Sensoren, MQTT und einige anderen Quellen werden in Signal k-Daten konvertiert, nachdem wie diese Datenquellen in den entsprechenden Reitern definiert haben:

{% page-ref page="pypilot/compass-calibration.md" %}

{% page-ref page="gpio/" %}

{% page-ref page="i2c/" %}

{% page-ref page="1w/" %}

{% page-ref page="spi/" %}

{% page-ref page="mqtt.md" %}

{% page-ref page="tools/analog-ads1115.md" %}

{% page-ref page="tools/analog-firmata.md" %}

Wenn Signal K-Daten aus diesen Quellen nach NMEA 0183 oder NMEA 2000 übersetzt werden sollen, muss vorher geprüft werden, ob NMEA 0183-Sequenzen oder NMEA 2000-PGN's für diese Daten bereits existieren. Beachte die vorhergehenden Abschnitte, um herausfinden, wie das gemacht wird.

