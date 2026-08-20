# Problemas comuns com Git e GitHub

Este arquivo lista erros comuns e formas simples de resolver.

## Git nao reconhecido

Erro parecido:

```text
git is not recognized
```

Possivel causa: o Git nao esta instalado ou nao foi adicionado ao PATH.

Como resolver:

1. Instale o Git em `https://git-scm.com`.
2. Feche e abra o terminal de novo.
3. Rode:

```bash
git --version
```

## Nao consigo fazer commit

Erro parecido:

```text
Please tell me who you are
```

Configure seu nome e e-mail:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
```

Depois tente o commit novamente.

## Nao aparece nada para commitar

Mensagem parecida:

```text
nothing to commit, working tree clean
```

Isso significa que nao existem alteracoes novas para salvar.

Verifique:

```bash
git status
```

Se voce editou um arquivo, confirme se salvou o arquivo no editor.

## Erro ao dar push

Mensagem possivel:

```text
rejected
```

Isso pode acontecer quando existem alteracoes no GitHub que ainda nao estao no seu computador.

Tente:

```bash
git pull
git push
```

Se houver conflito, sera preciso resolver os arquivos conflitantes.

## Conflito de merge

Um conflito acontece quando duas alteracoes mexem na mesma parte de um arquivo.

O Git marca o arquivo mais ou menos assim:

```text
<<<<<<< HEAD
minha alteracao
=======
alteracao de outra pessoa
>>>>>>> nome-da-branch
```

Como resolver:

1. Abra o arquivo.
2. Escolha qual conteudo deve ficar.
3. Apague as linhas com `<<<<<<<`, `=======` e `>>>>>>>`.
4. Salve o arquivo.
5. Rode:

```bash
git add .
git commit -m "resolve conflito"
git push
```

## Esqueci de fazer git add

Se voce rodar commit sem preparar arquivos, o Git pode dizer que nao tem nada para commitar.

Use:

```bash
git add .
git commit -m "mensagem do commit"
```

## Coloquei mensagem errada no ultimo commit

Se o commit ainda nao foi enviado para o GitHub:

```bash
git commit --amend -m "nova mensagem"
```

Se ja foi enviado, evite alterar sem pedir ajuda, principalmente em projetos com outras pessoas.

## Quero ver para onde estou enviando o projeto

```bash
git remote -v
```

Esse comando mostra a URL do repositorio remoto.

## Quero trocar a URL do repositorio remoto

```bash
git remote set-url origin https://github.com/seu-usuario/novo-repositorio.git
```

## Estou na branch errada

Veja as branches:

```bash
git branch
```

Troque para a branch desejada:

```bash
git checkout nome-da-branch
```

## Apaguei algo sem querer

Se o arquivo ainda nao foi commitado depois da alteracao, peca ajuda antes de rodar comandos de recuperacao.

Evite usar comandos como:

```bash
git reset --hard
```

Esse comando pode apagar alteracoes locais.

## Boa regra para evitar problemas

Antes de mexer no projeto:

```bash
git status
git pull
```

Depois de mexer:

```bash
git status
git add .
git commit -m "explique o que mudou"
git push
```

