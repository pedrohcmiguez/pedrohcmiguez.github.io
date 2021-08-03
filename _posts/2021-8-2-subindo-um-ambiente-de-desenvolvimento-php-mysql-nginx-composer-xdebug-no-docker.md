---
layout: post
title: Subindo um ambiente de desenvolvimento com PHP (Com composer e Xdebug), MYSQL, NGINX no Docker
---

Nos dias de hoje, os desenvolvedores precisam de eficiência para iniciar seus projetos e perder tempo com a criação de ambientes de desenvolvimentos é uma tarefa que vem se tornando mais simples com a utilização de ambientes prontos criados através de containers Docker. Aqui, ensinarei como levantar um ambiente para desenvolvimento em menos de 5 minutos:

## Pre-requisitos:
- [Git](https://pedrohcmiguez.github.io/instalando-o-git-no-ubuntu-20-04/)
- [Docker](https://pedrohcmiguez.github.io/instalando-docker-no-ubuntu-20-04/)
- [Docker-compose](https://pedrohcmiguez.github.io/instalando-o-docker-compose-no-ubuntu-20-04/)

### 1 - Em um local desejado na sua máquina, clone o repositório:
```sh
git clone https://github.com/pedrohcmiguez/docker-dev.git
```

### 2 - Após clonar, entre na pasta:
```sh
cd docker-dev
```

### 3 - Caso deseje, altere as versões do PHP, MYSQL e NGINX:
> Vá até a pasta "docker-dev/etc/" e entre nas respectivas pastas dos softwares e com um editor de texto abra o arquivo dockerfile e altere a linha (Mostratei o NGINX, mas pode ser feito com o PHP e o MYSQL também):
*FROM nginx:1.21*
> Onde tem '1.21' altere para a versão desejada.

### 4 - Basta subir o seu ambiente de desenvolvimento:
```sh
sudo docker-compose up -d
```
*Para rodar em background o parâmetro é o -d*
*Para atualizar as imagens após modificações informe o parâmetro --build no final*

### 5 - Para parar o seu ambiente:
```sh
sudo docker-compose down -v
```