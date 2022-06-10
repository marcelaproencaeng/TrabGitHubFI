# TrabGitHubFI

*Criar um diretório privado, adicionar arquivos e enviá-los para o Github.*

***
1. Fazer uma conta no GitHub.com

>Primeiramente uma conta no Github.com foi cadastrada.Após o cadastro, foram baixados o **Git bash** e **GitHub Desktop**, uma vez que a máquina de trabalho,ToshibaA305, apresenta o sistema operacional **Windows**, o qual logo após essa instalação(git bash) segue operando com um terminal igual ao S.O. Linux, o que facilita na execução dos comandos do github.Para o trabalho foram utilizados o terminal **git bash**, a conta cadastrada no **GitHub.com**, e o **VS Code**.Porém, pelo GitHub Desktop é possível realizar todas as etapas necessárias sem o auxílio do terminal.Logo de início, o terminal do git bash solicita a identificação do usuário, solucionada mediante os comandos:
```
*'git config -- global user.name'
*'git config -- global user.email'
 
```
Estes comandos serão utilizados uma única vez, caso o usuário tenha usado a opção --global, pois o Git usará essa informação para qualquer ação do usuário no sistema(git-scm.com). 
2. Criação de chaves SSH(ssh-keygen)

>Entrando em '~/.ssh',na opção "Git bash here" com o mouse, a qual possibilitou abrir o terminal diretamente na pasta onde contém as chaves.Como o trabalho foi realizado com o S.O. Windows, para a criação das chaves ssh foi necessária a inserção do agente 'eval "$(ssh-agent -s)"', uma vez que do contrário estas não são geradas e nem identificadas, logo é gerado um pid, o qual facilitará o processo de autentificação das chaves.Nos documentos do github.com é possível encontrar soluções para alguns tipos de erros na construção de trabalhos com o uso do git.

Então a sequência de comandos para a geração de chaves ssh pública(github) e privada(ToshibaA305) no S.O. Windows é: 

```
   1.'eval "$(ssh-agent -s)"'
   2.'ssh-keygen', a qual irá gerar duas chaves ssh, uma pública e outra privada;
   3.'ls', irá listar as chaves contidas na pasta ~/.ssh;
   4.'cat GitHubTToshibaA305FImpp.pub'(chave pública), a qual irá gerar um código, que será copiado no github.com, entrando no menu abaixo da foto do usuário em settings/SSH and GPG Keys-logo abaixo de public profile-New SSH key-um button verde-neste local o usuário irá colar a chave copiada no terminal git bash e inserir o seu nome, sem o .pub.
   5.'ssh-add GitHubTToshibaA305FImpp'(chave privada), caso o usuário não esteja na pasta ~/.ssh, inserir  'ssh-add ~/.ssh/GitHubTToshibaA305FImpp'. Como o trabalho foi realizado com o S.O.Windows, é necessário a cada abertura de terminal introduzir esse comando após o'eval "$(ssh-agent -s)"', que após o pid gerado e o comando subsequente, a chave será identificada. Com a identificação da chave o usuário terá permissão para agir com liberdade no projeto.

```
  A sequência começa a partir do item 2 caso o S.O. seja o Linux.

![alt identificação de chaves](/ImagensGit4/identificacaochavessh.png)

![alt geração das chaves ssh](/ImagensGit4/catsshpub.png)


3. Criação de um Diretório no GitHub.com

>Na página inicial do github, o button *new*, à esquerda da tela, conduz a página para a criação de repositórios(*Create a New Repository*), onde o usuário nomeia o seu repositório(TrabGitHubFI), o descreve, indica se é público ou privado(privado), adiciona um arquivo **REAME.md**(adicionado),no qual será descrito o projeto-caso não seja importado outro repositório existente- escolhe tipos de licenças as quais irão controlar os códigos(GNU v3.0) e adiciona o gitignore(PYTHON), onde há códigos binários e temporários a serem ignorados.Ao final, o repositório é criado.



![alt Arquivos gerados no README.md] (/ImagensGit4/catreadme.png)


4.  Criação do clone,branch e commit ('git clone', 'git add', 'git commit -m')
A.Clone

>Após a geração de chaves ssh(GitHubTToshibaA305FImpp/GitHubTToshibaA305FImpp.pub) e criação do repositório(TrabGitHubFI) no github.com,na pasta do projeto (~/projetosGit/TrabGitHubFI) o terminal git bash é aberto, em seguida no github.com, em repositórios, é escolhido aquele que deverá ser clonado(TrabGitHubFI), o qual ao ser clicado conduz a uma página com um button verde-code-que é selecionado, onde abre-se uma aba em que o usuário deve escolher ssh-clone(copiar).De volta a pasta do projeto(~/projetosGit/TrabGitHubFI) no terminal  git bash o comando 'git clone' git@github.com:marcelaproencaeng/TrabGitHubFI-'git clone'pasta do projeto copiada no github.com- será inserido, clonando a pasta do  servidor remoto à máquina ToshibaA305.O comando 'git clone' também contabiliza os objetos da pasta do projeto e os comprime.


![alt clone ](/ImagensGit4/gitclone.png)

B.Branch/Commit -m

>Na pasta do projeto, abre o terminal do Git bash, indroduz 'code .', o qual irá abrir o VS Code no projeto. Na tela à esquerda do VS Code, um novo arquivo é criado com o nome de *main.FI*(por exemplo), não versionado, tipo TXT.No terminal Git bash através do 'git status', é possível identificar um *branch Untracked*, não versionado(inclusive no próprio VS Code é possível essa visualização-U-Untracked-ao lado do nome do arquivo), o qual posteriormente será adicionado através do comando 'git add main.FI', após um 'git status' será utilizado, o qual indicará a presença de um *branch versionado* que deverá ser submetido a um commit, através do 'git commit -m', onde poderá ser descrita de forma breve a mensagem da alteração feita. 
```
1.git add
2.git status
3.git commit -m
4.git status
5.git log
6.git push

```
O comando 'git status' após o 'git commit' informa ao usuário que não há nada para comitar, logo para a verificação das alterações realizadas é utilizado o 'git log', o qual consta o commit inicial-main.FI- e os subsequentes.Para empurrar todas as modificações da servidor local(ToshibaA305) para o remoto(github.com) o comando 'git push' é utilizado.


![alt branch main.FI](/ImagensGit4/branchmainFI.png)


![alt git log](/ImagensGit4/gitlog.png)



5.  Empurrando as modificações para o Github(git push)

>Cada modificação realizada no projeto deverá ser empurrada para o github.com(remoto) através dos comandos 'git add', 'git commit -m','git push'.O comando 'git log' possibilita a visualização de todas as modificações realizadas durante a execução do projeto.O 'git push' contabiliza os arquivos,os comprime e os envia para o github. 
 


![alt  git push](/ImagensGit4/gitpush.png)



  


