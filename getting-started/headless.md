# Mode sans écran

## Premier démarrage

Après avoir créé la carte SD OpenPlotter sous NOOBS, l'insérer dans le Raspberry Pi, connecter l'alimentation et attendre l'apparition d'un nouveau réseau Wifi _openplotter_ dans la liste des points d'accès valides. Le process peut demander jusqu'à une demie heure pour se dérouler.

SSID: openplotter  
Mot de passe: 12345678

## Connexion

* Install [RealVNC Viewer](https://www.realvnc.com/en/connect/download/viewer/) on your laptop, desktop computer, tablet or smart-phone
* Open VNC Viewer and select _File -&gt; New connection_
* Introduce the OpenPlotter address and press _OK._ If OpenPlotter is working as access point, the address is **10.10.10.1**_._ If it is working as client of another access point, you have to find out what address has the access point given to OpenPlotter.

![](../.gitbook/assets/vnc_client1.png)

* Introduce the _Username_: pi
* Introduce the _Password_: raspberry
* Select _Remember password_, press _OK_ and you are in!

![](../.gitbook/assets/vnc_client2.png)

## Change passwords

{% hint style="danger" %}
Please change the WiFi access point defaul password and the _pi_ user default password as soon as possible. If you do not do this, anyone will be able to connect to your system. See _First settings._
{% endhint %}

{% page-ref page="first-settings.md" %}



