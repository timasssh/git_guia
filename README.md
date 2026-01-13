# Guia de Git para iniciantes
###### por Timas

---

### O que é Git?

Git é um sistema de versionamento de código, isto é: uma tecnologia que serve para armazenar e gerenciar diferentes versões de um código, permitindo trabalhar em cima de mais de uma versão do código ao mesmo tempo e facilitando a colaboração entre programadores em um sistema.

### Conteúdo desta explicação:

Como criar e gerenciar os arquivos de um repositório, assim como as modificações destes, como trabalhar simultaneamente com diferentes versões do código deste repositório e finalmente, como transfirir o código da sua máquina para um repositório remoto, e vice-versa, tal como comparar o conteúdo do repositório remoto e o local.

---

##### Índice:

1. [Maneiras de iniciar um repositório Git](https://github.com/timasssh/git_guia/blob/master/README.md#criando-um-repositório-git)

---

## Criando um repositório Git
` git clone ` - usado caso você queira copiar ou clonar um repositório que já existe para a sua máquina.
**Uso:** `git clone [link para um repositório] [nome desejado (opicional)]`
Exemplo: digitando `git clone https://github.com/git/git.git codigo_git` será criado na sua máquina um diretório chamado "codigo_git" com o conteúdo do repositório original do Git.

<br>

` git init ` - usado caso você queira criar um repositório git na sua própria máquina no diretório atual.
**Uso:** `git init`
Esse é mais simples, basta digitar o comando acima no terminal e o seu diretório atual virará um repositório git pronto para você gerenciar seus arquivos.

---