# CAN-USB Stick

![](../.gitbook/assets/can-usb-stick.png)

## Projet

Le projet du Stick CAN-USB a été conduit pour analyser le flux de données d'un réseau N2K en envoyant et recevant des messages CAN. Le Stick est isolé électriquement pour éviter les dommages.

 Le Stick CAN-USB V2 est basé sur un micro-contrôleur **stm32** \(MCU\) connecté à un émetteur/récepteur CAN et un adaptateur USB-Série.

Le programme du micro-controlleur \(MCU\) a été revu pour travailler de concert avec le [projet CANBOAT](https://github.com/canboat/canboat), lui-même utilisé par le [projet Signal K](http://signalk.org/). Ces deux paquetages sont utilisés par le projet OpenPlotter.

 Le Stick CAN-USB fonctionne également avec le [projet OpenSkipper](http://openskipper.org/).

N'ont pas été testés:

* [MacENC](http://macenc.com/)
* [PolarView NS](http://www.polarnavy.com/)

Le Stick CAN-USB utilise les mêmes commandes que celles de l'interface Actisense-série de CANBOAT. Envoyer et recevoir des données depuis un réseau N2K peut être fait directement sous OpenPlotter.

Les nouveaux PGNs ne sont pas bloqués, puisqu'ils fonctionnent avec CANBOAT sur d'autres appareils. La vitesse de transmission peut être réglée plus haute que la vitesse du bus CAN. D'autre appareils, compatibles CANBOAT, ont une vitesse de transfert plus basse que le réseau N2K et peuvent devenir des goulots d'étranglement.

{% hint style="success" %}
Cet article est disponible dans la [boutique Web](http://shop.sailoog.com).
{% endhint %}

## Avertissement

Le Stick CAN-USB est un projet de recherche sur la communication de données entre le bus CAN bus et un réseau N2K sur les bateaux.

Le programme est toujours en phase de développement et n'a pas été entièrement testé. Des disfonctionnements du Stick CAN-USB ou de tout appareil connecté sont possible à tout momment. Intervenir sur votre réseau N2K peut causer de dommages au appareils connectés.

**Ne pas se reposer sur les données fournies par le Stick CAN-USB et ne pas l'utiliser comme support principal à la navigation. Aucune responsabilité ne sera acceptée pour tout dommages, blessures de personnes ou disfonctionnements causés par cet appareil.**

Le Stick CAN-USB n'est pas certifié NMEA®.

L'utilisation du lecteur NMEA Actisense® pour le Stick CAN-USB n'est pas autorisée.

![](../.gitbook/assets/n2k_b.jpg)

![Exemple d&apos;un petit r&#xE9;seau N2K](../.gitbook/assets/n2k_a.jpg)

 Les [réseaux N2K sont décrit dans Wikipedia](https://en.wikipedia.org/wiki/NMEA_2000). La colonne vertébrale \(backbone\) commence et finit par un bouchon de terminaison 120Ω \(deux résistances peuvent travailler en parallèle, donc la résistance est de 120Ω/2=60Ω\). S'il y a un connection rompue dans le backbone vous ne pourrez mesurer que 120Ω ou rien mais pas 60Ω. C'est un moyen très facile de vérifier le bus.

![Bouchon de terminaison m&#xE2;le 120&#x3A9;](../.gitbook/assets/resistor_conn.jpg)

Une branche alimentant les appareils ne peut faire plus de 6m. La longueur du backbone est limitée à 100m.

Le Stick CAN-USB est isolé électriquement, les appareils et votre ordinateur sont donc protégés même s'ils sont alimentés par d'autres sources que votre réseau N2K.

## Connexion

Pour connecter le Stick CAN-USB au réseau, vous avez besoin d'un connecteur en T libre sur votre backbone et d'une branche. La branche doit avoir d'un coté un connecteur mâle M12 5 broches et de l'autre 5 fils \(bien que seuls 2 soient utilisés\). Le connecteur HIRSCHMANN ELST 5012 PG7 a une terminaison visée.

![Connecteur en T](../.gitbook/assets/t-conn.jpg)

![Branche cot&#xE9; connecteur m&#xE2;le M12 5 broches.](../.gitbook/assets/m12_conn.jpg)

![Branche cot&#xE9; fils](../.gitbook/assets/micro_cable.jpg)

![](../.gitbook/assets/can_usb_connect.jpg)

* Dévisser les vis de l'embout vert du Stick.
* Connecter le fil bleu de la broche 5 de la branche \(broche du milieu\) au CANL sur l'embout vert du Stick.
* Connecter le fil blanc de la broche 4 de la branche au CANH sur l'embout vert du Stick.
* Ouvrir l'interrupteur principal, pour être sûr qu'il n'y a plus du courant sur le réseau.
* Connecter la branche au connecteur en T libre sur votre backbone.
* Utiliser un volmétre pour mesurer la résistance entre CANH et CANL \(sur les vis\). Elle doit être d'environ 60Ω.
* Connecter l'embout vert au Stick CAN-USB.
* Vérifier à nouveau les 60Ω entre CANH et CANL.
* Il reste trois fils sur la branche qui doivent être isolés.
* Alumer l'alimentation principale.
* Alumer les instruments.

Si vous avez un réseau Seatalk, télécharger cette documentation très utile: [Raymarine SeaTalk Network Connection Cross Reference](http://shop.sailoog.com/index.php?controller=attachment&id_attachment=1).

Pour configurer votre Stick CAN-USB sous Windows, utiliser OpenSkipper. Pour le configurer sous OpenPlotter se référer au chapitre:

{% page-ref page="./" %}

## LED

La LED du Stick CAN-USB est éteinte pendant 10" durant la séquence de démarrage puis:

* Allumée en permanence, si non connecté au réseau.
* Allumée pendant 1", si connecté au réseau.
* Eteinte, s'il n'y a pas de flux de données.
* Scintillante si un flux de données transite.

## Support

 Si vous avez besoin de support, ou pour toute suggestion, vous pouvez publier vos questions sur le [forum OpenMarine](http://forum.openmarine.net/forumdisplay.php?fid=11).

