doune@doune-virtual-machine:~/TP-Docker$ nano docker-compose.yml
doune@doune-virtual-machine:~/TP-Docker$ nano docker-compose.yml
doune@doune-virtual-machine:~/TP-Docker$ sudo docker rm -f mysql57 phpmyadmin
[sudo] password for doune: 
mysql57
phpmyadmin
doune@doune-virtual-machine:~/TP-Docker$ sudo docker-compose up -d
Creating network "tp-docker_default" with the default driver
Creating volume "tp-docker_mysql_data" with default driver
Creating mysql57 ... done
Creating phpmyadmin ... done
doune@doune-virtual-machine:~/TP-Docker$ sudo docker ps
CONTAINER ID   IMAGE        COMMAND                  CREATED          STATUS          PORTS                                                    NAMES
f7aed4a501d2   phpmyadmin   "/docker-entrypoint.…"   10 seconds ago   Up 9 seconds    0.0.0.0:8081->80/tcp, [::]:8081->80/tcp                  phpmyadmin
16400cfab16e   mysql:5.7    "docker-entrypoint.s…"   10 seconds ago   Up 10 seconds   0.0.0.0:3306->3306/tcp, [::]:3306->3306/tcp, 33060/tcp   mysql57
51316fd2772e   nginx        "/docker-entrypoint.…"   43 minutes ago   Up 43 minutes   0.0.0.0:8080->80/tcp, [::]:8080->80/tcp                  mynginx
doune@doune-virtual-machine:~/TP-Docker$ ls
docker-compose.yml  etape2-commandes-base.md    etape6-mysql-phpmyadmin.md          etape8-reseau-compose.md  index.html
Dockerfile          etape5-dockerfile-build.md  etape7-compose-mysql-phpmyadmin.md  images                    README.md
doune@doune-virtual-machine:~/TP-Docker$ 

Capture pour ok de etape 8

a. À quoi sert le fichier docker-compose par rapport aux commandes docker run ? Pourquoi c’est pratique ?
Le fichier docker-compose.yml sert à rassembler toutes les infos sur tes conteneurs (images, ports, réseaux, variables, etc.) dans un seul fichier.
Au lieu d’écrire plusieurs commandes docker run une par une, tu peux tout lancer d’un coup avec une seule commande docker-compose up.

En plus, docker-compose s’occupe de démarrer les conteneurs dans le bon ordre. Par exemple, il attend que la base MySQL soit prête avant de lancer phpMyAdmin.

Ce fichier est super facile à partager, donc n’importe qui peut lancer le même environnement sans se prendre la tête.

Pour arrêter ou redémarrer tout, une seule commande suffit aussi (docker-compose down ou docker-compose restart).

Enfin, c’est très simple d’ajouter ou modifier des services sans taper plein de commandes compliquées.

b. Comment configurer facilement MySQL (utilisateur, base, mot de passe) quand on lance le conteneur ?
Tu peux passer des variables d’environnement directement dans ton fichier docker-compose.yml ou dans la commande docker run. Par exemple :

MYSQL_ROOT_PASSWORD : pour définir le mot de passe de l’utilisateur root

MYSQL_DATABASE : pour créer automatiquement une base de données à l’init

MYSQL_USER et MYSQL_PASSWORD : pour créer un utilisateur avec son mot de passe

L’image officielle MySQL utilise ces variables pour préparer la base dès le premier démarrage, donc pas besoin de faire ça à la main après.
