# Primeras configuraciones

## Cambiar el idioma de su sistema operativo \(Raspbian\)

Tras el primer arranque su sistema estará probablemente en inglés. Siga las siguientes instrucciones para cambiar el idioma del sistema.

Vaya a _Menu &gt; Preferences_ y seleccione _Raspberry Pi Configuration_ 

![](../.gitbook/assets/cambiaridioma_es.png)

Se abrirá una ventana donde usted podrá personalizar su sistema. Vaya a la pestaña _Localisation_ y pinche el botón _Set Locale..._

![](../.gitbook/assets/cambiaridioma2_es.png)

En el cuadro de diálogo que se le abre, cambie las siguientes configuraciones: _Language_ \(idioma\), elija es \(Spanish\) en la lista desplegable; _Country_ \(país\) elija el que corresponda en lista desplegable. Pulse _Ok_.

![](../.gitbook/assets/cambiaridioma3_es.png)

Cuando vuelva al cuadro _Raspberry Pi Configuration_ pulse Ok. En ese momento le aparecerá un mensaje en el que se le dice que "_Para que los cambios surtan efecto debe reiniciar la Raspberry Pi. ¿Desea reiniciarla ahora?_". Pulse _Yes_ para reiniciar.

![](../.gitbook/assets/cambiaridioma4_es.png)

## Ajustes generales

Vaya a _Menú &gt; Preferencias_ y seleccione _Configuración de Raspberry Pi  \(en un primer arranque usted encontrará el sistema en inglés\)_

![](../.gitbook/assets/ajustesgenerales_es.png)

Se abrirá una ventana donde usted podrá personalizar su sistema. 

![](../.gitbook/assets/ajustesgenerales2_es.png)

{% hint style="danger" %}
Es una buena idea cambiar la contraseña para hacer OpenPlotter más seguro. Haga click en _Cambiar Clave_ \(contraseña por defecto: raspberry\).

Si no cambia la contraseña cualquiera podrá conectarse a OpenPlotter de forma remota. Por favor, hágalo AHORA.
{% endhint %}

Si necesita cambiar el idioma de su sistema o configuraciones locales, haga clic en la pestaña _Localización_ y después utilice los botones _Configurar Local_ \(idioma\), _Ajustar Zona horaria_, _Configurar teclado_ o _Set Wifi Country_ \(seleccione el país en el que usa el Wifi\).

![](../.gitbook/assets/ajustesgenerales3_es.png)

## Configuraciones de red

{% hint style="danger" %}
Si está habilitado el punto de acceso Wifi, por favor cambie la contraseña por defecto cuanto antes en la pestaña _Red_. En esa pestaña podrá deshabilitar el punto de acceso o establecer algún otro modo de red.
{% endhint %}

{% page-ref page="../network.md" %}

## Ajustes de Signal K

El servidor Signal K ofrece muchas herramientas útiles y debería visitar a menudo el panel de administración. Vaya a _Menu_ &gt; _OpenPlotter_ &gt; _Signal K._

#### Contraseña

La visualización de los datos está abierta, pero para establecer ajustes es necesaria la autentificación. Presione el botón _Login_, arriba a la derecha, en las tres rayas.

Nombre de usuario: openplotter  
Contraseña: openplotter

![](../.gitbook/assets/signalk_login_es.png)

{% hint style="danger" %}
Por favor, cambie la contraseña cuanto antes. Identifíquese y vaya a _Signal K_ &gt; _Security_ &gt; _Users_ &gt; _openplotter_
{% endhint %}

#### Datos del barco

Si va a compartir datos con otros barcos debería tener un identificador único. Inicie sesión en Signal K y vaya a _Server_ &gt; _Vessel_ _data_ y cambie al menos el nombre del barco y el MMSI.

Aquí también puede incluir datos sobre su barco que pueden ser útiles para algunas herramientas de Signal K.

![](../.gitbook/assets/sk_vessel_data.png)

