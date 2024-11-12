# Projeto TECH - Autenticação com GitHub usando OAuth 2.0

## Descrição

Este projeto é uma aplicação web desenvolvida em Django que utiliza OAuth 2.0 para autenticar usuários via GitHub. A aplicação permite que os usuários façam login com suas contas do GitHub e, em seguida, acessam conteúdos protegidos na aplicação. Esse projeto é ideal para entender como implementar uma integração de autenticação via GitHub usando OAuth 2.0 no Django.

## Estrutura do Projeto

```
TECH/
├── core/                # Contém as configurações principais do Django
├── tech/                # Aplicação principal do projeto
├── templates/           # Arquivos HTML para o frontend
├── venv/                # Ambiente virtual Python (não incluso no repositório)
├── .env                 # Variáveis de ambiente (configurações sensíveis)
├── .gitignore           # Arquivos e pastas ignorados pelo Git
├── db.sqlite3           # Banco de dados SQLite para desenvolvimento
├── manage.py            # Script de gerenciamento do Django
└── requirements.txt     # Dependências do projeto
```

## Pré-requisitos

- Python 3.12 ou superior
- Ambiente virtual Python configurado (recomendado)
- Conta no GitHub e um OAuth App configurado para obter o **Client ID** e **Client Secret**

## Configuração do Projeto

1. Clone o repositório:

   ```bash
   git clone https://github.com/PedroTomasini/tech-oauth2.0.git
   cd tech-oauth2.0
   ```

2. Crie um ambiente virtual e ative-o:

   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Instale as dependências:

   ```bash
   pip install -r requirements.txt
   ```

4. Configure as variáveis de ambiente:

   - Crie um arquivo `.env` na raiz do projeto com as seguintes variáveis:

     ```plaintext
     CLIENT_ID=seu_client_id_do_github
     CLIENT_SECRET=seu_client_secret_do_github
     ```

5. Realize as migrações para configurar o banco de dados:

   ```bash
   python manage.py migrate
   ```

6. Execute o servidor de desenvolvimento:

   ```bash
   python manage.py runserver
   ```

7. Acesse a aplicação em `http://127.0.0.1:8000`.

## Funcionalidades

- **Autenticação via GitHub**: O usuário pode fazer login na aplicação usando sua conta GitHub. O OAuth 2.0 permite autenticação segura, sem que a aplicação precise acessar diretamente a senha do usuário.

## Arquivo .env

Para proteger informações sensíveis, como `CLIENT_ID` e `CLIENT_SECRET`, o projeto utiliza o arquivo `.env` com a biblioteca `python-dotenv`. Certifique-se de que o `.env` está incluído no `.gitignore` para que ele não seja compartilhado publicamente.

## Contribuição

Se desejar contribuir para o projeto, crie um fork, faça suas alterações em uma nova branch e envie um pull request.

## Licença

Este projeto está licenciado sob a licença MIT.
