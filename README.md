# Pesquisa e Biografia

* `https://github.com/gomex/docker-para-desenvolvedores`
* `https://school.linuxtips.io/courses/`
* `https://cursos.alura.com.br/course/docker-e-docker-compose`
* `https://www.mundodocker.com.br`
* `https://docs.docker.com/`

# Docker-Orbite, Estudo do Basico ao Avançado com Docker

# Instalação do docker via terminal

---
```

```
# Docker Hello World

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker run hello-world

```

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

``` 
$ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/
```
---

# Listar container

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker ps -a


CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                      PORTS               NAMES
24136025fa87        hello-world         "/hello"            10 seconds ago      Exited (0) 9 seconds ago                        festive_bardeen
04bd5c7ce1a6        hello-world         "/hello"            11 seconds ago      Exited (0) 10 seconds ago                       nostalgic_jennings
b67351a66eba        hello-world         "/hello"            12 seconds ago      Exited (0) 11 seconds ago                       intelligent_wing
73a7be80bc76        hello-world         "/hello"            14 seconds ago      Exited (0) 12 seconds ago                       admiring_easley
fea647289d44        hello-world         "/hello"            15 seconds ago      Exited (0) 14 seconds ago                       nervous_lamarr
683fc3478eb0        hello-world         "/hello"            17 seconds ago      Exited (0) 16 seconds ago                       cool_ride
```
---

# Remover todas as imagens baixadas Docker

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker container prune

WARNING! This will remove all stopped containers.
Are you sure you want to continue? [y/N] y
Deleted Containers:
24136025fa873e65d791799a1ae29522b9817acd12d57752fea80797e148169c
04bd5c7ce1a636f83537b58770f31cc8f18f39aa968cc8909967b51316ad5901
b67351a66ebaed785a95d11e7c6cd1022793f5b8944c8b0b35674ac4d31f7e59
73a7be80bc76aba90633733c4eebe98b11583c983e2e362f284a70c2a291c015
fea647289d4416a5f4a868cdab7394352607abd349d0a46dcd138461b7f7a4bc
683fc3478eb084e6535d31b1edc98f35aae2673b10a15c6fbd1480ed2830c83e

Total reclaimed space: 0B

```
---

# Executar uma imagem Docker

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker run ubuntu

```
---

# Executar uma imagem Docker e com intereção

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker run -it ubuntu

root@99280a034763:/# exit

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker ps -a

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                      PORTS               NAMES
99280a034763        ubuntu              "/bin/bash"         36 seconds ago      Exited (0) 32 seconds ago                       vigorous_ishizaka
85fbc0514784        ubuntu              "/bin/bash"         46 seconds ago      Exited (0) 45 seconds ago                       quirky_mccarthy
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker container run -a -it 85fbc0514784

```
---

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker ps

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker ps -a

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                          PORTS               NAMES
cae670ce05d1        ubuntu              "/bin/bash"         21 seconds ago      Exited (0) 19 seconds ago                           awesome_shirley
99280a034763        ubuntu              "/bin/bash"         5 minutes ago       Exited (0) 5 minutes ago                            vigorous_ishizaka
85fbc0514784        ubuntu              "/bin/bash"         5 minutes ago       Exited (0) About a minute ago                       quirky_mccarthy

```
---

# Executar um comando dentro da imagem do container e saindo

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker run ubuntu echo "Orbite"

Orbite
```
---

# Executar um comando dentro da imagem do container e interagindo

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker run -it ubuntu

root@2e1f9f6a6c41:/# exit

```
---

# Iniciar uma imagem de um container especifico

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker start 2e1f9f6a6c41

2e1f9f6a6c41

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker ps

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
2e1f9f6a6c41        ubuntu              "/bin/bash"         3 minutes ago       Up 9 seconds                            quizzical_hodgkin

```
---

# Parar uma imagem de um container especifico

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker stop 2e1f9f6a6c41

2e1f9f6a6c41

```
---

# Iniciar uma imagem de um container especifico e interagindo

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker start -a -i 2e1f9f6a6c41

root@2e1f9f6a6c41:/# exit

```

---

# Remover a imagem de um container baixada em sua máquina

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker ps -a

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                   PORTS               NAMES
2e1f9f6a6c41        ubuntu              "/bin/bash"         2 hours ago         Exited (0) 2 hours ago                       quizzical_hodgkin
ec50c72afa03        ubuntu              "echo Orbite"       2 hours ago         Exited (0) 2 hours ago                       charming_dewdney
cae670ce05d1        ubuntu              "/bin/bash"         2 hours ago         Exited (0) 2 hours ago                       awesome_shirley
99280a034763        ubuntu              "/bin/bash"         3 hours ago         Exited (0) 3 hours ago                       vigorous_ishizaka
85fbc0514784        ubuntu              "/bin/bash"         3 hours ago         Exited (0) 2 hours ago                       quirky_mccarthy

torbite@BIO-02059:~/Documents/Docker-Orbite$ docker con
config     container  context    

torbite@BIO-02059:~/Documents/Docker-Orbite$ docker con
config     container  context    

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker container rm 2e1f9f6a6c41
2e1f9f6a6c41

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker container rm ec5
ec5

```
---

# Remover todas as Imagens de containers baixadas em sua máquina

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker container prune

WARNING! This will remove all stopped containers.
Are you sure you want to continue? [y/N] y
Deleted Containers:
cae670ce05d196d4ec16f5255d2011099a0a9f1a5222140abafa4ef7cb87271e
99280a03476364bcf65957133bd7a9b4b8d68e712befcdf85892e1ca5cdf9cff
85fbc0514784732af742d590ba6daac525a670839cbb92283898f1d39d8e14c9

Total reclaimed space: 0B

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

```
---

# Listar as imagens baixadas em sua máquina do Docker

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker images

REPOSITORY                           TAG                 IMAGE ID            CREATED             SIZE
ubuntu                               latest              ccc6e87d482b        40 hours ago        64.2MB

```
---

# Ou

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker image list
REPOSITORY                           TAG                 IMAGE ID            CREATED             SIZE
orbite/nginx                         latest              bbbb318620f5        4 hours ago         127MB
orbite/alurabooks                    latest              5dde97f3aef0        4 hours ago         959MB
orbite82/node-teste-1                latest              c90e3bf3eace        46 hours ago        943MB
nginx                                latest              5ad3bd0e67a9        2 days ago          127MB
alpine                               latest              e7d92cdc71fe        6 days ago          5.59MB
mongo                                latest              105a8b77784b        6 days ago          364MB
teste                                latest              96f1e68cc1ea        7 days ago          808MB
ubuntu                               18.04               ccc6e87d482b        8 days ago          64.2MB
ubuntu                               latest              ccc6e87d482b        8 days ago          64.2MB
node                                 latest              f7756628c1ee        2 weeks ago         939MB
ubuntu                               14.04               6e4f1fe62ff1        5 weeks ago         197MB


```
---

# Remover uma imagem Docker baixada em sua máquina

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker rmi hello-world

Untagged: hello-world:latest
Untagged: hello-world@sha256:9572f7cdcee8591948c2963463447a53466950b3fc15a247fcad1917ca215a2f
Deleted: sha256:fce289e99eb9bca977dae136fbe2a82b6b7d4c372474c9235adc1741675f587e
Deleted: sha256:af0b15c8625bb1938f1d7b17081031f649fd14e6b233688eea3c5483994a66a3

```
---

# Baixar uma imagem com o numero e versão da distribuição especifica

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker run ubuntu:18.04

Unable to find image 'ubuntu:18.04' locally
18.04: Pulling from library/ubuntu
Digest: sha256:8d31dad0c58f552e890d68bbfb735588b6b820a46e459672d96e585871acc110
Status: Downloaded newer image for ubuntu:18.04

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker run ubuntu:14.04

Unable to find image 'ubuntu:14.04' locally
14.04: Pulling from library/ubuntu
2e6e20c8e2e6: Pull complete 
30bb187ac3fc: Pull complete 
b7a5bcc4a58a: Pull complete 
Digest: sha256:ffc76f71dd8be8c9e222d420dc96901a07b61616689a44c7b3ef6a10b7213de4
Status: Downloaded newer image for ubuntu:14.04

```
---

# Executar um container em BackGround

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker run -d dockersamples/static-site
030609d344a20c796c8564ce54eaa2065ce18713539ad3be50864a6476c3c78f

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker ps
CONTAINER ID        IMAGE                       COMMAND                  CREATED             STATUS              PORTS               NAMES
030609d344a2        dockersamples/static-site   "/bin/sh -c 'cd /usr…"   20 seconds ago      Up 19 seconds       80/tcp, 443/tcp     boring_haslett
d16daa7fb5a3        dockersamples/static-site   "/bin/sh -c 'cd /usr…"   4 minutes ago       Up 4 minutes        80/tcp, 443/tcp     jolly_mendeleev

```
---

