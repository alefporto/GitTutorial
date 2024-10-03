
# 🌟 Tutorial Simplificado de Git e Github 🚀

## O que é Git e Github? 🤔

Se você está começando agora no mundo da programação, provavelmente já ouviu falar MUITO em **Git** e **Github**. Mas o que são exatamente?

## Git 🛠️

Imagine que você está escrevendo um livro com seus amigos. Cada um escreve um capítulo e, para garantir que ninguém sobrescreva o capítulo do outro, vocês usam um sistema que salva todas as versões. É isso que o **Git** faz! Ele é um sistema de **controle de versões** que registra todas as mudanças nos arquivos de um projeto. Isso permite que várias pessoas trabalhem ao mesmo tempo no mesmo projeto, sem confusão. E, caso algo dê errado, você pode voltar para uma versão anterior como se estivesse voltando no tempo. ⏳

**Resumindo:**
- **Git** é tipo uma linha do tempo do seu projeto, onde você marca pontos importantes com os **commits** (pense nos commits como fotos dos momentos históricos do seu projeto).
- Cada linha do tempo é chamada de **branch**, então, se você quiser fazer algo novo sem estragar o que já fez, cria uma nova **branch**.

### ✨ Analogias
- **Commit:** É como salvar um checkpoint em um videogame. Se algo der errado, você volta naquele ponto.
- **Branch:** É como se cada vez que você quisesse tentar algo novo (sem mexer na versão principal), criasse uma linha paralela. Se der certo, você pode juntar de novo na principal depois.

## Github 🌍

Já o **Github** é onde o **Git** "vive" na internet. Imagine que é como o **Google Drive**, mas para programadores. Ele "hospeda" seu código, permite que outras pessoas colaborem com você, e ainda serve como backup dos seus projetos. 🌐

Basicamente:
- **Compartilha** seu código com o mundo.
- **Outros desenvolvedores** podem ver e até contribuir no seu projeto.
- **Faz backup** das suas coisas para garantir que você não perca nada!

Hoje, o Github virou quase uma "rede social" para devs! 🧑‍💻👩‍💻

## Git ≠ Github 🧐

Muita gente confunde os dois, mas Git e Github são coisas diferentes:
- **Git** = Sistema de controle de versões (gerencia o histórico do seu código localmente).
- **Github** = Plataforma para guardar seu repositório Git e colaborar com outros.

## Instalando o Git no seu computador 💻

1. [Clique aqui para baixar o Git](https://git-scm.com/downloads)
2. Siga as instruções de instalação para o seu sistema operacional.
3. Pronto! 🎉 Agora você já pode usar o Git no seu computador!

---

## Vamos colocar a mão na massa 👩‍💻👨‍💻

Agora que já entendemos o que é Git e Github, vamos ver como usá-los na prática! 😎

## ⚙️ Configurações iniciais do Git

Depois de instalar o Git, você precisa se "apresentar" para ele, para que ele saiba quem está fazendo as alterações.

1. Abra o **Git Bash** no terminal do VSCode.
2. Digite os seguintes comandos (trocando pelas suas informações):

```bash
git config --global user.name "Seu nome"
git config --global user.email seuemail@exemplo.com
```

Pronto! Agora o Git sabe quem você é. 😁

## Criando um repositório local do zero 🆕

1. Crie uma **pasta** no seu PC com o nome do seu projeto.
2. Abra o **VSCode** nessa pasta.
3. Abra o **terminal** do VSCode e execute:

```bash
git init
```

Agora você tem um repositório Git local criado!

## Clonando um repositório existente do Github 🌐

Se você já tem um repositório no Github ou quer colaborar em um projeto de outra pessoa, basta cloná-lo!

1. No repositório do Github, clique no botão `Code` e copie o link HTTPS.
   
   ![Botão Code](https://github.com/github/explore/raw/main/topics/git/git.png)
   
2. No seu terminal, use o comando abaixo (substitua pelo link do repositório que você copiou):

```bash
git clone link_do_repositório.git
```

Pronto! Agora o repositório está na sua máquina.

## 📂 Branches: Trabalhando em linhas do tempo diferentes

Cada **branch** é como uma nova linha do tempo do seu projeto. Sempre que for trabalhar em uma nova funcionalidade, crie uma nova branch. Isso evita que você mexa no código principal (chamado de **main** ou **master**).

### Principais comandos de branch:
- Ver as branches existentes:

```bash
git branch
```

- Criar uma nova branch:

```bash
git branch nome_da_branch
```

- Mudar para uma branch específica:

```bash
git checkout nome_da_branch
```

- Deletar uma branch (cuidado!):

```bash
git branch -D nome_da_branch
```

---

## Commits: Registrando as alterações 💾

Quando você fizer alterações no projeto, é importante registrar esses momentos com **commits**.

### Como fazer um commit:

1. Ver quais arquivos foram modificados:

```bash
git status
```

2. Adicionar os arquivos modificados para o "estágio" (ou seja, preparar para o commit):

```bash
git add nome_do_arquivo
```
Ou para adicionar todos de uma vez:

```bash
git add .
```

3. Fazer o commit:

```bash
git commit -m "Descrição do que foi feito"
```

Agora suas alterações estão registradas! 🎉

---

## Juntando tudo: Merge 🔀

Quando terminar de trabalhar na sua branch, você vai querer juntar suas alterações com a branch principal. Isso é feito com o **merge**.

1. Volte para a branch principal:

```bash
git checkout main
```

2. Faça o merge:

```bash
git merge nome_da_branch
```

---

## Push: Enviando suas alterações para o Github 🚀

Depois de tudo feito, você pode enviar suas alterações para o repositório remoto no Github.

- Para enviar suas alterações para o repositório remoto:

```bash
git push origin nome_da_branch
```

Se for a branch principal, pode ser algo assim:

```bash
git push origin main
```

---

## Pull: Atualizando seu código com as alterações do Github 🔄

Se alguém fizer alterações no repositório remoto, você pode atualizar seu código local com:

```bash
git pull origin main
```

---

## 🌟 Comandos principais:

Aqui está um resumo dos comandos que você vai usar com frequência:

- `git init`   - Inicializa um repositório local.
- `git clone`  - Clona um repositório do Github.
- `git status` - Mostra os arquivos modificados.
- `git add`    - Adiciona arquivos para o commit.
- `git commit` - Faz um commit com suas alterações.
- `git push`   - Envia suas alterações para o repositório remoto.
- `git pull`   - Atualiza seu código com o remoto.
- `git branch` - Trabalha com branches (criar, mudar, deletar).
- `git merge`  - Junta duas branches.

---

Com esse tutorial, você já consegue dar seus primeiros passos no Git e Github. 🚀
