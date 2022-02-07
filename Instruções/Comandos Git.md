# Git



## Comandos para a utilização do terminal Git:



Alguns comandos são usados tanto no Promp do Windows, quanto no Git:

- ### cd _caminho do diretório_

  Comando serve para entrar nas pastas.

- ### ls

  Comando para listar o conteúdo do diretório.

- ### mkdir

  Cria um novo diretório.

- ### mv _nome do arquivo_ ./_nome do diretório a ser movido_/

  Move arquivos para outro diretório.

- ### ls -a

  Flag que lista os arquivos ocultos presentes no diretório.

- ### Ctrl+L

  Tem a mesma função do "cls" do Prompt do Windows.

## Comandos para criar a chave SSH no Git:

- ### ssh-keygen -t ed25519 -C _e-mail_

  Comando para criação da chave SSH e senha para a comunicação entre o Git e o GitHub.

- ### cat id_ed25519.pub

  Comando para mostrar a chave SSH criada com o comando anterior.

- ### eval $(ssh-agent -s)

  Comando para iniciar o processo de SSH.

- ### ssh-add id_ed25519

  Comando para mostrar ao agent do SSH a chave privada, com senha.

Obs: não é necessário criar uma chave SSH toda vez que for usar o Git, ela é apenas para identificar o seu computador no servidor do GitHub, só será preciso criar outra, quando tiver de usar o Git em outra máquina.



## Comandos de Configuração:

- ### git config --list

  Lista as configurações do Git.

- ### git config --global unset "função"

  Deleta a função descrita entre aspas.

- ### git config --global "função"

  Configura a função entre aspas.

- ### git config --global user.email "_seu e-mail_"

- ### git config --global user.name "seu usuário do GitHub"

  Comandos para configuração inicial do Git.

## Criando um Repositório:

- ### git init

  Comando que inicializa o Git no repositório.

- ### git add * 

  Comando que adiciona o arquivo criado dentro do diretório ao commit.

  Obs.: o * serve para dizer pro Git que você está adicionando todo conteúdo da pasta para ser commitado, mas caso venha a criar novos arquivos e/ou pastas, digite *git add _nome do arquivo_ _nome da pasta ./_*

- ### git commit -m "commit inicial"

  Comando que associa o arquivo commitado ao sha1.

- ### git status

  Comando que monitora o status do arquivo.

- ### git commit -m "criar pasta, move arquivo"

  Quando se comita com a flag "-m" o "m" significa "mensagem", um recado que você pode deixar pra próxima pessoa que acessar o código saber o que foi feito naquele momento.

- ### echo > README.md

  Arquivo que serve de "capa" para o repositório.

- ### git remote add origin "link do repositório no GitHub"

  Associa o seu repositório na máquina local ao servidor do GitHub.

  "origin" serve como apelido do link a ser associado.

- ### git push origin master

  Comando para o GitHub "puxar" o repositório do computador para a nuvem.

  Nessa tela o servidor pedirá usuário e senha, ou o token de acesso.
  
  

Caso após o repositório ser upado, você queira fazer alguma alteração, mas ele já tenha sido alterado por outra pessoa você deve fazer:

- ### git pull origin

  Comando para trazer o repositório do GitHub para o Git.

  Provavelmente aparecerá uma mensagem de erro de associação dos projetos, você deve abrir o arquivo que apresentou problema e editar, adicionando as novas informações. 

- ### git add *

- ### git commit -m "resolve conflitos"



## Clonando Arquivos do GitHub

No GitHub, você procurará pelo repositório a ser copiado, copiará a URL e no Git irá digitar o seguinte comando:

- ### git clone _link do repositório_

  A partir desse momento, o repositório estará no seu computador e você poderá editar a vontade.