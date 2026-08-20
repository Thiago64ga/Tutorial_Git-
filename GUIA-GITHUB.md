# Guia do GitHub pelo navegador

Este guia explica como usar o GitHub pelo site.

## Criar uma conta

1. Acesse `https://github.com`.
2. Clique em `Sign up`.
3. Crie seu usuario, e-mail e senha.
4. Confirme o e-mail se o GitHub pedir.

## Criar um repositorio

1. Entre no GitHub.
2. Clique no botao `+`, no canto superior direito.
3. Clique em `New repository`.
4. Em `Repository name`, digite o nome do repositorio.
5. Escolha se ele sera:
   - `Public`: qualquer pessoa pode ver.
   - `Private`: apenas pessoas autorizadas podem ver.
6. Se quiser, marque `Add a README file`.
7. Clique em `Create repository`.

## Enviar um projeto local para o GitHub

Depois de criar o repositorio no site, o GitHub mostra alguns comandos.

Se o projeto ja existe no seu computador, normalmente o processo e:

```bash
git init
git add .
git commit -m "primeiro commit"
git branch -M main
git remote add origin https://github.com/seu-usuario/nome-do-repositorio.git
git push -u origin main
```

Troque a URL pela URL real do seu repositorio.

## Criar arquivo pelo site

1. Abra o repositorio no GitHub.
2. Clique em `Add file`.
3. Clique em `Create new file`.
4. Digite o nome do arquivo.
5. Escreva o conteudo.
6. No final da pagina, escreva a mensagem do commit.
7. Clique em `Commit changes`.

## Enviar arquivo pelo site

1. Abra o repositorio no GitHub.
2. Clique em `Add file`.
3. Clique em `Upload files`.
4. Arraste os arquivos ou clique para escolher.
5. Escreva a mensagem do commit.
6. Clique em `Commit changes`.

## Editar arquivo pelo site

1. Abra o arquivo no GitHub.
2. Clique no icone de lapis.
3. Faca a alteracao.
4. Escreva uma mensagem explicando o que mudou.
5. Clique em `Commit changes`.

## Baixar ZIP do repositorio

1. Abra o repositorio.
2. Clique no botao verde `Code`.
3. Clique em `Download ZIP`.

Isso baixa os arquivos, mas nao cria uma copia com historico Git. Para trabalhar com commits, prefira usar `git clone` ou GitHub Desktop.

## Copiar URL para clonar

1. Abra o repositorio.
2. Clique no botao verde `Code`.
3. Copie a URL HTTPS.

Exemplo:

```text
https://github.com/seu-usuario/nome-do-repositorio.git
```

Depois use:

```bash
git clone https://github.com/seu-usuario/nome-do-repositorio.git
```

## O que e README

O `README.md` e o arquivo inicial de explicacao do projeto.

Ele geralmente mostra:

- nome do projeto;
- objetivo;
- como instalar ou abrir;
- como usar;
- autores;
- tecnologias usadas.

## Exemplo simples de README

```md
# Nome do projeto

Descricao curta do projeto.

## Tecnologias usadas

- HTML
- CSS
- JavaScript

## Como abrir

Abra o arquivo index.html no navegador.
```

