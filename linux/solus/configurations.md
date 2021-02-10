---
description: Découvre ici comment installer un serveur local sur Solus
---

# Serveur LAMP

{% hint style="info" %}
Solus ne possède pas de paquet Lamp sur **eopkg** il faut donc installer les paquets séparément puis configurer l'ensemble
{% endhint %}

* php.conf

```bash
LoadModule proxy_module lib64/httpd/mod_proxy.so
LoadModule proxy_fcgi_module lib64/httpd/mod_proxy_fcgi.so
<FilesMatch .php$>
SetHandler "proxy:fcgi://127.0.0.1:9000"
</FilesMatch>

<IfModule dir_module>
DirectoryIndex index.php index.html
</IfModule>
```

* **httpd.conf**

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