# Docker stop formas mais rapida parar

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker stop 030609d344a2
030609d344a2

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker stop -t 0 d16daa7fb5a3
d16daa7fb5a3

```
---


# Docker com -P para comunicar com container

---
# Antes

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker run -d dockersamples/static-site
f80defd9bf08884eedb7f158feb454fbf25bee6a1bb8202c28d04b76bd52f91a

```
---
# Depois

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker run -d -P dockersamples/static-site
3d798eaeccbc6faf3f42655b175e55106432444d5419b9b9c746d0d0a5226baa


torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker ps
CONTAINER ID        IMAGE                       COMMAND                  CREATED             STATUS              PORTS                                           NAMES
3d798eaeccbc        dockersamples/static-site   "/bin/sh -c 'cd /usr…"   19 seconds ago      Up 18 seconds       0.0.0.0:32769->80/tcp, 0.0.0.0:32768->443/tcp   gifted_joliot
f80defd9bf08        dockersamples/static-site   "/bin/sh -c 'cd /usr…"   53 seconds ago      Up 52 seconds       80/tcp, 443/tcp                                 nifty_margulis

```
---

# Verificar a porta do container

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker port 3d798eaeccbc
443/tcp -> 0.0.0.0:32768
80/tcp -> 0.0.0.0:32769

```
---

# Acessar aplicação pela porta Hello Docker!

