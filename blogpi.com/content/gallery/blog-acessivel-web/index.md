---
title: "Deixando o Blog Acessível na Web"
date: 2020-04-26T16:23:19-03:00
 

categories: []
tags: ['Atualizacoes']
author: "Team Maya"
 

---

Inicialmente realizamos o cadastro para acesso ao site da AWS, Inicializamos uma máquina virtual utilizando o EC2 (Imagem 1), do AWS, rodando a distribuição Amazon Linux 2 (Imagem 2 e 3). Realizamos as atualizações do sistema operacional da VM (com o comando: sudo yum update) (Imagem 4) e instalamos o serviço Apache para criar o Host do blog na Web (Imagem 5), para isso foi necessário compilar o blog.

A fim de realizar um aceso mais fácil à estrutura do blog, instalamos o git para podermos clonar, transferir arquivos e versionarmos o blog (Imagem 6).
Com o projeto devidamente clonado, copiamos os arquivos compilados para a pasta do Apache (Imagem 7). 

Feito isso, configuramos o firewall da máquina, com o sistema de firewall já incluso no site da AWS (Imagem 8), retirando a necessidade de baixar qualquer outro aplicativo de firewall ou configurar diretamente dentro da VM. O sistema de Firewall da AWS permite criar facilmente regras de entrada e saída de dados (Imagem 9), para que o serviço do Apache com o nosso blog seja acessível de uma rede externa, criamos uma regra que permite conexões na porta 80 da máquina (porta utilizada pelo serviço Apache) (Imagem 10).

Após isso o nosso serviço estava funcionando normalmente, e ao digitarmos o IP público da VM no navegador (Imagem 11), o proprio navegador automaticamente já redireciona para a porta 80 da VM acessando o Apache e exibindo o nosso blog compilado (Imagem 12). 
