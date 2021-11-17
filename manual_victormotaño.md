Victor Montaño Hernandez


# Manual de instalación de Cloud


1. vamos a http://www.nextcloud.com y vamos a hacer lo siguiente.
2. le damos a get nexcloud y le damos a servers
3. luego le damos a descargar.

# Instal·lar apache2, mysql i algunes llibreries al contenidor
1. abrimos la terminal y entramos a la carpeta de Clouds con cd y el nombre de la carpeta.
~~~
[vmontano@alumne-1-13 ~]$ cd clouds/
~~~
2. hacemos los siguientes comandos para el apache2
~~~
[vmontano@alumne-1-13 clouds]$ apt install
~~~
~~~
[vmontano@alumne-1-13 clouds]$ apt upgrade
~~~
~~~ http://www.owncloud.org
[vmontano@alumne-1-13 clouds]$ apt install -y mysql-server
~~~
~~~
[vmontano@alumne-1-13 clouds]$ apt install php libapache2-mod-php
~~~
~~~
apt install php-fpm php-common php-mbstring php-xmlrpc php-soap php-gd php-xml php-intl php-mysql php-cli php-ldap php-zip php-curl
~~~
# Configuració de MySQL
escribiremos los siguientes comandos para la condiguración
~~~
[vmontano@alumne-1-13 clouds]$ CREATE DATABASE bbdd;
~~~
~~~
[vmontano@alumne-1-13 ~]$ CREATE USER 'usuario'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
~~~
en este comando siguente hay que poner en vez de esta IP hay que poner la que tengamos nosotros.
~~~
CREATE USER 'usuario'@'192.168.22.100' IDENTIFIED WITH mysql_native_password BY 'password';
~~~
~~~
[vmontano@alumne-1-13 ~]$ GRANT ALL ON bbdd.* to 'usuario'@'localhost';
~~~
~~~
GRANT ALL ON bbdd.* to 'usuario'@'192.168.22.100';
~~~
haremos exit para salir de la terminal
~~~
[vmontano@alumne-1-13 ~]$ exit
~~~

*Aplicació de permisos a les nostres aplicacions web*

los siguientes comandos son:

~~~
cd /var/www/html
~~~
~~~
chmod -R 775 .
~~~
~~~
chown -R root:www-data
~~~
