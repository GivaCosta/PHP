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



<h1>Instalando o MongoDB</h1>
Comandos Linux:
Baixando a chave de permissão
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv EA312927
Depois temos que atualizar o source.list. Execute o comando :
echo "deb http://repo.mongodb.org/apt/ubuntu "$(lsb_release -sc)"/mongodb-org/3.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.2.list
Depois atualize o linux:
sudo apt-get update
Finalizando a atualização do source.list, vamos instalar o MongoDB executando o comando:
sudo apt-get install mongodb-org
Para testar se o mongodb está rodando, execute:
service mongod status
Você pode iniciar ou parar o serviço com os comandos:
Iniciar o MongoDB:
sudo service mongod start
Parar o MongoDB
sudo service mongod stop
Para acessar a linha de comando do MongoDB que é o mongo shell use o comando em linux:
sudo mongo --port 27017
Sendo que a porta padrão do MongoDB é a 27017.
Windows:
Baixar a versão do mongoDB em:
https://www.mongodb.com/

Após finalizar a instalação, para executar o MongoDB temos o manual:
https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/#install-mdb-edition
Execute o comando CMD para abrir o interpretador de comandos (prompt);
Vá para o local: C:\ e execute o comando abaixo para criar a pasta do MongoDB
md "\data\db" "\data\log“
Para executar o MongoDB:
"C:\Program Files\MongoDB\Server\4.0\bin\mongod.exe" --dbpath="c:\data\db“
O mongoDB está rodando. Abra outro terminal com o comando CMD e execute o comando a seguir para acessar o mongo shell:
"C:\Program Files\MongoDB\Server\4.0\bin\mongo.exe"






