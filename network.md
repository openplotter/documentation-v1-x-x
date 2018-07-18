# Network

Network management has changed, now it is based on the native management system of Raspbian.

OpenPlotter can configure the built-in wlan device on Raspberry Pi 3 and 3+ to act as an Access Point \(AP\). On Raspberry Pi 3 you can set the built-in wlan device to act as OpenPlotter AP and connect as a client to the AP of the marina simultaneously. On Raspberry Pi 3+ you need an extra wlan device if you want to set OpenPlotter as AP and you want to connect to another AP as client too.

You can connect your mobile phone to the USB port and enable USB tethering to share the GSM/WLAN internet connection with all the devices connected to the AP OpenPlotter. Set _Sharing internet device_ to _USB0_. Android auto disables USB tethering. You must activate it everytime! The tethered connection can be used to remote control the RPi with VNC-viewer. You only need the IP address which android gives the RPi \(192.168.42.xxx\). The android app "Network Tools" from HE.NET does tell you the address in menu-&gt;device manager. In _client_ mode the ip address is fixed to 192.168.42.100. Many like this connection for:

* Emergency replacement if your display is broken
* Your mouse or keyboard does not work
* Your network does not work 
* Headless use

You can connect your laptop, plotter... to the ethernet port of the Raspberry and OpenPlotter will work as a router \(_bridge eth0_\).

What does bridge mean? This is how routers work. It doesn't matter if you connect your client to an ethernet port of the router or to the routers AP. It is not a good idea to connect a router \(or your RPi in bridge mode\) to a router \(only if it has an uplink port and you use it\)! Rpi ethernet port as client -&gt; no bridge RPi ethernet port as DHCP server -&gt; bridge

![Picture 1. RPI3: AP/client + bridge eth0](.gitbook/assets/network_rpi3_ap-sta.gif)

In picture 1, the RPi works like a router \(AP\) for your tablet or smartphone and gets Internet connection over the built-in WIFI. If the chartplotter has an ethernet port and a remote control app "gofree", you can connect it too. You can also connect your netbook to the ethernet port.

![Picture 2. RPI3: AP + client + bridge eth0](.gitbook/assets/network_rpi3_ap-sta2.gif)

Same as Picture 1 but with a second WIFI device.

![Picture 3. RPI3: AP + client + bridge eth0](.gitbook/assets/network_rpi3_ap_tethering.gif)

Same as picture 2 but with an android smartphone connected by USB as a replacement for the WIFI device. The smartphone can be connected to the marina WIFI or to GSM internet. USB tethering must be activated.

Choose one of the available standard configurations and click on _Set_ to enable it.

![](.gitbook/assets/network_modes.png)

Choose the device which has the internet connection \(client\). OpenPlotter will share it to the AP and to the ethernet port if a bridged mode is selected. Do not select wlan1 or uap0 \(AP\) in _Share internet device_.

![](.gitbook/assets/network_ui.png)

{% hint style="warning" %}
If you set a mode that is not _client_, wlan0 will be always the client and wlan1 or uap0 will be always the AP.
{% endhint %}

You can change the name of the AP \(SSID\).

{% hint style="danger" %}
You must change the password every time you set a new mode. If you do not change this, the password will be the default **12345678** and anyone will be able to connect to your system!!!
{% endhint %}

You can change the channel.

{% hint style="warning" %}
Channel until max 13 can be used for 2.4 GHz. Channel starting at 44 can be used for 5 GHz. The channels allowed in your country are set by the country code. OpenPlotter does not check if you set a wrong channel!
{% endhint %}

Click _Apply_ to write the configuration. **It will be activated after next boot**.

{% hint style="info" %}
On Raspberry Pi 3 you can use the built-in WIFI device as AP and client. No USB wlan stick is needed!

**Advantage**  
Less power consumption.  
A free USB port.  
You do not have to change the network mode when you are in the marina.

**Disadvantage**  
Lower download performance.  
OpenPlotter must be in a good place to get a good internet connection \(unrealistic\).
{% endhint %}

