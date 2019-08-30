---
description: Les premiers réglages à faire après avoir installé Linux Mint
---

# Configurer Linux Mint

## Problèmes de Wifi avec RTL8723BE

1. Préliminaires

* Vérifier votre carte wifi avec : `lspci | grep "Network"`
* Vérifier l'état de votre connexion : `iwlist scan | egrep -i 'ssid|quality'` 
* Mettre a Jout APT : voir ci-dessous 

2. Changer l'antenne utilisée :

* `echo "options rtl8723be fwlps=0 ant_sel=2" | sudo tee /etc/modprobe.d/rtl8723be.conf`
* Redémarrer le module : `sudo modprobe -r rtl8723be` puis `sudo modprobe rtl8723be`
* On peut aussi empêcher la mise en veille de la carte wifi : `echo "options rtl8723be fwlps=0" | sudo tee /etc/modprobe.d/rtl8723be.conf`

Source : [Topic Ubuntu](https://forum.ubuntu-fr.org/viewtopic.php?id=2019769)

## Mettre a Jour APT :

1. `sudo apt-get update && sudo apt-get upgrade -y`
2. La commande `sudo apt-get dist-upgrade` peut etre utile pour intelligemment metre a jour les dépendances !

