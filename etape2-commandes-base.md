Étape 2 - Tests des commandes Docker
Commandes lancées :
doune@doune-virtual-machine:~/TP-Docker$ sudo docker run hello-world

Résultats :


Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/


oune@doune-virtual-machine:~/TP-Docker$ docker run -it ubuntu bash
docker: permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Head "http://%2Fvar%2Frun%2Fdocker.sock/_ping": dial unix /var/run/docker.sock: connect: permission denied

Run 'docker run --help' for more information
doune@doune-virtual-machine:~/TP-Docker$ sudo docker run -it ubuntu bash
root@b6174bcfbf4d:/# docker images
bash: docker: command not found
root@b6174bcfbf4d:/# ls
bin   dev  home  lib64  mnt  proc  run   srv  tmp  var
boot  etc  lib   media  opt  root  sbin  sys  usr
root@b6174bcfbf4d:/# cd home/
root@b6174bcfbf4d:/home# ls
ubuntu
root@b6174bcfbf4d:/home# ls
ubuntu
root@b6174bcfbf4d:/home# cd ubuntu/
root@b6174bcfbf4d:/home/ubuntu# ls
root@b6174bcfbf4d:/home/ubuntu# docker images
bash: docker: command not found
root@b6174bcfbf4d:/home/ubuntu# 
exit
doune@doune-virtual-machine:~/TP-Docker$ docker images
permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Head "http://%2Fvar%2Frun%2Fdocker.sock/_ping": dial unix /var/run/docker.sock: connect: permission denied
doune@doune-virtual-machine:~/TP-Docker$ sudo docker images
REPOSITORY    TAG       IMAGE ID       CREATED        SIZE
ubuntu        latest    a0e45e2ce6e6   4 weeks ago    78.1MB
hello-world   latest    74cc54e27dc4   4 months ago   10.1kB
doune@doune-virtual-machine:~/TP-Docker$ ls
etape1-installation.md          etape6-mysql-phpmyadmin.md
etape2-commandes-base.md        etape7-compose-mysql-phpmyadmin.md
etape3-serveur-nginx-volume.md  etape8-reseau-compose.md
etape4-serveur-nginx-cp.md      README.md
etape5-dockerfile-build.md
doune@doune-virtual-machine:~/TP-Docker$ nano etape2-commandes-base.md 
doune@doune-virtual-machine:~/TP-Docker$ git add etape2-commandes.md
git commit -m "Étape 2 : Tests des commandes Docker"
fatal: pathspec 'etape2-commandes.md' did not match any files
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   etape2-commandes-base.md

no changes added to commit (use "git add" and/or "git commit -a")
doune@doune-virtual-machine:~/TP-Docker$ ls
etape1-installation.md          etape6-mysql-phpmyadmin.md
etape2-commandes-base.md        etape7-compose-mysql-phpmyadmin.md
etape3-serveur-nginx-volume.md  etape8-reseau-compose.md
etape4-serveur-nginx-cp.md      README.md
etape5-dockerfile-build.md
doune@doune-virtual-machine:~/TP-Docker$ git add etape2-commandes-base.md 
doune@doune-virtual-machine:~/TP-Docker$ git commit -m "Étape 2 : Tests des commandes Docker" 
[master d314d94] Étape 2 : Tests des commandes Docker
 1 file changed, 26 insertions(+)
doune@doune-virtual-machine:~/TP-Docker$ git status
On branch master
nothing to commit, working tree clean
doune@doune-virtual-machine:~/TP-Docker$ LS
LS: command not found
doune@doune-virtual-machine:~/TP-Docker$ ls
etape1-installation.md          etape6-mysql-phpmyadmin.md
etape2-commandes-base.md        etape7-compose-mysql-phpmyadmin.md
etape3-serveur-nginx-volume.md  etape8-reseau-compose.md
etape4-serveur-nginx-cp.md      README.md
etape5-dockerfile-build.md
doune@doune-virtual-machine:~/TP-Docker$ nano etape2-commandes-base.md 
doune@doune-virtual-machine:~/TP-Docker$ git commit -m "Étape 2 : tests des commandes Docker"
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   etape2-commandes-base.md

