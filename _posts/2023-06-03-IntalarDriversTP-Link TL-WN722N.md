---
layout:     post
title:      TP-Link TL-WN722N v2/v3 [realtek rtl8188eus]
subtitle:   La mejor para Hackear WIFI
date:       2023-06-03
author:     Jose Carrillo
header-img: img/IntalarDriversTP-Link TL-WN722N/TPLINKLogo2.png
catalog: true
tags:
    # - Hacking
---

## TP-Link TL-WN722N v2/v3 [realtek rtl8188eus]

### TARJETA DE RED TP-LINK

Se crea una carpeta para almacenar lo descargado
```	objc
 sudo mkdir drivers 
```

Accedemos a la carpeta posteriormente descargada 
```	objc
 cd drivers
```

Descargamos los drivers para la tarjeta
```	objc
 sudo git clone https://github.com/JoseLuisCarrilloVargas/rtl8188eus.git 
```

Ejecutamos el script 
```	objc
 sudo python3 mirrorscript-v2.py
```

Descargamos actualizaciones
```	objc
 sudo apt update
```

Aplicamos actualizaciones
```	objc
 sudo apt update
```

Reiniciamos la maquina
```	objc
 sudo reboot
```

Instalamos las dependencias de la paquetería bc
```	objc
 sudo apt install bc
```

Instalamos componentes
```	objc
 sudo apt-get install build-essential
```

Instalamos componentes
```	objc
 sudo apt-get install build-essential
```

Instalamos librerías 
```	objc
 sudo apt-get install libelf-dev
```

Instalamos librerías
```	objc
 sudo apt-get install linux-headers-$(uname -r)
```

Accedemos como modo super usuario
```	objc
 sudo -i
```

Ponemos en la blaclist los componentes 
```	objc
 echo "blacklist r8188eu" > "/etc/modprobe.d/realtek.conf"
```

Reiniciamos la maquina
```	objc
 sudo reboot
```

Accedemos al contenido de la carpeta 
```	objc
 cd drivers/ rtl8188eus
```

Ejecutamos el siguiente comando
```	objc
 sudo sh -c "$(curl -fsSL https://gitlab.com/KanuX/rtl8188eus/-/raw/master/scripts/build.sh)"
```


### MODO MONITOR

Verificamos que la tarjeta de red este conectada 
```	objc
 lsusb 
```
Verificamos la interfaz de red 
```	objc
 iwconfig 
```

Matamos servicios de red 
```	objc
 sudo airmon-ng check kill
```

Inicializamos la tarjeta de red junto a la interfaz en donde se encuentra 
```	objc
 sudo airmon-ng start wlan0
```
Verificamos la interfaz de red 
```	objc
 iwconfig 
```