![hello docker image 1](https://github.com/orbite82/Docker-Orbite/blob/master/hello%20docker.png)


4: docker0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc noqueue state UP group default 
    link/ether 02:42:76:86:d1:6b brd ff:ff:ff:ff:ff:ff
    inet 172.17.0.1/16 brd 172.17.255.255 scope global docker0
       valid_lft forever preferred_lft forever
    inet6 fe80::42:76ff:fe86:d16b/64 scope link 
       valid_lft forever preferred_lft forever


---

# Executar e colocar um nome no container

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker run -d -P --name orbite-container dockersamples/static-site
11bd90a2ca109c249cfaa18f7f46594d50a2a7033c431eb863e904b9d2d73a79

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker ps
CONTAINER ID        IMAGE                       COMMAND                  CREATED             STATUS              PORTS                                           NAMES
11bd90a2ca10        dockersamples/static-site   "/bin/sh -c 'cd /usr…"   9 seconds ago       Up 8 seconds        0.0.0.0:32771->80/tcp, 0.0.0.0:32770->443/tcp   orbite-container

```
---
# Criar uma imagem docker e personalizar

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container run -it --name criar-imagens-docker ubuntu:18.04 bash
root@20c489bf2ff0:/# apt-get update
root@20c489bf2ff0:/# exit
exit

```
---
# Commit como fazer uma imagem co commit anterior 

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker commit criar-imagens-docker nossoubuntu:nginx
sha256:7d54931606f8e8a571ef85b72a8ea65d84617df6d4c37f09e452ccb2e5ad3858

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ 
REPOSITORY                           TAG                 IMAGE ID            CREATED             SIZE
nossoubuntu                          nginx               7d54931606f8        16 seconds ago      152MB
orbite/nginx                         latest              bbbb318620f5        4 hours ago         127MB
orbite/alurabooks                    latest              5dde97f3aef0        4 hours ago         959MB
orbite82/node-teste-1                latest              c90e3bf3eace        47 hours ago        943MB
nginx                                latest              5ad3bd0e67a9        2 days ago          127MB
alpine                               latest              e7d92cdc71fe        6 days ago          5.59MB
mongo                                latest              105a8b77784b        6 days ago          364MB
teste                                latest              96f1e68cc1ea        7 days ago          808MB
ubuntu                               18.04               ccc6e87d482b        8 days ago          64.2MB
ubuntu                               latest              ccc6e87d482b        8 days ago          64.2MB
node                                 latest              f7756628c1ee        2 weeks ago         939MB
ubuntu                               14.04               6e4f1fe62ff1        5 weeks ago         197MB

```
`OBS:`sudo docker image list Ou sudo docker image list

---

# Testar imgem comitada com nginx nos passos anteriores

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container run -it --rm nossoubuntu:nginx dpkg -l nginx
Desired=Unknown/Install/Remove/Purge/Hold
| Status=Not/Inst/Conf-files/Unpacked/halF-conf/Half-inst/trig-aWait/Trig-pend
|/ Err?=(none)/Reinst-required (Status,Err: uppercase=bad)
||/ Name           Version      Architecture Description
+++-==============-============-============-=================================
ii  nginx          1.14.0-0ubun all          small, powerful, scalable web/pro

```
`OBS:` Não é a melhor prática fazer desta forma.
---

# Tutorial Parte 1 - Criar, Push e Push Image DockerHub

```
┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker run -it -d ubuntu
44483e6005fb49341cc7f7b0f9749e7e9a8ce30bc4dceb755588126e4660df0e

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker ps -a
CONTAINER ID        IMAGE                      COMMAND             CREATED             STATUS                      PORTS               NAMES
44483e6005fb        ubuntu                     "/bin/bash"         5 minutes ago       Up 5 minutes                                    tender_hertz
795c8ddb9002        orbite82/modified-ubuntu   "bash"              37 minutes ago      Up 37 minutes                                   infallible_proskuriakova
1d3c04acf556        ubuntu                     "/bin/bash"         50 minutes ago      Exited (0) 45 minutes ago                       lucid_lovelace

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker exec -it 44483e6005fb bash
root@44483e6005fb:/# ls
bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
root@44483e6005fb:/# mkdir TEST_DOCKER
root@44483e6005fb:/# ls
TEST_DOCKER  bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
root@44483e6005fb:/# exit
exit

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
ubuntu              latest              ccc6e87d482b        10 days ago         64.2MB

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker stop 44483e6005fb
44483e6005fb

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker commit 44483e6005fb orbite82/modified2-ubuntu
sha256:ad56effc7a3479b2ca0f871e5c1589f606419f9ec8643b6543f987fe8d285459

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker images
REPOSITORY                  TAG                 IMAGE ID            CREATED             SIZE
orbite82/modified2-ubuntu   latest              ad56effc7a34        12 seconds ago      64.2MB
orbite82/modified-ubuntu    latest              86920ea1596a        42 minutes ago      64.2MB
ubuntu                      latest              ccc6e87d482b        10 days ago         64.2MB

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker push orbite82/modified2-ubuntu
The push refers to repository [docker.io/orbite82/modified2-ubuntu]
f552bf8ea140: Pushed 
f55aa0bd26b8: Mounted from library/ubuntu 
1d0dfb259f6a: Mounted from library/ubuntu 
21ec61b65b20: Mounted from library/ubuntu 
43c67172d1d1: Mounted from library/ubuntu 
latest: digest: sha256:52c80f1b350d0cbf8460d98bd97443787f174f527b10730bfaaaf0f8148e7aa9 size: 1359

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker push orbite82/modified-ubuntu
The push refers to repository [docker.io/orbite82/modified-ubuntu]
51ab982046db: Pushed 
f55aa0bd26b8: Mounted from orbite82/modified2-ubuntu 
1d0dfb259f6a: Mounted from orbite82/modified2-ubuntu 
21ec61b65b20: Mounted from orbite82/modified2-ubuntu 
43c67172d1d1: Mounted from orbite82/modified2-ubuntu 
latest: digest: sha256:ef3572cca778113e6033eae4b3bc03d81fe6ec82640d110d499dcd89cba611f1 size: 1359

```
---
# Tutoria Parte 2 - Removendo e testando as images do DockerHub

```
┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker ps
CONTAINER ID        IMAGE                      COMMAND             CREATED             STATUS              PORTS               NAMES
795c8ddb9002        orbite82/modified-ubuntu   "bash"              About an hour ago   Up About an hour                        infallible_proskuriakova
┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker stop 795c8ddb9002
795c8ddb9002
┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker rm -f  795c8ddb9002
795c8ddb9002
┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker ps -a
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                         PORTS               NAMES
44483e6005fb        ubuntu              "/bin/bash"         35 minutes ago      Exited (0) 27 minutes ago                          tender_hertz
1d3c04acf556        ubuntu              "/bin/bash"         About an hour ago   Exited (0) About an hour ago                       lucid_lovelace
┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker rm 44483e6005fb
44483e6005fb
┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker rm 1d3c04acf556
1d3c04acf556
┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker ps -a
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker images
REPOSITORY                  TAG                 IMAGE ID            CREATED             SIZE
orbite82/modified2-ubuntu   latest              ad56effc7a34        26 minutes ago      64.2MB
orbite82/modified-ubuntu    latest              86920ea1596a        About an hour ago   64.2MB
ubuntu                      latest              ccc6e87d482b        10 days ago         64.2MB
┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker rmi orbite82/modified2-ubuntu orbite82/modified-ubuntu
Untagged: orbite82/modified2-ubuntu:latest
Untagged: orbite82/modified2-ubuntu@sha256:52c80f1b350d0cbf8460d98bd97443787f174f527b10730bfaaaf0f8148e7aa9
Deleted: sha256:ad56effc7a3479b2ca0f871e5c1589f606419f9ec8643b6543f987fe8d285459
Deleted: sha256:e4874b6fa1d0b02b119a7a8e325b96fae07e39c55ab388f66a567d1239c2fa95
Untagged: orbite82/modified-ubuntu:latest
Untagged: orbite82/modified-ubuntu@sha256:ef3572cca778113e6033eae4b3bc03d81fe6ec82640d110d499dcd89cba611f1
Deleted: sha256:86920ea1596a074d3099d88e19eec5c9953d25ca324b6269d8b3ff33b6ab31df
Deleted: sha256:a78b22468a57b10cb09214890810c7dd1cca347d7a997b56bb8c076cf1b653c2
┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker rmi ubuntu
Untagged: ubuntu:latest
Untagged: ubuntu@sha256:8d31dad0c58f552e890d68bbfb735588b6b820a46e459672d96e585871acc110
Deleted: sha256:ccc6e87d482b79dd1645affd958479139486e47191dfe7a997c862d89cd8b4c0
Deleted: sha256:d1b7fedd4314279a7c28d01177ff56bcff65300f6d41655394bf5d8b788567f6
Deleted: sha256:340bed96497252624f5e4b0f42accfe7edbb7a01047e2bb5a8142b2464008e73
Deleted: sha256:6357c335cdfcc3a120e288bbd203bf4c861a14245ce5094634ee097e5217085b
Deleted: sha256:43c67172d1d182ca5460fc962f8f053f33028e0a3a1d423e05d91b532429e73d
┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker run -it -d orbite82/modified2-ubuntu
Unable to find image 'orbite82/modified2-ubuntu:latest' locally
latest: Pulling from orbite82/modified2-ubuntu
5c939e3a4d10: Pull complete 
c63719cdbe7a: Pull complete 
19a861ea6baf: Pull complete 
651c9d2d6c4f: Pull complete 
9be446994aba: Pull complete 
Digest: sha256:52c80f1b350d0cbf8460d98bd97443787f174f527b10730bfaaaf0f8148e7aa9
Status: Downloaded newer image for orbite82/modified2-ubuntu:latest
3123957f0910acf065616f723a6afe593e82dcb18010817e968329457619df1f

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker images
REPOSITORY                  TAG                 IMAGE ID            CREATED             SIZE
orbite82/modified2-ubuntu   latest              ad56effc7a34        34 minutes ago      64.2MB

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker run -it -d orbite82/modified2-ubuntu
Unable to find image 'orbite82/modified2-ubuntu:latest' locally
latest: Pulling from orbite82/modified2-ubuntu
5c939e3a4d10: Pull complete 
c63719cdbe7a: Pull complete 
19a861ea6baf: Pull complete 
651c9d2d6c4f: Pull complete 
9be446994aba: Pull complete 
Digest: sha256:52c80f1b350d0cbf8460d98bd97443787f174f527b10730bfaaaf0f8148e7aa9
Status: Downloaded newer image for orbite82/modified2-ubuntu:latest
3123957f0910acf065616f723a6afe593e82dcb18010817e968329457619df1f

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker images
REPOSITORY                  TAG                 IMAGE ID            CREATED             SIZE
orbite82/modified2-ubuntu   latest              ad56effc7a34        34 minutes ago      64.2MB

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker ps -a
CONTAINER ID        IMAGE                       COMMAND             CREATED             STATUS              PORTS               NAMES
6f7d8dcaf3a4        orbite82/modified2-ubuntu   "/bin/bash"         16 seconds ago      Up 15 seconds                           stupefied_spence

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker ps
CONTAINER ID        IMAGE                       COMMAND             CREATED             STATUS              PORTS               NAMES
6f7d8dcaf3a4        orbite82/modified2-ubuntu   "/bin/bash"         21 seconds ago      Up 20 seconds                           stupefied_spence

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker exec -it  6f7d8dcaf3a4 bash
root@6f7d8dcaf3a4:/# ls
TEST_DOCKER  bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
root@6f7d8dcaf3a4:/# exit
exit

```
![dockerhub_personalizando_imagens]()
---

# Programa para check security via Docker

---

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker ps 
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker run -it --net host --pid host --cap-add audit_control -v /var/lib:/var/lib -v /var/run/docker.sock:/var/run/docker.sock -v /usr/lib/systemd:/usr/lib/systemd -v /etc:/etc --label docker_bench_security docker/docker-bench-security
Unable to find image 'docker/docker-bench-security:latest' locally
latest: Pulling from docker/docker-bench-security
cd784148e348: Pull complete 
48fe0d48816d: Pull complete 
164e5e0f48c5: Pull complete 
378ed37ea5ff: Pull complete 
Digest: sha256:ddbdf4f86af4405da4a8a7b7cc62bb63bfeb75e85bf22d2ece70c204d7cfabb8
Status: Downloaded newer image for docker/docker-bench-security:latest
# ------------------------------------------------------------------------------
# Docker Bench for Security v1.3.4
#
# Docker, Inc. (c) 2015-
#
# Checks for dozens of common best-practices around deploying Docker containers in production.
# Inspired by the CIS Docker Community Edition Benchmark v1.1.0.
# ------------------------------------------------------------------------------

Initializing Tue Jan 21 13:19:36 UTC 2020


[INFO] 1 - Host Configuration
[WARN] 1.1  - Ensure a separate partition for containers has been created
[NOTE] 1.2  - Ensure the container host has been Hardened
[INFO] 1.3  - Ensure Docker is up to date
[INFO]      * Using 19.03.5, verify is it up to date as deemed necessary
[INFO]      * Your operating system vendor may provide support and security maintenance for Docker
[INFO] 1.4  - Ensure only trusted users are allowed to control Docker daemon
[INFO]      * docker:x:999
[WARN] 1.5  - Ensure auditing is configured for the Docker daemon
[WARN] 1.6  - Ensure auditing is configured for Docker files and directories - /var/lib/docker
[WARN] 1.7  - Ensure auditing is configured for Docker files and directories - /etc/docker
[INFO] 1.8  - Ensure auditing is configured for Docker files and directories - docker.service
[INFO]      * File not found
[INFO] 1.9  - Ensure auditing is configured for Docker files and directories - docker.socket
[INFO]      * File not found
[WARN] 1.10  - Ensure auditing is configured for Docker files and directories - /etc/default/docker
[INFO] 1.11  - Ensure auditing is configured for Docker files and directories - /etc/docker/daemon.json
[INFO]      * File not found
[INFO] 1.12  - Ensure auditing is configured for Docker files and directories - /usr/bin/docker-containerd
[INFO]      * File not found
[INFO] 1.13  - Ensure auditing is configured for Docker files and directories - /usr/bin/docker-runc
[INFO]      * File not found


[INFO] 2 - Docker daemon configuration
[WARN] 2.1  - Ensure network traffic is restricted between containers on the default bridge
[PASS] 2.2  - Ensure the logging level is set to 'info'
[PASS] 2.3  - Ensure Docker is allowed to make changes to iptables
[PASS] 2.4  - Ensure insecure registries are not used
[PASS] 2.5  - Ensure aufs storage driver is not used
[INFO] 2.6  - Ensure TLS authentication for Docker daemon is configured
[INFO]      * Docker daemon not listening on TCP
[INFO] 2.7  - Ensure the default ulimit is configured appropriately
[INFO]      * Default ulimit doesn't appear to be set
[WARN] 2.8  - Enable user namespace support
[PASS] 2.9  - Ensure the default cgroup usage has been confirmed
[PASS] 2.10  - Ensure base device size is not changed until needed
[WARN] 2.11  - Ensure that authorization for Docker client commands is enabled
[WARN] 2.12  - Ensure centralized and remote logging is configured
[INFO] 2.13  - Ensure operations on legacy registry (v1) are Disabled (Deprecated)
[WARN] 2.14  - Ensure live restore is Enabled
[WARN] 2.15  - Ensure Userland Proxy is Disabled
[PASS] 2.16  - Ensure daemon-wide custom seccomp profile is applied, if needed
[PASS] 2.17  - Ensure experimental features are avoided in production
[WARN] 2.18  - Ensure containers are restricted from acquiring new privileges


[INFO] 3 - Docker daemon configuration files
[INFO] 3.1  - Ensure that docker.service file ownership is set to root:root
[INFO]      * File not found
[INFO] 3.2  - Ensure that docker.service file permissions are set to 644 or more restrictive
[INFO]      * File not found
[INFO] 3.3  - Ensure that docker.socket file ownership is set to root:root
[INFO]      * File not found
[INFO] 3.4  - Ensure that docker.socket file permissions are set to 644 or more restrictive
[INFO]      * File not found
[PASS] 3.5  - Ensure that /etc/docker directory ownership is set to root:root
[PASS] 3.6  - Ensure that /etc/docker directory permissions are set to 755 or more restrictive
[INFO] 3.7  - Ensure that registry certificate file ownership is set to root:root
[INFO]      * Directory not found
[INFO] 3.8  - Ensure that registry certificate file permissions are set to 444 or more restrictive
[INFO]      * Directory not found
[INFO] 3.9  - Ensure that TLS CA certificate file ownership is set to root:root
[INFO]      * No TLS CA certificate found
[INFO] 3.10  - Ensure that TLS CA certificate file permissions are set to 444 or more restrictive
[INFO]      * No TLS CA certificate found
[INFO] 3.11  - Ensure that Docker server certificate file ownership is set to root:root
[INFO]      * No TLS Server certificate found
[INFO] 3.12  - Ensure that Docker server certificate file permissions are set to 444 or more restrictive
[INFO]      * No TLS Server certificate found
[INFO] 3.13  - Ensure that Docker server certificate key file ownership is set to root:root
[INFO]      * No TLS Key found
[INFO] 3.14  - Ensure that Docker server certificate key file permissions are set to 400
[INFO]      * No TLS Key found
[PASS] 3.15  - Ensure that Docker socket file ownership is set to root:docker
[PASS] 3.16  - Ensure that Docker socket file permissions are set to 660 or more restrictive
[INFO] 3.17  - Ensure that daemon.json file ownership is set to root:root
[INFO]      * File not found
[INFO] 3.18  - Ensure that daemon.json file permissions are set to 644 or more restrictive
[INFO]      * File not found
[PASS] 3.19  - Ensure that /etc/default/docker file ownership is set to root:root
[PASS] 3.20  - Ensure that /etc/default/docker file permissions are set to 644 or more restrictive


[INFO] 4 - Container Images and Build File
[INFO] 4.1  - Ensure a user for the container has been created
[INFO]      * No containers running
[NOTE] 4.2  - Ensure that containers use trusted base images
[NOTE] 4.3  - Ensure unnecessary packages are not installed in the container
[NOTE] 4.4  - Ensure images are scanned and rebuilt to include security patches
[WARN] 4.5  - Ensure Content trust for Docker is Enabled
[WARN] 4.6  - Ensure HEALTHCHECK instructions have been added to the container image
[WARN]      * No Healthcheck found: [teste:latest]
[WARN]      * No Healthcheck found: [ubuntu:18.04 ubuntu:latest]
[WARN]      * No Healthcheck found: [ubuntu:18.04 ubuntu:latest]
[WARN]      * No Healthcheck found: [ubuntu:14.04]
[WARN]      * No Healthcheck found: [k8s.gcr.io/kube-proxy:v1.17.0]
[WARN]      * No Healthcheck found: [k8s.gcr.io/kube-scheduler:v1.17.0]
[WARN]      * No Healthcheck found: [k8s.gcr.io/kube-controller-manager:v1.17.0]
[WARN]      * No Healthcheck found: [k8s.gcr.io/kube-apiserver:v1.17.0]
[WARN]      * No Healthcheck found: [gcr.io/kubernetes-helm/tiller:v2.16.1]
[WARN]      * No Healthcheck found: [weaveworks/weave-npc:2.6.0]
[WARN]      * No Healthcheck found: [weaveworks/weave-kube:2.6.0]
[WARN]      * No Healthcheck found: [k8s.gcr.io/coredns:1.6.5]
[WARN]      * No Healthcheck found: [k8s.gcr.io/etcd:3.4.3-0]
[WARN]      * No Healthcheck found: [node:12.2.0-alpine]
[WARN]      * No Healthcheck found: [k8s.gcr.io/pause:3.1]
[WARN]      * No Healthcheck found: [dockersamples/static-site:latest]
[INFO] 4.7  - Ensure update instructions are not use alone in the Dockerfile
[INFO]      * Update instruction found: [k8s.gcr.io/kube-proxy:v1.17.0]
[INFO]      * Update instruction found: [weaveworks/weave-npc:2.6.0]
[INFO]      * Update instruction found: [weaveworks/weave-kube:2.6.0]
[NOTE] 4.8  - Ensure setuid and setgid permissions are removed in the images
[INFO] 4.9  - Ensure COPY is used instead of ADD in Dockerfile
[INFO]      * ADD in image history: [teste:latest]
[INFO]      * ADD in image history: [ubuntu:18.04 ubuntu:latest]
[INFO]      * ADD in image history: [ubuntu:18.04 ubuntu:latest]
[INFO]      * ADD in image history: [ubuntu:14.04]
[INFO]      * ADD in image history: [k8s.gcr.io/kube-proxy:v1.17.0]
[INFO]      * ADD in image history: [k8s.gcr.io/kube-scheduler:v1.17.0]
[INFO]      * ADD in image history: [k8s.gcr.io/kube-controller-manager:v1.17.0]
[INFO]      * ADD in image history: [k8s.gcr.io/kube-apiserver:v1.17.0]
[INFO]      * ADD in image history: [gcr.io/kubernetes-helm/tiller:v2.16.1]
[INFO]      * ADD in image history: [weaveworks/weave-npc:2.6.0]
[INFO]      * ADD in image history: [weaveworks/weave-kube:2.6.0]
[INFO]      * ADD in image history: [k8s.gcr.io/coredns:1.6.5]
[INFO]      * ADD in image history: [k8s.gcr.io/etcd:3.4.3-0]
[INFO]      * ADD in image history: [node:12.2.0-alpine]
[INFO]      * ADD in image history: [docker/docker-bench-security:latest]
[INFO]      * ADD in image history: [k8s.gcr.io/pause:3.1]
[INFO]      * ADD in image history: [dockersamples/static-site:latest]
[NOTE] 4.10  - Ensure secrets are not stored in Dockerfiles
[NOTE] 4.11  - Ensure verified packages are only Installed


[INFO] 5 - Container Runtime
[INFO]      * No containers running, skipping Section 5


[INFO] 6 - Docker Security Operations
[INFO] 6.1  - Avoid image sprawl
[INFO]      * There are currently: 16 images
[INFO] 6.2  - Avoid container sprawl
[INFO]      * There are currently a total of 8 containers, with 1 of them currently running


[INFO] 7 - Docker Swarm Configuration
[PASS] 7.1  - Ensure swarm mode is not Enabled, if not needed
[PASS] 7.2  - Ensure the minimum number of manager nodes have been created in a swarm (Swarm mode not enabled)
[PASS] 7.3  - Ensure swarm services are binded to a specific host interface (Swarm mode not enabled)
[PASS] 7.4  - Ensure data exchanged between containers are encrypted on different nodes on the overlay network
[PASS] 7.5  - Ensure Docker's secret management commands are used for managing secrets in a Swarm cluster (Swarm mode not enabled)
[PASS] 7.6  - Ensure swarm manager is run in auto-lock mode (Swarm mode not enabled)
[PASS] 7.7  - Ensure swarm manager auto-lock key is rotated periodically (Swarm mode not enabled)
[PASS] 7.8  - Ensure node certificates are rotated as appropriate (Swarm mode not enabled)
[PASS] 7.9  - Ensure CA certificates are rotated as appropriate (Swarm mode not enabled)
[PASS] 7.10  - Ensure management plane traffic has been separated from data plane traffic (Swarm mode not enabled)

[INFO] Checks: 74
[INFO] Score: 10

```
---

# Salvar dados com volumes

```
┌─[torbite]@[BIO-02059]:~
└──> $ docker run -v "/var/www" ubuntu

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker ps -a
CONTAINER ID        IMAGE                          COMMAND                  CREATED             STATUS                      PORTS               NAMES
1e48135c289a        ubuntu                         "/bin/bash"              10 minutes ago      Exited (0) 10 minutes ago                       trusting_engelbart

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker inspect 1e48135c289a

"Mounts": [
            {
                "Type": "volume",
                "Name": "bad1c6bc29c48d30d584e4d31eee0660eb2e2faa7af9d4303095dc205ed7365b",
                "Source": "/var/lib/docker/volumes/bad1c6bc29c48d30d584e4d31eee0660eb2e2faa7af9d4303095dc205ed7365b/_data",
                "Destination": "/var/www",
                "Driver": "local",
                "Mode": "",
                "RW": true,
                "Propagation": ""

```
---
# Salvar e direcionar os dados, logs e etc... do container na sua pasta local

```
┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker run -it -v "/home/torbite/Documents/Docker-Orbite/Docker-Files-Save:/var/www" ubuntu
root@d44133277375:/# ls
bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
root@d44133277375:/# cd var/www/
root@d44133277375:/var/www# touch novo-arquivo.txt
root@d44133277375:/var/www# echo "Arquivo criado dentro deste volume" > novo-arquivo.txt

```
![container-máquinalocal](https://github.com/orbite82/Docker-Orbite/blob/master/container-máquinalocal.png )

---

# Rodar o código dentro de um container

```
┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker run -p 8080:3000 -v "/home/torbite/Documents/Docker-Orbite/Docker-Files-Save/volume-exemplo/:/var/www" node npm start
Unable to find image 'node:latest' locally
latest: Pulling from library/node
146bd6a88618: Pull complete 
9935d0c62ace: Pull complete 
db0efb86e806: Pull complete 
e705a4c4fd31: Pull complete 
c877b722db6f: Pull complete 
645c20ec8214: Pull complete 
015773e73227: Pull complete 
ed90cb6d78c9: Pull complete 
cf4d9e2a1c31: Pull complete 
Digest: sha256:2822a3dad9c78add26f6265983d82b49882560c34c018cbbb09e594027a5d1bc
Status: Downloaded newer image for node:latest
npm ERR! code ENOENT
npm ERR! syscall open
npm ERR! path /package.json
npm ERR! errno -2
npm ERR! enoent ENOENT: no such file or directory, open '/package.json'
npm ERR! enoent This is related to npm not being able to find a file.
npm ERR! enoent 

npm ERR! A complete log of this run can be found in:
npm ERR!     /root/.npm/_logs/2020-01-22T18_15_53_818Z-debug.log

```
---

# Corrigir o ERR! , informando qual diretório deve ser executado

* vamos passar a flag `-w` (Working Directory)
```
┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker run -p 8080:3000 -v "/home/torbite/Documents/Docker-Orbite/Docker-Files-Save/volume-exemplo/:/var/www" -w "/var/www" node npm start

> volume-exemplo@1.0.0 start /var/www
> node .

Server is listening on port 3000
```
# OBS

* Se não passar o parametro -d, seu terminal vai travar, porém a apicação vai rodar e você conseve ver via localhost:8080 o resultado abaixo:

![eu-amo-docker](https://github.com/orbite82/Docker-Orbite/blob/master/eu-amo-docker.png)

```
┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker run -p 8080:3000 -v  "/home/torbite/Documents/Docker-Orbite/Docker-Files-Save/volume-exemplo/:/var/www" -w "/var/www" -d node npm start
008a001e129de2d503f7421d902fbf320a0a71b5fdecbe6feeae60b546b7b8c0

```
---

# Alterar a aplicação no quente para i-love-very-docker

![i-love-very-docker](https://github.com/orbite82/Docker-Orbite/blob/master/i-love-very-docker.png)

* acessar novamente ou reload localhost:8080

![i-love-very-docker2](https://github.com/orbite82/Docker-Orbite/blob/master/i-love-very-docker2.png)

# ou `-d` no começo

```
┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker run -d -p 8080:3000 -v  "/home/torbite/Documents/Docker-Orbite/Docker-Files-Save/volume-exemplo/:/var/www" -w "/var/www" node npm start
954e8831381205addf4f014853e9c47c6e4acaeaa08e4cb336f0ebd45dcefde8

```
---

# Criar um Dockerfile

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ ls
 command-initial-docker-test.txt   container-máquinalocal.png   Docker-Files-Save   eu-amo-docker.png  'hello docker.png'   i-love-very-docker2.png   i-love-very-docker.png   README.md   volume-exemplo.zip
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ cd Docker-Files-Save/
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/Docker-Files-Save
└──> $ ls
novo-arquivo.txt  volume-exemplo
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/Docker-Files-Save
└──> $ cd volume-exemplo/
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/Docker-Files-Save/volume-exemplo
└──> $ ls
Dockerfile  index.html  index.js  main.css  package.json

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/Docker-Files-Save/volume-exemplo
└──> $ sudo docker build -f Dockerfile -t orbite82/node-teste-1 .
Sending build context to Docker daemon  6.144kB
Step 1/7 : FROM node:latest
 ---> f7756628c1ee
Step 2/7 : MAINTAINER Thiago Orbite
 ---> Running in 09dbd434e599
Removing intermediate container 09dbd434e599
 ---> 564a852c3f48
Step 3/7 : COPY . /var/www
 ---> f78e9f6da5fd
Step 4/7 : WORKDIR /var/www
 ---> Running in 463d5432e9f3
Removing intermediate container 463d5432e9f3
 ---> a9fee9c3c68a
Step 5/7 : RUN npm install
 ---> Running in ffa8984421c6
npm notice created a lockfile as package-lock.json. You should commit this file.
npm WARN volume-exemplo@1.0.0 No description
npm WARN volume-exemplo@1.0.0 No repository field.

added 50 packages from 37 contributors and audited 126 packages in 4.431s
found 0 vulnerabilities

Removing intermediate container ffa8984421c6
 ---> 7401e2ce9447
Step 6/7 : ENTRYPOINT npm start
 ---> Running in 910e7add8c63
Removing intermediate container 910e7add8c63
 ---> 67771c5610f6
Step 7/7 : EXPOSE 3000
 ---> Running in 9afc106458e2
Removing intermediate container 9afc106458e2
 ---> a1be224ed3ed
Successfully built a1be224ed3ed
Successfully tagged orbite82/node-teste-1:latest

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/Docker-Files-Save/volume-exemplo
└──> $ sudo docker images
REPOSITORY                           TAG                 IMAGE ID            CREATED             SIZE
orbite82/node-teste-1                  latest              a1be224ed3ed        7 minutes ago       943MB

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/Docker-Files-Save/volume-exemplo
└──> $ sudo docker run -d -p 8080:3000 orbite82/node-teste-1
6e489adc0f1394886e742a76833cff286244ccc0dbbd225cc5d44f76bc7f1953

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/Docker-Files-Save/volume-exemplo
└──> $ sudo docker ps
CONTAINER ID        IMAGE                 COMMAND                  CREATED              STATUS              PORTS                    NAMES
6e489adc0f13        orbite82/node-teste-1   "/bin/sh -c 'npm sta…"   About a minute ago   Up About a minute   0.0.0.0:8080->3000/tcp   focused_mccarthy

```
---

# Subir uma imagem no DockerHub
---

# Docker Login

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/Docker-Files-Save/volume-exemplo
└──> $ sudo docker login
Login with your Docker ID to push and pull images from Docker Hub. If you don't have a Docker ID, head over to https://hub.docker.com to create one.
Username: orbite82
Password: 
WARNING! Your password will be stored unencrypted in /home/torbite/.docker/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded

```
---

# Tag na imagem docker

```

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker images
REPOSITORY                           TAG                 IMAGE ID            CREATED             SIZE
meuubuntu                            nginx               0d6db5dc3a86        10 minutes ago      206MB
nossoubuntu                          nginx               7d54931606f8        24 minutes ago      152MB
orbite/nginx                         latest              bbbb318620f5        5 hours ago         127MB


┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker tag orbite/nginx orbite82/orbite/nginx:latest

```
---

# Docker Push

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/Docker-Files-Save/volume-exemplo
└──> $ sudo docker push orbite82/node-teste-1
The push refers to repository [docker.io/orbite82/node-teste-1]
a2df4fd75275: Pushed 
96d223e7ea2d: Pushed 
0f9ac94f8ebe: Pushed 
8b6ab0bb1c8e: Pushed 
6f8fa9f09d6b: Pushed 
42f9c2f9c08e: Pushed 
99e8bd3efaaf: Pushed 
bee1e39d7c3a: Pushed 
1f59a4b2e206: Pushed 
0ca7f54856c0: Pushed 
ebb9ae013834: Pushed 
latest: digest: sha256:6065e5250f7f97eb467ba40ea8c9ef4d7d6dee357465879197b01b177d2368dc size: 2634

```
# Dockerhub 

![dockerhub1](https://github.com/orbite82/Docker-Orbite/blob/master/dockerhub1.png)


# Docker Pull para testar

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/Docker-Files-Save/volume-exemplo
└──> $ sudo docker pull orbite82/node-teste-1
Using default tag: latest
latest: Pulling from orbite82/node-teste-1
Digest: sha256:6065e5250f7f97eb467ba40ea8c9ef4d7d6dee357465879197b01b177d2368dc
Status: Image is up to date for orbite82/node-teste-1:latest
docker.io/orbite82/node-teste-1:latest

```
---

# Criar uma rede no docker

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker network create --driver bridge minha-rede2
58184c6ffe3811338d49c5f94f599d447a05757ddc798f8ad9715249b636dca2

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker network ls
NETWORK ID          NAME                DRIVER              SCOPE
158f5528ea4d        bridge              bridge              local
0643e57cda2b        host                host                local
c6633dd8eac4        minha-rede          bridge              local
58184c6ffe38        minha-rede2         bridge              local
7aa972bae58a        none                null                local

```

# Remover uma rede criada no docker

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker network rm minha-rede2
minha-rede2

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker network ls
NETWORK ID          NAME                DRIVER              SCOPE
158f5528ea4d        bridge              bridge              local
0643e57cda2b        host                host                local
c6633dd8eac4        minha-rede          bridge              local
7aa972bae58a        none                null                local

```
---

# Atrelar minha-rede criada para docker em containers

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker network ls
NETWORK ID          NAME                DRIVER              SCOPE
158f5528ea4d        bridge              bridge              local
0643e57cda2b        host                host                local
c6633dd8eac4        minha-rede          bridge              local
7aa972bae58a        none                null                local

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker run -it --name meu-container --network minha-rede alpine 
/ # hostname -i
172.23.0.2

```

```

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
a89a30980dac        alpine              "/bin/sh"           48 seconds ago      Up 47 seconds                           meu-container
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker inspect meu-container
[
    {
        "Id": "a89a30980dac7ac179f592f5ead5ef5a4f98964b2f24c09503a2281bd62b361b",
        "Created": "2020-01-23T12:34:44.490180032Z",
        "Path": "/bin/sh",
        "Args": [],
        "State": {
            "Status": "running",
            "Running": true,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 32477,
            "ExitCode": 0,
            "Error": "",
            "StartedAt": "2020-01-23T12:34:44.932913314Z",
            "FinishedAt": "0001-01-01T00:00:00Z"
        },
        "Image": "sha256:e7d92cdc71feacf90708cb59182d0df1b911f8ae022d29e8e95d75ca6a99776a",
        "ResolvConfPath": "/var/lib/docker/containers/a89a30980dac7ac179f592f5ead5ef5a4f98964b2f24c09503a2281bd62b361b/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/a89a30980dac7ac179f592f5ead5ef5a4f98964b2f24c09503a2281bd62b361b/hostname",
        "HostsPath": "/var/lib/docker/containers/a89a30980dac7ac179f592f5ead5ef5a4f98964b2f24c09503a2281bd62b361b/hosts",
        "LogPath": "/var/lib/docker/containers/a89a30980dac7ac179f592f5ead5ef5a4f98964b2f24c09503a2281bd62b361b/a89a30980dac7ac179f592f5ead5ef5a4f98964b2f24c09503a2281bd62b361b-json.log",
        "Name": "/meu-container",
        "RestartCount": 0,
        "Driver": "overlay2",
        "Platform": "linux",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "docker-default",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": null,
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "minha-rede",
            "PortBindings": {},
            "RestartPolicy": {
                "Name": "no",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "CapAdd": null,
            "CapDrop": null,
            "Capabilities": null,
            "Dns": [],
            "DnsOptions": [],
            "DnsSearch": [],
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "private",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 0,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": null,
            "UTSMode": "",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "ConsoleSize": [
                0,
                0
            ],
            "Isolation": "",
            "CpuShares": 0,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "",
            "BlkioWeight": 0,
            "BlkioWeightDevice": [],
            "BlkioDeviceReadBps": null,
            "BlkioDeviceWriteBps": null,
            "BlkioDeviceReadIOps": null,
            "BlkioDeviceWriteIOps": null,
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DeviceCgroupRules": null,
            "DeviceRequests": null,
            "KernelMemory": 0,
            "KernelMemoryTCP": 0,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": null,
            "OomKillDisable": false,
            "PidsLimit": null,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0,
            "MaskedPaths": [
                "/proc/asound",
                "/proc/acpi",
                "/proc/kcore",
                "/proc/keys",
                "/proc/latency_stats",
                "/proc/timer_list",
                "/proc/timer_stats",
                "/proc/sched_debug",
                "/proc/scsi",
                "/sys/firmware"
            ],
            "ReadonlyPaths": [
                "/proc/bus",
                "/proc/fs",
                "/proc/irq",
                "/proc/sys",
                "/proc/sysrq-trigger"
            ]
        },
        "GraphDriver": {
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/7dcafa906730c975e585e6d597bef5bf9be4a93b532f095c8d1337af79051727-init/diff:/var/lib/docker/overlay2/95186bfc05ad74cd1946a8d99447000e703cb14ef4240898bc3bf94c5cd80c9a/diff",
                "MergedDir": "/var/lib/docker/overlay2/7dcafa906730c975e585e6d597bef5bf9be4a93b532f095c8d1337af79051727/merged",
                "UpperDir": "/var/lib/docker/overlay2/7dcafa906730c975e585e6d597bef5bf9be4a93b532f095c8d1337af79051727/diff",
                "WorkDir": "/var/lib/docker/overlay2/7dcafa906730c975e585e6d597bef5bf9be4a93b532f095c8d1337af79051727/work"
            },
            "Name": "overlay2"
        },
        "Mounts": [],
        "Config": {
            "Hostname": "a89a30980dac",
            "Domainname": "",
            "User": "",
            "AttachStdin": true,
            "AttachStdout": true,
            "AttachStderr": true,
            "Tty": true,
            "OpenStdin": true,
            "StdinOnce": true,
            "Env": [
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
            ],
            "Cmd": [
                "/bin/sh"
            ],
            "Image": "alpine",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": null,
            "OnBuild": null,
            "Labels": {}
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "3a82edfbe93ddde27404f568486d4f04256a55297fc88871c827fa00ca4dcd16",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": {},
            "SandboxKey": "/var/run/docker/netns/3a82edfbe93d",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "",
            "Gateway": "",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "",
            "IPPrefixLen": 0,
            "IPv6Gateway": "",
            "MacAddress": "",

```
# Quebra de linha para melhor visualizar o "Networks"

```
            "Networks": {
                "minha-rede": {
                    "IPAMConfig": null,
                    "Links": null,
                    "Aliases": [
                        "a89a30980dac"
                    ],
                    "NetworkID": "c6633dd8eac44a2dc9eadcc905b7c101be1d878de7da8f4e42da0fdc085e5728",
                    "EndpointID": "91a54c12a86d4612372da4684ad85cc8fa1032636af988f4f821cca651134398",
                    "Gateway": "172.23.0.1",
                    "IPAddress": "172.23.0.2",
                    "IPPrefixLen": 16,
                    "IPv6Gateway": "",
                    "GlobalIPv6Address": "",
                    "GlobalIPv6PrefixLen": 0,
                    "MacAddress": "02:42:ac:17:00:02",
                    "DriverOpts": null
                }
            }
        }
    }
]

```
---

# Criar uma rede local enmtre container, pingando pelo nome do container

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker run --name meu-container1 -it -d --network minha-rede alpine
e29077d4d11106ea7bfd784ddcb9a606b86afdd5de1bcde406d730b118699464

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker run --name meu-container2 -it -d --network minha-rede alpine
f3875faf450c6c3bfeeab6e1ec7fb2bab184ef61d51662bd01be0b7a3d1500ab

```

# Rede já foi atrelada

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED              STATUS              PORTS               NAMES
f3875faf450c        alpine              "/bin/sh"           51 seconds ago       Up 51 seconds                           meu-container2
e29077d4d111        alpine              "/bin/sh"           About a minute ago   Up About a minute                       meu-container1

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker network ls
NETWORK ID          NAME                DRIVER              SCOPE
158f5528ea4d        bridge              bridge              local
0643e57cda2b        host                host                local
c6633dd8eac4        minha-rede          bridge              local
7aa972bae58a        none                null                local

```
# Pingar o container pelo nome do 2 container

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container attach f3875faf450c
/ # ping meu-container1
PING meu-container1 (172.23.0.2): 56 data bytes
64 bytes from 172.23.0.2: seq=0 ttl=64 time=0.269 ms
64 bytes from 172.23.0.2: seq=1 ttl=64 time=0.131 ms
64 bytes from 172.23.0.2: seq=2 ttl=64 time=0.149 ms
64 bytes from 172.23.0.2: seq=3 ttl=64 time=0.172 ms
^C
--- meu-container1 ping statistics ---
4 packets transmitted, 4 packets received, 0% packet loss
round-trip min/avg/max = 0.131/0.180/0.269 ms
/ #

```
---
# Pegar dados de um banco via docker

* Passo 1 logar no github baixar a imagem da aplicação 
```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker login
Authenticating with existing credentials...
WARNING! Your password will be stored unencrypted in /home/torbite/.docker/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker pull douglasq/alura-books:cap05
cap05: Pulling from douglasq/alura-books
ad74af05f5a2: Pull complete 
2b032b8bbe8b: Pull complete 
a9a5b35f6ead: Pull complete 
3245b5a1c52c: Pull complete 
afa075743392: Pull complete 
9fb9f21641cd: Pull complete 
b1074d048a61: Pull complete 
602b2c2b7041: Pull complete 
af5a13f5922f: Pull complete 
997eb00aa53e: Pull complete 
Digest: sha256:486bbfd2018823d7a6613c7fa532574371ac2aa40cf703178379ec08a340d25d
Status: Downloaded newer image for douglasq/alura-books:cap05
docker.io/douglasq/alura-books:cap05

```
`Obs:` https://hub.docker.com/r/douglasq/alura-books/
 
versão 05 e 06 disponível

---
```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker run -d -p 8080:3000 douglasq/alura-books:cap05
4b1e63035803ca9218e87cd307f45901c4b170e3d88f9530d70831b4795d6e7f

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker ps
CONTAINER ID        IMAGE                        COMMAND             CREATED             STATUS              PORTS                    NAMES
4b1e63035803        douglasq/alura-books:cap05   "npm start"         10 seconds ago      Up 10 seconds       0.0.0.0:8080->3000/tcp   condescending_poitras  
```
---

![aplicacao-livro](https://github.com/orbite82/Docker-Orbite/blob/master/aplicacao-livros.png)

---

* Após teste remover o container e seguir o procedimento de subir o banco mongo

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker ps

CONTAINER ID        IMAGE                        COMMAND             CREATED             STATUS              PORTS                    NAMES
4b1e63035803        douglasq/alura-books:cap05   "npm start"         30 minutes ago      Up 30 minutes       0.0.0.0:8080->3000/tcp   condescending_poitras
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker rm -f 4b1e63035803

4b1e63035803
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker network ls
NETWORK ID          NAME                DRIVER              SCOPE
158f5528ea4d        bridge              bridge              local
0643e57cda2b        host                host                local
c6633dd8eac4        minha-rede          bridge              local
7aa972bae58a        none                null                local

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker run -d --name meu-mongo --network minha-rede mongo

```
* Na sequencia subir a aplicação e validar

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker run --network minha-rede -d -p 8080:3000 douglasq/alura-books:cap05
6eed50b4b9434388819a015c0483a26557357814cdef74a93653e86cceffea17

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker ps
CONTAINER ID        IMAGE                        COMMAND                  CREATED              STATUS              PORTS                    NAMES
6eed50b4b943        douglasq/alura-books:cap05   "npm start"              14 seconds ago       Up 13 seconds       0.0.0.0:8080->3000/tcp   affectionate_cartwright
320ce661dcbe        mongo                        "docker-entrypoint.s…"   About a minute ago   Up About a minute   27017/tcp                meu-mongo

```
# Check se os container's estão na mesma rede : minha-rede

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker network inspect minha-rede
[
    {
        "Name": "minha-rede",
        "Id": "c6633dd8eac44a2dc9eadcc905b7c101be1d878de7da8f4e42da0fdc085e5728",
        "Created": "2020-01-23T09:21:33.842032995-03:00",
        "Scope": "local",
        "Driver": "bridge",
        "EnableIPv6": false,
        "IPAM": {
            "Driver": "default",
            "Options": {},
            "Config": [
                {
                    "Subnet": "172.23.0.0/16",
                    "Gateway": "172.23.0.1"
                }
            ]
        },
        "Internal": false,
        "Attachable": false,
        "Ingress": false,
        "ConfigFrom": {
            "Network": ""
        },
        "ConfigOnly": false,
        "Containers": {
            "320ce661dcbe0aa58d4589e68af2b1fbf88340756fcdfa14179b6bc2c2934cc1": {
                "Name": "meu-mongo",
                "EndpointID": "c79258d0f2812defbf7d6a321e681c1f357204474ed900d35334d2ec035024ea",
                "MacAddress": "02:42:ac:17:00:02",
                "IPv4Address": "172.23.0.2/16",
                "IPv6Address": ""
            },
            "e2dfe58f28a7b31b7971f2918e65377d70557dd117366883ff0e5555ded50aaf": {
                "Name": "quirky_gauss",
                "EndpointID": "82ec03b95bb0ca37e1ecfa1e194cedb57fcc48ddb81487e1b0f76111a99e90f9",
                "MacAddress": "02:42:ac:17:00:03",
                "IPv4Address": "172.23.0.3/16",
                "IPv6Address": ""
            }
        },
        "Options": {},
        "Labels": {}
    }
]

```
# Teste da aplicação
---

![livros-salvos](https://github.com/orbite82/Docker-Orbite/blob/master/livros-salvos.png)

---

# Teste novamente
---

![teste-novamente](https://github.com/orbite82/Docker-Orbite/blob/master/teste-novamente.png)

---

# Automatizando com Docker Compose

---
* Instalar o docker compose

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/alura-docker-cap06
└──> $ sudo apt install docker-compose

```
---
* Executar na raiz do projeto docker compose

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/alura-docker-cap06
└──> $ ls
config  database.js  docker  docker-compose.yml  models  package.json  public  README.md  routes  server.js  views

```
* Executar o comando docker-compose build

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/alura-docker-cap06
└──> $ sudo docker-compose build
mongodb uses an image, skipping
Building node2
Step 1/8 : FROM node:latest
 ---> f7756628c1ee
Step 2/8 : MAINTAINER Douglas Quintanilha
 ---> Running in 6bd30be7a524
Removing intermediate container 6bd30be7a524
 ---> 4e775b15f8d7
Step 3/8 : ENV NODE_ENV=development
 ---> Running in c20145ceee33
Removing intermediate container c20145ceee33
 ---> bc2548c79594
Step 4/8 : COPY . /var/www
 ---> 924a18b9ce7b
Step 5/8 : WORKDIR /var/www
 ---> Running in 26ab5c161077
Removing intermediate container 26ab5c161077
 ---> a1252d8f149b
Step 6/8 : RUN npm install
 ---> Running in efb83f21bbb2
npm notice created a lockfile as package-lock.json. You should commit this file.
added 117 packages from 110 contributors and audited 220 packages in 11.229s

1 package is looking for funding
  run `npm fund` for details

found 0 vulnerabilities

Removing intermediate container efb83f21bbb2
 ---> b2617c0f9387
Step 7/8 : ENTRYPOINT ["npm", "start"]
 ---> Running in 24bef6095469
Removing intermediate container 24bef6095469
 ---> a180f5389fc3
Step 8/8 : EXPOSE 3000
 ---> Running in e602d11cb6e7
Removing intermediate container e602d11cb6e7
 ---> 5dde97f3aef0
Successfully built 5dde97f3aef0
Successfully tagged orbite/alurabooks:latest
Building node3
Step 1/8 : FROM node:latest
 ---> f7756628c1ee
Step 2/8 : MAINTAINER Douglas Quintanilha
 ---> Using cache
 ---> 4e775b15f8d7
Step 3/8 : ENV NODE_ENV=development
 ---> Using cache
 ---> bc2548c79594
Step 4/8 : COPY . /var/www
 ---> Using cache
 ---> 924a18b9ce7b
Step 5/8 : WORKDIR /var/www
 ---> Using cache
 ---> a1252d8f149b
Step 6/8 : RUN npm install
 ---> Using cache
 ---> b2617c0f9387
Step 7/8 : ENTRYPOINT ["npm", "start"]
 ---> Using cache
 ---> a180f5389fc3
Step 8/8 : EXPOSE 3000
 ---> Using cache
 ---> 5dde97f3aef0
Successfully built 5dde97f3aef0
Successfully tagged orbite/alurabooks:latest
Building node1
Step 1/8 : FROM node:latest
 ---> f7756628c1ee
Step 2/8 : MAINTAINER Douglas Quintanilha
 ---> Using cache
 ---> 4e775b15f8d7
Step 3/8 : ENV NODE_ENV=development
 ---> Using cache
 ---> bc2548c79594
Step 4/8 : COPY . /var/www
 ---> Using cache
 ---> 924a18b9ce7b
Step 5/8 : WORKDIR /var/www
 ---> Using cache
 ---> a1252d8f149b
Step 6/8 : RUN npm install
 ---> Using cache
 ---> b2617c0f9387
Step 7/8 : ENTRYPOINT ["npm", "start"]
 ---> Using cache
 ---> a180f5389fc3
Step 8/8 : EXPOSE 3000
 ---> Using cache
 ---> 5dde97f3aef0
Successfully built 5dde97f3aef0
Successfully tagged orbite/alurabooks:latest
Building nginx
Step 1/8 : FROM nginx:latest
latest: Pulling from library/nginx
8ec398bc0356: Pull complete
a53c868fbde7: Pull complete
79daf9dd140d: Pull complete
Digest: sha256:70821e443be75ea38bdf52a974fd2271babd5875b2b1964f05025981c75a6717
Status: Downloaded newer image for nginx:latest
 ---> 5ad3bd0e67a9
Step 2/8 : MAINTAINER Douglas Quintanilha
 ---> Running in 4188268b2bad
Removing intermediate container 4188268b2bad
 ---> 9b7643d64838
Step 3/8 : COPY /public /var/www/public
 ---> 059bf9a43194
Step 4/8 : COPY /docker/config/nginx.conf /etc/nginx/nginx.conf
 ---> e36952bd343d
Step 5/8 : RUN chmod 755 -R /var/www/public
 ---> Running in a88c419265cc
Removing intermediate container a88c419265cc
 ---> 38599d1f7619
Step 6/8 : EXPOSE 80 443
 ---> Running in c8dfa996b016
Removing intermediate container c8dfa996b016
 ---> f87fcc5d6ca4
Step 7/8 : ENTRYPOINT ["nginx"]
 ---> Running in 2f93eafa49df
Removing intermediate container 2f93eafa49df
 ---> 13e0ef4046a1
Step 8/8 : CMD ["-g", "daemon off;"]
 ---> Running in a47be8d2a51e
Removing intermediate container a47be8d2a51e
 ---> bbbb318620f5
Successfully built bbbb318620f5
Successfully tagged orbite/nginx:latest

```
---
* Verificar imagens

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/alura-docker-cap06
└──> $ sudo docker images
REPOSITORY                           TAG                 IMAGE ID            CREATED             SIZE
orbite/nginx                         latest              bbbb318620f5        6 minutes ago       127MB
orbite/alurabooks                    latest              5dde97f3aef0        6 minutes ago       959MB
orbite82/node-teste-1                latest              c90e3bf3eace        42 hours ago        943MB
nginx                                latest              5ad3bd0e67a9        2 days ago          127MB
alpine                               latest              e7d92cdc71fe        6 days ago          5.59MB
mongo                                latest              105a8b77784b        6 days ago          364MB
teste                                latest              96f1e68cc1ea        6 days ago          808MB
ubuntu                               18.04               ccc6e87d482b        8 days ago          64.2MB
ubuntu                               latest              ccc6e87d482b        8 days ago          64.2MB
node                                 latest              f7756628c1ee        2 weeks ago         939MB
ubuntu                               14.04               6e4f1fe62ff1        5 weeks ago         197MB


```
# Resultado do teste do Load Balancer localhost:80

* Resultado do docker comnpose

![docker_compose_up](https://github.com/orbite82/Docker-Orbite/blob/master/docker_compose_up.png)

* Localhost:80 teste

![locahost:80](https://github.com/orbite82/Docker-Orbite/blob/master/localhost:80.png)

* Teste do Load Balancer 

![nginx_node_teste](https://github.com/orbite82/Docker-Orbite/blob/master/nginx_node_teste.png)

* Teste localhost/seed

![teste_BARRA_seed](https://github.com/orbite82/Docker-Orbite/blob/master/teste_BARRA_seed.png)

* Teste localhost/seed 2

![teste_BARRA_seed2](https://github.com/orbite82/Docker-Orbite/blob/master/teste_BARRA_seed2.png)

* Clique em voltar com a seta do navegador e F5

![teste_BARRA_seed3](https://github.com/orbite82/Docker-Orbite/blob/master/teste_BARRA_seed3.png)

# Validar ok

* Após validar a aplicação, ctrl + c

![ctrl_c](https://github.com/orbite82/Docker-Orbite/blob/master/ctrl_c.png)

---

# Docker container -d e liberar o terminal após acompanhar sua aplicação operando

```

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/alura-docker-cap06
└──> $ sudo docker-compose up -d
Starting aluradockercap06_mongodb_1 ... 
Starting aluradockercap06_mongodb_1 ... done
Starting alura-books-2 ... 
Starting alura-books-3 ... 
Starting alura-books-2
Starting alura-books-1 ... 
Starting alura-books-3
Starting alura-books-3 ... done
Starting nginx ... 
Starting nginx ... done

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/alura-docker-cap06
└──> $ sudo docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                         NAMES
cc9ecbfae755        orbite/nginx        "nginx -g 'daemon of…"   21 minutes ago      Up About a minute   0.0.0.0:80->80/tcp, 443/tcp   nginx
89f7a3c98e30        orbite/alurabooks   "npm start"              21 minutes ago      Up About a minute   0.0.0.0:32771->3000/tcp       alura-books-2
0cb2635e4ea7        orbite/alurabooks   "npm start"              21 minutes ago      Up About a minute   0.0.0.0:32773->3000/tcp       alura-books-3
c747cbdb417b        orbite/alurabooks   "npm start"              21 minutes ago      Up About a minute   0.0.0.0:32772->3000/tcp       alura-books-1
3995eb16eb7a        mongo               "docker-entrypoint.s…"   21 minutes ago      Up About a minute   27017/tcp                     aluradockercap06_mongodb_1

```

```

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/alura-docker-cap06
└──> $ sudo docker-compose ps
           Name                        Command             State              Ports           
----------------------------------------------------------------------------------------------
alura-books-1                npm start                     Up      0.0.0.0:32772->3000/tcp    
alura-books-2                npm start                     Up      0.0.0.0:32771->3000/tcp    
alura-books-3                npm start                     Up      0.0.0.0:32773->3000/tcp    
aluradockercap06_mongodb_1   docker-entrypoint.sh mongod   Up      27017/tcp                  
nginx                        nginx -g daemon off;          Up      443/tcp, 0.0.0.0:80->80/tcp

```
# Revomer e parar os container's docker-compose

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/alura-docker-cap06
└──> $ sudo docker-compose down

Stopping nginx                      ... done
Stopping alura-books-2              ... done
Stopping alura-books-3              ... done
Stopping alura-books-1              ... done
Stopping aluradockercap06_mongodb_1 ... done
Removing nginx                      ... done
Removing alura-books-2              ... done
Removing alura-books-3              ... done
Removing alura-books-1              ... done
Removing aluradockercap06_mongodb_1 ... done
Removing network aluradockercap06_production-network

```
---
```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/alura-docker-cap06
└──> $ sudo docker-compose ps
Name   Command   State   Ports
------------------------------

```
# Teste ping entre os container's

* Ping entre nome e node dos container's

```

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/alura-docker-cap06
└──> $ sudo docker-compose up -d
Starting aluradockercap06_mongodb_1 ... 
Starting aluradockercap06_mongodb_1 ... done
Starting alura-books-2 ... 
Starting alura-books-2
Starting alura-books-3 ... 
Starting alura-books-1 ... 
Starting alura-books-3
Starting alura-books-2 ... done
Starting nginx ... 
Starting nginx ... done

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/alura-docker-cap06
└──> $ sudo docker exec -it alura-books-1 ping alura-books-2
PING alura-books-2 (172.19.0.3) 56(84) bytes of data.
64 bytes from alura-books-2.aluradockercap06_production-network (172.19.0.3): icmp_seq=1 ttl=64 time=0.080 ms
64 bytes from alura-books-2.aluradockercap06_production-network (172.19.0.3): icmp_seq=2 ttl=64 time=0.040 ms
64 bytes from alura-books-2.aluradockercap06_production-network (172.19.0.3): icmp_seq=3 ttl=64 time=0.040 ms
64 bytes from alura-books-2.aluradockercap06_production-network (172.19.0.3): icmp_seq=4 ttl=64 time=0.049 ms
64 bytes from alura-books-2.aluradockercap06_production-network (172.19.0.3): icmp_seq=5 ttl=64 time=0.105 ms
^C
--- alura-books-2 ping statistics ---
5 packets transmitted, 5 received, 0% packet loss, time 4085ms
rtt min/avg/max/mdev = 0.040/0.062/0.105/0.027 ms

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/alura-docker-cap06
└──> $ sudo docker exec -it alura-books-1 ping node2
PING node2 (172.19.0.3) 56(84) bytes of data.
64 bytes from alura-books-2.aluradockercap06_production-network (172.19.0.3): icmp_seq=1 ttl=64 time=0.074 ms
64 bytes from alura-books-2.aluradockercap06_production-network (172.19.0.3): icmp_seq=2 ttl=64 time=0.127 ms
64 bytes from alura-books-2.aluradockercap06_production-network (172.19.0.3): icmp_seq=3 ttl=64 time=0.105 ms
64 bytes from alura-books-2.aluradockercap06_production-network (172.19.0.3): icmp_seq=4 ttl=64 time=0.131 ms
^C
--- node2 ping statistics ---
4 packets transmitted, 4 received, 0% packet loss, time 3048ms
rtt min/avg/max/mdev = 0.074/0.109/0.131/0.023 ms

```
