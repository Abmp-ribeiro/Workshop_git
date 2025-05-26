# Workshop_git
Esse repositório destina-se a ser um ambiente de teste e experimentação para os novos ingressantes de 2025 do time de robótica Ararabots aprenderem sobre as principais funcionalidades utilizadas no desenvolvimento de software, bem como ser uma fonte de consulta no futuro.

## Usando Git pela primeira vez

Antes de qualquer coisa é importante baixar o Git. A distribuição do ubunto utilizada pelo ararabots já inclui o Git no repositório padrão. Primeiramente, é considerado boa prática atualizar os repositórios com

'''
$ sudo apt update
'''

Para instalar o Git o comando utilizado é

'''
$ sudo apt install git-all
'''

Quando for solicitada a permissão para instalar o Git, digite **Y** e pressione **Enter**. A versão do git pode ser consultada com 

'''
$ git --version
'''

A instalação em outros sistemas operacionais pode ser consultada no link: 
[Instruções de instalação no site oficial do Git (em inglês)](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

Então é preciso configurar sua conta do Git, a fim de ter registrado a sua autoria das mudanças a serem realizadas. Isso pode ser feito com o comando **git config**. Basta especificar seu nome de usuário e email do GitHub pelos comandos:

'''
$ git config --global user.name "nome_de_usuario"
$ git config --global user.email "email@gmail.com"
'''
Substitua “nome_de_usuario” por seu nome de usuário real e "email@gmail.com" por seu endereço de email, *incluindo as aspas*.

É possível consultar essas informações com:

'''
$ cat .gitconfig
'''

## Utilizando o Git

Originalmente, a forma de chamar comandos do Git é por linhas de comando no terminal. No entanto existem diversas interfaces para facilitar seu uso, especialmente no começo. Para fins desse workshop, aprenderemos os comandos tradicionais, mas é fortemente recomendado a instalação da extensão do VSCode ***GitLens***.
