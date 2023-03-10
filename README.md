# Git - Todos os conceitos

![logo git](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e0/Git-logo.svg/1280px-Git-logo.svg.png)

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

## Git - Comandos fundamentais
### O que é um repositório?
* É onde o código será **armazenado**;
* Na maioria das vezes cada projeto tem **um repositório**;
* Quando criamos um repositório estamos iniciando um projeto;
* O repositório pode ir para servidores que são especializados em gerenciar repositórios, como: **GitHub** e **Bitbucket**;
* Cada um dos desenvolvedores do time pode baixar o repositório e **criar versões diferentes** em sua máquina;

### Criando repositórios
* Para criar um repositório utilizamos o comando: `git init`;
* Desta maneira o git vai criar os arquivos necessários para inicializá-lo;
* Que estão na pasta oculta **.git**;
* Após este comando o diretório atual **será reconhecido pelo git como um projeto** e responderá aos seus demais comandos;
* Para ver o status git, podemos utilizar o comando: `git status`;

### O que é o GitHub?
* É um **serviço para gerenciar repositórios**, gratuito e amplamente utilizado;
* Podemos **enviar nossos projetos** para o GitHub e disponibilizá-lo para outros devs;
* O GitHub é gratuito tanto para projetos públicos como **privados**;

### Enviando repositórios para o GitHub
* Podemos facilmente **enviar nossos repos** para o GitHub;
* Precisamos criar o projeto no GitHub, inicializar o mesmo no git em nossa máquina, sincronizar com o GitHub e enviar;
* E esta sequência que parece ser complexa é facilmente executada **por poucos comandos**;
* Vale lembrar que só fazemos **uma vez por projeto** este fluxo;
#### 10 passos para enviar o arquivo para o GitHub: 
1. Dentro do GitHub, vá na aba **'Repositories'** e clique na opção **'New'**;
2. Coloque o nome do repositório na opção **'Repository name'** clique **'Create repository'**;
3. Depois de criar o repositório o GitHub vai dar alguns passos para serem seguidos;
4. Escolha a pasta no seu computador que você quer criar o repositório e no terminal inicie o repo com o comando: `git init`;
5. Crie um arquivo dentro da pasta que você criou para ser subido para o seu repo no GitHub;
6. Agora que criou o arquivo, adcione dele utilizado o comando: `git add <nome do arquivo criado>`;
7. Para enviar os arquivos adicionados, utilize o comando: `git commit -m "Hello world Git"`. O **-m** é uma flag para adicionar uma descrição simples ao commit do arquivo;
8. Agora precisamos criar uma **Branch** que é uma ramificação do projeto e vamos chamar ela de **main**: `git branch -M main`;
9. Agora vamos copiar o código dado pelo GitHub para sincronizar com o repo do GitHub, o comando é gerado pelo GitHub e deve ser parecido com este: `git remote add origin https://github.com/Seu-Usuário/Nome-do-repositório.git`;
10. Agora que estamos sincronizados, vamos enviar nossos arquivos que já foram **commitados** para o GitHub: `git push -u origin main`. Se der algum erro, tente mudar o link de SSH para HTTP e remova a origin adicionada anteriormente com o comando: `git remote rm origin` e para vizualizar se foi excluida, utilize: `git remote -v`;
* OBS: Se você estiver tento problema após o `git push -u origin main`, pois não aceita sua senha na hora do push, leia esse artigo sobre as exigências do git e geração de Tokens: [Artigo](https://www.alura.com.br/artigos/nova-exigencia-do-git-de-autenticacao-por-token-o-que-e-o-que-devo-fazer).

### Verificando mudanças do projeto
* As mudanças do projetos podem ser verificadas por: `git status`;
* Este comando é utilizado **muito frequentemente**;
* Aqui serão mapeadas todas as alterações do projeto;
* Como: **arquivos não monitorados** e **arquivos modificados**;
* Podemos também dizer que é a **diferença** do que já está enviado ao servidor ou salvo no projeto;

### Adicionando arquivos ao projeto
* Para adicionar arquivos novos a um projeto utilizamos: `git add`;
* Podemos adicionar **um arquivo** específico como também **diversos de uma vez só**
* Somente adicionando arquivos eles serão monitorados pelo git;
* Ou seja, **se não adicionar ele não estará** no controle de versão;
* É interessante utilizar este comando de tempos em tempos para não perder algo por descuido;
#### Adicionar arquivo específico:
* `git add <nome do arquivo>`
#### Adicionar vários arquivos de uma só vez:
* `git add .`

### Salvando alterações do projeto
* As alterações do projetos são realizadas por: `git commit`;
* Podendo commitar **arquivos específicos** ou vários de uma vez com a flag `-a`;
* É uma boa prática enviar **uma mensagem a cada commit**, com as alterações que foram feitas;
* A mensagem pode ser adicionada com a flag `-m`
* Exemplo: `git commit -a -m "Mensagem do commit"`

### Enviando código ao repositório remoto
* Quando finalizamos uma funcionalidade nova, **enviamos o código ao repositório**, que é o código-fonte;
* Esta ação é feita pelo `git push`;
* Após está ação **o código do servidor será atualizado baseando-se no código local** enviado.

### Recebendo as mudanças
* É comum também ter que **sincronizar o local** com as mudanças do remoto;
* Esta ação é feita pelo: `git pull`;
* Após o comando serão **buscadas atualizações**, se encontradas elas **serão unidas ao código atual** existente na nossa máquina.
* Para este comando funcionar é preciso que o repo remoto tenha arquivos que o local não possua, então para testar essa funcionalidade, crie um arquivo dentro do GitHub.

### Clonando repositórios
* O ato de baixar um repositório de um servidor remoto é chamado de **clonar repositório**;
* Para esta ação utilizamos: `git clone <link do repo>`;
* Passando a **referência** do repositório remoto;
* A referência é dada pelo GitHub no botão __**Code**__ dentro do repositório;
* Este comando é utilizado quando **entramos em um novo projeto**, por exemplo;

### Removendo arquivos do repositório
* Os arquivos **podem ser deletados da monitoração** do git;
* O comando para deletar é: `git rm <arquivo>`
* Após deletar um arquivo do git ele não terá mais suas atualizações consideradas pelo git;
* Apenas quando for adicionado novamente pelo `git add`

### Histórico de alteração
* Podemos **acessar um log** de modificações feitas no projetos;
* O comando para este recurso é: `git log`;
* Você receberá uma informação dos **commits realizados** no projeto até então;

### Renomeando arquivos
* Com o comando `git mv <Nome do arquivo> <diretorio/novo nome>` podemos renomear um arquivo;
* O mesmo também pode ser **movido para outra pasta**;
* E isso fará com que este novo arquivo **seja monitorado pelo git**;
* O arquivo anterior é **excluído**;

### Desfazendo alteração
* O arquivo modificado pode ser **retornado ao estado original**;
* O comando utilizado é o `git checkout <nome do arquivo>`;
* Após a utilização do mesmo o arquivo sai do staging;
* Caso seja feita uma próxima alteração, ele entra em staging novamente.

### Ignorando arquivo no projeto
* Uma técnica muito utilizada é **ignorar arquivos do projetos**;
* Devemos inserir um arquivo chamado **.gitignore** na raiz do projeto;
* Nele podemos inserir todos os arquivos que não devem entrar no versionamento;
* Isso é útil para **arquivos gerados automaticamente** ou arquivos que contêm **informações sensíveis**;

### Desfazendo todas as alterações
* Com o comando `git reset` podemos resetar as mudanças feitas;
* Geralmente é utilizada com a flag **--hard**;
* Todas as alterações **commitadas** e **também as pendentes** serão excluídas.
* Exemplo: `git reset --flag branch`, `git reset --hard origin/main`

## Branches
### O que é um branch?
* Branch é a forma que o git **separa as versões dos projetos**;
* Quando um projeto é criado ele inicia na branch **main**, estamos trabalhando nela até esse ponto;
* Geralmente cada nova feature de um projeto **fica em um branch separado**;
* Após a finalização das alterações os **branchs são unidos** (_merge_)para ter o código-fonte final;

### Criando e visualizando os branches
* Para visualizar os branchs disponíveis basta digitar: `git branch`;
* Para criar um branch você precisa utilizar o comando: `git branch <nome>`;
* Estas duas operações são muito utilizadas no dia a dia de um dev;

### Deletando Branches
* Podemos deletar um branch com a flag `-d` ou `--delete`;
* **Não é comum deletar um branch**, normalmente guardamos o histórico do trabalho;
* Geralmente se usa o delete quando o branch foi criado errado;

### Mudando de branch
* Podemos mudar para outro branch utilizando o comando: `git checkout <nome>`;
* Se quiseremos criar um branch e mudar direto para ele, utilizamos o comando: `git checkout -b <nome>`;
* Este comando também é utilizado paradispensar mudanças de um arquivo;
* Alterando o branch podemos levar alterações que não foram commitadas juntos, **tome cuidado!**.

### Unindo branches
* O código de dois branches distintos pode ser unido pelo comando: `git merge <nome do branch>`;
* Outro comando para a lista dos **mais utilizados**;
* Normalmente é por meio dele que recebemos as atualizações de outros devs;

### Stash
* Podemos salvar as modificações atuais **para prosseguir com uma outra abordegem de solução** e não perder o código;
* O comando para esta ação é o: `git stash`;
* Após o comando o branch será resetado para a sua versão de acordo com o repositório;

### Recuperando stash
* Podemos verificar as stashs criadas pelo comando: `git stash list`;
* E também podemos recuperar a stash com o comando: `git stash apply <número>`;
* Podemos também ver as alterações da stash com o comando: `git stash show -p <number>`
* Desta maneira podemos continuar de onde paramos com os arquivos adicionados a stash.

### Removendo a stash
* Para limpar totalmente as stash de um branch podemos utilizar o comando: `git stash clear`;
* Caso seja necessário delletar uma stash específica podemos utilizar: `git stash drop <number>`;

### Utilizando tags
* Podemos criar tags nos branches por meio do comando: `git tag -a <nome> -m "<msg>"`;
* A tag é diferente do stash, serve como um **checkpoint de um branch**;
* É utilizada para demarcar estágios do desenvolvimento de algum recurso;
* Para visualizar as tags podemos utilizar o comando: `git tag`;

### Verificando e alterando tags
* Podemos verificar uma tag com o comando: `git show <name>`;
* Podemos trocar de tags com o comando: `git checkout <nome da tag>`;
* Desta maneira podemos retroceder ou avançar em checkpoints de um branch;
* Para remover uma tag podemos usar o comando: `git tag -d <nome da tag>`;

### Enviando e compartilhando tags
* As tags podem ser **enviadas para o repositório de código**, sendo compartilhada entre os devs;
* O comando é: `git push origin <nome>`;
* Ou se você quiser enviar mais tags: `git push origin --tags`;

## Compartilhamento e atualização

### Encontrando branches
* Branches novos são criados a todo tempo e o **seu git pode não estar mapeando eles**;
* Com o comando `git fetch -a` você é atualizado de todos os branchs e tags que ainda não estão reconhecidos por você;
* Este comando é útil para utilizar o branch de algum outro dev do time, por exemplo;
* O branch pode não aparecer direto quando utilizar o comando `git branch`, então é preciso mudar para ela usando o `git checkout <nome da branch>`;

### Recebendo alterações
* O comando `git pull` serve para recebermos atualizações do repositório remoto;
* Cada branch pode ser atualizado com o git pull;
* Utilizamos para atualizar o **main do repo** como também quando trabalhamos em conjunto em uma branch e queremos receber as atualizações de um dev;

### Enviando alterações
* O comando `git push` faz o inverso do pull, ele envia todas as alterações para o repo remoto;
* Serve também para **enviar as atualizações de um branch específico** para outro dev;
* Ou quando terminamos uma tarefa e precisamos enviar ao repositório;

### Utilizando o remote
* Com o `git remote` podemos fazer algumas ações como: adicionar um repo para trackear ou remover;
* Quando criamos um repo remoto, adicionamos ele ao git com `git remote add origin <link>`;
* Para remover um repo remoto podemos utilizar o comando: `git remote rm origin`;

### Trabalhando com submódulos
* Submódulo é a maneira que temos de possuir **dois ou mais projetos em um só repositório**;
* Podemos adicionar uma dependência ao nosso projeto atual, porém mantendo suas estruturas separadas;
* Para adicionar o submódulo utilizamos o comando: `git submodule add <repositório> <\diretorio>`;
* Para verificar os submódulos o comando é `git submodule`;

### Atualizando submódulo
* Para atualizar um submódulo primeiro devemos **commitar as mudanças**;
* E para enviar para o repo do submódulo utilizamos `git push --recurse-submodule=on-demand`;
* Este fluxo fará a atualização apenas do submódulo;

## Análises e inspenção

### Exibindo informações
* O comando `git show` nos dá diversas informações úteis;
* Ele nos dá as informações do branch atual e também **seus commits**;
* As **modificações de arquivos entre cada commit também são exibidas**;
* Podemos exibir as informações de tags também como: `git show <tag>`;

### Exibindo diferenças
* O comando `git diff <branch>` serve para exibir as diferenças de um branch;
* Quando utilizado as diferenças do branch atual com o remoto serão exibidas no terminal;
* Podemos também verificar a diferença entre arquivos: `git diff <arquivo a> <arquivo b>`;

### Log resumido
* O comando `git shortlog` nos dá um log resumido do projeto;
* Cada commit será unido por **nome do autor**;
* Podemos então saber quais commits foram enviados ao projeto e por quem;

## Administração do repositório

### Limpando arquivos untracked
* O comando `git clean` vai verificar e limpar arquivos que não estão sendo trackeados;
* A flag `-f` pode ser usada para forçar a limpeza caso dê algum erro;
* Ou seja, todos que vocês **não utilizou git add**;
* Utilizado para arquivos que são **gerados automaticamente**, por exemplo, e atrapalham a vizualização do que é realmente importante;

### Otimizando o repositório
* O comando `git gc` é uma abreviação para **garbage collector**;
* Ele identifica arquivos que **não são mais necessários** e os exclui;
* Isso fará com que o repositório seja otimizado em questões de **performance**;

### Checando integridade de arquivos
* O comando `git fsck` é uma abreviação de File System check;
* Esta instrução verifica a integridade de arquivos e sua conectividade;
* Verificando assim possíveis **corrupções em arquivos**;
* **Comando de rotina**, utilizado para ver se está tudo certo com nossos arquivos;

### Reflog
* O `git reflog` vai mapear todos os seus passos no repositório, até uma mudança de branch é inserida neste log;
* Já o `git log`, que vimos anteriormente, apenas armazena os commits de um branch;
* Os **reflogs ficam salvos até expirar**, o tempo de expiração padrão é de 30 dias;
* Podemos usar o `git reflog` para pegar a hash das alterações e navegar com o comando `git reset --hard <hash>`

### Transformando o repo para arquivo
* Com o comnado `git archive` podemos transformar o repo um arquivo compactado, por exemplo;
* O comando é `git archive --format <tipo> --output <nome.tipo> <branch>`;
* exemplo:`git archive --format zip --output main_files.zip main`;
* E então a branch main vai estar zipada no arquivo **main_files.zip**;

## Melhorando os commits do projeto

### A importância do commit
* **O problema**: commits sem sentido atrapalham o projeto;
* **Precisamos padronizar os commits**, para que o projeto cresça de forma saudável também no versionamento, isso ajuda em:
* Review do **Pull Request**;
* Melhoria dos log em `git log`;
* Manutenção do projeto (voltar código, por exemplo);

### Branches com commits ruins
* Há uma solução chamada **private branches**;
* Onde criamos branches que **não serão compartilhados no repositório**, então podemos colocar qualquer commit;
* Ao fim da solução do problema podemos fazer um **rebase**, reestruturar os commits;
* O comando será: `git rebase <branch atual> <branch privado> -i`;
* Escolhemos os branches para excluir (`squash`) e renomear com (`reword`);
* Para salvar as alterações no terminal, usamos o comando `:x!` para salvar o arquivo;

### Boas mensagens de commit
* Separar **assunto** do corpo da mensagem;
* Assunto com no **máximo 50 caracteres**;
* Assunto com **Letra inicial maiúscula**;
* Corpo com no **máximo 72 caracteres**;
* Explicar o **por que e como** do commit, e não como o código foi escrito;

# Markdown

![logo markdown](https://www.kamailio.org/w/wp-content/uploads/2022/05/markdown-logo.jpeg)

### Cabeçalhos
* Os **cabeçalhos em markdown** são determinados pelo símbolo `#`;
* Cabeçalhos são os famosos títulos ou **headings** do HTML;
* `# => h1, ## => h2, ### => h3` e assim por diante

### Ênfase
* Temos símbolos que podem dar **ênfase ao texto**;
* Para escrever em **negrito**: `**texto** ou __texto__`;
* Para escrever em itálico: `*texto* ou _texto_`;
* **Combinando** os dois: `_um **texto** combinado_`;

### Listas com Markdown
* Temos as listas __ordenadas__ e __não ordenadas__ em markdown;
* As listas não ordenadas começam os itens com: `* Item`;
* Exemplo:
```js
* algum item;
* Outro item;
* algum outro item.
```
* As listas ordenadas começam com: `1. Item`;
* Exemplo:
```js
1. algum item;
2. Outro item;
3. algum outro item.
```
* Podemos também criar listas mistas, por exemplo:
```js
* algum item;
    1. teste;
    2. teste 2
    3. teste 3
* Outro item;
* algum outro item.
```

### Inserir Imagens
* É possível **inserir imagens** em markdown também;
* Veja a sintaxe: `![Texto alternativo](Link/caminho da imagem)`;
* A imagem pode **estar no próprio repo** ou **ser externa**.

### Inserir Links
* Com o markdown podemos **inserir links** de forma fácil;
* A sintexa é bastante parecida com a de **imagens**, com a diferença que não tem a `!`;
    * `[texto do link](www.link.com)`
* Podemos transformar uma imagem em um link também;
* A sintaxe é: `[![texto alternativo](link/caminho da imagem)](www.link.com)`;
    * Colocamos a tag da imagem dentro de onde é o texto do link, apenas isso!
* Exemplo:
    * [![Minha foto - Ash](https://media.licdn.com/dms/image/C4E03AQEE-pTGVS6YLg/profile-displayphoto-shrink_200_200/0/1625778277950?e=1681948800&v=beta&t=3548RtDL5xuuZUGzWzX_f9buZo5F7UNHhEoCmfZxs1Y)](https://www.linkedin.com/in/jo%C3%A3o-victor-ferreira-palha-b67736216/)

### Inserindo código - Exclusivo do GitHub
* Podemos inserir **código** no Markdown também;
* A sintaxe é: ` ``` código ``` `
* exemplo:
```ts
    function soma(a:number, b:number){
        return a+b
    }
```
* Podemos colocar a sigla da linguagem que queremos usar logo após as aspas;
* ` ```js código em JS``` `

### Task List - Exclusivo do GitHub
* Podemos inserir uma **lista de tarefas** pelo Markdown;
* A sintaxe para tarefas concluídas: `- [x] CSS do rodapé`;
* Para não concluídas: `- [] CSS da página de contatos`;
* Esta sintaxe é do markdown **especial do GitHub**;
* Exemplo:
    * - [x] Terminar de escrever sessão do git;
    * - [x] Terminar de escrever sessão de Markdown;

# Conclusão
Finalmente o repo chegou ao fim, espero que quem tenha lido ele tenha aprendido alguma coisa, da mesma forma que eu aprendi bastante escrevendo. Deixando claro que esse repo não tem nenhum fim lucrativo somente informativo! Eu escrevi toda essa documentação baseada no curso do professor [Matheus battisti](https://www.udemy.com/user/matheus-battisti/) de Git e GitHub, eu recomendo fortemente quem leu essa documentação dar uma olhada nesse curso para expandir seus conhecimentos! [Curso de Git e gitHub](https://www.udemy.com/course/git-e-github-do-basico-ao-avancado-c-gist-e-github-pages/)!