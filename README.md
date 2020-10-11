# Controls Dockerized

This project is on my **Github**. The only thing that changes is that I have Dockerized it.

## Start 🚀 

### Requirements 📋

It is important to have installed Docker.oi & docker-compose.

### Install 🔧

_Clon the Proyect_

```
https://github.com/safernandez666/ControlsDockerized.git
```
_Configure the LDAP Server in login.php_

```
$host = '192.168.0.190';
$domain = 'ironbox.local';
$basedn = 'dc=ironbox,dc=local';
$group = 'Grupo_Controls';
```
_Inside the folder_

```
docker-compose up -d --build

```
Then to find out if the containers are running, you can run this command and you will see the Docker's

```
docker-compose ps


   Name                 Command               State                 Ports
---------------------------------------------------------------------------------------
mysql        docker-entrypoint.sh --def ...   Up      0.0.0.0:3306->3306/tcp, 33060/tcp
phpmyadmin   /docker-entrypoint.sh apac ...   Up      0.0.0.0:8080->80/tcp
webserver    apache2ctl -D FOREGROUND         Up      0.0.0.0:80->80/tcp

```

Now you can enjoy the Application on http://localhost.

If you want to set emails, you can configure /envios/enviar.py and croned in the Dockerfile
