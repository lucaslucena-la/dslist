<h1 align="center">🕹️ DSList - Catálogo de Jogos</h1>

<p align="center">
  Projeto desenvolvido no <strong>Intensivão Java Spring</strong> da <a href="https://devsuperior.com.br" target="_blank">DevSuperior</a> 🚀
</p>

## 🖥️ Sobre o projeto

O **DSList** é uma aplicação backend construída com Java e Spring Boot, que fornece uma API REST para gerenciamento de uma lista de jogos. O sistema permite:

- Listar todos os jogos
- Listar as coleções de jogos (GameLists)
- Consultar jogos por coleção
- Reordenar a posição dos jogos em uma lista

## 📷 Layout da API (Postman)

![GET /games](https://raw.githubusercontent.com/devsuperior/java-spring-dslist/main/resources/1.png)

### ✅ Exemplo de resposta para `/games`
```json
[
  {
    "id": 1,
    "title": "The Witcher 3: Wild Hunt",
    "year": 2015,
    "imgUrl": "...",
    "shortDescription": "..."
  }
]
```

### 🔄 Reordenação com `/lists/{listId}/replacement`
```json
{
  "sourceIndex": 3,
  "destinationIndex": 1
}
```

## 🛠️ Tecnologias utilizadas

- Java 21
- Spring Boot
- Spring Data JPA
- H2 Database
- Postman
- Maven

## 📚 Conteúdos abordados

### Aula 1 – Estrutura inicial
- Conceitos de APIs RESTful
- Criação do projeto com Maven
- Entidade `Game`
- Banco de dados H2
- DTOs, Repositories, Services e Controllers

### Aula 2 – Relacionamentos e SQL
- Relacionamento N:N com `GameList` e `Belonging`
- Uso de `@EmbeddedId`
- Consulta SQL com `@Query(nativeQuery = true)`
- Interface `GameMinProjection`

### Aula 3 – Homologação e CORS
- Perfis de aplicação (`test`, `dev`, `prod`)
- Preparação para deploy (opcional)
- Configuração de CORS
- Estratégias de CI/CD com Railway (teórico)

### Aula 4 – Endpoint especial
- Endpoint `POST /lists/{listId}/replacement`
- Atualização de posição com `@Modifying` e `@Transactional`
- Boas práticas com SQL e idempotência

## 🧪 Como executar o projeto

### Pré-requisitos:
- Java 17 ou superior
- Maven

```bash
# clonar repositório
git clone https://github.com/seuusuario/dslist.git

# entrar na pasta do projeto
cd dslist

# executar o projeto
./mvnw spring-boot:run
```

### Acessar o H2 console:
```
http://localhost:8080/h2-console
JDBC URL: jdbc:h2:mem:testdb
```

### Testar com Postman:
- `GET /games`
- `GET /lists`
- `GET /lists/{listId}/games`
- `POST /lists/{listId}/replacement`

## 👨‍💻 Autor

Feito com 💻 por **Lucas Lucena**  
📫 Entre em contato no [LinkedIn](https://www.linkedin.com/in/lucaslucenadev)

---

<p align="center">🔥 Projeto do treinamento gratuito <strong>Intensivão Java Spring</strong> - DevSuperior</p>
