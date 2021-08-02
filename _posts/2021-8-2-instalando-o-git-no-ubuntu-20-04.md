---
layout: post
title: Instalando o Git no Ubuntu 20.04
---

O Git é uma ferramenta de versionamento essencial para qualquer desenvolvedor nos dias de hoje, seja um desenvolvedor freelancer ou participante de grandes times. Nesse post de hoje, irei mostrar como é extremamente simples obter o git no Ubuntu 20.04 - Focal Fossa.

### 1 - Atualize o seu sistema:

```bash
sudo apt update && sudo apt upgrade
```

### 2 - Instale o Git:
```bash
sudo apt install git
```

### 3 - Confira se a instalação deu certo:
```bash
git --version
```
*Será exibido uma saída:*
>git version 2.25.1

Pronto, você acaba de ter o Git na sua máquina.