# Pesquisa e Biografia
* `https://cursos.alura.com.br/course/docker-e-docker-compose`
* `https://github.com/gomex/docker-para-desenvolvedores`
* `https://school.linuxtips.io/courses/`

# Docker-Orbite

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

# Executando uma imagem Docker

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker run ubuntu
```
---

# Executando uma imagem Docker e com intereção

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

# Executando um comando dentro da imagem do container e saindo

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker run ubuntu echo "Orbite"

Orbite
```
---

# Executando um comando dentro da imagem do container e interagindo

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker run -it ubuntu

root@2e1f9f6a6c41:/# exit

```
---

# Iniciando uma imagem de um container especifico

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker start 2e1f9f6a6c41

2e1f9f6a6c41

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker ps

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
2e1f9f6a6c41        ubuntu              "/bin/bash"         3 minutes ago       Up 9 seconds                            quizzical_hodgkin

```
---

# Parando uma imagem de um container especifico

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker stop 2e1f9f6a6c41

2e1f9f6a6c41

```
---

# Iniciando uma imagem de um container especifico e imteragindo

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker start -a -i 2e1f9f6a6c41

root@2e1f9f6a6c41:/# exit

```

---

# Removendo imagem de um container baixada em sua máquina

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

# Removendo todas as Imagens de containers baixadas em sua máquina

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

# Listando as imagens baixadas em sua máquina do Docker

```
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
```
---

# Removendo uma imagem Docker baixada em sua máquina

```
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker rmi hello-world

Untagged: hello-world:latest
Untagged: hello-world@sha256:9572f7cdcee8591948c2963463447a53466950b3fc15a247fcad1917ca215a2f
Deleted: sha256:fce289e99eb9bca977dae136fbe2a82b6b7d4c372474c9235adc1741675f587e
Deleted: sha256:af0b15c8625bb1938f1d7b17081031f649fd14e6b233688eea3c5483994a66a3

```
---

# Baixandou uma imagem com o numero e versão da distribuição especifica

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

# Executando umcontainer em BackGround

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

# Adicionando foto e acessando aplicação pela porta

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

# Salvando dados com volumes

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
# Salvando e direcionando os dados, logs e etc... do container na sua pasta local

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

# Rodando o código dentro de um container

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

# Corrigindo o ERR! , informando qual diretório deve ser executado

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

# Alterando a aplicação no quente para i-love-very-docker

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

