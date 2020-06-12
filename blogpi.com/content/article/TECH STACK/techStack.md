---
title: " Ferramentas Utilizadas "
date: 2020-02-03T22:25:57-03:00
tags: ['Tech Stack']
author: "Team Maya"
excludeFromIndex: true
---
### Static Gen: Hugo

<div style="text-align:center"><img src="https://cdn.discordapp.com/attachments/191299120336601097/720826865664655390/hugo-logo-wide.png" ></div>

Para começar a construção do blog, selecionamos um Static Gen (Static Site Generator) chamado Hugo, sua função é servir de base para um tema customizável.
Juntamente do Hugo, instalamos um tema chamado Billburry, o tema trata da parte visual do blog, enquanto o Hugo da parte de código. O Hugo possui um servidor
interno, utilizando ele podemos gerar um "preview" com as mudanças que fizemos ao tema, após fazer mudanças consideráveis, enviamos as alterações ao nosso
repositório no GitHub.


### Versionalização: GitHub
<div style="text-align:center"><img style="width:60%" src="https://www.somagnews.com/wp-content/uploads/2020/04/75-e1586981465263.png" ></div>

O GitHub é uma plataforma com o intuito de versionar projetos, é possível criar repositórios e armazenar arquivos (de projetos por exemplo) neles. O principal
motivo da utilização do GitHub para nós foi a possibilidade de todos nós trabalharmos num mesmo projeto e facilitar a junção de nosso progresso. Caso alguém faça
alguma modificação em algum arquivo, todos do grupo também terão essa modificação, pois os arquivos locais estão vinculados ao repositório.


### Virtualização: Amazon AWS

<div style="text-align:center"><img src= https://cuponomia-a.akamaihd.net/img/stores/original/amazon-636994893639686000.png ></div>

O serviço AWS da Amazon tem diversas funcionalidades, nós utilizados o sistema EC2 Manager, esse sistema irá "rodar" uma máquina virtual com um sistema operacional
de nossa escolha. Utilizamos o sistema operacional Amazon EC2 (uma distribuição linux da própria Amazon). O próprio EC2 Manager possui um painel de controle fora da
máquina virtual, por ele configuramos o firewall para ter acesso à máquina fora da rede local. Após isso instalamos um aplicativo chamado Apache para "hostear" o blog.


### Hospedagem: Apache

<div style="text-align:center"><img style="width:60%" src= https://upload.wikimedia.org/wikipedia/commons/thumb/d/db/Apache_HTTP_server_logo_%282016%29.svg/1200px-Apache_HTTP_server_logo_%282016%29.svg.png></div>

O Apache permite o acesso de página HTML fora da rede, isso significa que com o nosso blog configurado na pasta do Apache, acessando o IP da máquina irá automaticamente
redirecionar o acesso para o serviço do Apache acessar nosso blog via internet.


### Domínio: Name.com

<div style="text-align:center"><img style="width:60%" src= https://i.imgur.com/2Gx95at.png ></div>

O último passo foi a configuração do DNS, utilizando o site Name.com, adquirimos um domínio chamado teammaya.codes. Após isso, nas configurações do site, configuramos
o redirecionamento, fazendo com que ao digitar teammaya.codes na barra de pesquisa, você seja redirecionado ao servidor e automaticamente, por conta da presença do
Apache, visualizar o blog.

