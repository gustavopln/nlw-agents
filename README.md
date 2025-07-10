# NLW Agents - Server

Este é o backend do projeto **NLW Agents**, desenvolvido durante a 20ª edição do Next Level Week, um evento online promovido pela [Rocketseat](https://www.rocketseat.com.br/).

## Sobre o Projeto

A aplicação consiste em um servidor Node.js que gerencia a lógica de negócio e a comunicação com o banco de dados para o projeto NLW Agents.

## Tecnologias Utilizadas

O projeto foi construído utilizando uma stack moderna e performática, focada em produtividade e boas práticas de desenvolvimento:

*   **Node.js**: Ambiente de execução do JavaScript no servidor.
*   **TypeScript**: Superset do JavaScript que adiciona tipagem estática.
*   **Fastify**: Framework web focado em alta performance e baixo overhead.
*   **Drizzle ORM**: Um ORM "TypeScript-first" para interagir com o banco de dados de forma segura e tipada.
*   **PostgreSQL**: Banco de dados relacional utilizado no projeto.
*   **Zod**: Biblioteca para validação de schemas, garantindo a integridade dos dados que entram na aplicação.
*   **Biome**: Ferramenta de alta performance para lint e formatação de código, garantindo a consistência e qualidade do código.

## Setup e Configuração

Siga os passos abaixo para configurar e executar o projeto em seu ambiente local.

### Pré-requisitos

*   [Node.js](https://nodejs.org/en/) (versão 20 ou superior)
*   [NPM](https://www.npmjs.com/) ou outro gerenciador de pacotes
*   Uma instância do [PostgreSQL](https://www.postgresql.org/) rodando

### Instalação

1.  **Clone o repositório** (caso ainda não tenha feito):
    ```bash
    git clone <url-do-repositorio>
    cd nlw-agents/server
    ```

2.  **Instale as dependências**:
    ```bash
    npm install
    ```

3.  **Configure as variáveis de ambiente**:
    Crie um arquivo `.env` na raiz da pasta `server/` baseado no exemplo abaixo e preencha com as suas credenciais do banco de dados.

    **.env.example**
    ```env
    # Exemplo de URL de conexão com o PostgreSQL
    DATABASE_URL="postgresql://user:password@host:port/database"
    ```

4.  **Migrações do Banco de Dados**:
    O Drizzle Kit é utilizado para gerenciar as migrações. Para gerar uma nova migração baseada nos seus schemas, execute:
    ```bash
    npx drizzle-kit generate
    ```
    *Observação: Para aplicar as migrações, você precisará de um script adicional ou pode aplicá-las manualmente.*

## Scripts Disponíveis

No `package.json`, você encontrará os seguintes scripts:

*   **`npm run dev`**: Inicia o servidor em modo de desenvolvimento com watch mode. O servidor reiniciará automaticamente a cada alteração nos arquivos.

*   **`npm start`**: Inicia o servidor em modo de produção.

*   **`npm run db:seed`**: Executa o script para popular o banco de dados com dados iniciais (seeding).

---

Este `README.md` cobre os pontos essenciais para que outra pessoa possa entender e rodar seu projeto.


