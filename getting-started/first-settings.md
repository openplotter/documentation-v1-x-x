# First settings

Go to _Menu &gt; Preferences_ and select _Raspberry Pi Configuration_

![](../.gitbook/assets/rpisetup1.jpg)

A window will open where you can personalize your system. 

![](../.gitbook/assets/rpisetup3.jpg)

{% hint style="danger" %}
It is a good idea to change the password to make OpenPlotter more secure. Click on _Change Password_ \(default password: raspberry\).

If you do not change the password, anyone will be able to connect to OpenPlotter remotely. Please do it now.
{% endhint %}

If you need to set your system localisation, click on the _Localisation_ tab and then on _Set Locale_ \(language\), _Set Timezone, Set Keyboard_ and _Set WiFi Country_ buttons.

![](../.gitbook/assets/rpisetup2.jpg)

## Network settings

{% hint style="danger" %}
If a WiFi access point is enabled please change the default password as soon as possible in _Network_ tab. There you can disable the access point or set another network mode too.
{% endhint %}

{% page-ref page="../network.md" %}

## Signal K settings

Signal K server provides many useful tools and you will have to visit its administration panel often. Go to _Menu_ &gt; _OpenPlotter_ &gt; _Signal K._

#### Password

Data visualization is open but settings is under authentication. Press _Login_ button upper right.

User name: openplotter  
Password: openplotter

![](../.gitbook/assets/sk_login.png)

{% hint style="danger" %}
Please change this password as soon as possible. Login and go to _Signal K_ &gt; _Security_ &gt; _Users_ &gt; _openplotter_
{% endhint %}

#### Vessel data

If you are going to share data with other boats you should have an unique identifier. Login to Signal K and go to _Server_ &gt; _Vessel_ _data_ and change at least your bot name and MMSI.

Here you can also provide data about your boat that could be useful for some Signal K tools.

![](../.gitbook/assets/sk_vessel_data.png)

