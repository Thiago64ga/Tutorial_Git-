# README de commits e boas praticas de versionamento

Este guia mostra, de forma simples e visual, como fazer bons commits e manter o historico do projeto organizado.

Use este arquivo como uma cola de consulta enquanto trabalha com Git e GitHub.

## Mapa rapido

```text
Alterei arquivos
      |
      v
Vejo o que mudou
git status
      |
      v
Escolho o que vai entrar no commit
git add .
      |
      v
Salvo a versao no Git
git commit -m "mensagem clara"
      |
      v
Envio para o GitHub
git push
```

## O que e um commit

Um commit e um ponto salvo na historia do projeto.

Imagine uma linha do tempo:

```text
Projeto vazio
    |
    v
Commit 1: cria arquivos iniciais
    |
    v
Commit 2: adiciona estilos
    |
    v
Commit 3: corrige botao
```

Cada commit deve representar uma alteracao pequena e facil de entender.

## Comandos principais

| Comando | Para que serve |
| --- | --- |
| `git status` | Mostra arquivos alterados, novos ou apagados. |
| `git add .` | Prepara todas as alteracoes para o commit. |
| `git add nome-do-arquivo` | Prepara apenas um arquivo especifico. |
| `git commit -m "mensagem"` | Cria um commit com uma mensagem. |
| `git push` | Envia os commits para o GitHub. |
| `git pull` | Baixa alteracoes que estao no GitHub. |
| `git log --oneline` | Mostra o historico de commits resumido. |

## Fluxo basico para fazer commit

Use este passo a passo no dia a dia:

```bash
git status
git add .
git status
git commit -m "mensagem explicando a alteracao"
git push
```

Por que tem `git status` duas vezes?

```text
Primeiro git status  -> vejo o que mudou
Segundo git status   -> confiro o que esta pronto para commit
```

## Mensagem de commit: boa x ruim

Uma boa mensagem responde:

```text
O que eu mudei?
```

| Mensagem ruim | Problema | Mensagem melhor |
| --- | --- | --- |
| `coisas` | Nao explica nada. | `cria estrutura inicial do projeto` |
| `teste` | Nao diz o que foi testado. | `testa envio do formulario` |
| `final` | Nao mostra o que terminou. | `finaliza pagina de contato` |
| `alteracoes` | Muito generica. | `atualiza textos do README` |
| `arruma` | Nao diz o que foi corrigido. | `corrige link do menu principal` |

## Padrao simples recomendado

Comece a mensagem com um verbo no presente:

| Verbo | Quando usar | Exemplo |
| --- | --- | --- |
| `cria` | Algo novo foi criado. | `cria pagina inicial` |
| `adiciona` | Algo foi acrescentado. | `adiciona estilos do menu` |
| `corrige` | Um erro foi resolvido. | `corrige cor do botao` |
| `remove` | Algo foi apagado. | `remove codigo nao usado` |
| `atualiza` | Algo existente mudou. | `atualiza README do projeto` |
| `organiza` | Arquivos ou codigo foram arrumados. | `organiza arquivos de estilo` |
| `melhora` | Algo ficou melhor, mas nao era erro. | `melhora layout da pagina` |

Exemplos prontos:

```bash
git commit -m "cria pagina de contato"
git commit -m "adiciona validacao do formulario"
git commit -m "corrige link do menu"
git commit -m "remove arquivo temporario"
git commit -m "atualiza instrucoes do README"
```

## Commits pequenos sao melhores

Pense no commit como uma caixa. Cada caixa deve guardar um assunto.

Bom:

```text
[Commit 1] cria pagina inicial
[Commit 2] adiciona estilos da pagina inicial
[Commit 3] corrige link do botao
```

Ruim:

```text
[Commit unico] cria pagina, muda estilo, corrige link, altera README e remove arquivo
```

Por que separar?

- fica mais facil entender o historico;
- fica mais facil achar onde um erro apareceu;
- fica mais facil explicar o que foi feito;
- fica mais facil desfazer uma mudanca especifica.

## Quando fazer commit

Faca commit quando terminar uma parte pequena e funcional.

| Momento | Exemplo de mensagem |
| --- | --- |
| Criou um arquivo importante. | `cria arquivo index.html` |
| Terminou uma tela. | `cria pagina de login` |
| Corrigiu um erro. | `corrige erro no formulario` |
| Atualizou documentacao. | `atualiza guia de instalacao` |
| Organizou arquivos. | `organiza estrutura de pastas` |
| Testou e esta funcionando. | `finaliza validacao do cadastro` |

