# Projeto Unifil Portfolio Pessoal

É isso mesmo pessoal vamos trabalhar

# Framework utilizada para a criação do blog: Hugo
## Como utilizar o Hugo
O Hugo permite a instalação de diversos temas, os temas irão automaticamente "encaixar" o conteúdo criado
pelo usuário em seu template. Os temas podem ter vários tipos de "encaixamento" diferente, o tema que estamos
utlizando no projeto se chama [Billberry](https://themes.gohugo.io/bilberry-hugo-theme/), ele pode encaixar um
texto em formato de galeria de imagens, links, vídeos, artigos, citações, etc. Basta apenas digitar inserir o conteúdo de
acordo com seu tipo (um vídeo para um post na categoria vídeos por exemplo) em uma pasta com nome de seu tipo e ele irá
automaticamente formatar o conteúdo para o tipo de post específicado pela pasta.

## Como criar um post/utilizar comandos no Hugo
Para executar comandos do Hugo vocë pode utilizar o PowerShell do Windows, basta digitar o caminho do executável e help para
ter acesso a lista de comandos ( C:/*pastas*/hugo.exe help) e basta substituir help pelo comando desejado.

## Criando um site
Sabendo como executar um comando, para criar um site primeiro acesse o diretório que deseja armazenar o site eexecute o comando 
new site *nomedosite*. Será criada uma pasta no diretório do hugo com o nome do site escolhido. 
Para o site em si funcioar é necessário instalar um [tema.](https://themes.gohugo.io)
Basta baixar um dos temas da lista e jogar na pasta themes do site criado anteriormente.
Para acessar o site para testes é necessário abrir um server interno do Hugo, basta executar o diretório criado e executar
o comando server.

## Criando um post
Para criar um post primeiro é necessário saber qual tipo de post se deseja criar, o tema que estamos utilizando permite criar
os tipos artigo, audio, código, galeria, link, página, citação e vídeo.
Ao escolher um dos tipos de post execute o comando new *tipo*/nomedoposte.md
Para utilizar os tipos de post mais cutomizáveis dê uma olhada na pasta exampleSite que contém posts pré montados de cada tipo.
![perhaps](https://i.redd.it/dg6qctwlbrt21.jpg)
