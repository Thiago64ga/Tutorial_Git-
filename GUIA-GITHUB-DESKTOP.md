# Guia do GitHub Desktop

GitHub Desktop e um programa com interface visual para usar Git e GitHub sem precisar digitar todos os comandos no terminal.

## Quando usar GitHub Desktop

Use GitHub Desktop se voce prefere:

- ver os arquivos modificados em uma tela;
- escrever commits por uma interface;
- clonar repositorios sem terminal;
- enviar alteracoes com botao;
- evitar memorizar comandos no inicio.

Mesmo usando GitHub Desktop, e bom entender o significado de `commit`, `push`, `pull` e `branch`.

## Instalar

1. Acesse `https://desktop.github.com`.
2. Baixe o instalador.
3. Instale o programa.
4. Abra o GitHub Desktop.
5. Faca login com sua conta do GitHub.

## Clonar um repositorio

Clonar significa baixar um repositorio do GitHub para o computador.

1. Abra o GitHub Desktop.
2. Clique em `File`.
3. Clique em `Clone repository`.
4. Escolha a aba `GitHub.com`.
5. Selecione o repositorio.
6. Em `Local path`, escolha onde ele ficara salvo.
7. Clique em `Clone`.

Depois disso, a pasta do projeto aparecera no seu computador.

## Criar um repositorio novo pelo GitHub Desktop

1. Abra o GitHub Desktop.
2. Clique em `File`.
3. Clique em `New repository`.
4. Preencha:
   - `Name`: nome do repositorio;
   - `Description`: descricao curta;
   - `Local path`: local onde a pasta sera criada;
   - `Initialize this repository with a README`: marque se quiser criar um README.
5. Clique em `Create repository`.

Nesse momento o repositorio existe no seu computador, mas ainda pode nao estar publicado no GitHub.

## Publicar no GitHub

Depois de criar o repositorio no GitHub Desktop:

1. Clique em `Publish repository`.
2. Confira o nome.
3. Escolha se sera publico ou privado.
4. Clique em `Publish repository`.

Agora o repositorio tambem existe na sua conta do GitHub.

## Fazer commit no GitHub Desktop

1. Altere ou crie arquivos na pasta do projeto.
2. Volte para o GitHub Desktop.
3. Veja a lista de arquivos modificados no lado esquerdo.
4. Confira as alteracoes.
5. No campo `Summary`, escreva uma mensagem curta.
6. Se quiser, escreva mais detalhes em `Description`.
7. Clique em `Commit to main`.

Exemplos de mensagens:

```text
adiciona pagina inicial
cria arquivo de estilos
corrige titulo da pagina
```

## Enviar commits para o GitHub

Depois de fazer commit, clique em:

```text
Push origin
```

Isso envia seus commits para o GitHub.

## Baixar alteracoes do GitHub

Clique em:

```text
Fetch origin
```

Se houver alteracoes para baixar, o GitHub Desktop mostrara a opcao:

```text
Pull origin
```

Clique em `Pull origin` para trazer as alteracoes para o computador.

## Fluxo normal no GitHub Desktop

1. Abra o projeto.
2. Altere os arquivos.
3. Veja as mudancas no GitHub Desktop.
4. Escreva uma mensagem no campo `Summary`.
5. Clique em `Commit to main`.
6. Clique em `Push origin`.

Esse e o fluxo mais comum.

## Como abrir a pasta do projeto

No GitHub Desktop:

1. Clique em `Repository`.
2. Clique em `Show in Explorer`.

Isso abre a pasta do projeto no Windows.

## Como abrir no VS Code

Se o VS Code estiver instalado:

1. Clique em `Repository`.
2. Clique em `Open in Visual Studio Code`.

## Branch no GitHub Desktop

Branch e uma linha separada de trabalho.

Para criar:

1. Clique no menu de branch, perto do topo da janela.
2. Clique em `New branch`.
3. Digite o nome da branch.
4. Clique em `Create branch`.

Para trocar:

1. Clique no menu de branch.
2. Escolha a branch desejada.

## Pull request pelo GitHub Desktop

Pull request e um pedido para juntar alteracoes de uma branch em outra.

1. Faca commits na sua branch.
2. Clique em `Push origin`.
3. Clique em `Create Pull Request`.
4. O navegador abrira o GitHub.
5. Escreva um titulo e uma descricao.
6. Clique em `Create pull request`.

## Dicas para iniciantes

- Sempre leia a lista de arquivos antes de fazer commit.
- Escreva mensagens claras.
- Use `Push origin` depois de fazer commits.
- Use `Fetch origin` antes de comecar a trabalhar, principalmente em projetos com mais pessoas.
- Se aparecer erro, leia a mensagem com calma e consulte o arquivo [PROBLEMAS-COMUNS.md](PROBLEMAS-COMUNS.md).

