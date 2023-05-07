---
layout:     post
title:      Fern Wifi Cracker
subtitle:   Herramienta para auditorías de red
date:       2023-04-01
author:     Jose Carrillo
header-img: img/Fern-Wifi-Cracker/Fern-Wifi-Cracker.jpg
catalog: true
tags:
    # - Hacking
---

## Fern Wifi Cracker

Fern Wifi Cracker es una herramienta de seguridad informática que se utiliza para realizar pruebas de penetración en redes inalámbricas. Es una aplicación gratuita y de código abierto que permite a los profesionales de seguridad evaluar la seguridad de las redes Wi-Fi y detectar vulnerabilidades en su configuración.



## ¿Qué se necesita para utilizarla?

Es necesario tener un sistema operativo Linux instalado en el equipo desde el cual se ejecutará la herramienta. Además, se requiere una tarjeta de red inalámbrica compatible con modo monitor y modo inyección, que permita capturar el tráfico de la red y enviar paquetes falsificados. La tarjeta de red inalámbrica debe ser compatible con los controladores de la herramienta y debe estar configurada correctamente para que la herramienta funcione correctamente.

### Ejecución

Para poder hacer uso de esta herramienta lo primero que se realizo fue poner en modo monitor nuestra tarjeta de red. Un problema que surgió al hacer uso de esta herramienta fue que la tarjeta de red la detectaba como “wlan0mon” y no como “wlan0” como viene por defecto. 

Primero se debe deshabilitar la tarjeta de red

```	objc
 ip link set wlan0 down
```

Se asigna el nombre de la tarjeta de red 

```objc
 ip link set wlan0 name wlan0mon
```

Seleccionamos la tarjeta de red

![imagen](/img/Fern-Wifi-Cracker/TarjetaDeRed.png)

Luego de haber seleccionado la tarjeta de red, se seleccionó la opción de escanear las redes que se encuentran alrededor para luego observar las redes que fueron detectadas. 

![imagen](/img/Fern-Wifi-Cracker/SeleccionRed.png)


Se mostro un panel en donde nos mostrara datos sobre las redes, al igual que algunos parámetros identificadores de las redes. Como se puede ver en la figura la interfaz muestra las redes que tiene a su alrededor, que al momento de seleccionar alguna, muestra información sobre ella, también nos da la opción de seleccionar el diccionario que se utilizara, al igual que se seleccionar el dispositivo que se des autenticara. Una vez seleccionado el diccionario se selecciona la opción “Attack” la cual ayudara a que inicie el ataque. 
Al finalizar el ataque arrojó la contraseña que esta asignada a la red WIFI, todo el proceso lleva un determinado tiempo, por lo que depende de muchos fatores, como tipo de procesador de la computadora, línea en donde se encuentra la contraseña de la red, intensidad de la señal de la red y también si existen dispositivos conectados a ella, debido a que este tipo de ataque necesita realizar una des autenticación de algún dispositivo para obtener el Handshake y así poder validar con las contraseñas que se encuentren en el diccionario previamente insertado.


![imagen](/img/Fern-Wifi-Cracker/RedHack.jpeg)
