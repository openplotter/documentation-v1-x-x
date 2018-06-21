# Mode sans écran

## Premier démarrage

Après avoir créé la carte SD OpenPlotter sous NOOBS, l'insérer dans le Raspberry Pi, connecter l'alimentation et attendre l'apparition d'un nouveau réseau Wifi _openplotter_ dans la liste des points d'accès valides. Le process peut demander jusqu'à une demie heure pour se dérouler.

SSID: openplotter  
Mot de passe: 12345678

## Connexion

* Installer RealVNC Viewer sur votre portable, ordinateur, tablette ou smartphone
* Lancer VNC Viewer et sélectionner _Fichier -&gt; Nouvelle connexion_
* Renseigner l'adresse d'OpenPlotter et cliquer _OK._ Si OpenPlotter fonctionne en tant que point d'accès Wifi, son adresse est **10.10.10.1**_._ S'il est configuré comme client d'un autre point d'accès, vous devez trouver quelle adresse a été donnée à OpenPlotter au moment de sa connexion.

![](../.gitbook/assets/vnc_client1.png)

* Taper le _Nom utilisateur_: pi
* Taper le _Mot de passe_: raspberry
* Cliquer _OK_  et vous y êtes!

![](../.gitbook/assets/vnc_client2.png)

## Changer identité et mot de passe

{% hint style="danger" %}
Changer l'utilisateur du point d'accès et son mot de passe  par défaut au plus tôt. Sinon, n'importe qui pourra se connecter à votre système.
{% endhint %}

{% page-ref page="first-settings.md" %}



