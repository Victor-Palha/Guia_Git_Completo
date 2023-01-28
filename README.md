# Git - Todos os conceitos
## O que é controle de versão?
* Uma técnica que ajuda a **gerenciar o código-fonte** de uma aplicação;
* Registrando **todas as modificações** de código, podendo também reverter as mesmas;
* Criar versões de um software em diferentes estágios, podendo **alterar facilmente entre elas**;
* Cada membro da equipe pode trabalhar em uma versão diferente;
* Há ferramentas para trabalhar o controle de versão como: **git** e SVN.

## O que é git?
* O sistema de controle de versão **mais utilizado do mundo** atualmente;
* O git é baseado em **repositórios**, que contêm todas as versões do código e também as cópias de cada desenvolvedor;
* Todas as operações do git **são otimizadas para ter alto desempenho**;
* Todos os objetivos do git são **protegidos como criptografia** para evitar alterações indevidas e maliciosas;
* O git é um **projeto de código aberto**.

# Git - Comandos fundamentais
## O que é um repositório?
* É onde o código será **armazenado**;
* Na maioria das vezes cada projeto tem **um repositório**;
* Quando criamos um repositório estamos iniciando um projeto;
* O repositório pode ir para servidores que são especializados em gerenciar repositórios, como: **GitHub** e **Bitbucket**;
* Cada um dos desenvolvedores do time pode baixar o repositório e **criar versões diferentes** em sua máquina;

## Criando repositórios
* Para criar um repositório utilizamos o comando: `git init`;
* Desta maneira o git vai criar os arquivos necessários para inicializá-lo;
* Que estão na pasta oculta **.git**;
* Após este comando o diretório atual **será reconhecido pelo git como um projeto** e responderá aos seus demais comandos;
* Para ver o status git, podemos utilizar o comando: `git status`;

## O que é o GitHub?
* É um **serviço para gerenciar repositórios**, gratuito e amplamente utilizado;
* Podemos **enviar nossos projetos** para o GitHub e disponibilizá-lo para outros devs;
* O GitHub é gratuito tanto para projetos públicos como **privados**;

## Enviando repositórios para o GitHub
* Podemos facilmente **enviar nossos repos** para o GitHub;
* Precisamos criar o projeto no GitHub, inicializar o mesmo no git em nossa máquina, sincronizar com o GitHub e enviar;
* E esta sequência que parece ser complexa é facilmente executada **por poucos comandos**;
* Vale lembrar que só fazemos **uma vez por projeto** este fluxo;
* **Sequência de passos**: 
* 1 - Dentro do GitHub, vá na aba **'Repositories'** e clique na opção **'New'**;
* 2 - Coloque o nome do repositório na opção **'Repository name'** clique **'Create repository'**;
* 3 - Depois de criar o repositório o GitHub vai dar alguns passos para serem seguidos;
* 4 - Escolha a pasta no seu computador que você quer criar o repositório e no terminal inicie o repo com o comando: `git init`;
* 5 - Crie um arquivo dentro da pasta que você criou para ser subido para o seu repo no GitHub;
* 6 - Agora que criou o arquivo, adcione dele utilizado o comando: `git add <nome do arquivo criado>`;
* 7 - Para enviar os arquivos adicionados, utilize o comando: `git commit -m "Hello world Git"`. O **-m** é uma flag para adicionar uma descrição simples ao commit do arquivo