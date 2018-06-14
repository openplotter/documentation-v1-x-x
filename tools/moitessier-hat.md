# Moitessier HAT

![](../.gitbook/assets/moitessier-hat-quick-start-guide-page1.jpg)

## Features

* High-sensitivity \(better than -112 dBm\) **dual channel AIS receiver** with SMA antenna connector.
* High-performance **GNSS receiver** with integrated patch antenna and external antenna support via BNC connector.
* **Compass**, **heel** and **trim** from gyroscope, accelerometer and magnetometer sensors \(IMU\).
* **Barometric pressure**.
* Standalone usage or in combination with Raspberry Pi \(\). Sensors are directly accessible via Raspberry Pi. Standalone usage requires 3.3V power supply and sensors are controlled by the HAT’s microcontroller
* Fully compatible with Raspberry Pi models supporting 40-pin IO header.
* Data communication via SPI \(AIS, GNSS and meta data\) and via I2C \(sensor data\). Data accessible via device driver and device file.
* Supports ID EEPROM and automatic device tree loading
* 3 status LEDs \(AIS status, GNSS status, error\)
* Full OpenPlotter compatible. Plug and play.

{% hint style="success" %}
This item is available in our [Web Shop](http://shop.sailoog.com).
{% endhint %}

## Mounting the HAT

![](../.gitbook/assets/moitessier-hat-quick-start-guide-page2.jpg)

![](../.gitbook/assets/moitessier-hat-quick-start-guide-page3.jpg)

## Installing drivers

After mounting the HAT go to _OpenPlotter - Tools - Moitessier HAT_. A small window will open, press _start_.

![](../.gitbook/assets/moitessier_settings0.png)

A new window will open and you will see:

_Moitessier HAT is attached._   
_Moitessier HAT package is not installed!_

Go to _Install_ tab and check your Kernel version. In the picture below the Kernel version is _4.14.34_

Select the package matching your Kernel version in _Available packages_ field. Only the first 3 figures are important, in this case _4.14.34_

![](../.gitbook/assets/moitessier_settings1.png)

Press _Install_ and a terminal window will open. The drivers will be installed and the firmware of the HAT will be updated. The system will automatically reboot at the end of the process.

![](../.gitbook/assets/moitessier_settings2.png)

## Configuring GNSS and AIS reception

![](../.gitbook/assets/moitessier_settings3.png)

![](../.gitbook/assets/moitessier_settings4.png)

## Configuring compass, heel and trim reception

{% page-ref page="../pypilot/compass-calibration.md" %}

## Configuring pressure reception

## Getting info from the HAT

## Advanced settings

## Enclosure

![Moitessier HAT + Raspberry Pi enclosure](../.gitbook/assets/moitessier-enclosure-casing-by-rooco.jpg)

{% hint style="success" %}
This item is available in our [Web Shop](http://shop.sailoog.com).
{% endhint %}

## External antennas

{% hint style="success" %}
This item is available in our [Web Shop](http://shop.sailoog.com).
{% endhint %}



