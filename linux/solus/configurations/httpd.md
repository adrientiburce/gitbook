# Fichier httpd.conf

{% code title="httpd.conf" %}
```bash
<IfModule dir_module>
    Alias /projet /home/adrient/Documents/info/0php_project
    Alias /origenial /home/adrient/Documents/info/origenial.fr
    Alias /js /home/adrient/Documents/info/0js_web
    Alias /info /home/adrient/Documents/info
    Alias /wp /home/adrient/Documents/info/Demowordplate/public
    Alias /php /var/www/phpMyAdmin 
</IfModule>


#nom de domaine
 ServerName localhost:80

#on accepte aussi le www
# ServerAlias www.localhost  -> stop le serveur sur Solus /* NE PAS LE METTRE */


#Définition de la racine des sources php
DocumentRoot "/var/www"

<Directory "/var/www">
    Require all granted
</Directory>


<Directory "/home/adrient/Documents/info">
    Options Indexes Multiviews
    Require all granted
</Directory>

<Directory "/home/adrient/Documents/info/Demowordplate">

    Require all granted
</Directory>
```
{% endcode %}

