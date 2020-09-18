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
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ curl -fsSL https://get.docker.com | bash
# Executing docker install script, commit: f45d7c11389849ff46a6b4d94e0dd1ffebca32c1
+ sudo -E sh -c 'apt-get update -qq >/dev/null'
+ sudo -E sh -c 'DEBIAN_FRONTEND=noninteractive apt-get install -y -qq apt-transport-https ca-certificates curl >/dev/null'
+ sudo -E sh -c 'curl -fsSL "https://download.docker.com/linux/ubuntu/gpg" | apt-key add -qq - >/dev/null'
Warning: apt-key output should not be parsed (stdout is not a terminal)
+ sudo -E sh -c 'echo "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable" > /etc/apt/sources.list.d/docker.list'
+ sudo -E sh -c 'apt-get update -qq >/dev/null'
+ '[' -n '' ']'
+ sudo -E sh -c 'apt-get install -y -qq --no-install-recommends docker-ce >/dev/null'
+ sudo -E sh -c 'docker version'
Client: Docker Engine - Community
 Version:           19.03.5
 API version:       1.40
 Go version:        go1.12.12
 Git commit:        633a0ea838
 Built:             Wed Nov 13 07:29:52 2019
 OS/Arch:           linux/amd64
 Experimental:      false

Server: Docker Engine - Community
 Engine:
  Version:          19.03.5
  API version:      1.40 (minimum version 1.12)
  Go version:       go1.12.12
  Git commit:       633a0ea838
  Built:            Wed Nov 13 07:28:22 2019
  OS/Arch:          linux/amd64
  Experimental:     false
 containerd:
  Version:          1.2.10
  GitCommit:        b34a5c8af56e510852c35414db4c1f4fa6172339
 runc:
  Version:          1.0.0-rc8+dev
  GitCommit:        3e425f80a8c931f88e6d94a8c831b9d5aa481657
 docker-init:
  Version:          0.18.0
  GitCommit:        fec3683
If you would like to use Docker as a non-root user, you should now consider
adding your user to the "docker" group with something like:

  sudo usermod -aG docker docker-vm

Remember that you will have to log out and back in for this to take effect!

WARNING: Adding a user to the "docker" group will grant the ability to run
         containers which can be used to obtain root privileges on the
         docker host.
         Refer to https://docs.docker.com/engine/security/security/#docker-daemon-attack-surface
         for more information.
docker-vm@Docker-Ubuntu:~$ docker --version
Docker version 19.03.5, build 633a0ea838
```
# Docker Hello World

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container run hello-world

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
$ docker container run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/
```
---

# Comandos Docker em Geral

```

Management Commands:
  builder     Manage builds
  config      Manage Docker configs
  container   Manage containers
  context     Manage contexts
  engine      Manage the docker engine
  image       Manage images
  network     Manage networks
  node        Manage Swarm nodes
  plugin      Manage plugins
  secret      Manage Docker secrets
  service     Manage services
  stack       Manage Docker stacks
  swarm       Manage Swarm
  system      Manage Docker
  trust       Manage trust on Docker images
  volume      Manage volumes

Commands:
  attach      Attach local standard input, output, and error streams to a running container
  build       Build an image from a Dockerfile
  commit      Create a new image from a container's changes
  cp          Copy files/folders between a container and the local filesystem
  create      Create a new container
  diff        Inspect changes to files or directories on a container's filesystem
  events      Get real time events from the server
  exec        Run a command in a running container
  export      Export a container's filesystem as a tar archive
  history     Show the history of an image
  images      List images
  import      Import the contents from a tarball to create a filesystem image
  info        Display system-wide information
  inspect     Return low-level information on Docker objects
  kill        Kill one or more running containers
  load        Load an image from a tar archive or STDIN
  login       Log in to a Docker registry
  logout      Log out from a Docker registry
  logs        Fetch the logs of a container
  pause       Pause all processes within one or more containers
  port        List port mappings or a specific mapping for the container
  ps          List containers
  pull        Pull an image or a repository from a registry
  push        Push an image or a repository to a registry
  rename      Rename a container
  restart     Restart one or more containers
  rm          Remove one or more containers
  rmi         Remove one or more images
  run         Run a command in a new container
  save        Save one or more images to a tar archive (streamed to STDOUT by default)
  search      Search the Docker Hub for images
  start       Start one or more stopped containers
  stats       Display a live stream of container(s) resource usage statistics
  stop        Stop one or more running containers
  tag         Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE
  top         Display the running processes of a container
  unpause     Unpause all processes within one or more containers
  update      Update configuration of one or more containers
  version     Show the Docker version information
  wait        Block until one or more containers stop, then print their exit codes

```
---

# Listar container

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container ps -a


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
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container prune

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

ou
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker image prune -a

```
---

# Executar uma imagem Docker

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container run ubuntu

```
---

# Executar uma imagem Docker e com intereção

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container run -it ubuntu

root@99280a034763:/# exit

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker ps -a

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                      PORTS               NAMES
99280a034763        ubuntu              "/bin/bash"         36 seconds ago      Exited (0) 32 seconds ago                       vigorous_ishizaka
85fbc0514784        ubuntu              "/bin/bash"         46 seconds ago      Exited (0) 45 seconds ago                       quirky_mccarthy
torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker container run -a -it 85fbc0514784

```
---

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container ps

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container ps -a

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                          PORTS               NAMES
cae670ce05d1        ubuntu              "/bin/bash"         21 seconds ago      Exited (0) 19 seconds ago                           awesome_shirley
99280a034763        ubuntu              "/bin/bash"         5 minutes ago       Exited (0) 5 minutes ago                            vigorous_ishizaka
85fbc0514784        ubuntu              "/bin/bash"         5 minutes ago       Exited (0) About a minute ago                       quirky_mccarthy

```
---

# Executar um comando dentro da imagem do container e saindo

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container run ubuntu echo "Orbite"

Orbite
```
---

# Executar um comando dentro da imagem do container e interagindo

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container run -it ubuntu

root@2e1f9f6a6c41:/# exit

```
---

# Iniciar uma imagem de um container especifico

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container start 2e1f9f6a6c41

2e1f9f6a6c41

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container ps

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
2e1f9f6a6c41        ubuntu              "/bin/bash"         3 minutes ago       Up 9 seconds                            quizzical_hodgkin

```
---

# Parar uma imagem de um container especifico

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container container stop 2e1f9f6a6c41

2e1f9f6a6c41

```
---

