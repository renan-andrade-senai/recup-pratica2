# 🎮 Avaliação Prática — Sistema de Gerenciamento de Acervo para Locadora de Games

## Contexto

Você foi contratado como desenvolvedor front-end júnior pela **GameLoc**, uma locadora de
games que deseja modernizar sua operação. Sua missão é desenvolver uma aplicação web para
que os funcionários possam gerenciar o acervo de jogos disponíveis para locação.

---

## O que você vai desenvolver

Uma aplicação Vue.js 3 com as seguintes funcionalidades:

- Visualizar todos os jogos cadastrados no acervo
- Cadastrar um novo jogo
- Editar os dados de um jogo existente
- Remover um jogo do acervo

A aplicação se comunicará com uma API simulada localmente usando o **JSON Server**.

---

## Entidade principal

### 🎮 Jogo

| Atributo        | Tipo      | Descrição                                      |
|-----------------|-----------|------------------------------------------------|
| `id`            | `number`  | Identificador único do jogo (gerado pela API)  |
| `titulo`        | `string`  | Título do jogo                                 |
| `plataforma`    | `string`  | Plataforma (PS5, Xbox Series X, Switch, PC...) |
| `genero`        | `string`  | Gênero do jogo (Ação, RPG, Esporte...)         |
| `anoLancamento` | `number`  | Ano em que o jogo foi lançado                  |
| `disponivel`    | `boolean` | Indica se o jogo está disponível para locação  |

---

## Requisitos funcionais

### 1. Navegação
- A aplicação deve ter um componente `NavBar` fixo no topo com links para as páginas principais
- Deve haver no mínimo **4 rotas** configuradas no Vue Router

### 2. Tela inicial — Home (`/`)
- Tela de boas-vindas com o nome da locadora
- Botão que leva o usuário para a página de acervo

### 3. Listagem de jogos (`/jogos`)
- Exibir todos os jogos cadastrados em uma **tabela**
- Exibir a disponibilidade de cada jogo com um **badge colorido**:
  - 🟢 Verde (`bg-success`) → "Disponível"
  - 🔴 Vermelho (`bg-danger`) → "Locado"
- Botão **Editar** que redireciona para a tela de edição do jogo selecionado
- Botão **Excluir** que remove o jogo após confirmação do usuário
- Botão para acessar a tela de **cadastro de novo jogo**
- Mensagem informativa quando o acervo estiver vazio

### 4. Cadastro de novo jogo (`/jogos/novo`)
- Formulário com campos para todos os atributos do jogo
- Ao confirmar, os dados devem ser enviados para a API via **POST**
- Redirecionar para a listagem após o cadastro

### 5. Edição de jogo (`/jogos/:id/editar`)
- O **ID do jogo** deve ser obtido via parâmetro de rota
- Os dados do jogo devem ser carregados automaticamente ao abrir a tela via **GET**
- O formulário deve ser pré-preenchido com os dados atuais do jogo
- Ao confirmar, os dados atualizados devem ser enviados via **PUT**
- Redirecionar para a listagem após salvar

---

## Tecnologias utilizadas

| Tecnologia    | Versão   | Finalidade                         |
|---------------|----------|------------------------------------|
| Vue.js 3      | ^3.4.x   | Framework front-end principal      |
| TypeScript    | ^5.x     | Tipagem estática                   |
| Vue Router 4  | ^4.x     | Navegação entre páginas            |
| Axios         | ^1.x     | Requisições HTTP para a API        |
| Bootstrap 5   | ^5.x     | Estilização e componentes visuais  |
| JSON Server   | ^0.17.x  | API simulada local                 |

---

## Como rodar o projeto

### Pré-requisitos
- Node.js instalado (versão 18 ou superior)

### Passo a passo

1. Instale as dependências:
   ```bash
   npm install
   ```

2. Em um terminal, inicie a API simulada:
   ```bash
   npm run api
   ```
   > A API ficará disponível em: `http://localhost:3000`

3. Em outro terminal, inicie a aplicação:
   ```bash
   npm run dev
   ```
   > A aplicação ficará disponível em: `http://localhost:5173`

> ⚠️ **Importante:** os dois terminais devem estar rodando ao mesmo tempo
> para que a aplicação funcione corretamente.

---

## Critérios de avaliação

| #  | Critério                                                                      | Pontos  |
|----|-------------------------------------------------------------------------------|:-------:|
| 1  | Estrutura de pastas e organização geral do projeto                            | 0,5     |
| 2  | Configuração correta do Vue Router com no mínimo 4 rotas                      | 0,5     |
| 3  | Criação de componente de navegação (`NavBar`) reutilizável                    | 0,5     |
| 4  | Definição de `interface` TypeScript paras as entidades                        | 0,5     |
| 5  | Tipagem correta de variáveis, props e funções com TypeScript                  | 1,0     |
| 6  | Uso correto do `onMounted` para carregamento inicial dos dados                | 0,5     |
| 7  | Listagem dos jogos via Axios (`GET`) com renderização em tabela               | 1,5     |
| 8  | Cadastro de novo jogo via Axios (`POST`) com formulário                       | 1,5     |
| 9  | Edição de jogo via Axios (`PUT`) com pré-carregamento dos dados no formulário | 1,0     |
| 10 | Exclusão de jogo via Axios (`DELETE`) com confirmação do usuário              | 0,5     |
| 11 | Navegação programática após operações CRUD (redirecionar após salvar/excluir) | 0,5     |
| 12 | Uso de parâmetro de rota para identificar o jogo a ser editado                | 0,5     |
| 13 | Estilização geral com Bootstrap (layout, tabelas, formulários e botões)       | 1,0     |
|    | **Total**                                                                     | **10,0**|

---

## Instruções de entrega

1. Crie um repositório **público** no GitHub com o nome exato:
   ```
   avaliacao-vue-locadora-games
   ```

2. Faça o commit de todos os arquivos do projeto.
   > ⚠️ **Não suba a pasta `node_modules`!**
   > Certifique-se de que o arquivo `.gitignore` está presente no projeto.

3. O repositório deve conter um arquivo `README.md` com:
   - Seu **nome completo** e **turma**
   - Instruções de como rodar o projeto localmente (`npm install`, `npm run api`, `npm run dev`)

4. Envie o **link do repositório** no campo indicado pelo instrutor.

> ✅ Antes de entregar, verifique se:
> - O repositório está **público**
> - O projeto **roda corretamente** após um `npm install` em uma pasta limpa
> - O `README.md` com seus dados está presente

---

## Observações importantes

- ✏️ Esta é uma avaliação **individual**. Não é permitido compartilhar ou copiar
  código de colegas.
- 📚 É permitido consultar a **documentação oficial** do Vue.js, Vue Router,
  Axios e Bootstrap.
- 📁 O arquivo `db.json` já está configurado com dados iniciais.
  Você **não** precisa criar nem modificar a API.
- ⏱️ Gerencie bem o seu tempo — comece pelas partes que você tem mais domínio.
- 🔍 Leia **todos os requisitos** antes de começar a implementar.

# Imagens
![home](home.png)
![lista](lista.png)
![novo](novo.png)
![editar](editar.png)
