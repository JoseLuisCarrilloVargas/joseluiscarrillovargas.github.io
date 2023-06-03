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
TARJETA DE RED TP-LINK
sudo mkdir drivers -> Se crea una carpeta para almacenar lo descargado
cd drivers -> Accedemos a la carpeta posteriormente descargada 
sudo git clone https://github.com/JoseLuisCarrilloVargas/rtl8188eus.git -> Descargamos los drivers para la tarjeta
sudo python3 mirrorscript-v2.py -> Ejecutamos el script 
sudo apt update -> Descargamos actualizaciones
sudo apt upgrade -> Aplicamos actualizaciones
sudo reboot -> Reiniciamos la maquina
sudo apt install bc -> Instalamos las dependencias de la paquetería bc
sudo apt-get install build-essential -> Instalamos componentes
sudo apt-get install libelf-dev -> Instalamos librerías 
sudo apt-get install linux-headers-$(uname -r) -> Instalamos librerías
sudo -i -> Accedemos como modo super usuario
echo "blacklist r8188eu" > "/etc/modprobe.d/realtek.conf" -> Ponemos en la blaclist los componentes 
exit -> Salimos de la carpeta 
sudo reboot -> Reiniciamos 
cd drivers/ rtl8188eus -> Accedemos al contenido de la carpeta 
sudo sh -c "$(curl -fsSL https://gitlab.com/KanuX/rtl8188eus/-/raw/master/scripts/build.sh)" -> Ejecutamos el siguiente comando

MODO MONITOR
lsusb -> verificamos que la tarjeta de red este conectada 
iwconfig -> Verificamos la interfaz de red 
sudo airmon-ng check kill -> Matamos servicios de red 
sudo airmon-ng start wlan0 -> Inicializamos la tarjeta de red junto a la interfaz en donde se encuentra 
iwconfig -> Verificamos 
