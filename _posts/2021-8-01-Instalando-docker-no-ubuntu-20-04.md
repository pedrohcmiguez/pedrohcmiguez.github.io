---
layout: post
title: Instalando o Docker no Ubuntu 20.04
---

O Docker é uma ferramenta para simplificar a gestão de aplicações, permitindo o isolamento por contâiners dos softwares que serão executados da máquina de quem os executa. Abaixo vou citar alguns passos para que você tenha o Docker Community Edition instalado no seu Ubuntu 20.04.

### 1 - Atualize o seu sistema:

```bash
sudo apt update && sudo apt upgrade
```

### 2 - Instale os softwares pré-requisitos:

```bash
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```

### 3 - Instale a chave GPG para o repositório oficial do Docker:

```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

### 4 - Adicione o repositório do Docker:

```bash
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
```

### 5 - Atualize novamente para que você possa instalar o pacote do Docker:

```bash
sudo apt update
```

### 6 - Tenha certeza de que o pacote a ser instalado é o do repositório do Docker:

```bash
apt-cache policy docker-ce
```

*A saída será mais ou menos assim:*

> docker-ce:
  Installed: (none)
  Candidate: 5:19.03.9~3-0~ubuntu-focal
  Version table:
     5:19.03.9~3-0~ubuntu-focal 500
        500 https://download.docker.com/linux/ubuntu focal/stable amd64 Packages

### 7 - Instale o pacote de fato:

```bash
sudo apt install docker-ce
```

### 8 - Verifique se o docker está ativo:

sudo systemctl status docker

*A saída será mais ou menos assim:*

>● docker.service - Docker Application Container Engine
     Loaded: loaded (/lib/systemd/system/docker.service; enabled; vendor preset>
     Active: active (running) since Sun 2021-08-01 13:09:24 -03; 7h ago
TriggeredBy: ● docker.socket
       Docs: https://docs.docker.com
   Main PID: 9452 (dockerd)
      Tasks: 58
     Memory: 1.2G
     CGroup: /system.slice/docker.service

**Se tudo ocorreu bem, você está com o Docker instalado na sua máquina!**