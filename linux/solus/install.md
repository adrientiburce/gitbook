---
description: Comment installer Solus en DualBoot
---

# Installation

## 1. Préliminaires

* Télécharger l'iso sur le [Site officiel](https://getsol.us/download/)
* Copier l'iso sur une clé USB : sur Linux à l'aide de :

```text
sudo dd if=Solus-3.9999-Budgie.iso of=/dev/sdb bs=1M;sudo sync;sudo eject /dev/sdb
```

* Redémarer votre ordinateur avec la clé USB dedans ! 

## 2. Installation

Suivez l'installation puis redémarrez votre ordinateur en enlevant la clé !

## 3. Accédez à Solus

### Par le BIOS :

* Si Solus est présent dans les options de démarrage de votre UEFI : changer l'ordre et redémarrez l'ordinateur

### En y accédant par la partition BIOS

* Etape 0 : 

  Accédez à Solus et retenez le chemin `EFI/..`

Une fois sur Solus il faut ajouter à la main la partition Solus dans le menu UEFI :

* Etape 1 : Installer `efibootmgr` : `sudo eopkg it efibootmgr`
* Etape 2 : Taper `sudo fdisk -l` et noter la partition EFI `dev/sda1` normalement !
* Etape 2 : Remplacer `dev/sda1` par votre partition _EFI_

  ```text
  efibootmgr --create --disk /dev/sda1 --loader /EFI/Solus/grubx64.efi --label "Solus"
  ```

  par exemple, voici ma configuration :

  ```text
  efibootmgr --create --disk /dev/sda1 --loader /EFI/systemd/systemd-bootx64.efi --label "Solus"
  ```

* Etape 3 :
  * Pour changer l'ordre d'amorcage taper : 

    ```bash
    sudo efibootmgr -o 0001,3001
    ```

    * Si cette étape ne fonctionne pas changer directement l'ordre d'amorcage depuis _UEFI_ 

## 4. Pour avoir le choix entre Windows & Solus :

* Etape 1 : 

  Taper dans la console : `sudo clr-boot-manager set-timeout 5`

* Etape 2 : 

  Entrer `sudo clr-boot-manager update`

### NB :

1\) Solus utilise maintenant exclusivement `clr-boot-manager`, les paquets `goofiboot` ou encore `gummiboot` sont désormais dépreciés ! comme précisé par la [Core Team](https://github.com/solus-cold-storage/goofiboot) 2\)

## 5. Configuration

### Installation de `cpu-powersave`:

* Afin d'optimiser les perfomances de la batterie on peut se mettre en `powersave` mode 
* Installer le paquet [solus-hardware-config](https://github.com/solus-project/solus-hardware-config)
* Puis : `sudo cpu-powersave start`

