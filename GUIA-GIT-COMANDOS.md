# Guia de comandos Git

Este arquivo mostra os comandos mais usados no Git pelo terminal.

## Verificar se o Git esta instalado

```bash
git --version
```

Se aparecer uma versao, como `git version 2.45.0`, o Git esta instalado.

## Configurar seu nome e e-mail

Use esses comandos uma vez no computador:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
```

Para conferir:

```bash
git config --global user.name
git config --global user.email
```

## Criar um repositorio Git em uma pasta

Entre na pasta do projeto e rode:

```bash
git init
```

Isso cria o controle de versao naquela pasta.

## Ver o estado dos arquivos

```bash
git status
```

Esse comando mostra:

- arquivos novos;
- arquivos modificados;
- arquivos prontos para commit;
- se existem commits para enviar ao GitHub.

## Preparar arquivos para commit

Preparar todos os arquivos:

```bash
git add .
```

Preparar apenas um arquivo:

```bash
git add index.html
```

## Criar um commit

```bash
git commit -m "mensagem explicando a alteracao"
```

Exemplo:

```bash
git commit -m "adiciona pagina inicial"
```

Um commit e como um ponto salvo na historia do projeto.

## Ver historico de commits

```bash
git log
```

Versao resumida:

```bash
git log --oneline
```

## Conectar o projeto ao GitHub

Depois de criar um repositorio no GitHub, copie a URL dele.

Exemplo de URL:

```text
https://github.com/seu-usuario/nome-do-repositorio.git
```

Depois rode:

```bash
git remote add origin https://github.com/seu-usuario/nome-do-repositorio.git
```

Para conferir:

```bash
git remote -v
```

## Enviar commits para o GitHub

Primeiro envio:

```bash
git branch -M main
git push -u origin main
```

Depois disso, nos proximos envios normalmente basta:

```bash
git push
```

## Baixar alteracoes do GitHub

```bash
git pull
```

Use esse comando quando o repositorio no GitHub tiver alteracoes que ainda nao estao no seu computador.

## Clonar um repositorio

Clonar significa baixar uma copia de um repositorio do GitHub para o computador.

```bash
git clone https://github.com/seu-usuario/nome-do-repositorio.git
```

Depois entre na pasta:

```bash
cd nome-do-repositorio
```

## Criar uma branch

Branch e uma linha separada de trabalho.

```bash
git branch nome-da-branch
```

Entrar na branch:

```bash
git checkout nome-da-branch
```

Criar e entrar ao mesmo tempo:

```bash
git checkout -b nome-da-branch
```

## Ver branches

```bash
git branch
```

## Voltar para a branch main

```bash
git checkout main
```

## Juntar uma branch na main

Estando na `main`, rode:

```bash
git merge nome-da-branch
```

## Apagar uma branch local

```bash
git branch -d nome-da-branch
```

## Ciclo mais usado no dia a dia

```bash
git status
git add .
git commit -m "descreva o que mudou"
git pull
git push
```

Use `git pull` antes do `git push` quando outras pessoas tambem mexem no mesmo repositorio.

