---
layout: post
title: O que fazer após instalar o Ubuntu 20.04
---
O Ubuntu 20.04 LTS "Focal Fossa", com suporte até abril de 2025, foi lançado em 23 de abril de 2020. Irei listar abaixo algumas sugestões para melhorar o seu recém instalado sistema.

![Focal Fossa]({{ site.baseurl }}/images/focal.png)

### 1 - Atualizar o sistema:

```bash
sudo apt update -y
sudo apt upgrade -y
sudo apt dist-upgrade -y
```
### 2 - Instalar Codecs de mídia proprietários:

```bash
sudo apt install ubuntu-restricted-extras
```

### 3 - Limpando o sistema:

```bash
sudo apt autoremove
```
