# How does it work?

OpenPlotter can manage NMEA 0183, NMEA 2000 and Signal K data.

All data entering in NMEA 0183 and 2000 format are translated into Signal K format. Some sensors generate data in Signal K format directly.

Once data is converted into Signal K, you can display it in the different apps for visualization or convert it back to NMEA 0183 and 2000 to send it to other devices or apps.

## Data flow

![](.gitbook/assets/nav_data3.png)

## NMEA 0183

OpenPlotter can get NMEA 0183 data from connected serial devices \(USB, UART...\) or connecting to a TCP or UDP network sources.

Define serial devices on _Serial_ tab and network connections on _Kplex_ tab:

{% page-ref page="how-does-it-work.md" %}

{% page-ref page="how-does-it-work.md" %}

Signal K server gets NMEA 0183 data, converts all the NMEA 0183 sentences that it can understand into Signal K format and relays the raw NMEA 0183 data to TCP 10110 port.

If you have devices that generate Signal K data \(IMU, environment sensors...\) and you want to translate it to NMEA 0183 and send it to TCP 10110 port too, you will have to configure this in the _Convert Signal K to NMEA 0183_ plugin:

{% page-ref page="how-does-it-work.md" %}

## NMEA 2000

## SIGNAL K



