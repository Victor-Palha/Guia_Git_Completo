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
### 10 passos para enviar o arquivo para o GitHub: 
* 1 - Dentro do GitHub, vá na aba **'Repositories'** e clique na opção **'New'**;
* 2 - Coloque o nome do repositório na opção **'Repository name'** clique **'Create repository'**;
* 3 - Depois de criar o repositório o GitHub vai dar alguns passos para serem seguidos;
* 4 - Escolha a pasta no seu computador que você quer criar o repositório e no terminal inicie o repo com o comando: `git init`;
* 5 - Crie um arquivo dentro da pasta que você criou para ser subido para o seu repo no GitHub;
* 6 - Agora que criou o arquivo, adcione dele utilizado o comando: `git add <nome do arquivo criado>`;
* 7 - Para enviar os arquivos adicionados, utilize o comando: `git commit -m "Hello world Git"`. O **-m** é uma flag para adicionar uma descrição simples ao commit do arquivo;
* 8 - Agora precisamos criar uma **Branch** que é uma ramificação do projeto e vamos chamar ela de **main**: `git branch -M main`;
* 9 - Agora vamos copiar o código dado pelo GitHub para sincronizar com o repo do GitHub, o comando é gerado pelo GitHub e deve ser parecido com este: `git remote add origin https://github.com/Seu-Usuário/Nome-do-repositório.git`;
* 10 - Agora que estamos sincronizados, vamos enviar nossos arquivos que já foram **commitados** para o GitHub: `git push -u origin main`. Se der algum erro, tente mudar o link de SSH para HTTP e remova a origin adicionada anteriormente com o comando: `git remote rm origin` e para vizualizar se foi excluida, utilize: `git remote -v`;
* OBS: Se você estiver tento problema após o `git push -u origin main`, pois não aceita sua senha na hora do push, leia esse artigo sobre as exigências do git e geração de Tokens: [Artigo](https://www.alura.com.br/artigos/nova-exigencia-do-git-de-autenticacao-por-token-o-que-e-o-que-devo-fazer).

## Verificando mudanças do projeto
* As mudanças do projetos podem ser verificadas por: `git status`;
* Este comando é utilizado **muito frequentemente**;
* Aqui serão mapeadas todas as alterações do projeto;
* Como: **arquivos não monitorados** e **arquivos modificados**;
* Podemos também dizer que é a **diferença** do que já está enviado ao servidor ou salvo no projeto;

## Adicionando arquivos ao projeto
* Para adicionar arquivos novos a um projeto utilizamos: `git add`;
* Podemos adicionar **um arquivo** específico como também **diversos de uma vez só**
* Somente adicionando arquivos eles serão monitorados pelo git;
* Ou seja, **se não adicionar ele não estará** no controle de versão;
* É interessante utilizar este comando de tempos em tempos para não perder algo por descuido;
### Adicionar arquivo específico:
* `git add <nome do arquivo>`
### Adicionar vários arquivos de uma só vez:
* `git add .`

## Salvando alterações do projeto
* As alterações do projetos são realizadas por: `git commit`;
* Podendo commitar **arquivos específicos** ou vários de uma vez com a flag `-a`;
* É uma boa prática enviar **uma mensagem a cada commit**, com as alterações que foram feitas;
* A mensagem pode ser adicionada com a flag `-m`
* Exemplo: `git commit -a -m "Mensagem do commit"`

## Enviando código ao repositório remoto
* Quando finalizamos uma funcionalidade nova, **enviamos o código ao repositório**, que é o código-fonte;
* Esta ação é feita pelo `git push`;
* Após está ação **o código do servidor será atualizado baseando-se no código local** enviado.