# Iniciar uma imagem de um container especifico e interagindo

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container start -a -i 2e1f9f6a6c41

root@2e1f9f6a6c41:/# exit

```

---

# Remover a imagem de um container baixada em sua máquina

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container ps -a

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                   PORTS               NAMES
2e1f9f6a6c41        ubuntu              "/bin/bash"         2 hours ago         Exited (0) 2 hours ago                       quizzical_hodgkin
ec50c72afa03        ubuntu              "echo Orbite"       2 hours ago         Exited (0) 2 hours ago                       charming_dewdney
cae670ce05d1        ubuntu              "/bin/bash"         2 hours ago         Exited (0) 2 hours ago                       awesome_shirley
99280a034763        ubuntu              "/bin/bash"         3 hours ago         Exited (0) 3 hours ago                       vigorous_ishizaka
85fbc0514784        ubuntu              "/bin/bash"         3 hours ago         Exited (0) 2 hours ago                       quirky_mccarthy

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ docker conconfig  container  context    

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container rm 2e1f9f6a6c41
2e1f9f6a6c41

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container rm ec5
ec5

```
---

# Remover todas as Imagens de containers baixadas em sua máquina

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container prune

WARNING! This will remove all stopped containers.
Are you sure you want to continue? [y/N] y
Deleted Containers:
cae670ce05d196d4ec16f5255d2011099a0a9f1a5222140abafa4ef7cb87271e
99280a03476364bcf65957133bd7a9b4b8d68e712befcdf85892e1ca5cdf9cff
85fbc0514784732af742d590ba6daac525a670839cbb92283898f1d39d8e14c9

Total reclaimed space: 0B

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

```

---

# Ou Remover

```
┌─[torbite]@[Bio2059]:~/k8s-orbite/Kubernetes-K8S-Orbite
└──> $ sudo docker system prune
WARNING! This will remove:
  - all stopped containers
  - all networks not used by at least one container
  - all dangling images
  - all dangling build cache

Are you sure you want to continue? [y/N] y
Deleted Containers:
17ae0e2066e6ff42f739c3ea576c0033ab3cb09ed43a66dd3ef925d4ad879945
4e8b59d652099d36988b10f908d8b89c7fbd1339d06f11257e3324c900099a8e
292b8298219781e12d3a1f18856fb18981922bc17ba7ee32e0fe606fca850832
a0732d07179874a1f52e3bf9e2bd1165d48d281a5586b97b90d526b599b0c40d
b812578e1edbf51b3adfef4a61b61b220e66b5e8d5c8bb21904dd64b45e50704
a6dfe49e6d652a9dfe7183c8fbf96375b6e135b3223fd7d79e77fa19eb6769b6
93314050bb7f70558838c210667bb27b8cfb155d6eb34a2b3e9ba622b4bf9d4a
ef1d2249f1546f925904b33b7fe56deb6ab437ce6292b1e62561fecb10548bf2
52ae394dda26156d9b87a625c8031a4df23e3a2a27cbe5eaab29e605a39bbaf0
988a6c328ff5a754c5eca1bf35f8231e32f90301bf5600cda7ecbb337b848c52
808ccc357ced5a2f79188f42019e1893ad59b1eb58c5ba1c2d142914bf2f1b3c
e0feb14773b77fddd360bc6864263681a232637539d7324ab4c2aa96df693d37
e918c0b9904b09e2bffd5f37ba833b1614105c18bc3a6f43d824733e5b3b2e3f
330c07e31c1b18f40b5608396beece583819ee0820b635f784003930c1445495
429cb6e23684935b3d01245fae867bfdc01e7d3191fc1d657554e4713d629c82
293a5af4badee96262380e0458c03af751b331a7f3d16a9013f499c2c4b938b0
658c6bb99bcf1b2157092e0e6f4297139446b6f8b191bf13d4805f85f981693c

Deleted Networks:
docker_gwbridge

Total reclaimed space: 3.009kB

```

# Listar as imagens baixadas em sua máquina do Docker

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker images

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
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker rmi hello-world

Untagged: hello-world:latest
Untagged: hello-world@sha256:9572f7cdcee8591948c2963463447a53466950b3fc15a247fcad1917ca215a2f
Deleted: sha256:fce289e99eb9bca977dae136fbe2a82b6b7d4c372474c9235adc1741675f587e
Deleted: sha256:af0b15c8625bb1938f1d7b17081031f649fd14e6b233688eea3c5483994a66a3

```
---

# Baixar uma imagem com o numero e versão da distribuição especifica

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container run ubuntu:18.04

Unable to find image 'ubuntu:18.04' locally
18.04: Pulling from library/ubuntu
Digest: sha256:8d31dad0c58f552e890d68bbfb735588b6b820a46e459672d96e585871acc110
Status: Downloaded newer image for ubuntu:18.04

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container run ubuntu:14.04

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
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container run -d dockersamples/static-site
030609d344a20c796c8564ce54eaa2065ce18713539ad3be50864a6476c3c78f

torbite@BIO-02059:~/Documents/Docker-Orbite$ sudo docker ps
CONTAINER ID        IMAGE                       COMMAND                  CREATED             STATUS              PORTS               NAMES
030609d344a2        dockersamples/static-site   "/bin/sh -c 'cd /usr…"   20 seconds ago      Up 19 seconds       80/tcp, 443/tcp     boring_haslett
d16daa7fb5a3        dockersamples/static-site   "/bin/sh -c 'cd /usr…"   4 minutes ago       Up 4 minutes        80/tcp, 443/tcp     jolly_mendeleev

```
---

# Docker stop formas mais rapida parar

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container container stop 030609d344a2
030609d344a2

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container stop -t 0 d16daa7fb5a3
d16daa7fb5a3

```
---


# Docker com -P para comunicar com container

---
# Antes

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker contaner run -d dockersamples/static-site
f80defd9bf08884eedb7f158feb454fbf25bee6a1bb8202c28d04b76bd52f91a

```
---
# Depois

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container run -d -P dockersamples/static-site
3d798eaeccbc6faf3f42655b175e55106432444d5419b9b9c746d0d0a5226baa


┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container ps
CONTAINER ID        IMAGE                       COMMAND                  CREATED             STATUS              PORTS                                           NAMES
3d798eaeccbc        dockersamples/static-site   "/bin/sh -c 'cd /usr…"   19 seconds ago      Up 18 seconds       0.0.0.0:32769->80/tcp, 0.0.0.0:32768->443/tcp   gifted_joliot
f80defd9bf08        dockersamples/static-site   "/bin/sh -c 'cd /usr…"   53 seconds ago      Up 52 seconds       80/tcp, 443/tcp                                 nifty_margulis

```
---

