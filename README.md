-----

# 📧 AutoU: Automação e Análise de E-mails com IA

Uma aplicação full-stack para gerenciar e classificar e-mails de forma automatizada. O projeto integra um front-end **React** e um back-end **Flask** para demonstrar a aplicação de IA em um fluxo de trabalho de e-mails.

-----

## 🚀 Funcionalidades

### **Front-end (React)**

Interface de usuário para gerenciar e-mails.

  - **Login de Convidado:** Gera e salva um `guest_id` no `localStorage`.
  - **CRUD de E-mails:** Permite **Criar**, **Visualizar**, **Editar** e **Excluir** e-mails.
  - **Visualização Inteligente:** Exibe a classificação (produtivo/improdutivo) e, para e-mails produtivos, o resumo gerado pela OpenAI.

### **Back-end (Flask)**

API RESTful que gerencia a lógica de negócios e as integrações de IA.

  - **Endpoints:**
      - `POST /guest`: Cria um novo ID de convidado.
      - `POST /emails`: Recebe um e-mail, o classifica usando um modelo do **Hugging Face** e gera um resumo com a **OpenAI**. Salva no banco de dados.
      - `GET /emails?guest_id=...`: Retorna a lista de e-mails de um usuário.
      - `PUT /emails/<id>`: Atualiza um e-mail existente.
      - `DELETE /emails/<id>`: Exclui um e-mail.
  - **Banco de Dados:** Utiliza **SQLite** para persistir os dados.

-----

## 🛠️ Tecnologias

| Área | Tecnologia |
| :--- | :--- |
| **Front-end** | `React` |
| **Back-end** | `Flask`, `Hugging Face`, `OpenAI` |
| **Banco de Dados** | `SQLite` |

-----

## ⚙️ Como Rodar Localmente

### Pré-requisitos

Certifique-se de ter instalado:

  * Python 3.x, pip
  * Node.js, npm
  * Chave de API da OpenAI

### 1\. Configurar o Back-end

1.  Navegue até o diretório `back-end`.
2.  Instale as dependências:
    ```bash
    pip install -r requirements.txt
    ```
3.  Crie um arquivo `.env` e adicione sua chave da OpenAI:
    ```
    OPENAI_API_KEY=sua_chave_aqui
    ```
4.  Execute a API:
    ```bash
    flask run
    ```

### 2\. Configurar o Front-end

1.  Navegue até o diretório `front-end`.
2.  Instale as dependências:
    ```bash
    npm install
    ```
3.  Inicie a aplicação:
    ```bash
    npm start
    ```
