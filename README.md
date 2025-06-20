# Workshop_git
Esse repositório destina-se a ser um ambiente de teste e experimentação para os novos ingressantes de 2025 do time de robótica Ararabots aprenderem sobre as principais funcionalidades utilizadas no desenvolvimento de software, bem como ser uma fonte de consulta no futuro.

## Usando Git pela primeira vez

Antes de qualquer coisa é importante baixar o Git. A distribuição do ubunto utilizada pelo ararabots já inclui o Git no repositório padrão. Primeiramente, é considerado boa prática atualizar os repositórios com 
```
$ sudo apt update
```

Para instalar o Git o comando utilizado é 
```
$ sudo apt install git-all
```

Quando for solicitada a permissão para instalar o Git, digite **Y** e pressione **Enter**. A versão do git pode ser consultada com  
```
$ git --version
```

A instalação em outros sistemas operacionais pode ser consultada no link: 
[Instruções de instalação no site oficial do Git (em inglês)](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

Então é preciso configurar sua conta do Git, a fim de ter registrado a sua autoria das mudanças a serem realizadas. Isso pode ser feito com o comando **git config**. Basta especificar seu nome de usuário e email do GitHub pelos comandos: 
```
$ git config --global user.name "nome_de_usuario" 
$ git config --global user.email "email@gmail.com"
```
Substitua “nome_de_usuario” por seu nome de usuário real e "email@gmail.com" por seu endereço de email, *incluindo as aspas*.

Exite uma série de configurações possíveis, essas são apenas as excenciais. É possível consultar essas informações com: 
```
$ git config --list
```

## Utilizando o Git

Originalmente, a forma de chamar comandos do Git é por linhas de comando no terminal. No entanto existem diversas interfaces para facilitar seu uso, especialmente no começo. Para fins desse workshop, aprenderemos os comandos tradicionais, mas é fortemente recomendado a instalação da extensão do VSCode ***GitLens***.

### Clonar um repositório exitente
Primeiramente, vamos aprender a clonar um repositório existente. É possível criar um repositório diretamente por linha de comando, mas isso foge do escopo desse workshop. É necessário organizar os diretórios da sua máquina, criando e selecionando a pasta que deseja: 
```
$ mkdir <nome> 
$ cd <nome>
``` 
O comando **mkdir** cria o diretório/pasta no  ubunto e **cd** entra nesse diretório.

Então vamos clonar o repositório remoto para obter uma versão local usando **git clone** e o HTTPS: 
```
$ git clone https://github.com/Abmp-ribeiro/Workshop_git.git
```
Basta então entrar no repositório em questão usando cd.

### Abrindo o VSCode

Com o caminho certo no terminal digite:
```
$ code .
```

### Checando o status do seu repositório

A principal ferramenta que você usa para determinar quais arquivos estão em qual estado é o comando git status. Através dele você pode averiguar as condições do seu repositório local.
```
$ git status
```

### Movimentar-se entre branches

De forma padrão, ao clonar um repositório você se encontra na main. Para visualizar as branches usa-se o comando: 
```
$ git branch
``` 
Para visualizar também branches remotas utilize: 
```
$ git branch -a
``` 

Recuperar informações remotas: 
```
$ git fetch origin
```

Trocar efetivamente de branch: 
```
$ git checkout <branch_name>
``` 
Para trocar para uma nova branch use: 
```
$ git checkout -b <branch_name>
```

Ao trabalhar em uma mesma branch que outras pessoas ou caso deseje informações de outra branch na sua local é necessário atualizar sua versão local com informações que estão apenas remotas usando o comando: 
```
$ git pull <branch_remota> <brach_local>
```
Esse é o chamado pull request.


### Adicionando elementos a um commit

```
$ git add <nome_do_arquivo>
``` 
Alternativamente para o atual arquivo
```
$ git add .
```
### Removendo arquivos do add

``` 
$ git rm <nome_do_arquivo>
``` 
Alternativamente para o atual arquivo
```
$ git rm .
```

### "Commitando" suas mudanças

```
$ git commit -m "<mensagem>"
```
Por default, no repositório do Arara, não se pode commitar uma mudança sem um comentário, que deve ser em inglês por padrão. Além disso é uma boa prática escrever uma mensagem objetiva e clara, a fim de identificar as mudanças feitas sem grandes dificuldades. **NUNCA COMMITE NA MAIN**.

Se você quiser refazer esse commit, faça as alterações adicionais que você esqueceu, organize-as e faça o commit novamente usando a opção --amend. É importante entender que, ao alterar seu último commit, você não está exatamente corrigindo-o, mas sim substituindo-o por um novo commit aprimorado que remove o antigo do caminho e coloca o novo commit em seu lugar. Efetivamente, é como se o commit anterior nunca tivesse acontecido e não aparecesse no histórico do seu repositório. 
```
$ git commit -ammend
```

No entanto, até esse momento essas mudanças existem apenas na sua máquina (localmente), ainda é necessário disponibiliza-las remotamente. Para tal use: 
```
$ git push
```
Caso sua branch local não exista ainda no repositório remoto, apenas pela primeira vez o comando a ser dado segue o padrão:
```
$ git push --set-upstream origin <branch_name>
``` 

### Visualizar histórico de commits

```
$ git log
``` 
É possível abreviar essa relação adicionando "--stat" após o comando acima.

### Merge

Na branch que você deseja 
```
$ git merge <branch_name>
```

## Comandos Úteis

Caso precise de ajuda com algum comando do Git, é possível acessar o manual dele através do próprio terminal digitando: 
```
$ git help <comando>
```

Ou pode-se obter uma versão resumida e mais enxuta usando:
```
$ git <comando> -h
```
