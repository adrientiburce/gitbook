---
description: Comment installer oh-my-zsh pour avoir un joli terminal
---

# Oh-My-Zsh

## Installation

#### 1. Installer Zsh

```bash
sudo apt install zsh
```

#### 2. Installer Oh-My-Zsh

[Oh-My-Zsh](https://ohmyz.sh/) permet de personnaliser plus facilement Zsh pour installer des thèmes par exemple 

```bash
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```



## Personnalisation 

#### 1. T**hème**

1. Changer la ligne 11 du fichier `~/.zshrc`
2. Chosir un thème disponible [ici](https://github.com/robbyrussell/oh-my-zsh/wiki/Themes)

#### 2. Git

Si l'on veut ne pas avoir de sortie lorsque l'on tape `git branch` ou `git log` :

```bash
git config --global core.pager ''
```

#### 3. Auto-complétion

* Ajouter la ligne suivante à votre `.zshrc` \( ou ajoute une option avec la commande `setopt`\)

```bash
setopt correct
```

Désormais pour accéder à `Document/info` ou peut simplement taper : `cd ~/D/i` 

## Zsh par défaut

Pour que zsh devienne votre terminal par défaut \(et remplacer bash\) 

```bash
chsh -s $(which zsh)
```

