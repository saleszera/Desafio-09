<div  align="center">
	<h2>Desafio 09: Relacionamentos com banco de dados no Node.js</h1>
</div>


<p  align="center">

<a  href="#-sobre-o-projeto">Sobre</a> •

<a  href="#%EF%B8%8F-funcionalidades">Funcionalidades</a> •

<a  href="#-como-executar-o-projeto">Como executar</a> •

<a  href="#-tecnologias">Tecnologias</a> •

<a  href="#%EF%B8%8F-captura-de-tela">Captura de tela</a> •

</p>


## 💻 Sobre o projeto

Esta aplicação tem como objetivo por em pratica oque foi aprendido em aula, como injeção de dependências e relacionamento entre tabelas utilizando migrations.

Projeto desenvolvido durante o **BootCamp - GoStack** da Rocketseat

O GoStack é uma experiência online com muito conteúdo prático, desafios e hacks onde o conteúdo fica disponível durante uma semana.

---

## ⚙️ Funcionalidades

O usuário pode:

- [x] Cadastrar customers (clientes).
- [x] Cadastrar products (produtos)
- [x] Cadastrar orders (pedidos)
- [x] Listar orders pelo ID de um determinado customer

---

## 🚀 Como executar o projeto

### Pré-requisitos

Antes de começar, você vai precisar ter instalado em sua máquina as seguintes ferramentas:

- **[Git](https://git-scm.com)**
- **[Yarn](https://yarnpkg.com/getting-started/install)**
- **[Docker](https://www.docker.com/get-started)**
- **[Postgres + Docker](https://hub.docker.com/_/postgres)**

Além disto é bom ter um editor para trabalhar com o código como [VSCode](https://code.visualstudio.com/)

💡Para executar o projeto certifique-se de ter um banco de dados com a seguinte configuração:
```json
"port":  5432, // porta
"username":  "postgres", // usuário
"password":  "docker", // senha
"database":  "gostack_desafio09", // nome do banco de dados
```

### 🧭 Rodando a aplicação

```bash
# Clone este repositório
$ git clone clone https://github.com/saleszera/Desafio-09.git

# Acesse a pasta do projeto no seu terminal/cmd
$ cd Desafio-09

# Instale as dependências
$ yarn

# Execute as migrations
$ yarn typeorm migration:run

# Execute a aplicação
$ yarn dev:server
```

###  👨‍💻️Testando a aplicação
1. Criar customers:
>  - Crie uma requisição do tipo POST para a rota ```http://localhost:3333/customers```
>   - O corpo da requisição deverá ser enviado no formato JSON e deve ter o seguinte conteúdo:
>   ```json
>   "name": "nome do cliente",
>   "email": "email do cliente"
>   ```
>   Após enviar a requisição será retornado os dados do cliente criado
2. Criar products:
>  - Crie uma requisição do tipo POST para a rota ```http://localhost:3333/products```
>   - O corpo da requisição deverá ser enviado no formato JSON e deve ter o seguinte conteúdo:
>   ```json
>   "name": "nome do produto",
>   "price": 20.00, // valor do produto
>   "quantity": 1 // quantidade de produtos
>   ```
>   Após enviar a requisição será retornado os dados do produto criado
3. Criar orders:
>  - Crie uma requisição do tipo POST para a rota ```http://localhost:3333/orders```
>   - O corpo da requisição deverá ser enviado no formato JSON e deve ter o seguinte conteúdo:
>   ```json
>   "customer_id": "ID do cliente",
>   "products": [
>   {
>   "id": "ID do produto",
>   "quantity": 1 // quantidade de produtos
>   }
>   ]
>   ```
>   Após enviar a requisição será retornado os dados da ordem criada.
>   **Observação**: Caso o produto informado não exista ou caso não haja um saldo compatível com a quantidade informada, será retornado um erro.
4. Buscar ordens
>  - Crie uma requisição do tipo GET para a rota ```http://localhost:3333/(ID da ordem)```
>   Após enviar a requisição será retornado os dados da ordem.
>   **Observação**: Caso o ID não exista será retornado um erro

---
## 🛠 Tecnologias


As seguintes ferramentas foram usadas na construção do projeto:


- **[Node.js](https://nodejs.org/en/) + [TypeScript](https://www.typescriptlang.org/)**
- **[Express](https://github.com/expressjs/express)**
- **[Typeorm](https://typeorm.io/#/using-ormconfig)**
- **[Tsyringe](https://github.com/microsoft/tsyringe#tsyringe)**

> Veja o arquivo [package.json](https://github.com/saleszera/Fundamentos-React-Native/blob/master/package.json)


#### **Utilitários**

- Code Linting:  **[ESLint](https://eslint.org/)**,  **[Prettier](https://prettier.io/docs/en/integrating-with-linters.html)**

- Editor: **[Visual Studio Code](https://code.visualstudio.com/)** → Extensions: **[EditorConfig for VS Code](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)**

- Markdown: **[StackEdit](https://stackedit.io/)**

---
### 🎥️ Captura de tela
  <div align="center">
	  <img src="https://live.staticflickr.com/65535/50909322658_925e3e7cfa_b.jpg" width="957" height="533" alt="desafio09"/> 
  </div>

---

Feito com ❤️ por Raniery Sales 👋🏽 [Entre em contato!](https://www.linkedin.com/in/raniery-sales/)

---
