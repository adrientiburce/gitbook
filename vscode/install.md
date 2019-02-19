# Installation de VSCODE

## Installation 

* Etape 1: 
Sur le [site officiel](https://code.visualstudio.com/download) choisissez la version correspondant à votre OS et télécharger la 

* Etape 2
Décompressez l'archive et lancer l'application, dans le termianal :  `cd VSCODE` puis `./code `


## Etapes nécessaires 
* Désinstaller le raccourci **Ctrl+q** : `Settings-> Keymap` puis taper `action.workbench.quit` et enelever le raccourci

## Paquets Utiles :

#### Pour le Dev Wev ( PHP & JS)
- Activer *Tab* pour Emmet : le paquet est déjà installé par défaut. 
Il suffit donc d'ajouter à votre fichier _settings_ : 
 ```
 "emmet.triggerExpansionOnTab": true
 ```

- Intsaller **PHP Namespace Resolver** pour ajouter les namespaces 
Activer le raccourci `Ctrl+I` dans votre fichier `keybindings.json`

- **PHP Getter & Setter** : génère les getters et setters d'une classe 

### Visual Studio Code Settings Sync 
Cela permet de conserver les extensions installées ou les paramètres modifiés sur une autre machine. 

