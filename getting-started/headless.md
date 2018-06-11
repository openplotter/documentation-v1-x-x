# Modo sin monitor

## Primer arranque

Tras crear la SD con el instalador NOOBS de OpenPlotter, insértela en su Raspberry Pi, conéctela a la alimentación y espere hasta que una nueva red WiFi llamada _openplotter_ aparezca en la lista de los puntos de acceso accesibles. Puerde tardar hasta media hora en completar el proceso de instalación.

Nombre de red \(SSID\): openplotter  
Contraseña: 12345678

## Conectar con OpenPlotter

* Instale [RealVNC Viewer](https://www.realvnc.com/en/connect/download/viewer/) en su portátil, ordenador de sobremesa, tableta o smartphone
* Abra VNC Viewer y seleccione _File -&gt; New connection_
* Introduzca la dirección de OpenPlotter y clique en _OK._ Si OpenPlotter está funcinoando como punto de acceso, la dirección es **10.10.10.1**_._ Si está funcionando como cliente de otro punto de acceso, tendrá que averiguar la dirección del punto de acceso que está usando OpenPlotter.

![](../.gitbook/assets/vnc_client1.png)

* Introduzca el nombre de usuario \(_Username\)_: pi
* Introduzca la contraseña \(_Password\)_: raspberry
* Seleccione Recordar contraseña \(_Remember password\)_, haga clic en _OK_  y ¡usted estará dentro!

![](../.gitbook/assets/vnc_client2.png)

## Cambie las contraseñas

{% hint style="danger" %}
Por favor, cambie cuanto antes la contraseña por defecto del punto de acceso Wifi \(en el menú de OpenPlotter\)  y la contraseña por defecto del usuario _pi_ . Si no lo hace, cualquiera podría conectarse a su sistema. Vea _Primeras configuraciones._
{% endhint %}

{% page-ref page="first-settings.md" %}



