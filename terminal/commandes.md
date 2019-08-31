---
description: Petit mémo sur des commandes bash bien utiles
---

# Commandes bash

## Rechercher un fichier

* `find /home -name  <fichier>`
* `locate <fichier>`

## Modifier un fichier

* Ajouter une ligne : 

```bash
echo "1 ligne de plus" >> texte.txt
```

* Supprimer des lignes \(ici supprime seulement la sortie\)

  * `sed '3d' mon_fichier.txt`
  * `sed '$d' mon_fichier.txt`

  **Ajouter l'option** `-i` pour modifier effectivement le fichier !

  **Filtrer la sortie**

  * Commande `tail` : affiche que les liges de la fin : 

* Exemple : `tail -3 .bashrc` : affiche les 3 dernières lignes

