---
title: "Virtualização: Amazon AWS"
date: 2020-06-11T22:25:57-03:00
tags: ['Tech Stack']
author: "Team Maya"
---

O serviço AWS da Amazon tem diversas funcionalidades, nós utilizados o sistema EC2 Manager, esse sistema irá "rodar" uma máquina virtual com um sistema operacional
de nossa escolha. Utilizamos o sistema operacional Amazon EC2 (uma distribuição linux da própria Amazon). O próprio EC2 Manager possui um painel de controle fora da
máquina virtual, por ele configuramos o firewall para ter acesso à máquina fora da rede local. Após isso instalamos um aplicativo chamado Apache para "hostear" o blog.