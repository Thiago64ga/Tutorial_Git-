# Guia de ajuda do projeto

Este repositório serve como uma base simples para aprender e consultar comandos de Git e GitHub.

Ele foi pensado para uma pessoa iniciante, que sabe criar uma conta no GitHub, criar um repositório e fazer commits, mas ainda precisa de ajuda para lembrar os passos e entender o que cada comando faz.

## Arquivos deste guia

- [GUIA-GIT-COMANDOS.md](GUIA-GIT-COMANDOS.md): comandos principais do Git pelo terminal.
- [GUIA-GITHUB.md](GUIA-GITHUB.md): como criar repositório, enviar arquivos e trabalhar pelo site do GitHub.
- [GUIA-GITHUB-DESKTOP.md](GUIA-GITHUB-DESKTOP.md): passo a passo usando o GitHub Desktop.
- [README-COMMITS-E-VERSIONAMENTO.md](README-COMMITS-E-VERSIONAMENTO.md): como fazer bons commits e manter boas praticas de versionamento.
- [PROBLEMAS-COMUNS.md](PROBLEMAS-COMUNS.md): erros comuns e como resolver.

## Ordem recomendada de leitura

1. Leia primeiro o [GUIA-GITHUB.md](GUIA-GITHUB.md).
2. Depois veja o [GUIA-GIT-COMANDOS.md](GUIA-GIT-COMANDOS.md).
3. Se preferir usar programa com interface visual, leia o [GUIA-GITHUB-DESKTOP.md](GUIA-GITHUB-DESKTOP.md).
4. Leia o [README-COMMITS-E-VERSIONAMENTO.md](README-COMMITS-E-VERSIONAMENTO.md) para aprender boas praticas de commits.
5. Quando aparecer erro, consulte o [PROBLEMAS-COMUNS.md](PROBLEMAS-COMUNS.md).

## Resumo rapido do fluxo com Git

O fluxo mais comum de trabalho e:

```bash
git status
git add .
git commit -m "mensagem explicando a alteracao"
git push
```

Explicando:

- `git status`: mostra o que foi alterado.
- `git add .`: prepara todas as alteracoes para o commit.
- `git commit -m "mensagem"`: salva um ponto na historia do projeto.
- `git push`: envia os commits para o GitHub.

## Dica importante

Faca commits pequenos e com mensagens claras. Isso ajuda muito quando voce precisar entender o que mudou no projeto.

Exemplos bons:

```bash
git commit -m "cria estrutura inicial do site"
git commit -m "adiciona estilos da pagina inicial"
git commit -m "corrige link do menu"
```

Exemplo ruim:

```bash
git commit -m "coisas"
```
