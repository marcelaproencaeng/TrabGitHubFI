# TrabGitHubFI

Criar um diretório privado, adicionar arquivos e enviá-los para o Github.
## Fazer uma conta no GitHub.com
<p>Primeiramente uma conta no Github.com foi cadastrada.Após o cadastro, foram baixados o git bash e git Desktop, uma vez que a máquina de trabalho,ToshibaA305, apresenta o sistema operacional Windows, o qual logo após essa alteração  seguirá operando com um terminal igual ao do Linux, o que facilita a execução dos comandos do github.Para o trabalho foram utilizados o terminal gitbash, a conta cadastrada no GitHub.com, e o VS Code.Porém, pelo git desktop é possível realizar todas as etapas sem o auxílio do terminal.</p>


### Criação de chaves SSH(ssh-keygen)
<p>Entrando em ~/.ssh, foi clicado "Git bash here" com o mouse, o que possibilitou abrir o terminal diretamente na pasta onde contém as chaves.Como o trabalho foi realizado com o S.O. Windows, para a criação das chaves ssh foi necessário a inserção do agente "eval "$(ssh-agent -s)"", uma vez que do contrário estas não são geradas e nem identificadas, logo é gerado um pid, o qual facilitará o processo de criação de chaves e não irá gerar erros.Nos documentos do github.com é possível encontrar soluções para alguns tipos de erros na construção de trabalhos com o uso do git.
Então a sequência de comandos para a geração de chaves ssh pública(git) e privada(ToshibaA305) é: 

ssh-keygen, a qual irá gerar duas chaves ssh, uma pública e outra privada;
ls, irá listar as chaves contidas na pasta ~/.ssh;
cat GitHubTToshibaA305FImpp.pub(chave pública), a qual irá gerar uma chave, que será copiada no github.com, entrando no menu abaixo da foto do usuário em settings, depois abaixo de public profile em SSH and GPG Keys,New SSH key-um button verde-neste local o usuário irá colar a chave copiada no terminal git bash e inserir o seu nome, sem o pub.
ssh-add GitHubTToshibaA305FImpp(chave privada), caso o usuário não esteja na pasta ~/.ssh, inserir o comando ssh-add ~/.ssh/GitHubTToshibaA305FImpp, como o trabalho foi realizado com o S.O.Windows, é necessário a cada abertura de terminal introduzir esse comando após o "eval "$(ssh-agent -s)", que após o pid gerado, e o comando subsequente a chave será identificada.  


![alt Criação das chaves ssh] (C:\Users\Marcela\projetosGit\TrabGitHubFI\ImagensGit3\chavessh.png)

![alt Idetificação das chaves](C:\Users\Marcela\projetosGit\TrabGitHubFI\ImagensGit3\identificacaochavessh.png)
![](C:\Users\Marcela\projetosGit\TrabGitHubFI\ImagensGit3\catsshpub.png)
</p>
<br>

#### Criação de um Diretório no GitHub.com
<p>Na página inicial do github o button new, à esquerda da tela, conduz a página para a criação de repositórios(Create a New Repository), onde o usuário nomeia o seu repositório, o descreve, indica se é público ou privado, adiciona um arquivo REAME.md, no qual será descrito o projeto,caso não seja importado outro repositório existente, escolhe tipos de licensas as quais irão controlar os códigos e adiciona o gitignore, onde há códigos binários e temporários a serem ignorados.Ao final, o repsitório é criado.

![]()


##### Criação do Branch, commit e clone (git add, git commit, git clone)
Na pasta do projeto, abre o terminal do git bash, indroduz code ., o qual irá abrir o VS Code no projeto, na tela à esquerda do VS Code, um novo arquivo é criado com o nome de main.FI(por exemplo), não versionado, tipo TXT.No terminal git bash através do git status, é possível identificar um branch Untracked, não versionado, o qual posteriormente será adicionado através do comando, git add main.FI, após um git status será utilizado, o qual indicará a presença de um branch versionado que deverá ser submetido a um commit, através do git commit -m, onde poderá ser descrito de forma breve a mensagem da alteração feita.
![alt ](C:\Users\Marcela\projetosGit\TrabGitHubFI\ImagensGit3\branchmainFI.png)
![alt](C:\Users\Marcela\projetosGit\TrabGitHubFI\ImagensGit3\gitclone.png)
![alt](C:\Users\Marcela\projetosGit\TrabGitHubFI\ImagensGit3\gitlog.png)
###### Empurrando as modificações para o Github(git push)
![alt ](C:\Users\Marcela\projetosGit\TrabGitHubFI\ImagensGit3\gitpush.png )