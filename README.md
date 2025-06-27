
🔐 AuthServer - API de Autenticação com JWT
Este projeto é uma API de autenticação simples desenvolvida em Java 17 com Spring Boot, utilizando JWT (JSON Web Token) para autenticação e autorização de endpoints protegidos.

A aplicação oferece:
✅ Registro de usuários
✅ Login com geração de token JWT
✅ Proteção de endpoints com autenticação via token
✅ Documentação da API com Swagger

⚙️ Tecnologias Utilizadas
Java 17

Spring Boot

Spring Web

Spring Security

Spring Data JPA

H2 Database (banco de dados em memória para desenvolvimento)

Lombok

Swagger/OpenAPI para documentação interativa

JWT (Auth0 - java-jwt) para autenticação stateless

🚀 Executando o Projeto Localmente
Pré-requisitos
Java JDK 17 ou superior

Maven 3.8 ou superior

Passos
Clone o repositório:

bash
Copiar
Editar
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio
Execute o projeto:

bash
Copiar
Editar
./mvnw spring-boot:run
A aplicação estará rodando em:
📍 http://localhost:8080

Console do H2 (opcional)
URL: http://localhost:8080/h2-console

JDBC URL: jdbc:h2:mem:testdb

Usuário: sa

Senha: password

📖 Endpoints
📌 Autenticação
Método	Endpoint	Descrição	Exemplo de Corpo (JSON)
POST	/auth/register	Registra um novo usuário	{"login": "user", "password": "123"}
POST	/auth/login	Autentica e retorna um token JWT	{"login": "user", "password": "123"}

🔒 Endpoints Protegidos
Método	Endpoint	Descrição
GET	/test/protected	Retorna mensagem apenas se autenticado

Importante: Para acessar endpoints protegidos, envie o token JWT no cabeçalho da requisição:

http
Copiar
Editar
Authorization: Bearer SEU_TOKEN_JWT
📝 Documentação Interativa
Acesse o Swagger para visualizar e testar os endpoints:
http://localhost:8080/swagger-ui/index.html

💡 Considerações
Este projeto é uma base simples de autenticação, ideal para:
✅ Estudos de Spring Security e JWT
✅ Início de projetos que exijam segurança básica
✅ Demonstração de autenticação stateless com tokens