# Verificar a porta do container

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker port 3d798eaeccbc
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
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container run -d -P --name orbite-container dockersamples/static-site
11bd90a2ca109c249cfaa18f7f46594d50a2a7033c431eb863e904b9d2d73a79

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container ps
CONTAINER ID        IMAGE                       COMMAND                  CREATED             STATUS              PORTS                                           NAMES
11bd90a2ca10        dockersamples/static-site   "/bin/sh -c 'cd /usr…"   9 seconds ago       Up 8 seconds        0.0.0.0:32771->80/tcp, 0.0.0.0:32770->443/tcp   orbite-container

```
---
# Criar uma imagem docker e personalizar

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container container run -it --name criar-imagens-docker ubuntu:18.04 bash
root@20c489bf2ff0:/# apt-get update
root@20c489bf2ff0:/# exit
exit

```
---
# Commit como fazer uma imagem com commit anterior 

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker commit criar-imagens-docker nossoubuntu:nginx
sha256:7d54931606f8e8a571ef85b72a8ea65d84617df6d4c37f09e452ccb2e5ad3858

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker images
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
`Obs:`sudo docker image list Ou sudo docker image list

---

# Testar imgem comitada com nginx nos passos anteriores

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container container run -it --rm nossoubuntu:nginx dpkg -l nginx
Desired=Unknown/Install/Remove/Purge/Hold
| Status=Not/Inst/Conf-files/Unpacked/halF-conf/Half-inst/trig-aWait/Trig-pend
|/ Err?=(none)/Reinst-required (Status,Err: uppercase=bad)
||/ Name           Version      Architecture Description
+++-==============-============-============-=================================
ii  nginx          1.14.0-0ubun all          small, powerful, scalable web/pro

```
`Obs:` Não é a melhor prática fazer desta forma.
---

# Tutorial Parte 1 - Criar, Push e Push Image DockerHub

```
┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker container run -it -d ubuntu
44483e6005fb49341cc7f7b0f9749e7e9a8ce30bc4dceb755588126e4660df0e

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker container ps -a
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
└──> $ sudo docker container stop 44483e6005fb
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
# Tutorial Parte 2 - Removendo e testando as images do DockerHub

