
# Título do Projeto

# DSList

DSList é uma aplicação backend construída com Java e Spring Boot que permite gerenciar uma lista de jogos.  
Este projeto foi desenvolvido durante o evento **Semana DevSuperior 2.0**.

## Funcionalidades

- Listar todos os jogos disponíveis.
- Visualizar detalhes de um jogo específico.
- Organizar jogos em listas personalizadas.

## Tecnologias Utilizadas

- Java 17
- Spring Boot 3.0.2
- Maven
- Banco de dados H2

## Pré-requisitos

- Java Development Kit (JDK) 17 ou superior instalado.
- Maven instalado.

## Como Executar o Projeto

1. **Clone o repositório:**

```bash
git clone https://github.com/c4uan/dslist.git
```


2. **Navegue até o diretório do projeto:**
```bash
cd dslist
```

3. **Compile o projeto usando o maven:**
```bash
mvn clean install
```

4. **Execute a aplicação:**
```bash
mvn spring-boot:run
```


5. A aplicação estará disponível em `http://localhost:8080`.

## Estrutura do Projeto

O projeto segue a estrutura padrão do Spring Boot:

- `src/main/java/com/devsuperior/dslist`: Contém o código-fonte da aplicação.
- `src/main/resources`: Contém os recursos estáticos e arquivos de configuração.

## Endpoints Principais

- `GET /games`: Retorna a lista de todos os jogos.
- `GET /games/{id}`: Retorna os detalhes de um jogo específico.
- `GET /lists`: Retorna todas as listas de jogos.
- `POST /lists`: Cria uma nova lista de jogos.

## Banco de Dados

A aplicação utiliza dois bancos de dados, dependendo do ambiente:

- **H2**: Utilizado em memória para testes e desenvolvimento local.  
  Configuração padrão do H2 permite acessar o console web em `http://localhost:8080/h2-console` com as seguintes credenciais:
  
  - **URL JDBC**: `jdbc:h2:mem:testdb`
  - **Usuário**: `sa`
  - **Senha**: *(deixe em branco)*

- **PostgreSQL**: Utilizado para o armazenamento em produção. A configuração do banco PostgreSQL deve ser feita no arquivo de propriedades da aplicação, normalmente localizado em `src/main/resources/application.properties` ou `src/main/resources/application.yml`.

Exemplo de configuração para PostgreSQL:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/seu_banco
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=update
```


## Autor

Projeto em desenvolvido por [c4uan](https://github.com/c4uan) durante a Semana DevSuperior 2.0.





