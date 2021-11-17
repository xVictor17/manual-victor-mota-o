# Introducció als contenidors lxc/lxd

victor manuel montaño 

Creació d'un contenidor
~~~
[vmontano@alumne-1-13 ~]$  lxc launch ubuntu:20.04 elmeucontenidor
~~~
Obrir un contenidor previament creat i que està parat
~~~
[vmontano@alumne-1-13 ~]$  lxc start elmeucontenidor
~~~
Llistar els contenidors del sistema
~~~
lxc list

 +-----------------+---------+----------------------+-----------------------------------------------+-----------+-----------+
 |     NAME        |  STATE  |         IPV4         |                     IPV6                      |   TYPE    | SNAPSHOTS |
 +-----------------+---------+----------------------+-----------------------------------------------+-----------+-----------+
 | micontenedor | RUNNING | 10.160.100.194 (eth0) | fd42:5550:ddc5:fbe2:216:3eff:fe81:713d (eth0) | CONTAINER | 0         |
 +-----------------+---------+----------------------+-----------------------------------------------+-----------+-----------
 ~~~

 Executa un contenidor
~~~
[vmontano@alumne-1-13 ~]$ lxc exec elmeucontenidor -- /bin/bash
~~~
Atura un contenidor
~~~
[vmontano@alumne-1-13 ~]$ lxc stop elmeucontenidor
~~~
Aplicar els permisos corresponents
~~~
chmod -R 775 .
chown -R root:www-data .
~~~
con esto ya habriamos acabado la creación de los contenedores.
