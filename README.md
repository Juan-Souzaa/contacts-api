# Contacts API

API REST de contatos e endereços em Java com Spring Boot, feita nas aulas de APIs REST com Spring Boot do IFSP. Cada contato pode ter vários endereços.

<p>
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java">
  <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" alt="Spring Boot">
  <img src="https://img.shields.io/badge/H2-09476B?style=for-the-badge&logoColor=white" alt="H2">
</p>

## Endpoints

**Contatos**

| Método | Rota | Descrição |
|---|---|---|
| GET | `/api/contacts` | Lista os contatos |
| GET | `/api/contacts/{id}` | Busca um contato |
| GET | `/api/contacts/search?name=` | Busca por parte do nome |
| GET | `/api/contacts/{id}/addresses` | Lista os endereços de um contato |
| POST | `/api/contacts` | Cria um contato |
| PUT | `/api/contacts/{id}` | Atualiza o contato inteiro |
| PATCH | `/api/contacts/{id}` | Atualiza só os campos enviados |
| DELETE | `/api/contacts/{id}` | Exclui um contato |

**Endereços**

| Método | Rota | Descrição |
|---|---|---|
| GET | `/api/addresses` | Lista os endereços |
| GET | `/api/addresses/{id}` | Busca um endereço |
| GET | `/api/addresses/search/cidade`, `/estado`, `/cep` | Busca por cidade, estado ou CEP |
| POST | `/api/addresses` | Cria um endereço para um contato |
| PUT | `/api/addresses/{id}` | Atualiza um endereço |
| DELETE | `/api/addresses/{id}` | Exclui um endereço |

## Validação

Nome, e-mail e telefone são obrigatórios; o e-mail precisa ter formato válido e o telefone, de 8 a 15 caracteres. Os erros de validação voltam com a mensagem de cada campo.

## Como rodar

Pré-requisito: JDK 17. O banco é o H2 em memória.

```bash
git clone https://github.com/Juan-Souzaa/contacts-api.git
cd contacts-api
./mvnw spring-boot:run
```

A API sobe em http://localhost:8080.

## Material da disciplina

- `prints_postman/`: capturas das requisições de cada exercício no Postman
- `Exercicio3_REST_e_SOAP.txt`: respostas sobre as diferenças entre REST e SOAP
