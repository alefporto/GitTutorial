# Tutorial de como usar o Git e Github na prática de forma simplificada.

## Afinal, o que é Git e Github?

Se vc entrou agora no mundo da programação, você já deve ter ouvido falar DEMAIS em git e github. Mas afinal, o que é Git e Github?

## Git

O Git nada mais é que um software de controle de versões. Ele registra TODAS as mudanças que ocorrem nos arquivos de um projeto, assim, ele permite que o projeto seja alterado de forma simultânea, por várias pessoas, sem se preocupar que essas alterações sobrescrevam as outras. O Git funciona como uma linha do tempo, que permite você realizar commits (marcos históricos) no decorrer do projeto, tornando bem mais fácil voltar para determinado momento, caso algo dê errado e você não queira recomeçar tudo do zero.

Resumindo, o Git é super útil pra quando você vai realizar um projeto, por exemplo, da faculdade com seus colegas e cada um vai trabalhar em uma parte específica do projeto. Assim vocês poderão trabalhar simultaneamente no projeto e ao final, juntar todas as alterações em uma única branch (linhas do tempo)

* Marco histórico: Commit
* Linha do tempo: Branch

## Github

Já o Github é uma plataforma de hospedagem remota para repositórios Git. 

* "Hosteia" o seu código em um local seguro.
* Compartilha seu projeto facilmente com outros devs.
* Outros devs podem colaborar com seu projeto.
* Etc...

Hoje em dia, virou meio que uma "rede social" para desenvolvedores.

## Git é a mesma coisa que Github?

Geralmente, aspessoas confundem Git com Github, mas os dois são coisas diferentes.

* Git é o software de versionamento.
* Github é uma plataforma para criação de repositórios Git.

Resumindo, o Github permite a você criar um repositório Git remoto, o que possibilita outras pessoas acessarem seu repositório e trabalhar com você em um mesmo projeto, clonar o repositório localmente, fazer alterações e enviar essas alterações de volta para o repositório remoto no github.

É essencial que você use os dois, pois assim você vai ter mais segurança, por exemplo, em caso de perda de hardware e afins. Assim você sempre terá uma cópia dos seus arquivos em um servidor remoto e seguro.

## Instalando o Git no seu computador.