no changes added to commit (use "git add" and/or "git commit -a")
doune@doune-virtual-machine:~/TP-Docker$ git remote add origin https://github.com/Hamdoune001/TP-Docker.git
doune@doune-virtual-machine:~/TP-Docker$ git push -u origin master
Username for 'https://github.com': Hamdoune001
Password for 'https://Hamdoune001@github.com': 
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/Hamdoune001/TP-Docker.git/'
doune@doune-virtual-machine:~/TP-Docker$ git push -u origin master
Username for 'https://github.com': Hamdoune001
Password for 'https://Hamdoune001@github.com': 
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/Hamdoune001/TP-Docker.git/'
doune@doune-virtual-machine:~/TP-Docker$ git push -u origin master
Username for 'https://github.com': Hamdoune001 
Password for 'https://Hamdoune001@github.com': 
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/Hamdoune001/TP-Docker.git/'
doune@doune-virtual-machine:~/TP-Docker$ git push -u origin master
Username for 'https://github.com': Hamdoune001
Password for 'https://Hamdoune001@github.com': 
remote: Permission to Hamdoune001/TP-Docker.git denied to Hamdoune001.
fatal: unable to access 'https://github.com/Hamdoune001/TP-Docker.git/': The requested URL returned error: 403
doune@doune-virtual-machine:~/TP-Docker$ git push -u origin master
Username for 'https://github.com': Hamdoune001                             
Password for 'https://Hamdoune001@github.com': 
remote: Permission to Hamdoune001/TP-Docker.git denied to Hamdoune001.
fatal: unable to access 'https://github.com/Hamdoune001/TP-Docker.git/': The requested URL returned error: 403
doune@doune-virtual-machine:~/TP-Docker$ git push -u origin master
Username for 'https://github.com': Hamdoune001
Password for 'https://Hamdoune001@github.com': 
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 2 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 1.13 KiB | 578.00 KiB/s, done.
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
remote: error: GH007: Your push would publish a private email address.
remote: You can make your email public or disable this protection by visiting:
remote: https://github.com/settings/emails
To https://github.com/Hamdoune001/TP-Docker.git
 ! [remote rejected] master -> master (push declined due to email privacy restrictions)
error: failed to push some refs to 'https://github.com/Hamdoune001/TP-Docker.git'
doune@doune-virtual-machine:~/TP-Docker$ git push -u origin main
error: src refspec main does not match any
error: failed to push some refs to 'https://github.com/Hamdoune001/TP-Docker.git'
doune@doune-virtual-machine:~/TP-Docker$ git push -u origin master
Username for 'https://github.com': Hamdoune001
Password for 'https://Hamdoune001@github.com': 
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 2 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 1.13 KiB | 1.13 MiB/s, done.
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
remote: error: GH007: Your push would publish a private email address.
remote: You can make your email public or disable this protection by visiting:
remote: https://github.com/settings/emails
To https://github.com/Hamdoune001/TP-Docker.git
 ! [remote rejected] master -> master (push declined due to email privacy restrictions)
error: failed to push some refs to 'https://github.com/Hamdoune001/TP-Docker.git'
doune@doune-virtual-machine:~/TP-Docker$ git push -u origin master
Username for 'https://github.com': 148764285+Hamdoune001@users.noreply.github.com 
Password for 'https://148764285%2BHamdoune001%40users.noreply.github.com%20@github.com': 
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/Hamdoune001/TP-Docker.git/'
doune@doune-virtual-machine:~/TP-Docker$ git config --global user.email "148764285+Hamdoune001@users.noreply.github.com" 
doune@doune-virtual-machine:~/TP-Docker$ git commit --amend --reset-author
[master 1c0aedc] Étape 2 : Tests des commandes Docker
 1 file changed, 26 insertions(+)
doune@doune-virtual-machine:~/TP-Docker$ git push -f origin master
Username for 'https://github.com': Hamdoune
Password for 'https://Hamdoune@github.com': 
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 2 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 1.14 KiB | 1.14 MiB/s, done.
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/Hamdoune001/TP-Docker.git
 * [new branch]      master -> master
doune@doune-virtual-machine:~/TP-Docker$ docker images
permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Head "http://%2Fvar%2Frun%2Fdocker.sock/_ping": dial unix /var/run/docker.sock: connect: permission denied
doune@doune-virtual-machine:~/TP-Docker$ sudo docker images
[sudo] password for doune: 
REPOSITORY    TAG       IMAGE ID       CREATED        SIZE
ubuntu        latest    a0e45e2ce6e6   4 weeks ago    78.1MB
hello-world   latest    74cc54e27dc4   4 months ago   10.1kB
doune@doune-virtual-machine:~/TP-Docker$ sudo docker ps -a
CONTAINER ID   IMAGE         COMMAND    CREATED          STATUS                        PORTS     NAMES
b6174bcfbf4d   ubuntu        "bash"     34 minutes ago   Exited (127) 33 minutes ago             modest_sammet
c05edf6cdf0d   hello-world   "/hello"   37 minutes ago   Exited (0) 37 minutes ago               agitated_rosalind
98d07b478418   ubuntu        "bash"     38 minutes ago   Exited (0) 37 minutes ago               gifted_pascal
0871621bf095   hello-world   "/hello"   54 minutes ago   Exited (0) 54 minutes ago               upbeat_cartwright
7c813bdfda69   hello-world   "/hello"   55 minutes ago   Exited (0) 55 minutes ago               beautiful_feynman
doune@doune-virtual-machine:~/TP-Docker$ docker run -p 80:80 nginx
docker: permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Head "http://%2Fvar%2Frun%2Fdocker.sock/_ping": dial unix /var/run/docker.sock: connect: permission denied

