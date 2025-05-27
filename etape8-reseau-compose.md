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

