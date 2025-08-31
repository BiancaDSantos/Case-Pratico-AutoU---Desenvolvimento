# Case-Pratico-AutoU---Desenvolvimento
📧 AutoU: Automação e Análise de E-mails com IA
Uma aplicação full-stack para gerenciar e classificar e-mails de forma automatizada. O projeto integra um front-end React e um back-end Flask para demonstrar a aplicação de IA em um fluxo de trabalho de e-mails.

🚀 Funcionalidades
Front-end (React): Interface de usuário para gerenciar e-mails.
Login de Convidado: Gera e salva um guest_id no localStorage para uma experiência sem cadastro.
CRUD de E-mails: Permite Criar, Visualizar, Editar e Excluir e-mails.
Visualização Inteligente: Exibe a classificação (produtivo/improdutivo) e, para e-mails produtivos, o resumo gerado pela OpenAI.
Back-end (Flask): API RESTful que gerencia a lógica de negócios e as integrações de IA.

Endpoints:
POST /guest: Cria um novo ID de convidado.
POST /emails: Recebe um e-mail, o classifica usando um modelo do Hugging Face e gera um resumo com a OpenAI se for produtivo. Salva tudo no banco de dados.
GET /emails?guest_id=...: Retorna a lista de e-mails de um usuário.
PUT /emails/<id>: Atualiza um e-mail existente.
DELETE /emails/<id>: Exclui um e-mail.

Banco de Dados: 
Utiliza SQLite para persistir os dados dos e-mails e suas classificações/resumos.

🛠️ Tecnologias
Front-end: React
Back-end: Flask, Hugging Face, OpenAI
Banco de Dados: SQLite
Ambiente: Python 3.x, Node.js

⚙️ Como Rodar Localmente
Pré-requisitos
Python 3.x, pip
Node.js, npm
Chave de API da OpenAI

1. Back-end
Navegue até o diretório back-end.
Instale as dependências: pip install -r requirements.txt.
Configure sua chave da OpenAI em um arquivo .env como OPENAI_API_KEY=sua_chave_aqui.
Execute a API: flask run.

2. Front-end
Navegue até o diretório front-end.
Instale as dependências: npm install.
Inicie a aplicação: npm start.

3. Deploy: Heroku