```
┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker container ps
CONTAINER ID        IMAGE                      COMMAND             CREATED             STATUS              PORTS               NAMES
795c8ddb9002        orbite82/modified-ubuntu   "bash"              About an hour ago   Up About an hour                        infallible_proskuriakova

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker container stop 795c8ddb9002
795c8ddb9002

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker rm -f  795c8ddb9002
795c8ddb9002

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker container ps -a
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
└──> $ sudo docker container ps -a
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
└──> $ sudo docker container run -it -d orbite82/modified2-ubuntu
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
└──> $ sudo docker container run -it -d orbite82/modified2-ubuntu
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
└──> $ sudo docker container ps -a
CONTAINER ID        IMAGE                       COMMAND             CREATED             STATUS              PORTS               NAMES
6f7d8dcaf3a4        orbite82/modified2-ubuntu   "/bin/bash"         16 seconds ago      Up 15 seconds                           stupefied_spence

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker container ps
CONTAINER ID        IMAGE                       COMMAND             CREATED             STATUS              PORTS               NAMES
6f7d8dcaf3a4        orbite82/modified2-ubuntu   "/bin/bash"         21 seconds ago      Up 20 seconds                           stupefied_spence

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker container exec -it  6f7d8dcaf3a4 bash
root@6f7d8dcaf3a4:/# ls
TEST_DOCKER  bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
root@6f7d8dcaf3a4:/# exit
exit

```
![dockerhub_personalizando_imagens](https://github.com/orbite82/Docker-Orbite/blob/master/dockerhub_personalizando_imagens.png)
---

# Programa para check security via Docker

---

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker ps 
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container run -it --net host --pid host --cap-add audit_control -v /var/lib:/var/lib -v /var/run/docker.sock:/var/run/docker.sock -v /usr/lib/systemd:/usr/lib/systemd -v /etc:/etc --label docker_bench_security docker/docker-bench-security
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
# Volumes Docker - Bind

* `Mount Bind` Apesar de já estarem disponíveis há bastante tempo, o bind mounts são mais limitados que os volumes.

O bind mount realiza a montagem de um arquivo/diretório diretamente do host para o container. Por isso, a montagem é referenciada pelo seu caminho completo no hospedeiro.

Embora seja uma opção com bom desempenho, ela conta com a mesma estrutura do sistema de arquivos (FAT, NTFS, EXT…) do host.

Além do que, algumas questões de segurança devem ser pensadas, já que um container poderá ter acesso a arquivos e diretórios sensíveis na máquina hospedeira.

```
┌─[torbite]@[Bio2059]:~/Docker-Orbite
└──> $ sudo docker container run -d -ti --mount type=bind,src=/home/torbite/volume-bind,dst=/volume-bind ubuntu
2283ce6f3228483944c12f0865d74b9a481811cc9168f6bcfcc6eed1caeaa8c2

┌─[torbite]@[Bio2059]:~/Docker-Orbite
└──> $ sudo docker exec -it 8982bdc28e93 bash
root@8982bdc28e93:/# ls
bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var  volume-bind
root@8982bdc28e93:/# cd volume-bind/
root@8982bdc28e93:/volume-bind# touch teste1
root@8982bdc28e93:/volume-bind# ls
teste1
root@8982bdc28e93:/volume-bind# exit
exit

```

```
┌─[torbite]@[Bio2059]:~/volume-bind
└──> $ ls
teste1

┌─[torbite]@[Bio2059]:~/Docker-Orbite
└──> $ sudo docker exec -it 8982bdc28e93 bash
root@8982bdc28e93:/# df -h
Filesystem      Size  Used Avail Use% Mounted on
overlay         234G   34G  189G  16% /
tmpfs            64M     0   64M   0% /dev
tmpfs           7.8G     0  7.8G   0% /sys/fs/cgroup
shm              64M     0   64M   0% /dev/shm
/dev/sda2       234G   34G  189G  16% /volume-bind
tmpfs           7.8G     0  7.8G   0% /proc/asound
tmpfs           7.8G     0  7.8G   0% /proc/acpi
tmpfs           7.8G     0  7.8G   0% /proc/scsi
tmpfs           7.8G     0  7.8G   0% /sys/firmware

```
---
# Volumes Docker - Volumes
---

* `Volumes` Quando criamos um volume, o Docker armazena os dados em um diretório na sua área gerenciada no host. Assim, quando montarmos ele dentro de algum container, será esse mesmo diretório que montado.

É interessante notar que um volume poderá ser utilizado por vários containers simultaneamente. E, quando nenhum container estiver mais utilizando-o, ele ainda estará disponível para ser montado, pois o Docker não remove os volumes automaticamente.

```
┌─[torbite]@[Bio2059]:~/Docker-Orbite
└──> $ sudo docker volume create tipo-volumes
tipo-volumes
┌─[torbite]@[Bio2059]:~/Docker-Orbite
└──> $ sudo docker inspect tipo-volumes
[
    {
        "CreatedAt": "2020-02-03T12:34:31-03:00",
        "Driver": "local",
        "Labels": {},
        "Mountpoint": "/var/lib/docker/volumes/tipo-volumes/_data",
        "Name": "tipo-volumes",
        "Options": {},
        "Scope": "local"
    }
]

┌─[torbite]@[Bio2059]:~/Docker-Orbite
└──> $ sudo su 
root@Bio2059:/home/torbite/Docker-Orbite# cd /var/lib/docker/volumes/tipo-volumes/
root@Bio2059:/var/lib/docker/volumes/tipo-volumes# ls
_data
root@Bio2059:/var/lib/docker/volumes/tipo-volumes# cd _data/
root@Bio2059:/var/lib/docker/volumes/tipo-volumes/_data# ls
root@Bio2059:/var/lib/docker/volumes/tipo-volumes/_data# touch teste2
root@Bio2059:/var/lib/docker/volumes/tipo-volumes/_data# touch teste3
root@Bio2059:/var/lib/docker/volumes/tipo-volumes/_data# ls
teste2  teste3

```

```
┌─[torbite]@[Bio2059]:~/volume-bind
└──> $ sudo docker ps  
CONTAINER ID        IMAGE                  COMMAND                  CREATED             STATUS              PORTS               NAMES
4137923692e7        ubuntu                 "/bin/bash"              7 seconds ago       Up 5 seconds                            charming_napier

┌─[torbite]@[Bio2059]:~/volume-bind
└──> $ sudo docker exec -it 4137923692e7 bash
root@4137923692e7:/# ls
bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tipo-volumes  tmp  usr  var
root@4137923692e7:/# cd tipo-volumes/
root@4137923692e7:/tipo-volumes# ls
teste2  teste3
root@4137923692e7:/tipo-volumes#

```
---

# Remover volume

`Obs:` Cuidaddo ao remover o volume e verificar se não tem nada de importante salvo.

```
┌─[torbite]@[Bio2059]:~/Docker-Orbite
└──> $ sudo docker volume prune
WARNING! This will remove all local volumes not used by at least one container.
Are you sure you want to continue? [y/N] y
Deleted Volumes:
tipo-volumes

Total reclaimed space: 0B

```
---
* `OU`:

$ docker system prune -a --volumes

# Salvar dados com volumes

```
┌─[torbite]@[BIO-02059]:~
└──> $ docker container run -v "/var/www" ubuntu

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker container ps -a
CONTAINER ID        IMAGE                          COMMAND                  CREATED             STATUS                      PORTS               NAMES
1e48135c289a        ubuntu                         "/bin/bash"              10 minutes ago      Exited (0) 10 minutes ago                       trusting_engelbart

┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker container inspect 1e48135c289a

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
└──> $ sudo docker container run -it -v "/home/torbite/Documents/Docker-Orbite/Docker-Files-Save:/var/www" ubuntu
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
└──> $ sudo docker container run -p 8080:3000 -v "/home/torbite/Documents/Docker-Orbite/Docker-Files-Save/volume-exemplo/:/var/www" node npm start
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
└──> $ sudo docker container run -p 8080:3000 -v "/home/torbite/Documents/Docker-Orbite/Docker-Files-Save/volume-exemplo/:/var/www" -w "/var/www" node npm start

> volume-exemplo@1.0.0 start /var/www
> node .

Server is listening on port 3000
```
# Obs

* Se não passar o parametro -d, seu terminal vai travar, porém a apicação vai rodar e você conseve ver via localhost:8080 o resultado abaixo:

![eu-amo-docker](https://github.com/orbite82/Docker-Orbite/blob/master/eu-amo-docker.png)

```
┌─[torbite]@[BIO-02059]:~
└──> $ sudo docker container run -p 8080:3000 -v  "/home/torbite/Documents/Docker-Orbite/Docker-Files-Save/volume-exemplo/:/var/www" -w "/var/www" -d node npm start
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
└──> $ sudo docker container run -d -p 8080:3000 -v  "/home/torbite/Documents/Docker-Orbite/Docker-Files-Save/volume-exemplo/:/var/www" -w "/var/www" node npm start
954e8831381205addf4f014853e9c47c6e4acaeaa08e4cb336f0ebd45dcefde8

```
---

# Criar um Dockerfile

```
FROM ubuntu

MAINTAINER Thiago Orbite <thiagoorbite@gmail.com>

RUN apt-get update

RUN apt-get install -y nginx && apt-get clean

ADD ./configs/nginx.conf /etc/nginx/sites-enabled/default

RUN ln -sf /dev/stdout /var/log/nginx/access.log

RUN ln -sf /dev/stderr /var/log/nginx/error.log

RUN echo "daemon off;" >> /etc/nginx/nginx.conf

EXPOSE 8080

ENTRYPOINT [“/usr/sbin/nginx”]

CMD [“start”, “-g”]

```
---
* Imagem base
* O parâmetro `FROM` é a imagem que você vai usar como base para a criação de sua nova imagem ou tag específica.

FROM ubuntu
FROM ubuntu:latest

* O parâmetro `MAINTAINER` Mantenedor da imagem
 Empresa ou pessoa que mantem essa imagem atualizada ou personalizada.

MAINTAINER Thiago Orbite <thiagoorbite@gmail.com>

* O parâmetro `RUN` Executando comandos no container
Run executar comandos em um container criado com shell ou executar qualquer comando em uma camada sobre a imagem atual

RUN apt-get update
RUN apt-get install -y nginx && apt-get clean

* O parâmetro `ENTRYPOINT` Permite executar e configurar um container quer será executavel, 
Com esse parâmetro você pode setar se quer que algo seja executado na hora da instanciação do container. 
Então, quando você der um docker run nessa imagem, ela já vai instanciar e executar o programa que está no caminho que você colocar entre colchetes

ENTRYPOINT [“/usr/sbin/nginx”]

* O parâmetro `CMD` O principal objetivo de um CMD é fornecer padrões para um contêiner em execução. Esses padrões podem incluir um executável ou podem omitir o executável. Nesse caso, você também deve especificar uma instrução `ENTRYPOINT`.

CMD service nginx start -g

* O parâmetro `ADD`Adicionando arquivos de configuração no container, para organizar de forma limpa os arquivos de configuração podem ficar em locais semparados

ADD ./configs/nginx.conf /etc/nginx/sites-enabled/defa

* Monitorando os logs do container, `STDOUT` geralmente é a saída normal de um comando e `STDERR` é normalmente usado para gerar mensagens de erro. Por padrão, os logs do docker mostram os comandos `STDOUT` e `STDERR`

RUN ln -sf /dev/stdout /var/log/nginx/access.log
RUN ln -sf /dev/stderr /var/log/nginx/error.log

* O parâmetro `EXPOSE``Expondo portas do container

EXPOSE 8080

---

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/Docker-Files-Save/nginx-dockerfile
└──> $ sudo docker image build -t nginxdockerfile:1.0 .
Sending build context to Docker daemon  3.584kB
Step 1/11 : FROM ubuntu
 ---> ccc6e87d482b
Step 2/11 : MAINTAINER Thiago Orbite <thiagoorbite@gmail.com>
 ---> Using cache
 ---> 450ce053b104
Step 3/11 : RUN apt-get update -y
 ---> Using cache
 ---> b726b976e5b0
Step 4/11 : RUN apt-get install -y nginx && apt-get clean
 ---> Using cache
 ---> 8fd64a90bc30
Step 5/11 : ADD .configs/nginx.conf /etc/nginx/sites-enabled/default
 ---> Using cache
 ---> 887445035750
Step 6/11 : RUN ln -sf /dev/stdout /var/log/nginx/access.log
 ---> Running in f158b2c7414a
Removing intermediate container f158b2c7414a
 ---> bb0007d6ae04
Step 7/11 : RUN ln -sf /dev/stderr /var/log/nginx/error.log
 ---> Running in 1b570046b185
Removing intermediate container 1b570046b185
 ---> e408636b45dd
Step 8/11 : RUN echo "daemon off;" >> /etc/nginx/nginx.conf
 ---> Running in f83d6b682a1c
Removing intermediate container f83d6b682a1c
 ---> 76e551341680
Step 9/11 : EXPOSE 8080
 ---> Running in 732f4928614c
Removing intermediate container 732f4928614c
 ---> 1b7aa0bd214d
Step 10/11 : ENTRYPOINT [“/usr/sbin/nginx”]
 ---> Running in 65fcc7cb5042
Removing intermediate container 65fcc7cb5042
 ---> efdbcd57d1bb
Step 11/11 : CMD [“start”, “-g”]
 ---> Running in b288c53f473f
Removing intermediate container b288c53f473f
 ---> f1f045a9b7fb
Successfully built f1f045a9b7fb
Successfully tagged nginxdockerfile:1.0
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/Docker-Files-Save/nginx-dockerfile
└──> $ sudo docker image ls
REPOSITORY                  TAG                 IMAGE ID            CREATED             SIZE
nginxdockerfile             1.0                 f1f045a9b7fb        19 seconds ago      152MB

```

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/Docker-Files-Save/nginx-dockerfile
└──> $ ls -lha
total 16K
drwxrwxr-x 3 torbite torbite 4,0K jan 28 10:43 .
drwxrwxr-x 5 torbite torbite 4,0K jan 28 11:21 ..
drwxrwxr-x 2 torbite torbite 4,0K jan 28 10:38 .configs
-rw-rw-r-- 1 torbite torbite  417 jan 28 10:43 Dockerfile

```

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/Docker-Files-Save/nginx-dockerfile/.configs
└──> $ ls
nginx.conf

```

---

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
└──> $ sudo docker container run -d -p 8080:3000 orbite82/node-teste-1
6e489adc0f1394886e742a76833cff286244ccc0dbbd225cc5d44f76bc7f1953

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite/Docker-Files-Save/volume-exemplo
└──> $ sudo docker container ps
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
└──> $ sudo docker container run -it --name meu-container --network minha-rede alpine 
/ # hostname -i
172.23.0.2

```

```

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
a89a30980dac        alpine              "/bin/sh"           48 seconds ago      Up 47 seconds                           meu-container
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container inspect meu-container
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
└──> $ sudo docker container run --name meu-container1 -it -d --network minha-rede alpine
e29077d4d11106ea7bfd784ddcb9a606b86afdd5de1bcde406d730b118699464

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container run --name meu-container2 -it -d --network minha-rede alpine
f3875faf450c6c3bfeeab6e1ec7fb2bab184ef61d51662bd01be0b7a3d1500ab

```

# Rede já foi atrelada

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container ps
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
└──> $ sudo docker container run -d -p 8080:3000 douglasq/alura-books:cap05
4b1e63035803ca9218e87cd307f45901c4b170e3d88f9530d70831b4795d6e7f

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container ps
CONTAINER ID        IMAGE                        COMMAND             CREATED             STATUS              PORTS                    NAMES
4b1e63035803        douglasq/alura-books:cap05   "npm start"         10 seconds ago      Up 10 seconds       0.0.0.0:8080->3000/tcp   condescending_poitras  
```
---

![aplicacao-livro](https://github.com/orbite82/Docker-Orbite/blob/master/aplicacao-livros.png)

---

* Após teste remover o container e seguir o procedimento de subir o banco mongo

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container ps

CONTAINER ID        IMAGE                        COMMAND             CREATED             STATUS              PORTS                    NAMES
4b1e63035803        douglasq/alura-books:cap05   "npm start"         30 minutes ago      Up 30 minutes       0.0.0.0:8080->3000/tcp   condescending_poitras
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container rm -f 4b1e63035803

4b1e63035803
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker network ls
NETWORK ID          NAME                DRIVER              SCOPE
158f5528ea4d        bridge              bridge              local
0643e57cda2b        host                host                local
c6633dd8eac4        minha-rede          bridge              local
7aa972bae58a        none                null                local

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container run -d --name meu-mongo --network minha-rede mongo

```
* Na sequencia subir a aplicação e validar

```
┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container run --network minha-rede -d -p 8080:3000 douglasq/alura-books:cap05
6eed50b4b9434388819a015c0483a26557357814cdef74a93653e86cceffea17

┌─[torbite]@[BIO-02059]:~/Documents/Docker-Orbite
└──> $ sudo docker container ps
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
└──> $ sudo docker container ps
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
└──> $ sudo docker container exec -it alura-books-1 ping alura-books-2
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
└──> $ sudo docker container exec -it alura-books-1 ping node2
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

---

# Docker Swarm

* Se não conseguir subir em VM ou na sua propria máquinas por motivos de desempenho pode usar o site abaixo para montar um cluster totalmente gratuito por 4 horas usando sua conta do docker hub: -->

https://labs.play-with-docker.com/

```
┌─[torbite]@[Bio2059]:~
└──> $ sudo docker swarm --help

Usage:	docker swarm COMMAND

Manage Swarm

Commands:
  ca          Display and rotate the root CA
  init        Initialize a swarm
  join        Join a swarm as a node and/or manager
  join-token  Manage join tokens
  leave       Leave the swarm
  unlock      Unlock swarm
  unlock-key  Manage the unlock key
  update      Update the swarm

Run 'docker swarm COMMAND --help' for more information on a command.

```
`Obs:` Se ocorrer o erro abaixo no docker swarm init seguir desta forma, pois você precisa passar qual rede ele vai usar:

```
┌─[torbite]@[Bio2059]:~
└──> $ sudo docker swarm init
Error response from daemon: could not choose an IP address to advertise since this system has multiple addresses on different interfaces (192.168.4.121 on wlp2s0 and 172.16.1.1 on vboxnet0) - specify one with --advertise-addr

┌─[torbite]@[Bio2059]:~
└──> $ sudo ip add
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host 
       valid_lft forever preferred_lft forever
2: enp1s0: <NO-CARRIER,BROADCAST,MULTICAST,UP> mtu 1500 qdisc fq_codel state DOWN group default qlen 1000
    link/ether 88:6f:d4:fe:b7:e0 brd ff:ff:ff:ff:ff:ff
3: wlp2s0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc noqueue state UP group default qlen 1000
    link/ether c0:b5:d7:ed:ee:6b brd ff:ff:ff:ff:ff:ff
    inet 192.168.4.121/23 brd 192.168.5.255 scope global dynamic noprefixroute wlp2s0
       valid_lft 254633sec preferred_lft 254633sec
    inet6 fe80::64b6:db33:e3d5:d0ed/64 scope link noprefixroute 
       valid_lft forever preferred_lft forever
4: docker0: <NO-CARRIER,BROADCAST,MULTICAST,UP> mtu 1500 qdisc noqueue state DOWN group default 
    link/ether 02:42:dd:7f:38:32 brd ff:ff:ff:ff:ff:ff
    inet 172.17.0.1/16 brd 172.17.255.255 scope global docker0
       valid_lft forever preferred_lft forever
    inet6 fe80::42:ddff:fe7f:3832/64 scope link 
       valid_lft forever preferred_lft forever
5: vboxnet0: <NO-CARRIER,BROADCAST,MULTICAST,UP> mtu 1500 qdisc fq_codel state DOWN group default qlen 1000
    link/ether 0a:00:27:00:00:00 brd ff:ff:ff:ff:ff:ff
    inet 172.16.1.1/24 brd 172.16.1.255 scope global vboxnet0
       valid_lft forever preferred_lft forever
    inet6 fe80::800:27ff:fe00:0/64 scope link 
       valid_lft forever preferred_lft forever
┌─[torbite]@[Bio2059]:~
└──> $ docker swarm init --advertise-addr 192.168.4.121
Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Post http://%2Fvar%2Frun%2Fdocker.sock/v1.40/swarm/init: dial unix /var/run/docker.sock: connect: permission denied
┌─[torbite]@[Bio2059]:~
└──> $ sudo docker swarm init --advertise-addr 192.168.4.121
Swarm initialized: current node (7m7gmyff2qxwlp78p11kegs5j) is now a manager.

To add a worker to this swarm, run the following command:

    docker swarm join --token SWMTKN-1-314a8iatk7kly2wjjgxiw5iwi5lzmx76m7fegc2gvxc10ptq35-29c6f1oyramh8se1nh3eflh8r 192.168.4.121:2377

To add a manager to this swarm, run 'docker swarm join-token manager' and follow the instructions.

┌─[torbite]@[Bio2059]:~
└──> $ sudo docker node ls
ID                            HOSTNAME            STATUS              AVAILABILITY        MANAGER STATUS      ENGINE VERSION
7m7gmyff2qxwlp78p11kegs5j *   Bio2059             Ready               Active              Leader              19.03.5

```

* Para adicionar novas máquinas ao cluster apenas executar em cada uma delas este comando:


`Obs:` As máquinas deve ter o docker instalado : > $ curl -fsSL https://get.docker.com | bash

```
docker swarm join --token SWMTKN-1-314a8iatk7kly2wjjgxiw5iwi5lzmx76m7fegc2gvxc10ptq35-29c6f1oyramh8se1nh3eflh8r 192.168.4.121:2377

```
node master:

```

[node1] (local) root@192.168.0.13 ~
$ docker node ls
ID                            HOSTNAME            STATUS              AVAILABILITY        MANAGER STATUS      ENGINE VERSION
iuka4rgfk7832ht4bfwyp1ore *   node1               Ready               Active              Leader              19.03.4
i8y2g32izmwbdgctxa6nt7mvr     node2               Ready               Active                                  19.03.4
lrgndnyumgy1fvl8h1yil2346     node3               Ready               Active                                  19.03.4

```

node 2:

```
[node2] (local) root@192.168.0.12 ~
$ docker swarm join --token SWMTKN-1-24d2id2wqu1znyji3z4vuikr65ztc60ysxtvhhwdt106c3a8mq-1fdwc6ornqjjgyrb1ctw69mam 192.168.0.13:2377
This node joined a swarm as a worker.

```

node 3:

```
[node3] (local) root@192.168.0.11 ~
$ docker swarm join --token SWMTKN-1-24d2id2wqu1znyji3z4vuikr65ztc60ysxtvhhwdt106c3a8mq-1fdwc6ornqjjgyrb1ctw69mam 192.168.0.13:2377
This node joined a swarm as a worker.

```

```
[node1] (local) root@192.168.0.13 ~
$ docker node promote node2
Node node2 promoted to a manager in the swarm.
[node1] (local) root@192.168.0.13 ~
$ docker node promote node3
Node node3 promoted to a manager in the swarm.
[node1] (local) root@192.168.0.13 ~
$ docker node ls
ID                            HOSTNAME            STATUS              AVAILABILITY        MANAGER STATUS      ENGINE VERSION
iuka4rgfk7832ht4bfwyp1ore *   node1               Ready               Active              Leader              19.03.4
i8y2g32izmwbdgctxa6nt7mvr     node2               Ready               Active              Reachable           19.03.4
lrgndnyumgy1fvl8h1yil2346     node3               Ready               Active              Reachable           19.03.4

```

```
[node1] (local) root@192.168.0.13 ~
$ docker swarm join-token worker
To add a worker to this swarm, run the following command:

    docker swarm join --token SWMTKN-1-24d2id2wqu1znyji3z4vuikr65ztc60ysxtvhhwdt106c3a8mq-1fdwc6ornqjjgyrb1ctw69mam 192.168.0.13:2377

```

```
[node1] (local) root@192.168.0.13 ~
$ docker swarm join-token manager
To add a manager to this swarm, run the following command:

    docker swarm join --token SWMTKN-1-24d2id2wqu1znyji3z4vuikr65ztc60ysxtvhhwdt106c3a8mq-77gocg3pnesc2hph1o2iwsygs 192.168.0.13:2377

```

# Criando uma Secret no docker swarm

```
[node1] (local) root@192.168.0.18 ~
$ docker node ls
ID                            HOSTNAME            STATUS              AVAILABILITY        MANAGER STATUS      ENGINE VERSION
rm165loiupn01usqbh0pr7kfp *   node1               Ready               Active              Leader              19.03.4
urlzua3k9q6sqb77m0wn6e4nb     node2               Ready               Active              Reachable           19.03.4
vleygl31te4wqs1i91lghg2sx     node3               Ready               Active              Reachable           19.03.4

[node1] (local) root@192.168.0.18 ~
$ echo "ConteudoDoSecret" | docker secret create um-secret -
r9umne27crwnzb98i9b2mdqu6

```

* Listando secret

```
[node1] (local) root@192.168.0.18 ~
$ docker secret ls
ID                          NAME                DRIVER              CREATED             UPDATED
r9umne27crwnzb98i9b2mdqu6   um-secret                               5 minutes ago       5 minutes ago

```
* Executando inspect

```
[node1] (local) root@192.168.0.18 ~
$ docker secret inspect um-secret
[
    {
        "ID": "r9umne27crwnzb98i9b2mdqu6",
        "Version": {
            "Index": 31
        },
        "CreatedAt": "2020-02-07T17:39:56.723200135Z",
        "UpdatedAt": "2020-02-07T17:39:56.723200135Z",
        "Spec": {
            "Name": "um-secret",
            "Labels": {}
        }
    }
]

```
* Como passar e usar uma secret

```
[node1] (local) root@192.168.0.18 ~
$ docker service create --name nginx -p 8080:80 --secret um-secret nginx
0trwg612mlyjdhdsyhfggkvg7
overall progress: 1 out of 1 tasks 
1/1: running   [==================================================>] 
verify: Service converged 

[node1] (local) root@192.168.0.18 ~
$ docker service ls
ID                  NAME                MODE                REPLICAS            IMAGE               PORTS
0trwg612mlyj        nginx               replicated          1/1                 nginx:latest        *:8080->80/tcp

```

* Localizar e visulizar a sua secret

```
[node1] (local) root@192.168.0.18 ~
$ docker service inspect nginx
[
    {
        "ID": "0trwg612mlyjdhdsyhfggkvg7",
        "Version": {
            "Index": 34
        },
        "CreatedAt": "2020-02-07T17:51:42.205162724Z",
        "UpdatedAt": "2020-02-07T17:51:42.210122782Z",
        "Spec": {
            "Name": "nginx",
            "Labels": {},
            "TaskTemplate": {
                "ContainerSpec": {
                    "Image": "nginx:latest@sha256:ad5552c786f128e389a0263104ae39f3d3c7895579d45ae716f528185b36bc6f",
                    "Init": false,
                    "StopGracePeriod": 10000000000,
                    "DNSConfig": {},
                    "Secrets": [
                        {
                            "File": {
                                "Name": "um-secret",
                                "UID": "0",
                                "GID": "0",
                                "Mode": 292
                            },
                            "SecretID": "r9umne27crwnzb98i9b2mdqu6",
                            "SecretName": "um-secret"
                        }
                    ],
                    "Isolation": "default"
                },
                "Resources": {
                    "Limits": {},
                    "Reservations": {}
                },
                "RestartPolicy": {
                    "Condition": "any",
                    "Delay": 5000000000,
                    "MaxAttempts": 0
                },
                "Placement": {
                    "Platforms": [
                        {
                            "Architecture": "amd64",
                            "OS": "linux"
                        },
                        {
                            "OS": "linux"
                        },
                        {
                            "Architecture": "arm64",
                            "OS": "linux"
                        },
                        {
                            "Architecture": "386",
                            "OS": "linux"
                        },
                        {
                            "Architecture": "ppc64le",
                            "OS": "linux"
                        },
                        {
                            "Architecture": "s390x",
                            "OS": "linux"
                        }
                    ]
                },
                "ForceUpdate": 0,
                "Runtime": "container"
            },
            "Mode": {
                "Replicated": {
                    "Replicas": 1
                }
            },
            "UpdateConfig": {
                "Parallelism": 1,
                "FailureAction": "pause",
                "Monitor": 5000000000,
                "MaxFailureRatio": 0,
                "Order": "stop-first"
            },
            "RollbackConfig": {
                "Parallelism": 1,
                "FailureAction": "pause",
                "Monitor": 5000000000,
                "MaxFailureRatio": 0,
                "Order": "stop-first"
            },
            "EndpointSpec": {
                "Mode": "vip",
                "Ports": [
                    {
                        "Protocol": "tcp",
                        "TargetPort": 80,
                        "PublishedPort": 8080,
                        "PublishMode": "ingress"
                    }
                ]
            }
        },
        "Endpoint": {
            "Spec": {
                "Mode": "vip",
                "Ports": [
                    {
                        "Protocol": "tcp",
                        "TargetPort": 80,
                        "PublishedPort": 8080,
                        "PublishMode": "ingress"
                    }
                ]
            },
            "Ports": [
                {
                    "Protocol": "tcp",
                    "TargetPort": 80,
                    "PublishedPort": 8080,
                    "PublishMode": "ingress"
                }
            ],
            "VirtualIPs": [
                {
                    "NetworkID": "il4gwa4cpyos297c3pcu9zxyi",
                    "Addr": "10.255.0.5/16"
                }
            ]
        }
    }
]

```
* Usando o scale para verificar minha secret dentro do cluster do swarm

```
[node1] (local) root@192.168.0.18 ~
$ docker service scale nginx=10
nginx scaled to 10
overall progress: 10 out of 10 tasks 
1/10: running   [==================================================>] 
2/10: running   [==================================================>] 
3/10: running   [==================================================>] 
4/10: running   [==================================================>] 
5/10: running   [==================================================>] 
6/10: running   [==================================================>] 
7/10: running   [==================================================>] 
8/10: running   [==================================================>] 
9/10: running   [==================================================>] 
10/10: running   [==================================================>] 
verify: Service converged 
[node1] (local) root@192.168.0.18 ~
$ docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS               NAMES
1a87d6e61fd9        nginx:latest        "nginx -g 'daemon of…"   12 seconds ago      Up 10 seconds       80/tcp              nginx.4.0n3cda8ha36vhg24uiv1j9yqf
11c6eb36bb44        nginx:latest        "nginx -g 'daemon of…"   12 seconds ago      Up 10 seconds       80/tcp              nginx.9.sjm8c2clum6eekgimsakvhnod
0abae48be931        nginx:latest        "nginx -g 'daemon of…"   12 seconds ago      Up 10 seconds       80/tcp              nginx.2.pw8a6t0elpqxuyb0ca6x237m1
d09eefca9295        nginx:latest        "nginx -g 'daemon of…"   12 seconds ago      Up 10 seconds       80/tcp              nginx.8.q8ca1obpvqxcfa9yf49hkoglq

```

* Entrar no container para certificar que a secret está dentro dos container's

```
[node1] (local) root@192.168.0.18 ~
$ docker exec -it 1a87d6e61fd9 bash
root@1a87d6e61fd9:/# ls
bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
root@1a87d6e61fd9:/# ls  -lha
total 8.0K
drwxr-xr-x   1 root root   28 Feb  7 18:01 .
drwxr-xr-x   1 root root   28 Feb  7 18:01 ..
-rwxr-xr-x   1 root root    0 Feb  7 18:01 .dockerenv
drwxr-xr-x   2 root root 4.0K Jan 30 00:00 bin
drwxr-xr-x   2 root root    6 Nov 10 12:17 boot
drwxr-xr-x   5 root root  340 Feb  7 18:01 dev
drwxr-xr-x   1 root root   66 Feb  7 18:01 etc
drwxr-xr-x   2 root root    6 Nov 10 12:17 home
drwxr-xr-x   1 root root   56 Feb  2 08:06 lib
drwxr-xr-x   2 root root   34 Jan 30 00:00 lib64
drwxr-xr-x   2 root root    6 Jan 30 00:00 media
drwxr-xr-x   2 root root    6 Jan 30 00:00 mnt
drwxr-xr-x   2 root root    6 Jan 30 00:00 opt
dr-xr-xr-x 672 root root    0 Feb  7 18:01 proc
drwx------   2 root root   37 Jan 30 00:00 root
drwxr-xr-x   1 root root   38 Feb  7 18:01 run
drwxr-xr-x   2 root root 4.0K Jan 30 00:00 sbin
drwxr-xr-x   2 root root    6 Jan 30 00:00 srv
dr-xr-xr-x  13 root root    0 Jan 31 18:20 sys
drwxrwxrwt   1 root root    6 Feb  2 08:06 tmp
drwxr-xr-x   1 root root   66 Jan 30 00:00 usr
drwxr-xr-x   1 root root   19 Jan 30 00:00 var
root@1a87d6e61fd9:/# cd /run/
root@1a87d6e61fd9:/run# ls
lock  nginx.pid  secrets  utmp
root@1a87d6e61fd9:/run# cd secrets/
root@1a87d6e61fd9:/run/secrets# ls
um-secret

root@1a87d6e61fd9:/run/secrets# cat um-secret 
ConteudoDoSecret

```

`Obs:` Aqui temos certeza que é uma `secret` e não uma `variavel`

```
root@1a87d6e61fd9:/run/secrets# set
BASH=/bin/bash
BASHOPTS=checkwinsize:cmdhist:complete_fullquote:expand_aliases:extquote:force_fignore:globasciiranges:hostcomplete:interactive_comments:progcomp:promptvars:sourcepath
BASH_ALIASES=()
BASH_ARGC=([0]="0")
BASH_ARGV=()
BASH_CMDS=()
BASH_LINENO=()
BASH_SOURCE=()
BASH_VERSINFO=([0]="5" [1]="0" [2]="3" [3]="1" [4]="release" [5]="x86_64-pc-linux-gnu")
BASH_VERSION='5.0.3(1)-release'
COLUMNS=163
DIRSTACK=()
EUID=0
GROUPS=()
HISTFILE=/root/.bash_history
HISTFILESIZE=500
HISTSIZE=500
HOME=/root
HOSTNAME=1a87d6e61fd9
HOSTTYPE=x86_64
IFS=$' \t\n'
LINES=38
MACHTYPE=x86_64-pc-linux-gnu
MAILCHECK=60
NGINX_VERSION=1.17.8
NJS_VERSION=0.3.8
OLDPWD=/run
OPTERR=1
OPTIND=1
OSTYPE=linux-gnu
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
PIPESTATUS=([0]="0")
PKG_RELEASE=1~buster
PPID=0
PS1='${debian_chroot:+($debian_chroot)}\u@\h:\w\$ '
PS2='> '
PS4='+ '
PWD=/run/secrets
SHELL=/bin/bash
SHELLOPTS=braceexpand:emacs:hashall:histexpand:history:interactive-comments:monitor
SHLVL=1
TERM=xterm
UID=0
_=um-secret

```
