doune@doune-virtual-machine:~/TP-Docker$ sudo docker pull nginx
[sudo] password for doune: 
Using default tag: latest
latest: Pulling from library/nginx
Digest: sha256:fb39280b7b9eba5727c884a3c7810002e69e8f961cc373b89c92f14961d903a0
Status: Image is up to date for nginx:latest
docker.io/library/nginx:latest
doune@doune-virtual-machine:~/TP-Docker$ nano index.html
doune@doune-virtual-machine:~/TP-Docker$ docker run -d -p 8080:80 -v $(pwd)/index.html:/usr/share/nginx/html/index.html nginx
docker: permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Head "http://%2Fvar%2Frun%2Fdocker.sock/_ping": dial unix /var/run/docker.sock: connect: permission denied

Run 'docker run --help' for more information
doune@doune-virtual-machine:~/TP-Docker$ sudo docker run -d -p 8080:80 -v $(pwd)/index.html:/usr/share/nginx/html/index.html nginx
506d13af4b13ae0c318368da25e5b7cac0c6fef99161e18dec13d1c955fb66ba

![Capture d'écran résultat docker](images from PageBienVenueServerpng)


doune@doune-virtual-machine:~/TP-Docker$ sudo docker rm -f great_zhukovsky
great_zhukovsky
doune@doune-virtual-machine:~/TP-Docker$ sudo docker run -d --name mynginx -p 8080:80 nginx
51316fd2772e4d5ceafc61cc09b4f283a65c60d7389e68c913a539b680e40af1
doune@doune-virtual-machine:~/TP-Docker$ sudo docker cp index.html mynginx:/usr/share/nginx/html/index.html
Successfully copied 3.07kB to mynginx:/usr/share/nginx/html/index.html
doune@doune-virtual-machine:~/TP-Docker$ 

[Capture d'écran résultat docker](images from resultat_docker-cp.png>
