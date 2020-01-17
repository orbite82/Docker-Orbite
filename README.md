# Docker-Orbite

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker run hello-world

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

# Listar container

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker ps -a


CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                      PORTS               NAMES
24136025fa87        hello-world         "/hello"            10 seconds ago      Exited (0) 9 seconds ago                        festive_bardeen
04bd5c7ce1a6        hello-world         "/hello"            11 seconds ago      Exited (0) 10 seconds ago                       nostalgic_jennings
b67351a66eba        hello-world         "/hello"            12 seconds ago      Exited (0) 11 seconds ago                       intelligent_wing
73a7be80bc76        hello-world         "/hello"            14 seconds ago      Exited (0) 12 seconds ago                       admiring_easley
fea647289d44        hello-world         "/hello"            15 seconds ago      Exited (0) 14 seconds ago                       nervous_lamarr
683fc3478eb0        hello-world         "/hello"            17 seconds ago      Exited (0) 16 seconds ago                       cool_ride

# Remover todas as imagens baixadas Docker

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

-----

# Executando uma imagem Docker

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker run ubuntu

# Executando uma imagem Docker e com intereção

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker run -it ubuntu

root@99280a034763:/# exit

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker ps -a

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                      PORTS               NAMES
99280a034763        ubuntu              "/bin/bash"         36 seconds ago      Exited (0) 32 seconds ago                       vigorous_ishizaka
85fbc0514784        ubuntu              "/bin/bash"         46 seconds ago      Exited (0) 45 seconds ago                       quirky_mccarthy
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker container run -a -it 85fbc0514784

----

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker ps

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker ps -a

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                          PORTS               NAMES
cae670ce05d1        ubuntu              "/bin/bash"         21 seconds ago      Exited (0) 19 seconds ago                           awesome_shirley
99280a034763        ubuntu              "/bin/bash"         5 minutes ago       Exited (0) 5 minutes ago                            vigorous_ishizaka
85fbc0514784        ubuntu              "/bin/bash"         5 minutes ago       Exited (0) About a minute ago                       quirky_mccarthy

# Executando um comando dentro da imagem do container e saindo

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker run ubuntu echo "Orbite"

Orbite


----
# Executando um comando dentro da imagem do container e interagindo

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker run -it ubuntu

root@2e1f9f6a6c41:/# exit

----
# Iniciando uma imagem de um container especifico

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker start 2e1f9f6a6c41

2e1f9f6a6c41

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker ps

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
2e1f9f6a6c41        ubuntu              "/bin/bash"         3 minutes ago       Up 9 seconds                            quizzical_hodgkin

# Parando uma imagem de um container especifico

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker stop 2e1f9f6a6c41

2e1f9f6a6c41

# Iniciando uma imagem de um container especifico e imteragindo

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker start -a -i 2e1f9f6a6c41

root@2e1f9f6a6c41:/# exit


----

# Removendo imagem de um container baixada em sua máquina

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

# Removendo todas as Imagens de containers baixadas em sua máquina

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

---

# Listando as imagens baixadas em sua máquina do Docker

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker images

REPOSITORY                           TAG                 IMAGE ID            CREATED             SIZE
ubuntu                               latest              ccc6e87d482b        40 hours ago        64.2MB
k8s.gcr.io/kube-proxy                v1.17.0             7d54289267dc        5 weeks ago         116MB
k8s.gcr.io/kube-apiserver            v1.17.0             0cae8d5cc64c        5 weeks ago         171MB
k8s.gcr.io/kube-scheduler            v1.17.0             78c190f736b1        5 weeks ago         94.4MB
k8s.gcr.io/kube-controller-manager   v1.17.0             5eb3b7486872        5 weeks ago         161MB
gcr.io/kubernetes-helm/tiller        v2.16.1             1f92aa902d73        2 months ago        91.2MB
weaveworks/weave-npc                 2.6.0               5105e13e253e        2 months ago        34.9MB
weaveworks/weave-kube                2.6.0               174e0e8ef23d        2 months ago        114MB
k8s.gcr.io/coredns                   1.6.5               70f311871ae1        2 months ago        41.6MB
k8s.gcr.io/etcd                      3.4.3-0             303ce5db0e90        2 months ago        288MB
hello-world                          latest              fce289e99eb9        12 months ago       1.84kB
k8s.gcr.io/pause                     3.1                 da86e6ba6ca1        2 years ago         742kB

# Removendo uma imagem Docker baixada em sua máquina

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker rmi hello-world

Untagged: hello-world:latest
Untagged: hello-world@sha256:9572f7cdcee8591948c2963463447a53466950b3fc15a247fcad1917ca215a2f
Deleted: sha256:fce289e99eb9bca977dae136fbe2a82b6b7d4c372474c9235adc1741675f587e
Deleted: sha256:af0b15c8625bb1938f1d7b17081031f649fd14e6b233688eea3c5483994a66a3

---

# Baixandou uma imagem com o numero e versão da distribuição especifica

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



