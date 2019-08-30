---
description: Divers Alias utiles sur Solus
---

# Bashrc

```bash
source /usr/share/defaults/etc/profile

alias bureau="cd /home/adrient/Bureau";

alias phpr="systemctl restart php-fpm";
alias phps="systemctl status php-fpm";
alias httpdr="systemctl restart httpd";
alias httpds="systemctl status httpd";
alias run="php -S localhost:8080";

alias cherche="eopkg sr";
alias gg="gedit ~/.bashrc";
alias ll="ls -lhcp";
alias lla="ls -lahcp";
alias info="cd ~/Documents/info";
alias kk="cd ~/gitkraken/ && ./gitkraken";
alias ssho="ssh adrien@origenial.fr";
alias phps="php bin/console server:start";
alias phprun="php -S localhost:8000 -t public/";
```

