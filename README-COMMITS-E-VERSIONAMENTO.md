# README de commits e boas praticas de versionamento

Este guia explica como fazer commits melhores e manter um historico de versoes organizado.

## O que e um commit

Um commit e um registro de uma alteracao no projeto.

Pense nele como um ponto salvo na historia do codigo. Se algo der errado depois, os commits ajudam a entender o que mudou e quando mudou.

## Fluxo basico para fazer commit

Antes de fazer commit, veja o que foi alterado:

```bash
git status
```

Prepare os arquivos:

```bash
git add .
```

Crie o commit:

```bash
git commit -m "mensagem explicando a alteracao"
```

Envie para o GitHub:

```bash
git push
```

## Como escrever uma boa mensagem de commit

Uma boa mensagem deve dizer claramente o que foi feito.

Exemplos bons:

```bash
git commit -m "cria estrutura inicial do projeto"
git commit -m "adiciona estilos da pagina principal"
git commit -m "corrige erro no menu de navegacao"
git commit -m "atualiza README com instrucoes de uso"
```

Exemplos ruins:

```bash
git commit -m "coisas"
git commit -m "alteracoes"
git commit -m "final"
git commit -m "teste"
```

## Padrao simples recomendado

Use verbos no presente:

- `cria`
- `adiciona`
- `corrige`
- `remove`
- `atualiza`
- `organiza`
- `melhora`

Exemplos:

```bash
git commit -m "cria pagina de contato"
git commit -m "adiciona validacao do formulario"
git commit -m "corrige cor do botao principal"
git commit -m "remove codigo nao utilizado"
git commit -m "atualiza textos do README"
```

## Commits pequenos sao melhores

Evite colocar muitas alteracoes diferentes no mesmo commit.

Melhor:

```text
Commit 1: cria pagina inicial
Commit 2: adiciona estilos da pagina inicial
Commit 3: corrige link do botao
```

Pior:

```text
Commit unico: cria pagina, muda estilo, corrige link, altera README e remove arquivo
```

Commits pequenos ajudam a entender o historico e facilitam corrigir erros.

## Quando fazer commit

Faca commit quando terminar uma parte pequena e funcional.

Bons momentos para commitar:

- depois de criar um arquivo importante;
- depois de terminar uma tela;
- depois de corrigir um erro;
- depois de atualizar a documentacao;
- antes de tentar uma mudanca grande;
- depois de testar e ver que esta funcionando.

Evite fazer commit com codigo quebrado, a menos que seja uma branch de teste e voce saiba o que esta fazendo.

## Antes de commitar

Confira:

```bash
git status
```

Veja se os arquivos listados fazem sentido.

Se quiser ver detalhes das mudancas:

```bash
git diff
```

Depois prepare os arquivos:

```bash
git add .
```

Confira novamente:

```bash
git status
```

Entao faca o commit:

```bash
git commit -m "mensagem clara"
```

## Nao coloque arquivos desnecessarios no commit

Evite commitar:

- senhas;
- chaves de API;
- arquivos pessoais;
- arquivos temporarios;
- arquivos muito grandes sem necessidade;
- pastas de dependencias, como `node_modules`.

Para ignorar arquivos, use um arquivo chamado `.gitignore`.

Exemplo de `.gitignore`:

```gitignore
node_modules/
.env
*.log
```

## O que e versionamento

Versionamento e o controle da evolucao do projeto.

Com ele, voce consegue:

- ver o historico de alteracoes;
- voltar para uma versao anterior;
- trabalhar com outras pessoas;
- testar ideias em branches;
- entender quem alterou cada parte do projeto.

## Boas praticas de versionamento

1. Faca commits pequenos e frequentes.
2. Use mensagens claras.
3. Teste antes de commitar.
4. Use branches para mudancas grandes.
5. Atualize o repositorio antes de comecar a trabalhar.
6. Envie seus commits para o GitHub com frequencia.
7. Nao misture assuntos diferentes no mesmo commit.

## Fluxo recomendado para trabalhar sozinho

Antes de comecar:

```bash
git status
git pull
```

Durante o trabalho:

```bash
git status
git add .
git commit -m "descreva a alteracao"
```

Ao terminar:

```bash
git push
```

## Fluxo recomendado para trabalhar em grupo

Antes de comecar:

```bash
git pull
git status
```

Crie uma branch:

```bash
git checkout -b nome-da-sua-alteracao
```

Faca commits normalmente:

```bash
git add .
git commit -m "mensagem clara"
```

Envie a branch:

```bash
git push -u origin nome-da-sua-alteracao
```

Depois abra um Pull Request no GitHub para juntar sua branch com a `main`.

## Exemplo de nomes de branch

Use nomes simples e descritivos:

```text
pagina-inicial
formulario-contato
corrige-menu
atualiza-readme
```

Evite:

```text
teste
coisas
nova
abc
```

## Checklist antes do commit

Antes de fazer commit, pergunte:

- O codigo esta salvo?
- O projeto ainda funciona?
- A mensagem do commit explica o que mudou?
- Estou commitando apenas arquivos relacionados?
- Nao estou enviando senha ou arquivo pessoal?

## Exemplo completo

```bash
git status
git add .
git status
git commit -m "adiciona guia de boas praticas de commits"
git push
```

Esse e um bom fluxo para usar no dia a dia.

