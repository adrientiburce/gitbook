---
description: Comment installer oh-my-zsh pour avoir un joli terminal
---

# Oh-My-Zsh

1. Installation de _Zsh_

```bash
sudo apt install zsh
```

1. Installation de **Oh-my-zsh**

```bash
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

1. On peut changer de **thème** :
2. Changer la ligne 11 du fichier `~/.zshrc`
3. Chosir un thème disponible [ici](https://github.com/robbyrussell/oh-my-zsh/wiki/Themes)
4. Astuces pour git avec zsh

   Si l'on veut ne pas avoir de sortie lorsque l'on tape `git branch` ou `git log` :

```bash
git config --global core.pager ''
```

1. Avoir zsh par **défaut** :

```bash
chsh -s $(which zsh)
```

1. Une auto-complétion sympa : Ajouter la ligne suivante à votre `.zshrc` \( ou ajoute une option avec la commande `setopt`\)

```bash
setopt correct
```

* désormains pour accéder à `Document/info` ou peut simplement taper : `cd ~/D/i` 

