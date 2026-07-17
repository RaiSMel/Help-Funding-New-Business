# Utilizando os comandos do Git
<br>

Antes de realizar os testes abaixo será necessário realizar a autenticação do usuário através do GitHub e Git com a chave SSH.

Utilize a lista abaixo para ir até o conteúdo de interesse.

- [Configurações do Git](#Configuracoes-do-Git)
- [Inicializando e linkando pasta Git](#Inicializando-e-linkando-pasta-Git)
- [Comparando os commits, branches e verificando logs](#Comparando-os-commits,-branches-e-verificando-logs)
- [](#)

<hr>
<br>
## Configurações do Git

Com o comando config --list é listado todas as configurações do git dentro da máquina.

`
git config --list
`

<br>
<hr>
<br>



## Inicializando e linkando pasta Git

<br>
Para verificar a versão utilizamos o comando

`
git --version
`

Para realizar a inicialização da do git dentro da pasta abra o local no terminal e utilize o comando abaixo

`
git init
`

Com isso criamos a pasta chamada .git que contém as informações de versionamento do nosso projeto.

Agora vamos fazer a linkagem do repositório local e o online, troque o URL pelo link no sistema abaixo. (origin é o nome padrão utilizado para apelido do repositório local).

`
git remote add origin URL
`

Logo após, iremos realizar o download dos dados que estão dentro da pasta remota, utilizando o -u (de update) e indicando o nome do repositório local (origin).

`
git pull -u origin
`

Após isso realizar as edições do seu projeto, assim iremos adicionar e verificar o status do que foi alterado nesse commit.

Abaixo realizamos a adição das modificações gerais com o "." no stage, caso queira adicionar um arquivo especifíco utilize o nome do arquivo no lugar do ponto (com sua extensão, exemplo: teste.txt)
`
git add .
`

abaixo caso queira tirar algo que não queira dentro do commit, uma saida para ignorar determinados arquivos é a utilização do arquivo .gitignore

`
git restore .
`

Para verificar o status do que será adicionado e enviado para o repositório remoto, utilize o comando abaixo

`
git status
`

Para fazer o commit utilize o comando abaixo, adicione o que foi modificado brevemente.

`
git commit -m"ESCREVA"
`

Agora para finalizar iremos fazer o envio com o comando de enviar que é o pull, utilizando novamente o -u, indicando o repositório local e a branch.

`
git push -u origin main
`

<br>
<hr>
<br>

## Comparando os commits, branches e verificando logs

o comando diff podemos validar a diferença e mudanças de dois commits, branches e filtar por arquivos em específico.

Comando faz validação do que ocorreu de modificação para o que já foi para o stage e o que ainda não foi.

`
git diff
`

Verificar as modificações que estão dentro do stage 

`
git diff --staged
`

Verificar todos as modificações não comitadas

`
git diff HEAD
`

Podemos utilizar a forma abaixo para comparar ou dois commits ou duas branches

`
git diff EXE1 EXE1
`

Limitar a visualização de um arquivo conforme abaixo

`
git diff ARQUIVO
`

Para verificar o histórico de commits 

`
git log
`

Se caso queira validar quem fez quais modificações em quais commits em um arquivo utilize o comando 

`
git blame ARQUIVO
`
