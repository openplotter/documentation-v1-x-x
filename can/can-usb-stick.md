# CAN-USB Stick

![](../.gitbook/assets/can-usb-stick.png)

## Proyecto

El proyecto del dispositivo CAN-USB Stick se realizó para analizar el flujo de datos en una red N2K enviando y recibiendo mensajes CAN. Está aislada eléctricamente para evitar daños.

El  CAN-USB Stick se basa en un micro controlador \(MCU\) stm32 conectado a un transceptor CAN aislado y a un convertidor USB a serie.

El programa del MCU se ha rediseñado para trabajar conjuntamente con el proyecto [CANBOAT](https://github.com/canboat/canboat), que es utilizado en el proyecto [Signal K](http://signalk.org/). Ambos paquetes se usan en OpenPlotter.

El CAN-USB Stick tambien funciona con el proyecto [OpenSkipper](http://openskipper.org/).

No se ha probado:

* [MacENC](http://macenc.com/)
* [PolarView NS](http://www.polarnavy.com/)

Por lo tanto utiliza el conjunto de comandos que a su vez se usan en el programa CANBOAT actisense-serie. Desde OpenPlotter también se puede enviar y recibir datos de red N2K directamente.

Los nuevos PGNs no están bloqueados, porque están en otros dispositivos capaces de funcionar con CANBOAT. Se puede establecer una velocidad de transmisión mayor que la velocidad del CAN bus. Otros dispositivos capaces de trabajar con CANBOAT tienen una tasa de transferencia más baja que las redes N2K, por lo que pueden sufrir un efecto de  cuello de botella.

{% hint style="success" %}
Este artículo está disonible en nuestra [Tienda de la Web](http://shop.sailoog.com).
{% endhint %}

## Aviso / Descargo de responsabilidad

El CAN-USB Stick es un proyecto de investigación sobre comunicación de datos en CAN bus y redes N2K en barcos.

El software está todavía en desarrollo y no ha sido probado totalmente. Funcionarmientos inadecuados del CAN-USB Stick or any connected device might be possible at any time. Manipulating your N2K network could cause damage to connected devices.

Do not rely on data from this device and do not use it as primary source for navigation. Liability cannot be accepted for any damages, personal injuries or malfunctions caused by this device.

The CAN-USB Stick is not certified by NMEA®.

It is not allowed to use the Actisense® NMEA Reader software for the CAN-USB Stick.

## N2K networks

![](../.gitbook/assets/n2k_b.jpg)

![Example of a small N2K Network](../.gitbook/assets/n2k_a.jpg)

N2K networks are described in [Wikipedia](https://en.wikipedia.org/wiki/NMEA_2000). The backbone \(or trunk\) starts with a 120Ω terminator and ends with a 120Ω terminator. Two resistors are working in parallel, so the resistance is 120Ω/2=60Ω. If there is a broken connection in the backbone you can measure only 120Ω or nothing but not 60Ω. That is a very easy way to check the bus.

![M12 male 120&#x3A9; terminator](../.gitbook/assets/resistor_conn.jpg)

The drop line to devices should not be longer than 6 m. The backbone can have 100m in length.

The CAN-USB Stick is electrically isolated so devices and your computer are protected even if they are powered by a different source than your N2K network.

## Connection

To connect the CAN-USB Stick to the network you need a free T-connector on your backbone and a drop line. The drop line should have a M12, 5 pin male connector in one side and 5 wires \(but we only need 2\) in the other side. The HIRSCHMANN ELST 5012 PG7 connector has a screw terminal.

![T-connector](../.gitbook/assets/t-conn.jpg)

![Drop line M12, 5 pins male connector side](../.gitbook/assets/m12_conn.jpg)

![Drop line wires side](../.gitbook/assets/micro_cable.jpg)

![](../.gitbook/assets/can_usb_connect.jpg)

* Pull out the green screw terminal of the stick.
* Connect the drop line blue wire from pin 5 \(pin in the middle\) to the green terminal on CANL.
* Connect the drop line white wire from pin 4 to the green terminal on CANH.
* Turn off the main power switch to be sure that there is no power on the network.
* Connect the drop line to the free T-connector on your backbone.
* Use a multimeter and measure the resistance between CANH and CANL \(on the screws\). The resistance should be around 60 Ohm.
* Connect the green screw terminal to the CAN-USB Stick.
* Check again the 60 Ohm between CANH and CANL.
* On the drop line there are three cables left. They have to be isolated.
* Turn on the main power.
* Switch on instrumentation.

To configure your CAN-USB Stick on Windows use OpenSkipper To configure it on OpenPlotter go to chapter:

{% page-ref page="./" %}

## LED

The CAN-USB Stick LED will be **OFF** 10" during the boot sequence and then:

* Fixed **ON** if it is not connected to the network.
* **ON** for a second if it is connected to the network.
* Fixed **OFF** if there are not input data.
* **FLASHING** if there are input data.

## Support

If you need support or you have any suggestion you can publish your questions on [OpenMarine forum](http://forum.openmarine.net/forumdisplay.php?fid=11).

