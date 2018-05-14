# CAN-USB Stick

![](../.gitbook/assets/can-usb-stick.png)

## Project

The CAN-USB Stick project was done to analyse the data stream on a N2K network sending and receiving CAN messages. It is electrically isolated to avoid damages.

The program of the MCU has been re-engineered to work together with [CANBOAT](https://github.com/canboat/canboat) project, which is used by [Signal K](http://signalk.org/) project. Both packets are used in OpenPlotter.

The CAN-USB Stick does also work with [OpenSkipper](http://openskipper.org/) project.

Not tested:

* [MacENC](http://macenc.com/)
* [PolarView NS](http://www.polarnavy.com/)

So it does use the command set which is used in the CANBOAT actisense-serial program. Sending and receiving data into the N2K network can be done directly from OpenPlotter too.

New PGNs are not blocked, as they are on other devices capable to work with CANBOAT. The transmission speed can be set higher than the CAN bus speed. Other devices capable to work with CANBOAT have a lower transferrate than N2K networks and they may suffer a bottleneck.

{% hint style="info" %}
This item is available in our [Web Shop](http://shop.sailoog.com).
{% endhint %}

## Hardware

The CAN-USB Stick V2 is based on a stm32 micro-controller \(MCU\) connected to an isolated CAN transceiver and an USB to serial converter.

## Warning / Disclaimer

CAN-USB Stick is a research project on data communication on CAN bus and N2K networks in boats.

The software is still under development and has not been fully tested. Malfunctions of the CAN-USB Stick or any connected device might be possible at any time. Manipulating your N2K network could cause damage to connected devices.

Do not rely on data from this device and do not use it as primary source for navigation. Liability cannot be accepted for any damages, personal injuries or malfunctions caused by this device.

The CAN-USB Stick is not certified by NMEA®.

It is not allowed to use the Actisense® NMEA Reader software for the CAN-USB Stick.

## N2K networks

![](../.gitbook/assets/n2k_b.jpg)

![](../.gitbook/assets/n2k_a.jpg)

Example of a small N2K Network.

N2K networks are described in [Wikipedia](https://en.wikipedia.org/wiki/NMEA_2000). The backbone \(or trunk\) starts with a 120Ω terminator and ends with a 120Ω terminator. Two resistors are working in parallel, so the resistance is 120Ω/2=60Ω. If there is a broken connection in the backbone you can measure only 120Ω or nothing but not 60Ω. That is a very easy way to check the bus.

![](../.gitbook/assets/resistor_conn.jpg)

M12 male 120Ω terminator

The drop line to devices should not be longer than 6 m. The backbone can have 100m in length.

The CAN-USB Stick is electrically isolated so devices and your computer are protected even if they are powered by a different source than your N2K network.

