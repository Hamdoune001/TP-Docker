doune@doune-virtual-machine:~/TP-Docker$ sudo docker pull mysql:5.7 
sudo docker pull phpmyadmin
5.7: Pulling from library/mysql
20e4dcae4c69: Pull complete 
1c56c3d4ce74: Pull complete 
e9f03a1c24ce: Pull complete 
68c3898c2015: Pull complete 
6b95a940e7b6: Pull complete 
90986bb8de6e: Pull complete 
ae71319cb779: Pull complete 
ffc89e9dfd88: Pull complete 
43d05e938198: Pull complete 
064b2d298fba: Pull complete 
df9a4d85569b: Pull complete 
Digest: sha256:4bc6bc963e6d8443453676cae56536f4b8156d78bae03c0145cbe47c2aad73bb
Status: Downloaded newer image for mysql:5.7
docker.io/library/mysql:5.7
Using default tag: latest
latest: Pulling from library/phpmyadmin
61320b01ae5e: Already exists 
b4ce612dc732: Pull complete 
093338982d92: Pull complete 
0c2a0ba9eb0c: Pull complete 
442abaed7751: Pull complete 
aa4e51934eef: Pull complete 
924949db942b: Pull complete 
153d2fb08c64: Pull complete 
26f17ce45149: Pull complete 
64a857ca8a6a: Pull complete 
7443480a6bdb: Pull complete 
d4dfcfe68eba: Pull complete 
91e76e37da73: Pull complete 
4f4fb700ef54: Pull complete 
708105cf3285: Pull complete 
97739253e39f: Pull complete 
6722b89322cb: Pull complete 
9ebc473a2663: Pull complete 
39ff72c5f974: Pull complete 
2daa1390d242: Pull complete 
Digest: sha256:73467128842bc4406372310f068bc9ccb6727a82c7b5dc9c4f3d815ead33eab8
Status: Downloaded newer image for phpmyadmin:latest
docker.io/library/phpmyadmin:latest
doune@doune-virtual-machine:~/TP-Docker$ sudo docker run -d --name mysql57 -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=demo -p 3306:3306 mysql:5.7
143b5c190be7e3a127a8c73922c650e5fac51572d501d070d6a54f482ab3030a
doune@doune-virtual-machine:~/TP-Docker$ sudo docker run -d --name phpmyadmin -e PMA_HOST=mysql57 -p 8081:80 --link mysql57 phpmyadmin
20fc6f71fdf7cd752714ca5f66e92bec242a2dcc32ece49329f8690e02f02116
doune@doune-virtual-machine:~/TP-Docker$ 

Capture_level_7_demo_tab_users.png
