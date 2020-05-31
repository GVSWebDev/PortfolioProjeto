---
title: "Registrando e Configurando o Domínio"
date: 2020-05-30T20:25:43-03:00


categories: []
tags: ['Atualizacoes']
author: "Gabriel Vilela Serra"

---

A parte mais desafiadora de registrar um domínio é a escolha do nome ... Tantas possibilidades criativas, combinações interessantes, e engraçadas também. Contemplamos adquirir nomes como ronaldinho.soccer, maya.team, teammata.wtf, entre muitos outros. No final, escolhemos o teammaya.codes mesmo, que combina com o intuito do site, e soa bem até. Um dos principais motivos que levaram a essa escolha, foi o fato que eu consegui o pacote de Estudante do GitHub, que me deu um desconto de 100% no primeiro domínio da provedora Name.com. Uma boa iniciativa do GitHub!

Após "comprar" o domínio, tive que descobrir como configurava o DNS. De início, eu só fui passando pelas funcionalidades oferecidas pela Dashboard do Name.com, até que cheguei em uma denomeada de "URL Forwarding", que servia para redirecionar o dominio para outra URL. A primeira coisa que fiz foi fazer com que o dominio redirecionasse para o IP do nosso site. Mas não era tão simples assim aparentemente, pois o dominio ainda retornada um erro dizendo que não era possível resolver o Hostname. Continuei procurando, e achei o painel de configuração dos Registros de DNS. Alguns provedores de dominios já configuram "de fábrica", mas não tinha nada pré-configurado lá. O bom é que o próprio site tinha uma certa documentação que especificava o que cada coisa fazia de forma bem simples de entender. Lá, aprendi que pecisava fazer Registros de DNS tipo A, para conectar o domínio ao nosso site. Fiz 2 registros, um para todos os subdominios, e outro pra uso geral, todos apontando ao IP do nosso site. 

Também já aproveitei e fui atrás de configurar os registros MX para redirecionamento dos emails, como especificado na atividade. De inicio, tentei fazer algo direto com o Gmail, usando o G Suite, até descobrir que era pago. Depois, procurei uma alternativa pela Amazon. Descobri o serviço Amazon Simple Email Service (SES) que prometia fazer redirecionamento de emails. Para isso, precisava verificar que era dono do domínio adicionando um Registro TXT com um certo código que eles providenciaram. Esse processo demoraria até 72h para ser completo, então fiz o que foi pedido e deixei por assim mesmo. Mas curioso, ainda continuei pesquisando sobre as funcionalidades do Dashboard do Name.com. Então, achei um serviço de redirecionamento de emails deles mesmos! Bastava colocar o endereço de email ao qual seriam redirecionados para. Em questão de minutos, o site já estava funcionando com o domínio correto, e os emails já estavam sendo redirecionados com sucesso para o email de teste no qual eu configurei previamente. Sucesso!