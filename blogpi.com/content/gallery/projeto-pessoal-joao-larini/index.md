---
title: "Projeto pessoal João Larini"
date: 2020-05-31T16:23:19-03:00
 

categories: []
tags: ['Projetos Pessoais']
author: "João Larini"
 

---

Em 2017 comecei um curso para aprender mais sobre o hardware do computador e servidores e seus usos/configuração. No final do curso precisei fazer um
trabalho para conclusão utilizando todos os assuntos ensinados. Minha decisão foi fazer uma lâmpada/abajur ser ligado remotamente pelo celular ou computador.
Para isso utilizei um micro computador chamado Raspberry PI [Imagem 1], ele possui vários barramentos idênticos ao de um computador normal (USB, Ethernet,
etc) e utiliza um micro SD como armazenamento. Para configurá-lo inicialmente, baixei a iso do sistema Raspbian, uma variação da distribuição Debian
feita especialmente para o Raspberry PI, como o poder de processamento do micro computador é relativamente baixo (Processador de 700MHz e 512 MB de RAM)
essa distro é mais leve para poder rodar mais facilmente no seu hardware limitado. Utilizando o programa Rufus [Imagem 2] para gravar a iso no micro SD e
deixar ele "bootável". Após isso comecei a teorizar a parte física do projeto, o Raspberry PI possui pinos (iguais aos pinos da placa mãe para
configuração do painel frontal do computador) para saída de energia, para poder ligar ou desligar a lâmpada utilizei um relê [Imagem 3] conectado aos
pinos 5 Volts e Ground, o relê funcionará como um interruptor (igual os usados em casa para ligar as luzes), um fio sairá da tomada, será interceptado
pelo relê que irá deixar a corrente passar ao ser ativado, porém invés da ativação ser fisicamente (apertar o interrupetor com a mão para ligar a luz)
ele deixa a corrente passar ou não recebendo a corrente dos pinos do raspberry [Imagem 4]. Próximo passo será configurar a ativação dos pinos do Raspberry,
por padrão os pinos não fornecem energia, estão no estado 0, para mudar o estado deles para 1 (ativado) programei alguns scripts em python que mudam o
estado dos pinos, a partir dessa parte as luzes já acendem/apagam quando os scripts são executados, um script muda o estado do pino para 1, fazendo o relê
ser acionado e deixar a corrente passar da tomada para a lâmpada e ligando a luz. O outro script deixa o estado do pino em 0 para reverter o processo e
desligar as luzes. A partir daí comecei trabalhar na parte remota, instalei a aplicação Apache no raspberry que hosteia páginas web, e programei uma página
PHP com dois botões, um dos botões irá executar o script para ligar a lâmpada e outro para desligar. Utilizei um adaptador de rede USB para conectar o
Raspberry à minha rede local, feito isso basta estar na mesma rede que ele com outro dispositivo e digitar seu endereço de IP interno (192.168.0.X) que
o Apache faz o serviço de mostrar a página com os botões, ao clicar nos botões os scripts são executados e a lâmpada acende e apaga normalmente.