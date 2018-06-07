# Empezando

Antes que nada reúna por lo menos los elementos requeridos de hardware:

{% page-ref page="../what-do-you-need.md" %}

Después, ejecute el software en su Raspberry. **OpenPlotter** es una versión modificada de [Raspbian](https://www.raspbian.org/), el sistema operativo oficial para la Raspberry Pi. Tiene todo lo que pueda necesitar. OpenPlotter es software de código abierto y libre.

## Instalando OpenPlotter

Raspberry Pi, y la mayoría de sistemas embebidos, utilizan una tarjeta micro-SD como disco duro. Casi todas las tarjetas compatibles micro-SD funcionarán en su Raspberry.

{% hint style="warning" %}
Se requiere un mínimo de 8GB pero se recomiendan 16GB.
{% endhint %}

Para empezar, es siempre una buena idea asegurarse de que ha formateado su tarjeta micro-SD. Asegúrese de que su ordenador tiene un lector de tarjetas SD integrado o utilice, en otro caso, un lector USB de tarjetas micro-SD.

* Visite la [Web de la Asociación SD](http://www.sdcard.org) y descargue el programa [SD Formatter](https://www.sdcard.org/downloads/formatter_4/index.html) para Windows o Mac.
* Siga las instrucciones para instalar el programa.
* Inserte su tarjeta micro-SD en lector de tarjetas SD de su ordenador o portátil y tome nota de la letra de unidad asignada a aquella, por ejemplo `F:/`
* En SD Formatter, selecciones la letra de unidad de su tarjeta micro-SD y formatéela.

![SDFormatter V4.0](../.gitbook/assets/sd-formatter.jpg)

{% hint style="warning" %}
Si su tarjeta micro-SD tiene 64GB o más, será automáticamente formateada como exFAT, que no es compatible con OpenPlotter. Siga [estas instrucciones](https://www.raspberrypi.org/documentation/installation/sdxc_formatting.md) para formatear su tarjeta micro-SD como FAT32 para que pueda usar OpenPlotter.
{% endhint %}

* [Bájese la última versión del instalador NOOBS de **OpenPlotter**](http://www.sailoog.com/blog-categories/openplotter-rpi)**.** Es un archivo comprimido de cerca de 1GB, por lo que puede llevar un tiempo. 
* Descomprima el archivo **openplotter\_vx.x.x\_noobs.zip**
* Seleccione todos los archivos y carpetas presentes dentro de la carpeta extraída NOOBS y arrástrelos adentro de la tarjeta micro-SD.
* Así, todos los archivos necesarios se transferirán a la tarjeta micro-SD.
* Cuando haya terminado, extraiga en modo seguro la tarjeta micro-SD e insértela en su  Raspberry Pi.

![](../.gitbook/assets/boot1.png)

## Primer arranque

Conecte la alimentación a su Raspberry Pi.

El instalador NOOBS de OpenPlotter hará una instalación silenciosa; esto es, usted no tendrá que hacer nada. Este proceso tardará unos cuantos minutos, para formatear e instalar el sistema.

Una vez que el instalador NOOBS de Once the OpenPlotter haya terminado de instalar el sistema, OpenPlotter se iniciará automáticamente cada vez que conecte la Raspberry Pi.

![](../.gitbook/assets/empezando-openplotter-v1.x.x.png)

Se autodetectará la resolución nativa del monitor de 800x480. ¡La configuración correcta funcionará en el próximo arranque! Si tiene un monitor, reinície el sistema de nuevo.

OpenPlotter está configurado por defecto como un punto de acceso WiFi. Puede conectarse a él usando esta contraseña:

Nombre de la red \(SSID\): openplotter  
Contraseña: 12345678

{% hint style="danger" %}
Debe cambiar la contraseña lo antes que pueda. Debiera cambiar también otras configuraciones importantes; por favor, vaya a la página _Configuraciones iniciales_ para ver cómo hacerlo. 
{% endhint %}

{% page-ref page="first-settings.md" %}

También puede ejecutar OpenPlotter en modo sin monitor, usando cualquier portátil, ordenador de sobemesa, tableta o smartphone como cliente de escritorio remoto.

{% page-ref page="headless.md" %}

## Actualizando

Desde OpenPlotter  v1.0.0 puede actualizar su instalación sin necesidad de grabar de nuevo la tarjeta micro-SD.

Asegúrese de estar conectado a Internet y vaya a _Actualizaciones_ en el menú principal de OpenPlotter y después a \[_Update OpenPlotter\]_. OpenPlotter comprobará si necesita una actualización mayor o menor  y hará todo el trabajo por usted.

También puede actualizar OpenCPN y sus plugins a la última versión estable liberada y restaurar las configuraciones de escritorio si ha habido cambios tras una actualización.

![](../.gitbook/assets/update.png)

### Numeración de las versiones {#version-numbering}

OpenPlotter releases have three numbers: **a**.**b**.**c** \(v0.10.0, v1.0.0...\) and a word \(**alpha**, **beta** and **stable**\).

When **c** increases, there is a minor change and means that only the OpenPlotter code has changed. When **b** increases, there is a major change and means that other packages or dependencies need to be added or updated too. When **a** increases, there is an upgrade and means that Raspbian needs to be upgraded. In this case a new OpenPlotter image will be released and you have to burn a new SD card.

**Alpha** means that some parts still need development. **Beta** means that all parts have been developed and there are not fatal errors but it needs to be tested by users in different scenarios. Text will be translated from English into other languages on this stage. **Stable** means that OpenPlotter code and dependencies have already been tested and there are not errors.

You can know what version you are running selecting the option _About_ in _Help_ menu.

![](../.gitbook/assets/about.png)

## Backup

## Recovery system

If our system gets damaged or unstable, we can recover it from the NOOBS installer that resides on your SD and install OpenPlotter again. Press the Shift key when you see this symbol at startup:

![](../.gitbook/assets/recovery.png)

{% hint style="danger" %}
**You will lose all data, manually installed programs and settings after recovering.**
{% endhint %}