Evite fazer commit com o projeto quebrado. Se precisar salvar uma tentativa, use uma branch separada.

## Antes de commitar

Use este checklist:

```text
[ ] Salvei os arquivos no editor?
[ ] O projeto ainda funciona?
[ ] Rodei git status?
[ ] A mensagem explica o que mudou?
[ ] Estou commitando apenas arquivos relacionados?
[ ] Nao estou enviando senha, token ou arquivo pessoal?
```

Comandos para conferir:

```bash
git status
git diff
```

Depois:

```bash
git add .
git status
git commit -m "mensagem clara"
```

## O que nao deve ir para um commit

Evite commitar:

| Tipo de arquivo | Motivo |
| --- | --- |
| Senhas | Pode expor dados importantes. |
| Chaves de API | Outra pessoa pode usar sua chave. |
| Arquivos pessoais | Nao fazem parte do projeto. |
| Arquivos temporarios | Sujam o historico. |
| Arquivos muito grandes | Deixam o repositorio pesado. |
| `node_modules/` | Pode ser recriado com instalacao de dependencias. |
| `.env` | Normalmente guarda dados secretos. |

Para ignorar arquivos, crie um arquivo chamado `.gitignore`.

Exemplo:

```gitignore
node_modules/
.env
*.log
```

## O que e versionamento

Versionamento e o controle da evolucao do projeto.

Ele ajuda a responder perguntas como:

```text
O que mudou?
Quando mudou?
Quem mudou?
Por que mudou?
Como voltar para uma versao anterior?
```

## Exemplo visual de historico

```text
main
 |
 |-- cria estrutura inicial
 |
 |-- adiciona estilos
 |
 |-- cria script principal
 |
 |-- corrige erro no botao
 |
 |-- atualiza README
```

Um historico assim e facil de ler porque cada commit tem um objetivo claro.

## Boas praticas de versionamento

| Boa pratica | Por que ajuda |
| --- | --- |
| Fazer commits pequenos. | Facilita entender e corrigir problemas. |
| Usar mensagens claras. | Deixa o historico legivel. |
| Testar antes de commitar. | Evita salvar codigo quebrado. |
| Usar branches para mudancas grandes. | Permite testar sem baguncar a `main`. |
| Dar `git pull` antes de trabalhar. | Evita conflito com alteracoes novas. |
| Dar `git push` com frequencia. | Mantem backup no GitHub. |
| Nao misturar assuntos. | Cada commit fica mais facil de revisar. |

## Fluxo recomendado para trabalhar sozinho

```text
Comecar o dia
    |
    v
git pull
    |
    v
Editar arquivos
    |
    v
git status
    |
    v
git add .
    |
    v
git commit -m "mensagem clara"
    |
    v
git push
```

Comandos:

```bash
git pull
git status
git add .
git commit -m "descreva a alteracao"
git push
```

## Fluxo recomendado para trabalhar em grupo

Quando mais pessoas trabalham no mesmo projeto, use branch.

```text
main
 |
 |-------------------------
 |                        |
 v                        v
codigo principal       minha-branch
                         |
                         v
                    meus commits
                         |
                         v
                    Pull Request
                         |
                         v
                        main
```

Comandos:

```bash
git pull
git checkout -b nome-da-sua-alteracao
git add .
git commit -m "mensagem clara"
git push -u origin nome-da-sua-alteracao
```

Depois abra um Pull Request no GitHub para juntar sua branch com a `main`.

## Nomes de branch

Use nomes simples e descritivos.

| Bom nome | Quando usar |
| --- | --- |
| `pagina-inicial` | Criacao ou alteracao da pagina inicial. |
| `formulario-contato` | Trabalho no formulario de contato. |
| `corrige-menu` | Correcao no menu. |
| `atualiza-readme` | Alteracao na documentacao. |

Evite:

```text
teste
coisas
nova
abc
branch1
```

## Exemplo completo comentado

```bash
# mostra o que foi alterado
git status

# prepara todas as alteracoes
git add .

# confere se esta tudo pronto
git status

# cria o commit
git commit -m "adiciona guia de boas praticas de commits"

# envia para o GitHub
git push
```

## Cola final

Se estiver com duvida, siga este mini roteiro:

```text
1. Salvei os arquivos?
2. Rodei git status?
3. As mudancas fazem sentido juntas?
4. Rodei git add .?
5. Escrevi uma mensagem clara?
6. Rodei git push?
```

Comando mais usado:

```bash
git status
git add .
git commit -m "mensagem clara"
git push
```

