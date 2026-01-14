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
2. [Adicionando/removendo arquivos de *staging* e fazendo commits](https://github.com/timasssh/git_guia/blob/master/README.md#criando-commits)

---

## Criando um repositório Git
1. ` git clone ` - usado caso você queira copiar ou clonar um repositório que já existe para a sua máquina.

**Uso:** `git clone [link para um repositório] [nome desejado (opicional)]`
- Exemplo: digitando `git clone https://github.com/git/git.git codigo_git` será criado na sua máquina um diretório chamado "codigo_git" com o conteúdo do repositório original do Git.

<br>

2. ` git init ` - usado caso você queira criar um repositório git na sua própria máquina no diretório atual.

**Uso:** `git init`

Esse é mais simples, basta digitar o comando acima no terminal e o seu diretório atual virará um repositório git pronto para você gerenciar seus arquivos.

---

## Criando commits
Depois de inicializar um repositório e fazer algumas alterações nos arquivos é hora de adicionar as modificações feitas a **staging** ou **index** e depois fazer **commits**.

1. ` git add ` - usado para adicionar os arquivos a *staging* antes de commita-los.

**Uso:** `git add [arquivo(s)]`

**É possível fazer uso do símbolo `*` que será "traduzido" pelo Git como "todos".**

Exemplos:
- `git add *.md` - adiciona a *staging* todos os arquivos MarkDown do diretório atual, não incluindo os subdiretórios.
- `git add *t* README.md` - adiciona todos os arquivos que tem a letra **t** no nome e o arquivo README.md.
- `git add *` e `git add .` adicionam a *staging* todos os arquivos do diretório e seus subdiretórios.
- `git add diretorio1/ diretorio2/teste.md` adiciona todos os arquivos da pasta "diretorio1" e o arquivo "teste.md" da pasta "diretorio2".

<br>

2. ` git restore --staged ` - usado para remover os arquivos de *staging* antes de fazer. Pode ser útil caso tenha adicionado a *index* um arquivo que não deveria fazer parte de seu próximo commit.

**Uso:** `git restore --staged [arquivo(s)]`

- Exemplo: `git restore --staged *` remove de *staging* todos os arquivos.

<br>

3. ` git status ` e ` git diff ` - usados para ver as alterações e estado dos arquivos, com `diff` sendo mais específico e mostrando as linhas alteradas nos arquivos.

**Uso:** `git status` e `git diff`

<br>

4. ` git commit -m "" ` - usado para salvar as alterações adicionadas a *staging* em um *commit* juntamente com uma mensagem de descrição destas alterações. A descrição das alterações deve ser digitada entre aspas após o parâmetro `-m` ("m" vem de *message* neste caso), e deve responder claramente o que foi feito e o porquê.

**Uso:** `git commit -m ""`

- Exemplo: `git commit -m "fix: Função somarParesDoVetor somava um número a mais"`.

<br>

5. ` git reset HEAD ` - usado para descartar alterações feitas, "sincronizando" o conteúdo local com algum commit feito.

**Uso:**
- `git reset --hard HEAD~1` - volta para o último commit e descarta alterações em staging.
- `git reset --soft HEAD~2` - volta para o penúltimo commit e mantém alterações em staging.
- `git reset --hard [hash de um commit]` - volta para um commit específico (`git reflog` para obter hash de um commit).

<br>