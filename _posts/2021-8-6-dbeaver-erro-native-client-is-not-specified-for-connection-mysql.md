---
layout: post
title: DBeaver (MySQL) - Erro - Native client is not specified for connection no ubuntu 20.04
---

>error executing process utility 'mysql' not found in client home '/usr/bin' (/usr/bin) utility 'mysql' not found in client home '/usr/bin' (/usr/bin)

![DBeaver erro MySQL](https://i.imgur.com/vSeWPe0.png)

Um erro bastante comum para quem utiliza o aplicativo DBeaver para gerenciar o seu banco de dados MySQL é o "Native client is not specified for connection" ao tentar fazer o dump ou restore. Isso ocorre por que o DBeaver não identificou o local onde está instalado o mysql na sua máquina e para solucionar esse problema é bastante simples. Vamos ver logo abaixo:

### 1 - Antes de tudo, localize onde está instalado o seu MySQL através do comando:
```sh
which mysql
```
A saída será:
> /usr/bin/mysql (No meu caso)

### 2 - Com o botão direito, clique na base de dados a qual você deseja fazer o DUMP ou o RESTORE, vá em ferramentas e em seguida DUMP DATABASE ou RESTORE DATABASE:

![DBeaver erro MySQL](https://i.imgur.com/vSeWPe0.png)

### 3 - Após isso, vá em "Local Client":

![Local Client](https://i.imgur.com/Iab36Je.png)

### 4 - Em "Local Client", clique no combobox e selecione a opção "Browse":
![Browse](https://i.imgur.com/j5E2pN0.png)

### 5 - Agora é só clicar em "Add Home" e localizar o MySQL, o qual achamos no passo 1 */usr/bin*.
![Add Home](https://i.imgur.com/PbXwa5f.png)
![Localização](https://i.imgur.com/ekY3fxr.png)