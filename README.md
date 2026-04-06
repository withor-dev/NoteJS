# 📝 NoteJS - Dynamic Notes Platform

Uma aplicação Fullstack desenvolvida para o gerenciamento inteligente de anotações. O grande diferencial do projeto é o suporte a **campos dinâmicos**, permitindo que o usuário personalize a estrutura dos formulários e notas de acordo com a sua necessidade, além de suportar a ordenação personalizada das anotações.

## 🚀 Tecnologias Utilizadas

O projeto foi construído separando as responsabilidades entre uma Single Page Application (SPA) e uma API RESTful robusta.

**Front-end (Client):**
* **React.js (v17)** - Construção da interface de usuário baseada em componentes.
* **React Router DOM** - Gerenciamento de rotas e navegação da SPA.
* **Sass (SCSS)** - Estilização avançada e componentizada.
* **Axios** - Integração via requisições HTTP assíncronas com o Back-end.

**Back-end (API):**
* **Java 8** - Lógica de negócios e backend.
* **Spring Boot (v2.1)** - Framework base (Spring Web / MVC) para roteamento e endpoints REST.
* **Maven** - Gerenciamento de dependências e build do projeto.

**Banco de Dados:**
* **PostgreSQL** - Persistência de dados relacionais (estruturado com chaves sequenciais automáticas `SERIAL`).

---

## 🧠 Estrutura do Banco de Dados

A arquitetura de dados foi projetada para suportar a dinamicidade da aplicação:
* `users`: Gerenciamento de acessos e credenciais.
* `notes`: Armazenamento das anotações, contendo um sistema de ordenação (`ordernotes`).
* `form`: Tabela responsável pela engine de campos dinâmicos, armazenando o nome (`nameCamp`) e o tipo do campo (`typeCamp`).

---

## 🛠️ Como executar o projeto localmente

### 1. Pré-requisitos
* Node.js e npm (ou yarn)
* Java Development Kit (JDK 8)
* Apache Maven
* PostgreSQL

### 2. Setup do Banco de Dados
1. Crie um banco de dados no PostgreSQL.
2. Execute o script `NoteBD.sql` (localizado na raiz do projeto) para gerar as tabelas e popular os dados iniciais de teste.
3. Certifique-se de configurar as credenciais do seu banco de dados no arquivo `application.properties` do Spring Boot.

### 3. Rodando o Back-end (Spring Boot)
Navegue até a pasta do servidor e inicie a aplicação Maven:

```bash
cd BackEnd
mvn spring-boot:run
```
_A API estará disponível por padrão na porta 8080._

### 4. Rodando o Front-end (React)
Abra um novo terminal, navegue até a pasta do cliente, instale as dependências e inicie:

```bash
cd FrontEnd
npm install
npm start
```
_A interface estará disponível em http://localhost:3000._
