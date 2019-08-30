# Commandes bash utiles : 

Quelques commandes utiles sur Linux

## Rechercher un fichier : 
 
- `find /home -name  <fichier>`
- `locate <fichier>`

## Modifier un fichier : 
- Ajouter une ligne : `echo "1 ligne de plus" >> texte.txt`
- Suppirmer des lignes (ici supprime slmt la sortie)
  - `sed '3d' mon_fichier.txt`
  - `sed '$d' mon_fichier.txt`
  
 **Ajouter l'option** `-i` pour modifier effectivement le fichier !
 
 ## Filtrer la sortie 
 - Commande `tail` : affiche que les liges de la fin : 
 
- Exemple : `tail -3 .bashrc` : affiche les 3 dernières lignes 