* [Link para download do Git](https://git-scm.com/downloads)

## Agora vamos para a prática

De uma forma simples, o Git trabalha com uma arquitetura em ramificações (Branch).
Cada novo commit, ou melhor, alteração no código, cria um novo marco na ramificação atual (Branch).

## Configurações iniciais do Git

Para as pessoas saberem quem você é quando fizer algum commit ou pull request.

* Após instalar o Git, Abra o Git Bash no seu terminal do VSCode.
* Digite `git config --global user.name "Seu nome"`.
* Digite `git config --global user.email seuemail@exemplo.com`.

## Criando um repositório local do zero.

* Crie uma pasta no seu PC com o nome do seu projeto.

* Abra o VSCode nessa pasta.

* Abra o Git Bash no seu terminal do VSCode

* Digite `git init` para inicializar o repositório local.

## Clonando na sua máquina um repositório já existente no Github.

Como você pode baixar um código já existente no Github?

Sempre que você entrar em um repositório, seja o seu ou o de outra pessoa, terá o botão `Code`, que quando você clica e aparece um link.

<img src="https://thumbs2.imgbox.com/29/a5/7QIa5zR3_t.png"/>

* Vá até o repositório no GitHub, copie esse link HTTP e vá para o terminal.
* Para clonar o repositório na sua maquina, use o comando: `git clone link_do_repositório.git`

Diferente do `git init`, não precisa criar um repositório antes disso. Com o git clone basta abrir o terminal, clonar o projeto e pronto!

## Branchs

* Cada branch presente em um repositório é uma nova ramificação, independente, onde podemos alterar os arquivos sem interferir nos originais.

* Criar uma nova branch é uma boa prática ao se trabalhar em uma nova funcionalidade do projeto e afins.

* Por padrão, um repositório é inicializado com somente UMA branch, a `main` ou `master`.

### Para trabalhar com as branchs temos alguns comandos principais:

* `git branch` [Mostra quais as branchs existentes].

* `git branch nome_da_branch` [Cria uma nova branch].

* `git checkout nome_da_branch` [Vai da sua branch atual pra branch desejada].

* `git branch -D nome_da_branch` [Deleta a branch passada como parâmetro].

## Commits

Ao longo do projeto, você irá alterar o código-fonte de algum arquivo, deletar algum arquivo, adicionar outro, etc.

Ao fazer essas mudanças, é importante realizar commits de pontos importantes de alterações.
Exemplo: atualização de um arquivo da branch.

É importante que a descrição de cada commit seja objetiva, pois ela vai ficar salva no histórico das alterações.

### Passos pra se realizar um commit

1. Verificando os arquivos alterados:

* `git status` [Mostra todos os arquivos que foram alterados].

Para ignorar arquivos que não queremos que apareçam no `git status`, criamos um arquivo chamado `.gitignore` e dentro dele escrevemos o nome do arquivo que queremos ignorar.

2. Adicionando ao stage:

* `git add nome_do_arquivo_alterado` [Adiciona o arquivo desejado à lista de prontos pra serem commitados].
* `git add .` [Pra não ter que ficar adicionando arquivo por arquivo, esse comando adiciona todos os arquivos alterados].

3. Realizando o commit:

* `git commit -m "Descrição do commit"` [Realiza o commit no seu repositório local].
* Para se polpar tempo, podemos usar o git add  eo git commit em um mesmo comando: `git add . && git commit -m "Descrição do commit"`

### Após o commit

Podemos listando todos os commits já realizados usando o comando: `git log`.

Podemos voltar a linha do tempo até um commit específico usando o comando: `git checkout id_do_commit`.

Pra voltar a linha do tempo ao commit mais recente usamos o comando: `git checkout master`.

## Merge

Após realizar todas as alterações e adições desejadas na branch criada por você, para juntar essas alterações à branch principal, temos que realizar alguns passos.

1. Voltar para a branch principal:

* `git checkout master` [Vai para a branch master do seu repositório].

2. Realizando o merge da branch secundária:

* `git merge nome_da_branch_secundária` [Realiza o merge da branch passada como parâmetro com a branch atual em que você está].

## Push

Após realizar todas as alterações, commits e mergeds desejados no seu repositório LOCAL, chega a hora de atualizar seu repositório remoto no Github, para isso usamos um comando bastante simples:

#### Caso você tenha clonado o repositório do Github

* `git push branch_desejada`

* Exemplo: `git push master`

#### Caso você tenha criado um repositório local com o git init

* `git push link_do_repositório branch_desejada`

* Exemplo: `git push git@github.com:alefporto/GitTutorial.git master`

## Pull

Se você estiver trabalhando com um colega no mesmo repositório do Github, caso ele realize alguma alteração, você pode atualizar o seu repositório local com a alteração dele.

* Basta executar o comando `git pull` [Puxa todas as alterações feitas no repositório do Github para o seu repositório local].

## Principais comandos

Resumindo os principais comandos usados quando trabalhamos com Git:

* `git init` [Inicia um repositório local na pasta atual].

* `git status` [Lista os arquivos que foram alterados no projeto e qual estão prontos para serem commitados].

* `git add` [Adiciona todos os do `git status` à pasta de arquivos prontos para serem commitados].

* `git commit` [Realiza um commit com o nome passado].

* `git log` [Lista todos os commits feitos até o momento].

* `git clone` [Clona o repositório do github para sua máquina].

* `git pull` [Atualiza seu repositório LOCAL com as alterações do repositório REMOTO].

* `git push` [Atualiza seu repositório REMOTO com as alterações feitas no repositório LOCAL].

* `git merge` [Serve pra mesclar commits e branchs na branch atual].
