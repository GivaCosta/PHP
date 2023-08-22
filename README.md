# PHP
#Links utilizados na aula:
https://www.mongodb.com/
http://db-engines.com/en
http://php.net/downloads.php

#Instalando o PHP

#Comandos Linux:
#Debian
apt update
apt upgrade
#Instale o PHP e o módulo para o Apache:
#apt install php(Versao do Apache) libapache2-mod-php(Versão do Apache)
apt install apache2 libapache2-mod-php8.2
#Ir no diretorio a seguir e criar um arquivo (info.php) para testar

/var/www/html/
<?php phpinfo(); ?>
http://your_server_ip/info.php

/var/www/html/public_html/
<?php phpinfo(); ?>
http://your_server_ip/info.php

#E reinicie o servidor Apache2 com o comando:
systemctl restart apache2

#RedHat
yum update && upgrade -y
sudo yum install php
php -v
/etc/httpd/conf/httpd.conf ou /etc/apache2/apache2.conf #para alterar a porta
sudo systemctl restart httpd

Instalar o servidor Apache:

sudo apt-get update 
sudo apt-get install apache2







