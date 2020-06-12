---
title: "Deixando o Blog Acessível na Web"
date: 2020-04-26T16:23:19-03:00
 

categories: []
tags: ['Atualizacoes']
author: "Team Maya"
 

---

Inicialmente realizamos o cadastro para acesso ao site da AWS, Inicializamos uma máquina virtual utilizando o EC2 ,

<div style="text-align:center"><img src="https://cdn.discordapp.com/attachments/555568413674700800/704047870277582978/unknown.png" ></div>

 do AWS, rodando a distribuição Amazon Linux 2.
 
 <div style="text-align:center"><img src="https://cdn.discordapp.com/attachments/555568413674700800/704048067455746179/unknown.png" ></div>
 
***

 <div style="text-align:center"><img src="https://cdn.discordapp.com/attachments/555568413674700800/704049341098098893/unknown.png" ></div>

Realizamos as atualizações do sistema operacional da VM (com o comando: sudo yum update) 

 <div style="text-align:center"><img style="width:60%" src="https://cdn.discordapp.com/attachments/555568413674700800/704049568144293908/unknown.png" ></div>

e instalamos o serviço Apache para criar o Host do blog na Web,

 <div style="text-align:center"><img style="width:60%" src="https://cdn.discordapp.com/attachments/555568413674700800/704050113172996256/unknown.png" ></div>

 para isso foi necessário compilar o blog.

A fim de realizar um aceso mais fácil à estrutura do blog, instalamos o git para podermos clonar, transferir arquivos e versionarmos o blog.

 <div style="text-align:center"><img style="width:60%" src="https://cdn.discordapp.com/attachments/555568413674700800/704050443441012896/unknown.png" ></div>

Com o projeto devidamente clonado, copiamos os arquivos compilados para a pasta do Apache.

<div style="text-align:center"><img style="width:60%" src=https://cdn.discordapp.com/attachments/555568413674700800/704050961005543484/unknown.png ></div>

Feito isso, configuramos o firewall da máquina, com o sistema de firewall já incluso no site da AWS, 

<div style="text-align:center"><img src=https://cdn.discordapp.com/attachments/555568413674700800/704051343731720253/unknown.png ></div>

retirando a necessidade de baixar qualquer outro aplicativo de firewall ou configurar diretamente dentro da VM. O sistema de Firewall da AWS permite criar facilmente regras de entrada e saída de dados,

<div style="text-align:center"><img src=https://media.discordapp.net/attachments/555568413674700800/704051766005596190/unknown.png?width=1026&height=94 ></div>

 para que o serviço do Apache com o nosso blog seja acessível de uma rede externa, criamos uma regra que permite conexões na porta 80 da máquina (porta utilizada pelo serviço Apache).

 <div style="text-align:center"><img src=https://media.discordapp.net/attachments/555568413674700800/704052989068836884/unknown.png ></div>

Após isso o nosso serviço estava funcionando normalmente, e ao digitarmos o IP público da VM no navegador (Imagem 11), o proprio navegador automaticamente já redireciona para a porta 80 da VM acessando o Apache e exibindo o nosso blog compilado. 

<div style="text-align:center"><img src=https://media.discordapp.net/attachments/555568413674700800/704053227880054934/unknown.png?width=1026&height=347 ></div>
