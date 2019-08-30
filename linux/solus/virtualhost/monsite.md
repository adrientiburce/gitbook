## Example de fichier `monsite.conf`

```bash

<VirtualHost *:80>
        #nom de domaine
	ServerName monsite
        #logs d'erreur
	ErrorLog /var/www/monsite.dev/logs/error.log 
        #logs de connexion
	CustomLog /var/www/monsite.dev/logs/access.log common

        #Définition de la racine des sources php
	DocumentRoot "/var/www/monsite.dev/web"

	<Directory "/var/www/monsite.dev/web">
		Options Indexes MultiViews
   		Order allow,deny
    		Allow from all
    		# New directive needed in Apache 2.4.3: 
   		require all granted
	</Directory>
</VirtualHost>

```
