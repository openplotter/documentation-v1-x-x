# Première configuration

## Paramétrage général

Dans le menu général Raspberry choisir _Preferences_ puis sélectionner _Raspberry Pi Configuration_

![](../.gitbook/assets/rpisetup1.jpg)

Une fenêtre s'ouvrira, vous permettant de personaliser votre système. 

![](../.gitbook/assets/rpisetup3.jpg)

Si vous avez besoin de préciser la localisation de votre système \(et si vous lisez ces pages, c'est probable\), cliquez sur l'onglet _Localisation_ puis le bouton _Set Locale_ \(pour choisir la langue\), puis sur les boutons _Set Timezone, Set Keyboard  et Set WiFi Country_.

![](../.gitbook/assets/rpisetup2.jpg)

{% hint style="danger" %}
C'est une bonne idée que de changer le mot de passe pour rendre OpenPlotter plus sécure. Pour cela, cliquez sur _Change Password_ \( mot de passe par défaut : raspberry\).

Si vous ne le faites pas, n'importe qui pourra se connecter à distance à OpenPlotter. S'il vous plait, faites le maintenant.

Il est préférable d'avoir choisit la localisation avant, de manière à ce que le clavier soit correctement interprété.
{% endhint %}

## Configuration du réseau

{% hint style="danger" %}
If a WiFi access point is enabled please change the default password as soon as possible in _Network_ tab. There you can disable the access point or set another network mode too.
{% endhint %}

{% page-ref page="../network.md" %}

## Configuration Signal K

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

If you are going to share data with other boats you should have an unique identifier. Login to Signal K and go to _Server_ &gt; _Vessel_ _data_ and change at least your boat name and MMSI.

Here you can also provide data about your boat that could be useful for some Signal K tools.

![](../.gitbook/assets/sk_vessel_data.png)