Run 'docker run --help' for more information
doune@doune-virtual-machine:~/TP-Docker$ sudo docker run -p 80:80 nginx
Unable to find image 'nginx:latest' locally
latest: Pulling from library/nginx
61320b01ae5e: Pull complete 
670a101d432b: Pull complete 
405bd2df85b6: Pull complete 
cc80efff8457: Pull complete 
2b9310b2ee4b: Pull complete 
6c4aa022e8e1: Pull complete 
abddc69cb49d: Pull complete 
Digest: sha256:fb39280b7b9eba5727c884a3c7810002e69e8f961cc373b89c92f14961d903a0
Status: Downloaded newer image for nginx:latest
/docker-entrypoint.sh: /docker-entrypoint.d/ is not empty, will attempt to perform configuration
/docker-entrypoint.sh: Looking for shell scripts in /docker-entrypoint.d/
/docker-entrypoint.sh: Launching /docker-entrypoint.d/10-listen-on-ipv6-by-default.sh
10-listen-on-ipv6-by-default.sh: info: Getting the checksum of /etc/nginx/conf.d/default.conf
10-listen-on-ipv6-by-default.sh: info: Enabled listen on IPv6 in /etc/nginx/conf.d/default.conf
/docker-entrypoint.sh: Sourcing /docker-entrypoint.d/15-local-resolvers.envsh
/docker-entrypoint.sh: Launching /docker-entrypoint.d/20-envsubst-on-templates.sh
/docker-entrypoint.sh: Launching /docker-entrypoint.d/30-tune-worker-processes.sh
/docker-entrypoint.sh: Configuration complete; ready for start up
2025/05/27 01:02:19 [notice] 1#1: using the "epoll" event method
2025/05/27 01:02:19 [notice] 1#1: nginx/1.27.5
2025/05/27 01:02:19 [notice] 1#1: built by gcc 12.2.0 (Debian 12.2.0-14) 
2025/05/27 01:02:19 [notice] 1#1: OS: Linux 6.8.0-59-generic
2025/05/27 01:02:19 [notice] 1#1: getrlimit(RLIMIT_NOFILE): 1048576:1048576
2025/05/27 01:02:19 [notice] 1#1: start worker processes
2025/05/27 01:02:19 [notice] 1#1: start worker process 29
2025/05/27 01:02:19 [notice] 1#1: start worker process 30
172.17.0.1 - - [27/May/2025:01:02:50 +0000] "GET / HTTP/1.1" 200 615 "-" "Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/116.0" "-"
2025/05/27 01:02:50 [error] 29#29: *1 open() "/usr/share/nginx/html/favicon.ico" failed (2: No such file or directory), client: 172.17.0.1, server: localhost, request: "GET /favicon.ico HTTP/1.1", host: "localhost", referrer: "http://localhost/"
172.17.0.1 - - [27/May/2025:01:02:50 +0000] "GET /favicon.ico HTTP/1.1" 404 153 "http://localhost/" "Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/116.0" "-"
^C2025/05/27 01:03:54 [notice] 1#1: signal 2 (SIGINT) received, exiting
2025/05/27 01:03:54 [notice] 29#29: exiting
2025/05/27 01:03:54 [notice] 29#29: exit
2025/05/27 01:03:54 [notice] 30#30: exiting
2025/05/27 01:03:54 [notice] 30#30: exit
2025/05/27 01:03:55 [notice] 1#1: signal 17 (SIGCHLD) received from 30
2025/05/27 01:03:55 [notice] 1#1: worker process 29 exited with code 0
2025/05/27 01:03:55 [notice] 1#1: worker process 30 exited with code 0
2025/05/27 01:03:55 [notice] 1#1: exit
doune@doune-virtual-machine:~/TP-Docker$ docker run -d -p 80:80 nginx
docker: permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Head "http://%2Fvar%2Frun%2Fdocker.sock/_ping": dial unix /var/run/docker.sock: connect: permission denied

Run 'docker run --help' for more information
doune@doune-virtual-machine:~/TP-Docker$ sudo docker run -d -p 80:80 nginx
debef6f518fbb1ea3703a6f5edb77079bd1011ecabe85aa2217d4533812df7a3
