---
title: "Deixando o Blog Acessível na Web"
date: 2020-04-26T16:23:19-03:00
 

categories: []
tags: ['Atualizacoes']
author: "Team Maya"
 

---

Inicialmente realizamos o cadastro para acesso ao site da AWS, Inicializamos uma máquina virtual utilizando o EC2, do AWS, rodando a distribuição Amazon Linux 2. Realizamos as atualizações do sistema operacional da VM (com o comando: sudo yum update) e instalamos o serviço Apache para criar o Host do blog na Web, para isso foi necessário compilar o blog.
A fim de ralizar um aceso mais fácil à estrutura do blog, instalamos o git para podermos clonar, transferir arquivos e versionarmos o blog.
Com o projeto devidamente clonado, copiamos os arquivos compilados para a pasta do Apache. Feito isso, configuramos o firewall da máquina, com o sistema de firewall já incluso no site da AWS, retirando a necessidade de baixar qualquer outro aplicativo de firewall ou configurar diretamente dentro da VM. O sistema de Firewall da AWS permite criar facilmente regras de entrada e saída de dados, para que o serviço do Apache com o nosso blog seja acessível de uma rede externa, criamos uma regra que permite conexões na porta 80 da máquina (porta utilizada pelo serviço Apache).
Após isso o nosso serviço estava funcionando normalmente, e ao digitarmos o IP público da VM no navegador, o proprio navegador automaticamente já redireciona para a porta 80 da VM acessando o Apache e exibindo o nosso blog compilado. 
