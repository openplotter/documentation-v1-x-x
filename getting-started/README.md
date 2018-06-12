# Par où commencer?

Tout d'abord, il vaus faut assembler les éléments prérequis:

{% page-ref page="../what-do-you-need.md" %}

Puis, éxécuter le logiciel sur votre Raspberry. **OpenPlotter** est une version modifiée de Ra[spbian](https://www.raspbian.org/), l'OS officiel pour Raspberry Pi. Tout ce dont vous avez besoin est inclus. OpenPlotter est open-source et gratuit.

## Installer OpenPlotter

Raspberry Pi, ainsi que la plupart des systèmes inclus, utilise une carte SD en tant que disque dur. Presque toutes les cartes micro-SD-compatible fonctionneront avec votre Raspberry.

{% hint style="warning" %}
8GB minimum sont requis, mais 16GB sont recommandés.
{% endhint %}

Un bon commencement est de vérifier que la carte SD est formattée. Assurez-vous que votre ordinateur dispose d'un lecteur de Cartes SD intégré, à défault, vous pourrez en utiliser un USB.

* Télécharger [SD Formatter](https://www.sdcard.org/downloads/formatter_4/index.html) \(pour Windows ou Mac\) depuis le [site de l'Association SD Card](http://www.sdcard.org//).
* Suivre les instructions pour installer le logiciel.
* Insérer votre carte SD dans le lecteur de carte de l'ordinateur ou du portable  et noter le disque alloué`ici F:/`
* Dans SD Formatter, sélectionner le disque correspondant à votre carte SD et formater.

![SDFormatter V4.0](../.gitbook/assets/sd-formatter.jpg)

{% hint style="warning" %}
Si votre carte SD est de 64GB ou plus, elle sera automatiquement formatée en exFAT, ce qui n'est pas compatible avec OpenPlotter. Suivez ces [instructions](https://www.raspberrypi.org/documentation/installation/sdxc_formatting.md) pour forcer le formatage de votre carte SD en FAT32, afin de pouvoir utiliser.
{% endhint %}

* [Télécharger la dernière version d'](http://www.sailoog.com/blog-categories/openplotter-rpi)[**OpenPlotter**](http://www.sailoog.com/blog-categories/openplotter-rpi)[ sous NOOBS](http://www.sailoog.com/blog-categories/openplotter-rpi)**.** Il s'agit d'un fichier compressé ****de presque ****1GB, cela prendra donc un peu de temps. 
* Extraire les fichiers du dossier compressé **openplotter\_vx.x.x\_noobs.zip**
* Les copier tous sur le disque correspondant à la carte SD.
* Quand la copie est terminée, retirer avec sécurité la carte SD et l'insérer dans votre Raspberry Pi.

![](../.gitbook/assets/boot1.png)

## Premier démarrage

Mettre le Raspberry Pi sous tension.

NOOBS procède à une installation silencieuse d'OpenPlotter, ce qui veut dire que vous n'avez rien à faire. Cela va prendre quelques minutes pour formater les partitions et installer le système.

Une fois fait, OpenPlotter démarrera directement, chaque fois que Raspberry Pi sera allumé.

![OpenPlotter startup window](../.gitbook/assets/startup.png)

La résolution native des écrans de 800x480 est automatiquement détectée. Le bon réglage pour que cela fonctionnement correctement sera opérationnel au prochain démarrage! Si vous avez un tel écran, re-démarrez.

OpenPlotter est configuré en tant que point d'accès WiFi par défaut. Le mot de passe pour s'y connecter est le suivant:

SSID: openplotter  
Mot de passe: 12345678

{% hint style="danger" %}
Vou devriez changer ce mot de passe dès que possible. Il y a d'autres paramétrages importants qui devraient être changés, rendez-vous sur please go to _First settings_ page to know how.
{% endhint %}

{% page-ref page="first-settings.md" %}

You can also run OpenPlotter without monitor \(headless\) using any laptop, desktop computer, tablet or smart-phone as a remote desktop client.

{% page-ref page="headless.md" %}

## Mettre à jour

From OpenPlotter  v0.10.0, you can update your installation without need of burning a new SD card.

Be sure you are connected to Internet and go to _Updates_ in the OpenPlotter main menu and then to _Update OpenPlotter_. OpenPlotter will check if you need to do a minor or a major update and it will do all the work for you.

You can also update OpenCPN and plugins to the latest stable releases and restore the desktop settings if it has changed after an update.

![](../.gitbook/assets/update.png)

### Numérotation des versions {#version-numbering}

OpenPlotter releases have three numbers: **a**.**b**.**c** \(v0.10.0, v1.0.0...\) and a word \(**alpha**, **beta** and **stable**\).

When **c** increases, there is a minor change and means that only the OpenPlotter code has changed. When **b** increases, there is a major change and means that other packages or dependencies need to be added or updated too. When **a** increases, there is an upgrade and means that Raspbian needs to be upgraded. In this case a new OpenPlotter image will be released and you have to burn a new SD card.

**Alpha** means that some parts still need development. **Beta** means that all parts have been developed and there are not fatal errors but it needs to be tested by users in different scenarios. Text will be translated from English into other languages on this stage. **Stable** means that OpenPlotter code and dependencies have already been tested and there are not errors.

You can know what version you are running selecting the option _About_ in _Help_ menu.

![](../.gitbook/assets/about.png)

## Sauvegarde

## Système de restauration

If our system gets damaged or unstable, we can recover it from the NOOBS installer that resides on your SD and install OpenPlotter again. Press the Shift key when you see this symbol at startup:

![](../.gitbook/assets/recovery.png)

{% hint style="danger" %}
**You will lose all data, manually installed programs and settings after recovering.**
{% endhint %}

