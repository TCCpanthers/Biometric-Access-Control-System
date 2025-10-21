# 💻 Backend (TypeScript/Node.js)

Este diretório contém o código-fonte do **Backend** do Sistema de Controle de Acesso Biométrico. Ele é responsável pela lógica de negócios, comunicação com o banco de dados (via **Prisma ORM**) e exposição da **API RESTful** para o frontend e outros serviços.

O backend é construído utilizando **TypeScript** e **Node.js** com o framework **Fastify**, garantindo alta performance e escalabilidade.

## ⚙️ Tecnologias Principais

| Tecnologia | Descrição |
| :--- | :--- |
| **TypeScript** | Linguagem de programação que adiciona tipagem estática ao JavaScript, melhorando a manutenibilidade e a detecção de erros em tempo de desenvolvimento. |
| **Node.js** | Ambiente de execução JavaScript assíncrono e orientado a eventos, ideal para construir APIs rápidas e escaláveis. |
| **Fastify** | Framework web rápido e de baixo overhead para Node.js, focado em fornecer a melhor experiência de desenvolvedor com o mínimo de sobrecarga. |
| **Prisma ORM** | Moderno ORM (Object-Relational Mapper) para Node.js e TypeScript, utilizado para interagir de forma segura e tipada com o banco de dados **PostgreSQL**. |
| **Zod** | Biblioteca de validação de esquemas, usada para garantir que os dados de entrada (como requisições HTTP) estejam no formato esperado. |

## 🚀 Como Executar

### Pré-requisitos

Certifique-se de ter instalado:

1.  **Node.js** (versão 20 ou superior)
2.  **npm** (gerenciador de pacotes)
3.  **PostgreSQL** (servidor de banco de dados)

### Passos

1.  **Navegue para o diretório do Backend:**
    ```bash
    cd backend
    ```

2.  **Instale as dependências:**
    ```bash
    npm install
    ```

3.  **Configure as variáveis de ambiente:**
    Crie um arquivo `.env` na raiz do diretório `backend` (pode usar o `.env-example` como base) e configure a string de conexão com o banco de dados:
    ```env
    # Exemplo de configuração de conexão com o PostgreSQL
    DATABASE_URL="postgresql://USUARIO:SENHA@HOST:PORTA/NOME_DO_BANCO?schema=public"
    ```

4.  **Execute as Migrações do Banco de Dados:**
    O Prisma irá criar as tabelas necessárias no seu banco de dados.
    ```bash
    npx prisma migrate dev --name init
    ```

5.  **Inicie o Servidor de Desenvolvimento:**
    O servidor será iniciado e reiniciado automaticamente ao detectar alterações no código-fonte (`src/`).
    ```bash
    npm run dev
    ```

O servidor estará acessível em `http://localhost:3333` (porta padrão, pode ser alterada no `.env`). A documentação da API (Swagger/OpenAPI) estará disponível em `http://localhost:3333/docs`.

---

[Voltar para o README Principal](../README.md)

