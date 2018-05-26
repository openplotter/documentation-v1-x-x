The Network configuration has changed.

It base on standard raspbian.



OpenPlotter can configure the wlan to act as an "AP" access point. \(Raspberry Pi 3 and 3+ for Raspberry Pi 2 it depends on the used wifi usb stick\)



You can connect to an wlan AP in the habour while the Pi works as AP.

You can connect your mobile phone to the usb port and enable usb teathering to use the GSM internet connection or you can connect via wlan to the internet and share the connection to the Pi by the usb port.

You can connect your notebook, plotter,... to the ethernet port of the Pi. The Pi can work as a router \(bridge to AP\)

![](/assets/network_ui.png)

pic: network ui



Choose one of the available standard configurations. To activate the selection click on "Set".

![](/assets/network_modes.png)

pic: standard configurations



Particularity: For the Pi 3 you can use the internal wifi as an AP and client! No usb wlan stick is needed!

advantage:

* less power consumption
* a free usb port

disadvantage:

* the download performance is lower
* to get a good connection to the internet the Pi must be in a good place





Choose the device which has an internet connection. The Pi will use it and will share it to the AP and to the ethernet port \(if in briged mode\). 

You can change the SSID \(name of the AP\) and the Password.

The channel can be changed. Warning! Channel until max 13 can be used for 2.4 GHz wlan. Channel starting at 44 can be used for the 5 GHz. The channels which are allowed to use in your country is set by the country code. OpenPlotter doesn't check if you put in a wrong channel!

Click "Apply" to write the configuration. It will be activated on next boot.

 



