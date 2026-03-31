# trabalho-springboot4-jpa  
[![NPM](https://img.shields.io/npm/l/react)](https://github.com/Malenia2612/trabalho-springboot4-jpa/blob/main/LICENSE)

# Sobre o projeto

Este projeto foi desenvolvido durante o curso do DevSuperior na plataforma Udemy, sendo meu primeiro contato com o ecossistema do Spring Boot.

A aplicação consiste em uma API REST construída com Java e Spring Boot, onde são realizadas operações de CRUD e testes de requisições HTTP utilizando o Postman.

Durante o desenvolvimento, foram aplicados conceitos importantes como:
- Estruturação de projetos com base nos princípios SOLID
- Modelagem utilizando diagramas URI
- Integração com banco de dados em memória H2
- Tratamento de exceções HTTP (200 OK, 204 No Content, 404 Not Found, 400 Bad Request)

O projeto tem como foco consolidar fundamentos de desenvolvimento back-end e servirá como base para futuras aplicações full stack.

## 📚 Aprendizados

Neste projeto eu aprendi:

- Estruturação de APIs REST com Spring Boot
- Uso de JPA/Hibernate para persistência de dados
- Tratamento de exceções HTTP
- Organização de código com princípios SOLID
- Testes de endpoints utilizando Postman
## Modelo de Dominio


![Domain Model](https://github.com/Malenia2612/Assets/blob/main/DomainModel.png)

## Testes da API

### Execução do projeto
![Run Spring Boot](https://github.com/Malenia2612/Assets/blob/main/foto1.png)

### Busca de usuário (GET /users/1)
Retorno com status **200 OK** e dados do usuário.  
![Get User](https://github.com/Malenia2612/Assets/blob/main/foto2get.png)

### Busca de pedidos (GET /orders/1)
Retorna os dados do cliente e seus pedidos relacionados com status **200 OK**.  
![Get Orders](https://github.com/Malenia2612/Assets/blob/main/foto2ordersGet.png)

### Tentativa de deletar usuário inexistente
Retorna status **404 Not Found** com estrutura de erro personalizada.  
![Delete Not Found](https://github.com/Malenia2612/Assets/blob/main/foto3usersDeletenotfound404.png)

### Tentativa de deletar usuário com pedidos associados
Retorna status **400 Bad Request**, impedindo a exclusão por integridade de dados.  
![Delete Bad Request](https://github.com/Malenia2612/Assets/blob/main/foto4usersDeleteBadrequestwithorders.png)

### H2 Console
Testando o banco de dados.  
![H2 Console Test](https://github.com/Malenia2612/Assets/blob/main/H2Console.png)

# Tecnologias utilizadas

## Back end
- Java 25
- Spring Boot
- JPA / Hibernate
- Maven
- H2 Database

## Ferramentas
- Postman

# Como executar o projeto

## Back end
Pré-requisitos: **Java 25**
- Spring tools for Eclipse
- Ou IDE de sua preferência
## Execução via terminal
```bash
# clonar repositório
git clone https://github.com/Malenia2612/trabalho-springboot4-jpa.git

# entrar na pasta do projeto
cd trabalho-springboot4-jpa

# executar o projeto
./mvnw spring-boot:run
```
## Execução pela IDE (Spring Tools / Eclipse)

- Clique com o botão direito no projeto  
- CourseApplication.java → Run As → Spring Boot App  

## Configuração importante

## 🌐 Endpoints

A API roda localmente em:
http://localhost:8080

Antes de executar o projeto, verifique se os arquivos de configuração estão corretos.
### application.properties
```bash
spring.application.name=course
spring.profiles.active=test
spring.jpa.open-in-view=true
```

### No H2 console configurar usuario e senha e o nome do banco de dados
## 🗄️ Banco de dados H2

Acesse o console do banco em:
http://localhost:8080/h2-console

JDBC URL: jdbc:h2:mem:testdb  
User: sa  
Password: (vazio)
### application-test.properties
```bash
# DATASOURCE
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.username=sa
spring.datasource.password=

# H2 CLIENT
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console

# JPA, SQL
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.jpa.defer-datasource-initialization=true
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
```

# Autor
## William Barcelos Rosa
🔗 LinkedIn: https://www.linkedin.com/in/william-barcelos-rosa-024b01234/
