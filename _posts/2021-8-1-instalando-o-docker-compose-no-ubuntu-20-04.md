---
layout: post
title: Instalando o Docker-compose no Ubuntu 20.04
---

O Docker é uma apliação bastante útil para os desenvolvedores nos dias de hoje o que torna bastante rápido o processo de criação de um ambiente de desenvolvimento. Porém, subir diversas imagens do docker pode ser uma tarefa cuja gestão não seja tão trivial. Dessa forma, o Docker-compose chega para cumprir essa missão, tornando mais simples o ato de gerir essas imagens. Abaixo irei mostrar como instalaremos o Docker-compose em uma máquina Linux. (Ubuntu 20.04 - Focal Fossa):

### 1 - Atualize o seu sistema:

```bash
sudo apt update && sudo apt upgrade
```

### 2 - Verifique a última versão do docker-compose em seu repositório oficial no github:

>https://github.com/docker/compose/releases

### 3 - Instale a versão desejada com o comando abaixo (utilizamos a versão 1.26.0):

```bash
sudo curl -L "https://github.com/docker/compose/releases/download/1.26.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
### 4 - Dê permissão de escrita para o docker-compose:

```bash
sudo chmod +x /usr/local/bin/docker-compose
```

### 5 - Verifique se tudo deu certo com o comando:

```bash
docker-compose --version
```
*Se tudo deu certo a saída será mais ou menos assim:*

>Output
>docker-compose version 1.26.0, build 8a1c60f6

**Pronto! Agora você possui o Docker-compose instalado e com um arquivo**  _docker-compose.yml_ **configurado você pode subir as imagens com o comando: docker-compose up -d e parar com docker-compose down -v**.