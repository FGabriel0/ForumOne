# Fórum Alura com a Oracle - Spring Boot e MySQL

Este é um projeto de um fórum desenvolvido utilizando **Spring Boot** como framework de backend e **MySQL** como banco de dados. O objetivo do projeto é fornecer uma aplicação básica onde usuários possam criar tópicos, comentar e interagir em uma interface RESTful.

## Funcionalidades

- Cadastro e autenticação de usuários.
- CRUD de tópicos (Criar, Ler, Atualizar e Excluir).
- CRUD de comentários em tópicos.
- Organização dos tópicos por categorias.
- Sistema de validação e tratamento de erros.
- Integração com MySQL para persistência de dados.

## Tecnologias Utilizadas

<div align="center">
	<code><img width="50" src="https://raw.githubusercontent.com/marwin1991/profile-technology-icons/refs/heads/main/icons/postman.png" alt="Postman" title="Postman"/></code>
	<code><img width="50" src="https://raw.githubusercontent.com/marwin1991/profile-technology-icons/refs/heads/main/icons/java.png" alt="Java" title="Java"/></code>
	<code><img width="50" src="https://raw.githubusercontent.com/marwin1991/profile-technology-icons/refs/heads/main/icons/spring.png" alt="Spring" title="Spring"/></code>
	<code><img width="50" src="https://raw.githubusercontent.com/marwin1991/profile-technology-icons/refs/heads/main/icons/spring_boot.png" alt="Spring Boot" title="Spring Boot"/></code>
	<code><img width="50" src="https://raw.githubusercontent.com/marwin1991/profile-technology-icons/refs/heads/main/icons/maven.png" alt="Maven" title="Maven"/></code>
	<code><img width="50" src="https://raw.githubusercontent.com/marwin1991/profile-technology-icons/refs/heads/main/icons/hibernate.png" alt="Hibernate" title="Hibernate"/></code>
</div>

## Pré-requisitos

Certifique-se de que as seguintes ferramentas estão instaladas:

- **Java JDK 17** ou superior
- **MySQL** (ou MariaDB)
- **Maven**
- Uma IDE como IntelliJ IDEA ou Eclipse (opcional)

## Configuração do Ambiente

1. Clone este repositório:
   ```bash
   git clone https://github.com/FGabriel0/ForumOne.git
   cd forum-spring-boot

2. **Configure o banco de dados:**
   - Crie um banco chamado `forumhub`.
   - Atualize as configurações no arquivo `application.properties` ou `application.yml`.

3. **Execute as migrações do Flyway:**
   ```bash
   mvn flyway:migrate
   ```

4. **Compile e inicie a aplicação:**
   ```bash
   mvn spring-boot:run
   ```

5. **Acesse a documentação interativa:**
   - URL: `http://localhost:8080/swagger-ui.html`

---

## Endpoints de Acesso

- **POST /login:** Gera um token JWT para autenticação.
- **GET /usuarios:** Lista todos os usuários cadastrados.
- **POST /usuarios:** Registra um novo usuário.
- **PUT /usuarios:** Atualiza nome e senha do usuário autenticado.
- **DELETE /usuarios:** Realiza um delete lógico, tornando o usuário inativo.
- **GET /usuarios/topicos:** Lista os tópicos criados pelo usuário autenticado, paginados em 10 itens.

- **GET /topicos:** Lista todos os tópicos do fórum, paginados em 10 itens.
- **POST /topicos:** Cria um novo tópico.
- **GET /topicos/{id}:** Detalha um tópico específico.
- **PUT /topicos/{id}:** Atualiza um tópico pelo ID (se criado pelo usuário autenticado).
- **DELETE /topicos/{id}:** Exclui um tópico pelo ID (se criado pelo usuário autenticado).

- **POST /respostas/{id}:** Adiciona uma resposta a um tópico. Atualiza o status do tópico automaticamente.
- **PUT /respostas/{id}:** Atualiza uma resposta específica pelo ID.
- **DELETE /respostas/{id}:** Remove uma resposta pelo ID. Caso seja a última resposta, o status do tópico retorna para `NAO_RESPONDIDO`.

> Consulte a documentação do Swagger para mais detalhes sobre os dados enviados e recebidos em cada endpoint.

---

## Contribuições
Contribuições são bem-vindas! Sinta-se à vontade para abrir uma issue ou enviar um pull request.



