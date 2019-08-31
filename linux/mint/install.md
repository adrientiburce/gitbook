---
description: Les premiers réglages à faire après avoir installé Linux Mint
---

# Configuration

## Mettre a Jour APT :

{% hint style="info" %}
**APT** est la bibliothèque des paquet des forks d'Ubuntu, de Linux Mint 
{% endhint %}

#### 1. Mise à jour

```bash
sudo apt-get update && sudo apt-get upgrade -y
```

#### 2. Régler les conflits 

Pour mettre à jour intelligemment les dépendances :

```bash
sudo apt-get dist-upgrade
```

## Problèmes de Wifi avec RTL8723BE

{% hint style="warning" %}
Ces problèmes ont été rencontrés sur un **HP** 
{% endhint %}

#### 1. **Préliminaires**

* Vérifier votre carte wifi avec : `lspci | grep "Network"`
* Vérifier l'état de votre connexion : `iwlist scan | egrep -i 'ssid|quality'` 
* Mettre a Jour [APT](https://developer.webrush.fr/linux/mint/install#mettre-a-jour-apt)

#### 2. Configurer

* Changer l'antenne utilisée :

```bash
echo "options rtl8723be fwlps=0 ant_sel=2" | 
sudo tee /etc/modprobe.d/rtl8723be.conf
```

* Redémarrer le module : 

`sudo modprobe -r rtl8723be` puis `sudo modprobe rtl8723be`

* On peut aussi empêcher la mise en veille de la carte wifi : 

```bash
echo "options rtl8723be fwlps=0" | sudo tee
/etc/modprobe.d/rtl8723be.conf
```

Source : [Topic Ubuntu](https://forum.ubuntu-fr.org/viewtopic.php?id=2019769)



